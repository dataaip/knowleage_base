# Definitions and ODR (One Definition Rule)

From cppreference.com
< cpp‎ | language
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

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Punctuation | | | | |
| Names and identifiers | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| Scope | | | | |
| Object lifetime | | | | |
| Storage duration and linkage | | | | |
| ****Definitions and ODR**** | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

**Definitions** are declarations that fully define the entity introduced by the declaration. Every declaration is a definition, except for the following:

- A function declaration without a function body:

```
int f(int); // declares, but does not define f

```

- Any declaration with an extern storage class specifier or with a language linkage specifier (such as extern "C") without an initializer:

```
extern const int a;     // declares, but does not define a
extern const int b = 1; // defines b

```

- Declaration of a non-inline(since C++17) static data member inside a class definition:

```
struct S
{
    int n;               // defines S::n
    static int i;        // declares, but does not define S::i
    inline static int x; // defines S::x
};                       // defines S
 
int S::i;                // defines S::i

```

|  |  |
| --- | --- |
| - (deprecated) Namespace scope declaration of a static data member that was defined within the class with the `constexpr` specifier:  ```text struct S {     static constexpr int x = 42; // implicitly inline, defines S::x };   constexpr int S::x; // declares S::x, not a redefinition ``` | (since C++17) |

- Declaration of a class name (by forward declaration or by the use of the elaborated type specifier in another declaration):

```
struct S;             // declares, but does not define S
 
class Y f(class T p); // declares, but does not define Y and T (and also f and p)

```

|  |  |
| --- | --- |
| - An opaque declaration of an enumeration:  ```text enum Color : int; // declares, but does not define Color ``` | (since C++11) |

- Declaration of a template parameter:

```
template<typename T> // declares, but does not define T

```

- A parameter declaration in a function declaration that isn't a definition:

```
int f(int x); // declares, but does not define f and x
 
int f(int x)  // defines f and x
{
    return x + a;
}

```

- A typedef declaration:

```
typedef S S2; // declares, but does not define S2 (S may be incomplete)

```

|  |  |
| --- | --- |
| - An alias-declaration:  ```text using S2 = S; // declares, but does not define S2 (S may be incomplete) ``` | (since C++11) |

- A using-declaration:

```
using N::d; // declares, but does not define d

```

|  |  |
| --- | --- |
| - Declaration of a deduction guide (does not define any entities) | (since C++17) |
| - A static_assert declaration (does not define any entities) - An attribute declaration (does not define any entities) | (since C++11) |

- An empty declaration (does not define any entities)
- A using-directive (does not define any entities)

|  |  |
| --- | --- |
| - An explicit instantiation declaration (an "extern template"):  ```text extern template f<int, char>; // declares, but does not define f<int, char> ``` | (since C++11) |

- An explicit specialization whose declaration is not a definition:

```
template<>
struct A<int>; // declares, but does not define A<int>

```

An asm declaration does not define any entities, but it is classified as a definition.

Where necessary, the compiler may implicitly define the default constructor, copy constructor, move constructor, copy assignment operator, move assignment operator, and the destructor.

If the definition of any object results in an object of incomplete type or abstract class type, the program is ill-formed.

### One Definition Rule

Only one definition of any variable, function, class type, enumeration type, concept(since C++20) or template is allowed in any one translation unit (some of these may have multiple declarations, but only one definition is allowed).

One and only one definition of every non-inline function or variable that is **odr-used** (see below) is required to appear in the entire program (including any standard and user-defined libraries). The compiler is not required to diagnose this violation, but the behavior of the program that violates it is undefined.

For an inline function or inline variable(since C++17), a definition is required in every translation unit where it is **odr-used** ﻿.

For a class, a definition is required wherever the class is used in a way that requires it to be complete.

There can be more than one definition in a program of each of the following: class type, enumeration type, inline function, inline variable(since C++17), templated entity (template or member of template, but not full template specialization), as long as all following conditions are satisfied:

- Each definition appears in a different translation unit.

|  |  |
| --- | --- |
| - The definitions are not attached to a named module. | (since C++20) |

- Each definition consists of the same sequence of tokens (typically, appears in the same header).
- Name lookup from within each definition finds the same entities (after overload resolution), except that:

:   - Constants with internal or no linkage may refer to different objects as long as they are not odr-used and have the same values in every definition.

