# Constraints and concepts

From cppreference.com
< cpp‎ | experimental
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| ****Concepts**** (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

This page describes an experimental core language feature. For named type requirements used in the specification of the standard library, see named requirements

Class templates, function templates, and non-template functions (typically members of class templates) may be associated with a **constraint**, which specifies the requirements on template arguments, which can be used to select the most appropriate function overloads and template specializations.

Constraints may also be used to limit automatic type deduction in variable declarations and function return types to only the types that satisfy specified requirements.

Named sets of such requirements are called **concepts**. Each concept is a predicate, evaluated at compile time, and becomes a part of the interface of a template where it is used as a constraint:

Run this code

```
#include <string>
#include <locale>
using namespace std::literals;
 
// Declaration of the concept "EqualityComparable", which is satisfied by
// any type T such that for values a and b of type T,
// the expression a==b compiles and its result is convertible to bool
template<typename T>
concept bool EqualityComparable = requires(T a, T b) {
    { a == b } -> bool;
};
 
void f(EqualityComparable&&); // declaration of a constrained function template
// template<typename T>
// void f(T&&) requires EqualityComparable<T>; // long form of the same
 
int main() {
  f("abc"s); // OK, std::string is EqualityComparable
  f(std::use_facet<std::ctype<char>>(std::locale{})); // Error: not EqualityComparable 
}

```

Violations of constraints are detected at compile time, early in the template instantiation process, which leads to easy to follow error messages.

```
std::list<int> l = {3,-1,10};
std::sort(l.begin(), l.end()); 
//Typical compiler diagnostic without concepts:
//  invalid operands to binary expression ('std::_List_iterator<int>' and
//  'std::_List_iterator<int>')
//                           std::__lg(__last - __first) * 2);
//                                     ~~~~~~ ^ ~~~~~~~
// ... 50 lines of output ...
//
//Typical compiler diagnostic with concepts:
//  error: cannot call std::sort with std::_List_iterator<int>
//  note:  concept RandomAccessIterator<std::_List_iterator<int>> was not satisfied

```

The intent of concepts is to model semantic categories (Number, Range, RegularFunction) rather than syntactic restrictions (HasPlus, Array). According to ISO C++ core guideline T.20, "The ability to specify a meaningful semantics is a defining characteristic of a true concept, as opposed to a syntactic constraint."

If feature testing is supported, the features described here are indicated by the macro constant __cpp_concepts with a value equal or greater 201507.

### Placeholders

The unconstrained placeholder auto and **constrained placeholders** which have the form concept-name `<` template-argument-list(optional)`>`, are placeholders for the type that is to be deduced.

Placeholders may appear in variable declarations (in which case they are deduced from the initializer) or in function return types (in which case they are deduced from return statements)

```
std::pair<auto, auto> p2 = std::make_pair(0, 'a'); // first auto is int,
                                                   // second auto is char
 
Sortable x = f(y); // the type of x is deduced from the return type of f, 
                   // only compiles if the type satisfies the constraint Sortable
 
auto f(Container) -> Sortable; // return type is deduced from the return statement
                               // only compiles if the type satisfies Sortable

```

Placeholders may also appear in parameters, in which case they turn function declarations into template declarations (constrained if the placeholder is constrained)

```
void f(std::pair<auto, EqualityComparable>); // this is a template with two parameters:
       // unconstrained type parameter and a constrained non-type parameter

```

Constrained placeholders may be used anywhere auto may be used, for example, in generic lambda declarations

```
auto gl = [](Assignable& a, auto* b) { a = *b; };

```

If constrained type specifier designates a non-type or a template, but is used as a constrained placeholder, the program is ill-formed:

```
template<size_t N> concept bool Even = (N%2 == 0);
struct S1 { int n; };
int Even::* p2 = &S1::n; // error, invalid use of a non-type concept
void f(std::array<auto, Even>); // error, invalid use of a non-type concept
template<Even N> void f(std::array<auto, N>); // OK

```

### Abbreviated templates

If one or more placeholders appears in a function parameter list, the function declaration is actually a function template declaration, whose template parameter list includes one invented parameter for every unique placeholder, in order of appearance

```
// short form
void g1(const EqualityComparable*, Incrementable&);
// long form:
// template<EqualityComparable T, Incrementable U> void g1(const T*, U&);
// longer form:
// template<typename T, typename U>
// void g1(const T*, U&) requires EqualityComparable<T> && Incrementable<U>;
 
void f2(std::vector<auto*>...);
// long form: template<typename... T> void f2(std::vector<T*>...);
 
void f4(auto (auto::*)(auto));
// long form: template<typename T, typename U, typename V> void f4(T (U::*)(V));

```

All placeholders introduced by equivalent constrained type specifiers have the same invented template parameter. However, each unconstrained specifier (`auto`) always introduces a different template parameter

```
void f0(Comparable a, Comparable* b);
// long form: template<Comparable T> void f0(T a, T* b);
 
void f1(auto a, auto* b);
// long form: template<typename T, typename U> f1(T a, U* b);

```

Both function templates and class templates can be declared using a **template introduction**, which has the syntax concept-name `{` parameter-list(optional)`}` , in which case the keyword `template` is not needed: each parameter from the parameter-list of the template introduction becomes a template parameter whose kind (type, non-type, template) is determined by the kind of the corresponding parameter in the named concept.

Besides declaring a template, template introduction associates a **predicate constraint** (see below) that names (for variable concepts) or invokes (for function concepts) the concept named by the introduction.

```
EqualityComparable{T} class Foo;
// long form: template<EqualityComparable T> class Foo;
// longer form: template<typename T> requires EqualityComparable<T> class Foo;
 
template<typename T, int N, typename... Xs> concept bool Example = ...;
Example{A, B, ...C} struct S1;
// long form template<class A, int B, class... C> requires Example<A,B,C...> struct S1;

```

For function templates, template introduction can be combined with placeholders:

```
Sortable{T} void f(T, auto);
// long form: template<Sortable T, typename U> void f(T, U);
// alternative using only placeholders: void f(Sortable, auto);

```

|  |  |
| --- | --- |
|  | This section is incomplete Reason: touch up template declaration pages to link here |

### Concepts

A concept is a named set of requirements. The definition of a concept appears at namespace scope and has the form of a function template definition (in which case it is called **function concept**) or variable template definition (in which case it is called **variable concept**). The only difference is that the keyword concept appears in the decl-specifier-seq:

```
// variable concept from the standard library (Ranges TS)
template <class T, class U>
concept bool Derived = std::is_base_of<U, T>::value;
 
// function concept from the standard library (Ranges TS)
template <class T>
concept bool EqualityComparable() { 
    return requires(T a, T b) { {a == b} -> Boolean; {a != b} -> Boolean; };
}

```

The following restrictions apply to function concepts:

- `inline` and `constexpr` are not allowed, the function is automatically `inline` and `constexpr`
- `friend` and `virtual` are not allowed
- exception specification is not allowed, the function is automatically `noexcept(true)`.
- cannot be declared and defined later, cannot be redeclared
- the return type must be `bool`
- return type deduction is not allowed
- parameter list must be empty
- the function body must consist of only a `return` statement, whose argument must be a **constraint-expression** (predicate constraint, conjunction/disjunction of other constraints, or a requires-expression, see below)

The following restrictions apply to variable concepts:

- Must have the type `bool`
- Cannot be declared without an initializer
- Cannot be declared or at class scope.
- `constexpr` is not allowed, the variable is automatically `constexpr`
- the initializer must be a constraint expression (predicate constraint, conjunction/disjunction of constraints, or a requires-expression, see below)

Concepts cannot recursively refer to themselves in the body of the function or in the initializer of the variable:

```
template<typename T>
concept bool F() { return F<typename T::type>(); } // error
template<typename T>
concept bool V = V<T*>; // error

```

Explicit instantiations, explicit specializations, or partial specializations of concepts are not allowed (the meaning of the original definition of a constraint cannot be changed)

### Constraints

A constraint is a sequence of logical operations that specifies requirements on template arguments. They can appear within **requires-expression**s (see below) and directly as bodies of concepts

There are 9 types of constraints:

1) conjunctions2) disjunctions3) predicate constraints4) expression constraints (only in a **requires-expression**)5) type constraints (only in a **requires-expression**)6) implicit conversion constraints (only in a **requires-expression**)7) argument deduction constraints (only in a **requires-expression**)8) exception constraints (only in a **requires-expression**)9) parametrized constraints (only in a **requires-expression**)

