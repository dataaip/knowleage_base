# Explicit type conversion

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Explicit conversions**** | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | ****Explicit conversions**** | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Converts between types using a combination of explicit and implicit conversions.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `(` type-id `)` unary-expression | (1) |  |
|  | | | | | | | | | |
| simple-type-specifier `(` expression-list ﻿(optional) `)` simple-type-specifier `(` initializer-list ﻿(optional) `)` | (2) | (until C++11) (since C++11) |
|  | | | | | | | | | |
| simple-type-specifier `{` initializer-list ﻿(optional) `}` | (3) | (since C++11) |
|  | | | | | | | | | |
| simple-type-specifier `{` designated-initializer-list `}` | (4) | (since C++20) |
|  | | | | | | | | | |
| `typename` identifier `(` initializer-list ﻿(optional) `)` | (5) | (since C++11) |
|  | | | | | | | | | |
| `typename` identifier `{` initializer-list ﻿(optional) `}` | (6) | (since C++11) |
|  | | | | | | | | | |
| `typename` identifier `{` designated-initializer-list `}` | (7) | (since C++20) |
|  | | | | | | | | | |

Explicitly converts any number of values to a value of the target type.

1) Explicit type conversion (cast notation), also called **C-style cast**.2-7) Explicit type conversion (functional notation), also called **function-style cast**.

|  |  |  |
| --- | --- | --- |
| type-id | - | a type-id |
| unary-expression | - | an unary expression (whose top-level operator does not have a precedence higher than that of C-style cast) |
| simple-type-specifier | - | a simple type specifier |
| expression-list | - | a comma-separated list of expressions (except unparenthesized comma expressions) |
| initializer-list | - | a comma-separated list of initializer clauses |
| designated-initializer-list | - | a comma-separated list of designated initializer clauses |
| identifier | - | a (possibly qualified) identifier (including template identifiers) |

### Explanation

1) When the C-style cast is encountered, the compiler attempts to interpret it as the following cast expressions, in this order:a) `const_cast`<type-id ﻿>(unary-expression ﻿);b) `static_cast`<type-id ﻿>(unary-expression ﻿), with extensions: pointer or reference to a derived class is additionally allowed to be cast to pointer or reference to unambiguous base class (and vice versa) even if the base class is inaccessible (that is, this cast ignores the private inheritance specifier). Same applies to casting pointer to member to pointer to member of unambiguous non-virtual base;c) a static_cast (with extensions) followed by const_cast;d) `reinterpret_cast`<type-id ﻿>(unary-expression ﻿);e) a reinterpret_cast followed by const_cast. The first choice that satisfies the requirements of the respective cast operator is selected, even if it is ill-formed (see example). If a static_cast followed by a const_cast is used and the conversion can be interpreted in more than one way as such, the conversion is ill-formed. In addition, C-style casts can cast from, to, and between pointers to incomplete class type. If both type-id and the type of unary-expression are pointers to incomplete class types, it is unspecified whether static_cast or reinterpret_cast gets selected.2-7) A function-style cast specifies a ****type**** (simple-type-specifier ﻿ or identifier ﻿(since C++11)) and an ****initializer**** (the remaining parts), it constructs a value of the target type `T`, which is determined from the specified type and initializer(since C++17):

|  |  |
| --- | --- |
| `T` is the specified type. | (until C++17) |
| `T` is determined as follows:   - If the specified type is a placeholder for a deduced class type, `T` is the return type of the function selected by overload resolution for class template deduction.  |  |  | | --- | --- | | - Otherwise, if the specified type contains a placeholder type, `T` is the deduced type. | (since C++23) |  - Otherwise, `T` is the specified type. | (since C++17) |

 The conversion result is determined as follows:

- If the function-style cast is of syntax (2), and there is exactly one expression in parentheses, this cast is equivalent to the corresponding C-style cast.
- Otherwise, if `T` is (possibly cv-qualified) void, the result is an rvalue(until C++11)a prvalue(since C++11) of type void that performs no initialization.

|  |  |
| --- | --- |
| - If the initializer is not (), the program is ill-formed. | (until C++11) |
| - If the initializer is not () or {} after pack expansion (if any), the program is ill-formed. | (since C++11) |