|  |  |
| --- | --- |
| - Lambda expressions that are not in a default argument or a default template argument(since C++20) are uniquely identified by the sequence of tokens used to define them. | (since C++11) |

- Overloaded operators, including conversion, allocation, and deallocation functions refer to the same function from each definition (unless referring to one defined within the definition).
- Corresponding entities have the same language linkage in each definition (e.g. the include file is not inside an extern "C" block).
- If a `const` object is constant-initialized in any of the definitions, it is constant-initialized in each definition.
- The rules above apply to every default argument used in each definition.
- If the definition is for a class with an implicitly-declared constructor, every translation unit where it is odr-used must call the same constructor for the base and members.

|  |  |
| --- | --- |
| - If the definition is for a class with a defaulted three-way comparison, every translation unit where it is odr-used must call the same comparison operator for the base and members. | (since C++20) |

- If the definition is for a template, then all these requirements apply to both names at the point of definition and dependent names at the point of instantiation.

If all these requirements are satisfied, the program behaves as if there is only one definition in the entire program. Otherwise, the program is ill-formed, no diagnostic required.

Note: in C, there is no program-wide ODR for types, and even extern declarations of the same variable in different translation units may have different types as long as they are compatible. In C++, the source-code tokens used in declarations of the same type must be the same as described above: if one .cpp file defines struct S { int x; }; and the other .cpp file defines struct S { int y; };, the behavior of the program that links them together is undefined. This is usually resolved with unnamed namespaces.

#### Naming an entity

A variable is **named** by an expression if the expression is an identifier expression that denotes it.

A function is **named** by an expression or conversion in following cases:

- A function whose name appears as an expression or conversion (including named function, overloaded operator, user-defined conversion, user-defined placement forms of operator new, non-default initialization) is named by that expression if it is selected by overload resolution, except when it is an unqualified pure virtual member function or a pointer-to-member to a pure virtual function.
- An allocation or deallocation function for a class is named by a new expression appearing in an expression.
- A deallocation function for a class is named by a delete expression appearing in an expression.
- A constructor selected to copy or move an object is considered to be named by the expression or conversion even if copy elision takes place. Using a prvalue in some contexts does not copy or move an object, see mandatory elision.(since C++17)

A potentially evaluated expression or conversion odr-uses a function if it names it.

|  |  |
| --- | --- |
| A potentially constant evaluated expression or conversion that names a constexpr function makes it needed for constant evaluation, which triggers definition of a defaulted function or instantiation of a function template specialization, even if the expression is unevaluated. | (since C++11) |

#### Potential results

The set of **potential results** of an expression E is a (possibly empty) set of identifier expressions that appear within E, combined as follows:

- If E is an identifier expression, the expression E is its only potential result.
- If E is a subscript expression (E1[E2]) where one of the operands is an array, the potential results of that operand is included in the set.
- If E is a class member access expression of the form E1.E2 or E1.template E2 naming a non-static data member, the potential results of E1 is included in the set.
- If E is a class member access expression naming a static data member, the identifier expression designating the data member is included in the set.
- If E is a pointer-to-member access expression of the form E1.\*E2 or E1.\*template E2 whose second operand is a constant expression, the potential results of E1 are included in the set.
- If E is an expression in parentheses ((E1)), the potential results of E1 are included in the set.
- If E is a glvalue conditional expression (E1 ? E2 : E3, where E2 and E3 are glvalues), the union of the potential results of E2 and E3 are both included in the set.
- If E is a comma expression (E1, E2), the potential results of E2 are in the set of potential results.
- Otherwise, the set is empty.

#### ODR-use (informal definition)

An object is odr-used if its value is read (unless it is a compile time constant) or written, its address is taken, or a reference is bound to it,

A reference is odr-used if it is used and its referent is not known at compile time,

A function is odr-used if a function call to it is made or its address is taken.

If an entity is odr-used, its definition must exist somewhere in the program; a violation of that is usually a link-time error.

```
struct S
{
    static const int x = 0; // static data member
    // a definition outside of class is required if it is odr-used
};
 
const int& f(const int& r);
 
int n = b ? (1, S::x) // S::x is not odr-used here
          : f(S::x);  // S::x is odr-used here: a definition is required

```

#### ODR-use (formal definition)