The first three types of constraints may appear directly as the body of a concept or as an ad-hoc requires-clause:

```
template<typename T>
requires // requires-clause (ad-hoc constraint)
sizeof(T) > 1 && get_value<T>() // conjunction of two predicate constraints
void f(T);

```

When multiple constraints are attached to the same declaration, the total constraint is a conjunction in the following order: the constraint introduced by **template introduction**, constraints for each template parameter in order of appearance, the **requires** clause after the template parameter list, constraints for each function parameter in order of appearance, trailing **requires** clause:

```
// the declarations declare the same constrained function template 
// with the constraint Incrementable<T> && Decrementable<T>
template<Incrementable T> void f(T) requires Decrementable<T>;
template<typename T> requires Incrementable<T> && Decrementable<T> void f(T); // ok
 
// the following two declarations have different constraints:
// the first declaration has Incrementable<T> && Decrementable<T>
// the second declaration has Decrementable<T> && Incrementable<T>
// Even though they are logically equivalent.
// The second declaration is ill-formed, no diagnostic required
 
template<Incrementable T> requires Decrementable<T> void g();
template<Decrementable T> requires Incrementable<T> void g(); // error

```

#### Conjunctions

Conjunction of constraints `P` and `Q` is specified as P && Q.

```
// example concepts from the standard library (Ranges TS)
template <class T>
concept bool Integral = std::is_integral<T>::value;
template <class T>
concept bool SignedIntegral = Integral<T> && std::is_signed<T>::value;
template <class T>
concept bool UnsignedIntegral = Integral<T> && !SignedIntegral<T>;

```