- Otherwise, if `T` is a reference type, the function-style cast has the same effect as direct-initializing an invented variable t of type `T` from the specified initializer, and the result is the initialized t.

|  |  |
| --- | --- |
| - The result is an lvalue. | (until C++11) |
| - If `T` is an lvalue reference type or an rvalue reference to function type, the result is an lvalue. - Otherwise, the result is an xvalue. | (since C++11) |

- Otherwise, the result is an rvalue(until C++11)a prvalue(since C++11) of of type `T` designating a temporary(until C++17)whose result object is(since C++17) direct-initialized with the specified initializer.

### Ambiguity Resolution

#### Ambiguous declaration statement

In the case of an ambiguity between an expression statement with a function-style cast expression as its leftmost subexpression and a declaration statement, the ambiguity is resolved by treating it as a declaration. This disambiguation is purely syntactic: it does not consider the meaning of names occurring in the statement other than whether they are type names:

```
struct M {};
struct L { L(M&); };
 
M n;
void f()
{
    M(m);    // declaration, equivalent to M m;
    L(n);    // ill-formed declaration, equivalent to L n;
    L(l)(m); // still a declaration, equivalent to L l((m));
}

```

|  |  |
| --- | --- |
| However, if the outermost declarator in the ambiguous declaration statement has a trailing return type, the statement will only be treated as a declaration statement if the trailing return type starts with auto:   ```text struct M;   struct S {     S* operator()();     int N;     int M;       void mem(S s)     {         auto(s)()->M; // expression (S::M hides ::M), invalid before C++23     } };   void f(S s) {     {         auto(s)()->N; // expression, invalid before C++23         auto(s)()->M; // function declaration, equivalent to M s();     }     {         S(s)()->N;    // expression         S(s)()->M;    // expression     } } ``` | (since C++11) |

#### Ambiguous function parameter

The ambiguity above can also occur in the context of a declaration. In that context, the choice is between an object declaration with a function-style cast as the initializer and a declaration involving a function declarator with a redundant set of parentheses around a parameter name. The resolution is also to consider any construct, such as the potential parameter declaration, that could possibly be a declaration to be a declaration:

```
struct S
{
    S(int);
};
 
void foo(double a)
{
    S w(int(a)); // function declaration: has a parameter `a` of type int
    S x(int());  // function declaration: has an unnamed parameter of type int(*)() 
                 // that is adjusted from int()
 
    // Ways to avoid ambiguity:
    S y((int(a))); // object declaration: extra pair of parentheses
    S y((int)a);   // object declaration: C-style cast
    S z = int(a);  // object declaration: no ambiguity for this syntax
}

```

|  |  |
| --- | --- |
| However, if the outermost declarator in the ambiguous parameter declaration has a trailing return type, the ambiguity will only be resolved by treating it as a declaration if it starts with auto:   ```text typedef struct BB { int C[2]; } *B, C;   void foo() {     S a(B()->C);    // object declaration: B()->C cannot declare a parameter     S b(auto()->C); // function declaration: has an unnamed parameter of type C(*)()                     // that is adjusted from C() } ``` | (since C++11) |

#### Ambiguous type-id

An ambiguity can arise from the similarity between a function-style cast and a type-id. The resolution is that any construct that could possibly be a type-id in its syntactic context shall be considered a type-id:

```
// `int()` and `int(unsigned(a))` can both be parsed as type-id:
// `int()`            represents a function returning int
//                    and taking no argument
// `int(unsigned(a))` represents a function returning int
//                    and taking an argument of type unsigned
void foo(signed char a)
{
    sizeof(int());            // type-id (ill-formed)
    sizeof(int(a));           // expression
    sizeof(int(unsigned(a))); // type-id (ill-formed)
 
    (int()) + 1;            // type-id (ill-formed)
    (int(a)) + 1;           // expression
    (int(unsigned(a))) + 1; // type-id (ill-formed)
}

```

