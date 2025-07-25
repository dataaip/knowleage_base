# Explicit (full) template specialization

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Template specialization**** | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

Declarations

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | ****Explicit template specialization**** | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

 Templates

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Parameters and arguments | | | | |
| Class templates | | | | |
| Function templates | | | | |
| Class member templates | | | | |
| Variable templates (C++14) | | | | |
| Template argument deduction | | | | |
| Class template argument deduction (C++17) | | | | |
| ****Explicit (full) specialization**** | | | | |
| Partial specialization | | | | |
| Dependent names | | | | |
| Packs (C++11) | | | | |
| `sizeof...` (C++11) | | | | |
| Fold expressions (C++17) | | | | |
| Pack indexing (C++26) | | | | |
| SFINAE | | | | |
| Constraints and concepts (C++20) | | | | |
| Requires expression (C++20) | | | | |

Allows customizing the template code for a given set of template arguments.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `template <>` declaration |  |  |
|  | | | | | | | | | |

Any of the following can be fully specialized:

1. function template
2. class template
3. variable template(since C++14)
4. member function of a class template
5. static data member of a class template
6. member class of a class template
7. member enumeration of a class template
8. member class template of a class or class template
9. member function template of a class or class template
10. member variable template of a class or class template(since C++14)

For example,

Run this code

```
#include <type_traits>
 
template<typename T> // primary template
struct is_void : std::false_type {};
template<>           // explicit specialization for T = void
struct is_void<void> : std::true_type {};
 
int main()
{
    static_assert(is_void<char>::value == false,
        "for any type T other than void, the class is derived from false_type");
    static_assert(is_void<void>::value == true,
        "but when T is void, the class is derived from true_type");
}

```

### In detail

Explicit specialization may be declared in any scope where its primary template may be defined (which may be different from the scope where the primary template is defined; such as with out-of-class specialization of a member template). Explicit specialization has to appear after the non-specialized template declaration.

```
namespace N
{
    template<class T> // primary template
    class X { /*...*/ };
    template<>        // specialization in same namespace
    class X<int> { /*...*/ };
 
    template<class T> // primary template
    class Y { /*...*/ };
    template<>        // forward declare specialization for double
    class Y<double>;
}
 
template<> // OK: specialization in same namespace
class N::Y<double> { /*...*/ };

```

Specialization must be declared before the first use that would cause implicit instantiation, in every translation unit where such use occurs:

```
class String {};
 
template<class T>
class Array { /*...*/ };
 
template<class T> // primary template
void sort(Array<T>& v) { /*...*/ }
 
void f(Array<String>& v)
{
    sort(v); // implicitly instantiates sort(Array<String>&), 
}            // using the primary template for sort()
 
template<> // ERROR: explicit specialization of sort(Array<String>)
void sort<String>(Array<String>& v); // after implicit instantiation

```

A template specialization that was declared but not defined can be used just like any other incomplete type (e.g. pointers and references to it may be used):

```
template<class T> // primary template
class X;
template<>        // specialization (declared, not defined)
class X<int>;
 
X<int>* p; // OK: pointer to incomplete type
X<int> x;  // error: object of incomplete type

```

Whether an explicit specialization of a function or variable(since C++14) template is `inline`/`constexpr`(since C++11)/`constinit`/`consteval`(since C++20) is determined by the explicit specialization itself, regardless of whether the primary template is declared with that specifier. Similarly, attributes appearing in the declaration of a template have no effect on an explicit specialization of that template:(since C++11)

```
template<class T>
void f(T) { /* ... */ }
template<>
inline void f<>(int) { /* ... */ } // OK, inline
 
template<class T>
inline T g(T) { /* ... */ }
template<>
int g<>(int) { /* ... */ }         // OK, not inline
 
template<typename>
[[noreturn]] void h([[maybe_unused]] int i);
template<> void h<int>(int i)
{
    // [[noreturn]] has no effect, but [[maybe_unused]] has
}

```

### Explicit specializations of function templates

When specializing a function template, its template arguments can be omitted if template argument deduction can provide them from the function arguments:

```
template<class T>
class Array { /*...*/ };
 
template<class T> // primary template
void sort(Array<T>& v);
template<>        // specialization for T = int
void sort(Array<int>&);
 
// no need to write
// template<> void sort<int>(Array<int>&);

```

A function with the same name and the same argument list as a specialization is not a specialization (see template overloading in function template).

Default function arguments cannot be specified in explicit specializations of function templates, member function templates, and member functions of class templates when the class is implicitly instantiated.