A conjunction of two constraints is satisfied only if both constraints are satisfied. Conjunctions are evaluated left to right and short-circuited (if the left constraint is not satisfied, template argument substitution into the right constraint is not attempted: this prevents failures due to substitution outside of immediate context). User-defined overloads of `operator&&` are not allowed in constraint conjunctions.

#### Disjunctions

Disjunction of constraints `P` and `Q` is specified as P || Q.

A disjunction of two constraints is satisfied if either constraint is satisfied. Disjunctions are evaluated left to right and short-circuited (if the left constraint is satisfied, template argument deduction into the right constraint is not attempted). User-defined overloads of `operator||` are not allowed in constraint disjunctions.

```
// example constraint from the standard library (Ranges TS)
template <class T = void>
requires EqualityComparable<T>() || Same<T, void>
struct equal_to;

```

#### Predicate constraints

A predicate constraint is a constant expression of type bool. It is satisfied only if it evaluates to true

```
template<typename T> concept bool Size32 = sizeof(T) == 4;

```

Predicate constraints can specify requirements on non-type template parameters and on template template arguments.

Predicate constraints must evaluate directly to bool, no conversions allowed:

```
template<typename T> struct S {
    constexpr explicit operator bool() const { return true; }
};
template<typename T>
requires S<T>{} // bad predicate constraint: S<T>{} is not bool
void f(T);
f(0); // error: constraint never satisfied

```

### Requirements

The keyword requires is used in two ways:

1) To introduce a **requires-clause**, which specifies constraints on template arguments or on a function declaration.