A variable x that is named by a potentially-evaluated expression expr that appears at a point `P` is odr-used by expr, unless any of the following conditions is satisfied:

- x is a reference that is usable in constant expressions at `P`.
- x is not a reference and (until C++26)expr is an element of the set of potential results of an expression E, and any of the following conditions is satisfied:
  - E is a discarded-value expression, and no lvalue-to-rvalue conversion is applied to it.
  - x is a non-volatile(since C++26) object that is usable in constant expressions at `P` and has no mutable subobjects, and any of the following conditions is satisfied:

|  |  |
| --- | --- |
| - E is a class member access expression naming a non-static data member of reference type and whose object expression has non-volatile-qualified type. | (since C++26) |

:   :   - E has non-volatile-qualified non-class type, and the lvalue-to-rvalue conversion is applied to it.

```
struct S { static const int x = 1; }; // applying lvalue-to-rvalue conversion
                                      // to S::x yields a constant expression
 
int f()
{
    S::x;        // discarded-value expression does not odr-use S::x
 
    return S::x; // expression where lvalue-to-rvalue conversion
                 // applies does not odr-use S::x
}

```

\*this is odr-used if this appears as a potentially-evaluated expression (including the implicit this in a non-static member function call expression).

|  |  |
| --- | --- |
| A structured binding is odr-used if it appears as a potentially-evaluated expression. | (since C++17) |

A function is odr-used in following cases:

- A function is odr-used if it is named by (see below) a potentially-evaluated expression or conversion.
- A virtual member function is odr-used if it is not a pure virtual member function (addresses of virtual member functions are required to construct the vtable).
- A non-placement allocation or deallocation function for a class is odr-used by the definition of a constructor of that class.
- A non-placement deallocation function for a class is odr-used by the definition of the destructor of that class, or by being selected by the lookup at the point of definition of a virtual destructor.
- An assignment operator in a class `T` that is a member or base of another class `U` is odr-used by an implicitly-defined copy-assignment or move-assignment functions of `U`.
- A constructor (including default constructors) for a class is odr-used by the initialization that selects it.
- A destructor for a class is odr-used if it is potentially invoked.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: list of all situations where odr-use makes a difference |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 261 | C++98 | a deallocation function for a polymorphic class might be odr-used even if there were no relevant new or delete expressions in the program | supplemented the odr-use cases to cover constructors and destructors |
| CWG 678 | C++98 | an entity could have definitions with different language linkages | the behavior is undefined in this case |
| CWG 1472 | C++98 | reference variables which satisfy the requirements for appearing in a constant expression were odr-used even if the lvalue-to-rvalue conversion is immediately applied | they are not odr-used in this case |
| CWG 1614 | C++98 | taking address of a pure virtual function odr-used it | the function is not odr-used |
| CWG 1741 | C++98 | constant objects that are immediately lvalue-to-rvalue converted in potentially-evaluated expressions were odr-used | they are not odr-used |
| CWG 1926 | C++98 | array subscript expressions did not propagate potential results | they propagate |
| CWG 2242 | C++98 | it was unclear whether a `const` object that is only constant-initialized in part of its definitions violates ODR | ODR is not violated; the object is constant-initialized in this case |
| CWG 2300 | C++11 | lambda expressions in different translation units could never have the same closure type | the closure type can be the same under one definition rule |
| CWG 2353 | C++98 | a static data member was not a potential result of a member access expression accessing it | it is |
| CWG 2433 | C++14 | a variable template could not have multiple definitions in a program | it can |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 6.3 One definition rule [basic.def.odr]

- C++20 standard (ISO/IEC 14882:2020):

:   - 6.3 One definition rule [basic.def.odr]

- C++17 standard (ISO/IEC 14882:2017):

:   - 6.2 One definition rule [basic.def.odr]

- C++14 standard (ISO/IEC 14882:2014):

:   - 3.2 One definition rule [basic.def.odr]

- C++11 standard (ISO/IEC 14882:2011):

:   - 3.2 One definition rule [basic.def.odr]

- C++03 standard (ISO/IEC 14882:2003):

:   - 3.2 One definition rule [basic.def.odr]

- C++98 standard (ISO/IEC 14882:1998):

:   - 3.2 One definition rule [basic.def.odr]

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/definition&oldid=178487>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 December 2024, at 01:34.