|  |  |
| --- | --- |
| However, if the outermost abstract-declarator in the ambiguous type-id has a trailing return type, the ambiguity will only be resolved by treating it as a type-id if it starts with auto:   ```text typedef struct BB { int C[2]; } *B, C;   void foo() {     sizeof(B()->C[1]);    // OK, sizeof(expression)     sizeof(auto()->C[1]); // error: sizeof of a function returning an array } ``` | (since C++11) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_auto_cast` | `202110L` | (C++23) | auto(x) and auto{x} |

### Example

Run this code

```
#include <cassert>
#include <iostream>
 
double f = 3.14;
unsigned int n1 = (unsigned int)f; // C-style cast
unsigned int n2 = unsigned(f);     // function-style cast
 
class C1;
class C2;
C2* foo(C1* p)
{
    return (C2*)p; // casts incomplete type to incomplete type
}
 
void cpp23_decay_copy_demo()
{
    auto inc_print = [](int& x, const int& y)
    {
        ++x;
        std::cout << "x:" << x << ", y:" << y << '\n';
    };
 
    int p{1};
    inc_print(p, p); // prints x:2 y:2, because param y here is an alias of p
    int q{1};
    inc_print(q, auto{q}); // prints x:2 y:1, auto{q} (C++23) casts to prvalue,
                           // so the param y is a copy of q (not an alias of q)
}
 
// In this example, C-style cast is interpreted as static_cast
// even though it would work as reinterpret_cast
struct A {};
struct I1 : A {};
struct I2 : A {};
struct D : I1, I2 {};
 
int main()
{
    D* d = nullptr;
//  A* a = (A*)d;                   // compile-time error
    A* a = reinterpret_cast<A*>(d); // this compiles
    assert(a == nullptr);
 
    cpp23_decay_copy_demo();
}

```

Output:

```
x:2 y:2
x:2 y:1

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1223 (P2915R0) | C++11 | the addition of trailing return type introduced more ambiguities | resolves them |
| CWG 1893 | C++11 | function-style cast did not consider pack expansions | considers them |
| CWG 2351 | C++11 | void{} was ill-formed | made well-formed |
| CWG 2620 | C++98 | the resolution of ambiguous function parameters might be misinterpreted | improved the wording |
| CWG 2828 | C++98 | a C-style cast was ill-formed if multiple interpretations of a static_cast followed by a const_cast exist, regardless of whether these conversions are actually used | only considers the conversions possibly being used |
| CWG 2894 | C++98 | function-style casts could create reference rvalues | can only create reference lvalues |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 7.6.1.4 Explicit type conversion (functional notation) [expr.type.conv]

:   - 7.6.3 Explicit type conversion (cast notation) [expr.cast]

- C++20 standard (ISO/IEC 14882:2020):

:   - 7.6.1.4 Explicit type conversion (functional notation) [expr.type.conv]

:   - 7.6.3 Explicit type conversion (cast notation) [expr.cast]

- C++17 standard (ISO/IEC 14882:2017):

:   - 8.2.3 Explicit type conversion (functional notation) [expr.type.conv]

:   - 8.4 Explicit type conversion (cast notation) [expr.cast]

- C++14 standard (ISO/IEC 14882:2014):

:   - 5.2.3 Explicit type conversion (functional notation) [expr.type.conv]

:   - 5.4 Explicit type conversion (cast notation) [expr.cast]

- C++11 standard (ISO/IEC 14882:2011):

:   - 5.2.3 Explicit type conversion (functional notation) [expr.type.conv]

:   - 5.4 Explicit type conversion (cast notation) [expr.cast]

- C++03 standard (ISO/IEC 14882:2003):

:   - 5.2.3 Explicit type conversion (functional notation) [expr.type.conv]

:   - 5.4 Explicit type conversion (cast notation) [expr.cast]

- C++98 standard (ISO/IEC 14882:1998):

:   - 5.2.3 Explicit type conversion (functional notation) [expr.type.conv]

:   - 5.4 Explicit type conversion (cast notation) [expr.cast]

### See also

|  |  |
| --- | --- |
| `const_cast` conversion | adds or removes const |
| `static_cast` conversion | performs basic conversions |
| `dynamic_cast` conversion | performs checked polymorphic conversions |
| `reinterpret_cast` conversion | performs general low-level conversions |
| standard conversions | implicit conversions from one type to another |
| C documentation for cast operator | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/explicit_cast&oldid=179764>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 January 2025, at 17:42.