```
template<typename T>
void f(T&&) requires Eq<T>; // can appear as the last element of a function declarator
 
template<typename T> requires Addable<T> // or right after a template parameter list
T add(T a, T b) { return a + b; }

```

 In this case, the keyword **requires** must be followed by some constant expression (so it's possible to write "requires true;"), but the intent is that a named concept (as in the example above) or a conjunction/disjunction of named concepts or a **requires-expression** is used.2) To begin a **requires-expression**, which is a prvalue expression of type bool that describes the constraints on some template arguments. Such expression is `true` if the corresponding concept is satisfied, and false otherwise:

```
template<typename T>
concept bool Addable = requires (T x) { x + x; }; // requires-expression
 
template<typename T> requires Addable<T> // requires-clause, not requires-expression
T add(T a, T b) { return a + b; }
 
template<typename T>
requires requires (T x) { x + x; } // ad-hoc constraint, note keyword used twice
T add(T a, T b) { return a + b; }

```

The syntax of **requires-expression** is as follows:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `requires` `(` parameter-list(optional) `)` `{`  requirement-seq `}` |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| parameter-list | - | a comma-separated list of parameters like in a function declaration, except that default arguments are not allowed and the last parameter cannot be an ellipsis. These parameters have no storage, linkage or lifetime. These parameters are in scope until the closing `}`  of the requirement-seq. If no parameters are used, the round parentheses may be omitted as well |
| requirement-seq | - | whitespace-separated sequence of **requirements**, described below (each requirement ends with a semicolon). Each requirement adds another constraint to the **conjunction** of constraints that this requires-expression defines. |

Each requirement in the requirements-seq is one of the following:

- simple requirement
- type requirements
- compound requirements
- nested requirements

Requirements may refer to the template parameters that are in scope and to the local parameters introduced in the parameter-list. When parametrized, a requires-expression is said to introduce a **parametrized constraint**

The substitution of template arguments into a requires-expression may result in the formation
of invalid types or expressions in its requirements. In such cases,

- If a substitution failure occurs in a requires-expression that is used outside of a templated entity declaration, then the program is ill-formed.
- If the requires-expression is used in a declaration of a templated entity, the corresponding constraint is treated as "not satisfied" and the substitution failure is not an error, however
- If a substitution failure would occur in a requires-expression for every possible template argument, the program is ill-formed, no diagnostic required:

```
template<class T> concept bool C = requires {
    new int[-(int)sizeof(T)]; // invalid for every T: ill-formed, no diagnostic required
};

```

#### Simple requirements

A simple requirement is an arbitrary expression statement. The requirement is that the expression is valid (this is an **expression constraint**). Unlike with predicate constraints, evaluation does not take place, only language correctness is checked.

```
template<typename T>
concept bool Addable =
requires (T a, T b) {
    a + b; // "the expression a+b is a valid expression that will compile"
};
 
// example constraint from the standard library (ranges TS)
template <class T, class U = T>
concept bool Swappable = requires(T&& t, U&& u) {
    swap(std::forward<T>(t), std::forward<U>(u));
    swap(std::forward<U>(u), std::forward<T>(t));
};

```

#### Type requirements

A type requirement is the keyword typename followed by a type name, optionally qualified. The requirement is that the named type exists (a **type constraint**): this can be used to verify that a certain named nested type exists, or that a class template specialization names a type, or that an alias template names a type.

```
template<typename T> using Ref = T&;
template<typename T> concept bool C =
requires {
    typename T::inner; // required nested member name
    typename S<T>;     // required class template specialization
    typename Ref<T>;   // required alias template substitution
};
 
//Example concept from the standard library (Ranges TS)
template <class T, class U> using CommonType = std::common_type_t<T, U>;
template <class T, class U> concept bool Common =
requires (T t, U u) {
    typename CommonType<T, U>; // CommonType<T, U> is valid and names a type
    { CommonType<T, U>{std::forward<T>(t)} }; 
    { CommonType<T, U>{std::forward<U>(u)} }; 
};

```

#### Compound Requirements

A compound requirement has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `{` expression `}`  `noexcept`(optional) trailing-return-type(optional) `;` |  |  |
|  | | | | | | | | | |

and specifies a conjunction of the following constraints:

1) expression is a valid expression (**expression constraint**)2) If `noexcept` is used, expression must also be noexcept (**exception constraint**)3) If trailing-return-type that names a type that uses placeholders, the type must be deducible from the type of the expression (**argument deduction constraint**)4) If trailing-return-type that names a type that does not use placeholders, then two more constraints are added:4a) the type named by trailing-return-type is valid (**type constraint**)4b) the result of the expression is implicitly convertible to that type (**implicit conversion constraint**)