An explicit specialization cannot be a friend declaration.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: review the exception specification requirement across different C++ versions |

### Members of specializations

When defining a member of an explicitly specialized class template outside the body of the class, the syntax template<> is not used, except if it's a member of an explicitly specialized member class template, which is specialized as a class template, because otherwise, the syntax would require such definition to begin with template<parameters> required by the nested template

```
template<typename T>
struct A
{
    struct B {};      // member class 
 
    template<class U> // member class template
    struct C {};
};
 
template<> // specialization
struct A<int> 
{
    void f(int); // member function of a specialization
};
// template<> not used for a member of a specialization
void A<int>::f(int) { /* ... */ }
 
template<> // specialization of a member class
struct A<char>::B
{
    void f();
};
// template<> not used for a member of a specialized member class either
void A<char>::B::f() { /* ... */ }
 
template<> // specialization of a member class template
template<class U>
struct A<char>::C
{
    void f();
};
 
// template<> is used when defining a member of an explicitly
// specialized member class template specialized as a class template
template<>
template<class U>
void A<char>::C<U>::f() { /* ... */ }

```

An explicit specialization of a static data member of a template is a definition if the declaration includes an initializer; otherwise, it is a declaration. These definitions must use braces for default initialization:

```
template<>
X Q<int>::x;    // declaration of a static member
template<>
X Q<int>::x (); // error: function declaration
template<>
X Q<int>::x {}; // definition of a default-initialized static member

```

A member or a member template of a class template may be explicitly specialized for a given implicit instantiation of the class template, even if the member or member template is defined in the class template definition.

```
template<typename T>
struct A
{
    void f(T);         // member, declared in the primary template
 
    void h(T) {}       // member, defined in the primary template
 
    template<class X1> // member template
    void g1(T, X1);
 
    template<class X2> // member template
    void g2(T, X2);
};
 
// specialization of a member
template<>
void A<int>::f(int);
 
// member specialization OK even if defined in-class
template<>
void A<int>::h(int) {}
 
// out of class member template definition
template<class T>
template<class X1>
void A<T>::g1(T, X1) {}
 
// member template specialization
template<>
template<class X1>
void A<int>::g1(int, X1);
 
// member template specialization
template<>
template<>
void A<int>::g2<char>(int, char); // for X2 = char
 
// same, using template argument deduction (X1 = char)
template<> 
template<>
void A<int>::g1(int, char);

```

A member or a member template may be nested within many enclosing class templates. In an explicit specialization for such a member, there's a template<> for every
enclosing class template that is explicitly specialized.

```
template<class T1>
struct A
{
    template<class T2>
    struct B
    {
        template<class T3>
        void mf();
    };
};
 
template<>
struct A<int>;
 
template<>
template<>
struct A<char>::B<double>;
 
template<>
template<>
template<>
void A<char>::B<char>::mf<double>();

```

In such a nested declaration, some of the levels may remain unspecialized (except that it can't specialize a class member template in namespace scope if its enclosing class is unspecialized). For each of those levels, the declaration needs template<arguments>, because such specializations are themselves templates:

```
template<class T1>
class A
{
    template<class T2>
    class B
    {
        template<class T3> // member template
        void mf1(T3);
 
        void mf2();        // non-template member
    };
};
 
// specialization
template<>        // for the specialized A
template<class X> // for the unspecialized B
class A<int>::B
{
    template<class T>
    void mf1(T);
};
 
// specialization
template<>        // for the specialized A
template<>        // for the specialized B
template<class T> // for the unspecialized mf1
void A<int>::B<double>::mf1(T t) {}
 
// ERROR: B<double> is specialized and is a member template, so its enclosing A
// must be specialized also
template<class Y>
template<>
void A<Y>::B<double>::mf2() {}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 531 | C++98 | the syntax of defining members of explicit specializations in namespace scope was not specified | specified |
| CWG 727 | C++98 | partial and full specializations not allowed in class scope | allowed in any scope |
| CWG 730 | C++98 | member templates of non-template classes could not be fully specialized | allowed |
| CWG 2478 | C++20 | it was unclear whether the constinit and consteval of the primary template are carried over into its explicit specializations | not carried over |
| CWG 2604 | C++11 | it was unclear whether the attributes of the primary template are carried over into its explicit specializations | not carried over |

### See also

- templates
- class template
- function template
- partial specialization
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/template_specialization&oldid=170153>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 March 2024, at 14:14.