```
template<typename T> concept bool C2 =
requires(T x) {
    {*x} -> typename T::inner; // the expression *x must be valid
                               // AND the type T::inner must be valid
                               // AND the result of *x must be convertible to T::inner
};
 
// Example concept from the standard library (Ranges TS)
template <class T, class U> concept bool Same = std::is_same<T,U>::value;
template <class B> concept bool Boolean =
requires(B b1, B b2) {
    { bool(b1) }; // direct initialization constraint has to use expression
    { !b1 } -> bool; // compound constraint
    requires Same<decltype(b1 && b2), bool>; // nested constraint, see below
    requires Same<decltype(b1 || b2), bool>;
};

```

#### Nested requirements

A nested requirement is another **requires-clause**, terminated with a semicolon. This is used to introduce **predicate constraints** (see above) expressed in terms of other named concepts applied to the local parameters (outside a requires clause, predicate constraints can't use parameters, and placing an expression directly in a requires clause makes it an expression constraint which means it is not evaluated)

```
// example constraint from Ranges TS
template <class T>
concept bool Semiregular = DefaultConstructible<T> &&
    CopyConstructible<T> && Destructible<T> && CopyAssignable<T> &&
requires(T a, size_t n) {  
    requires Same<T*, decltype(&a)>;  // nested: "Same<...> evaluates to true"
    { a.~T() } noexcept;  // compound: "a.~T()" is a valid expression that doesn't throw
    requires Same<T*, decltype(new T)>; // nested: "Same<...> evaluates to true"
    requires Same<T*, decltype(new T[n])>; // nested
    { delete new T };  // compound
    { delete new T[n] }; // compound
};

```

### Concept resolution

Like any other function template, a function concept (but not variable concept) can be overloaded: multiple concept definitions may be provided that all use the same concept-name.

Concept resolution is performed when a concept-name (which may be qualified) appears in

1) a constrained type specifier void f(Concept); std::vector<Concept> x = ...;2) a constrained parameter template<Concept T> void f();3) a template introduction Concept{T} struct X;4) a **constraint-expression** template<typename T> void f() requires Concept<T>;

```
template<typename T> concept bool C() { return true; } // #1
template<typename T, typename U> concept bool C() { return true; } // #2
void f(C); // the set of concepts referred to by C includes both #1 and #2;
           // concept resolution (see below) selects #1.

```

In order to perform concept resolution, **template parameters** of each concept that matches the name (and the qualification, if any) is matched against a sequence of **concept arguments**, which are template arguments and **wildcards**. A wildcard can match a template parameter of any kind (type, non-type, template). The argument set is constructed differently, depending on the context

1) For a concept name used as part of a constrained type specifier or parameter, if the concept name is used without a parameter list, the argument list is a single wildcard.

```
template<typename T> concept bool C1() { return true; } // #1
template<typename T, typename U> concept bool C1() { return true; } // #2
void f1(const C1*); // <wildcard> matches <T>, selects #1

```

2) For a concept name used as part of a constrained type specifier or parameter, if the concept name is used with a template argument list, the argument list is a single wildcard followed by that argument list.

```
template<typename T> concept bool C1() { return true; } // #1
template<typename T, typename U> concept bool C1() { return true; } // #2
void f2(C1<char>); // <wildcard, char> matches <T, U>, selects #2

```

3) If a concept appears in a template introduction, the argument list is a sequence of placeholders as long as the list of parameters in the template introduction

```
template<typename... Ts>
concept bool C3 = true;
C3{T} void q2();     // OK: <T> matches <...Ts>
C3{...Ts} void q1(); // OK: <...Ts> matches <...Ts>

```

4) If a concept appears as the name of a template-id, the concept argument list is exactly the sequence of arguments of that template-id

```
template<typename T> concept bool C() { return true; } // #1
template<typename T, typename U> concept bool C() { return true; } // #2
 
template <typename T>
void f(T) requires C<T>(); // matches #1

```

Concept resolution is performed by matching each argument against the corresponding parameter of each visible concept. Default template arguments (if used) are instantiated for each paramter that doesn't correspond to an argument, and are then appended to the argument list. Template parameter matches an argument only if it has the same kind (type, non-type, template), unless the argument is a wildcard. A parameter pack matches zero or more arguments as long as all arguments match the pattern in kind (unless they are wildcards).

If any argument does not match its corresponding parameter or if there are more arguments than parameters and the last parameter is not a pack, the concept is not viable. If there is zero or more than one viable concept, the program is ill-formed.

```
template<typename T> concept bool C2() { return true; }
template<int T> concept bool C2() { return true; }
 
template<C2<0> T> struct S1; // error: <wildcard, 0> matches 
                             // neither <typename T> nor <int T>
template<C2 T> struct S2; // both #1 and #2 match: error

```

|  |  |
| --- | --- |
|  | This section is incomplete Reason: needs an example with meaningful concepts, not these 'return true' placeholders |

### Partial ordering of constraints

Before any further analysis, constraints are **normalized** by substituting the body of every name concept and every requires expression until what is left is a sequence of conjunctions and disjunctions on atomic constraints, which are predicate constraints, expression constraints, type constraints, implicit conversion constraints, argument deduction constraints, and exception constraints.

Concept `P` is said to **subsume** concept `Q` if it can be proven that `P` implies `Q` without analyzing types and expressions for equivalence (so `N >= 0` does not subsume `N > 0`)

Specifically, first `P` is converted to disjunctive normal form and `Q` is converted to conjunctive normal form, and they are compared as follows:

- each atomic constraint `A` subsumes equivalent atomic constraint `A`
- each atomic constraint `A` subsumes a disjunction `A||B` and does not subsume a conjunction `A&&B`
- each conjunction `A&&B` subsumes `A`, but a disjunction `A||B` does not subsume `A`

Subsumption relationship defines partial order of constraints, which is used to determine:

- the best viable candidate for a non-template function in overload resolution
- the address of a non-template function in an overload set
- the best match for a template template argument
- partial ordering of class template specializations
- partial ordering of function templates

|  |  |
| --- | --- |
|  | This section is incomplete Reason: backlinks from the above to here |

If declarations `D1` and `D2` are constrained and D1's normalized constraints subsume D2's normalized constraints (or if D1 is constrained and D2 is unconstrained), then D1 is said to be **at least as constrained** as D2. If D1 is at least as constrained as D2 and D2 is not at least as constrained as D1, then D1 is **more constrained** than D2.

```
template<typename T>
concept bool Decrementable = requires(T t) { --t; };
template<typename T>
concept bool RevIterator = Decrementable<T> && requires(T t) { *t; };
 
// RevIterator subsumes Decrementable, but not the other way around
// RevIterator is more constrained as Decrementable
 
void f(Decrementable); // #1
void f(RevIterator);   // #2
 
f(0);       // int only satisfies Decrementable, selects #1
f((int*)0); // int* satisfies both constraints, selects #2 as more constrained
 
void g(auto);          // #3 (unconstrained)
void g(Decrementable); // #4
 
g(true);  // bool does not satisfy Decrementable, selects #3
g(0);     // int satisfies Decrementable, selects #4 because it is more constrained

```

### Keywords

concept,
requires

### Compiler support

GCC >= 6.1 supports this technical specification (required option -fconcepts)

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/constraints&oldid=146516>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 January 2023, at 15:53.