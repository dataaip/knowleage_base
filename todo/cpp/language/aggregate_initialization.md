# Aggregate initialization

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Aggregate initialization**** | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

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

 Initialization

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Initializer | | | | |
| Default initialization | | | | |
| Value initialization | | | | |
| Direct initialization | | | | |
| Copy-initialization | | | | |
| List initialization (C++11) | | | | |
| ****Aggregate initialization**** | | | | |
| Reference initialization | | | | |
| Copy elision | | | | |
| Static initialization | | | | |
| Zero initialization | | | | |
| Constant initialization | | | | |
| Dynamic non-local initialization | | | | |
| Ordered dynamic initialization | | | | |
| Unordered dynamic initialization | | | | |
| Class member initialization | | | | |
| Member initializer list | | | | |
| Default member initializer (C++11) | | | | |

Initializes an aggregate from an initializer list. It is a form of list-initialization(since C++11).

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| T object`= {` arg1, arg2, ... `};` | (1) |  |
|  | | | | | | | | | |
| T object `{` arg1, arg2, ... `};` | (2) | (since C++11) |
|  | | | | | | | | | |
| T object`= { .`des1`=`arg1 `, .`des2 `{` arg2 `}` ... `};` | (3) | (since C++20) |
|  | | | | | | | | | |
| T object `{ .`des1`=`arg1 `, .`des2 `{` arg2 `}` ... `};` | (4) | (since C++20) |
|  | | | | | | | | | |

1,2) Initializing an aggregate with an ordinary initializer list.3,4) Initializing an aggregate with designated initializers (aggregate class only).

### Definitions

#### Aggregate

An **aggregate** is one of the following types:

- array types
- class types that has

|  |  |
| --- | --- |
| - no user-declared constructors | (until C++11) |
| - no user-provided, inherited, or explicit constructors | (since C++11) (until C++20) |
| - no user-declared or inherited constructors | (since C++20) |

:   - no private or protected direct non-static data members

|  |  |
| --- | --- |
| - no base classes | (until C++17) |
| - no virtual base classes - no private or protected direct base classes | (since C++17) |

:   - no virtual member functions

|  |  |
| --- | --- |
| - no default member initializers | (since C++11) (until C++14) |

#### Element

The **elements** of an aggregate are:

- for an array, the array elements in increasing subscript order, or

|  |  |
| --- | --- |
| - for a class, the non-static data members that are not anonymous bit-fields, in declaration order. | (until C++17) |
| - for a class, the direct base classes in declaration order, followed by the direct non-static data members that are neither anonymous bit-fields nor members of an anonymous union, in declaration order. | (since C++17) |

#### Appertainment

Each initializer clause in a brace-enclosed initializer list is said to **appertain** to an element of the aggregate being initialized or to an element of one of its subaggregates.

Considering the sequence of initializer clauses, and the sequence of aggregate elements initially formed as the sequence of elements of the aggregate being initialized and potentially modified as described below:

- For each initializer clause, if any of the following conditions is satisfied, it appertains to the corresponding aggregate element elem:

:   - elem is not an aggregate.
    - The initializer clause begins with {.
    - The initializer clause is an expression, and an implicit conversion sequence can be formed that converts the expression to the type of elem.
    - elem is an aggregate that itself has no aggregate elements.

- Otherwise, elem is an aggregate and that subaggregate is replaced in the list of aggregate elements by the sequence of its own aggregate elements, and the appertainment analysis resumes with the first such element and the same initializer clause. In other words, these rules apply recursively to the aggregate’s subaggregates.

The analysis is complete when all initializer clauses have been exhausted. If any initializer clause remains that does not appertain to an element of the aggregate or one of its subaggregates, the program is ill-formed.

```
struct S1 { int a, b; };
struct S2 { S1 s, t; };
 
// Each subaggregate of “x” is appertained to an initializer clause starting with {
S2 x[2] =
{
    // appertains to “x[0]”
    {
        {1, 2}, // appertains to “x[0].s”
        {3, 4}  // appertains to “x[0].t”
    },
    // appertains to “x[1]”
    {
        {5, 6}, // appertains to “x[1].s”
        {7, 8}  // appertains to “x[1].t”
    }
};
 
// “x” and “y” have the same value (see below)
S2 y[2] = {1, 2, 3, 4, 5, 6, 7, 8};
 
// The process of the appertainment analysis of “y”:
// 1. Initializes the aggregate element sequence (x[0], x[1]) and
//    the initializer clause sequence (1, 2, 3, 4, 5, 6, 7, 8).
// 2. Starting from the first elements of each sequence,
//    checks whether 1 appertains to x[0]:
//    · x[0] is an aggregate.
//    · 1 does not begin with {.
//    · 1 is an expression, but it cannot be implicitly converted to S2.
//    · x[0] has aggregate elements.
// 3. 0 cannot appertain to x[0], therefore x[0] is replaced by x[0].s and x[0].t,
//    the aggregate element sequence becomes (x[0].s, x[0].t, x[1]).
// 4. Resumes the appertainment check, but 1 cannot appertain to x[0].s either.
// 5. The aggregate element sequence now becomes (x[0].s.a, x[0].s.b, x[0].t, x[1]).
// 6. Resumes the appertainment check again:
//    1 appertains to x[0].s.a, and 2 appertains to x[0].s.b.
// 7. The rest of the appertainment analysis works similarly.
 
char cv[4] = {'a', 's', 'd', 'f', 0}; // Error: too many initializer clauses

```

### Initialization process

#### Determining element kind

The effects of aggregate initialization are:

1) Determine the **explicitly initialized elements** of the aggregate as follows:

|  |  |
| --- | --- |
| - If the initializer list is a designated initializer list (the aggregate can only be of class type), the identifier in each designator shall name a direct non-static data member of the class, and the explicitly initialized elements of the aggregate are the elements that are, or contain, those members. | (since C++20) |

:   - Otherwise, if the initializer list is non-empty, the explicitly initialized elements of the aggregate are the elements with an appertained initializer clause and the elements having a subaggregate with an appertained initializer clause.
    - Otherwise, the initializer list must be empty ({}), and there are no explicitly initialized elements.

:   The program is ill-formed if the aggregate is a union and there are two or more explicitly initialized elements:

```
union u { int a; const char* b; };
 
u a = {1};                   // OK: explicitly initializes member `a`
u b = {0, "asdf"};           // error: explicitly initializes two members
u c = {"asdf"};              // error: int cannot be initialized by "asdf"
 
// C++20 designated initializer lists
u d = {.b = "asdf"};         // OK: can explicitly initialize a non-initial member
u e = {.a = 1, .b = "asdf"}; // error: explicitly initializes two members

```

2) Initialize each element of the aggregate in the element order. That is, all value computations and side effects associated with a given element are sequenced before those of any element that follows it in order(since C++11).

#### Explicitly initialized elements

For each explicitly initialized element:

|  |  |
| --- | --- |
| - If the element is an anonymous union member and the initializer list is a designated initializer list, the element is initialized by the designated initializer list {D}, where `D` is the designated initializer clause naming a member of the anonymous union member. There shall be only one such designated initializer clause.  ```text struct C {     union     {         int a;         const char* p;     };       int x; } c = {.a = 1, .x = 3}; // initializes c.a with 1 and c.x with 3 ```  - Otherwise, if the initializer list is a designated initializer list, the element is initialized with the initializer of the corresponding designated initializer clause.   - If that initializer is of syntax (1), and a narrowing conversion is required to convert the expression, the program is ill-formed. | (since C++20) |

|  |  |
| --- | --- |
| - The initializer list is a brace-enclosed initializer list: | (until C++20) |
| - Otherwise, the initializer list is a non-designated brace-enclosed initializer list: | (since C++20) |

:   - If an initializer clause appertains to the aggregate element, then the aggregate element is copy-initialized from the initializer clause.
    - Otherwise, the aggregate element is copy-initialized from a brace-enclosed initializer list consisting of all of the initializer clauses that appertain to subobjects of the aggregate element, in the order of appearance.

```
struct A
{
    int x;
 
    struct B
    {
        int i;
        int j;
    } b;
} a = {1, {2, 3}}; // initializes a.x with 1, a.b.i with 2, a.b.j with 3
 
struct base1 { int b1, b2 = 42; };
 
struct base2
{
    base2()
    {
        b3 = 42;
    }
 
    int b3;
};
 
struct derived : base1, base2
{
    int d;
};
 
derived d1{{1, 2}, {}, 4}; // initializes d1.b1 with 1, d1.b2 with 2,
                           //             d1.b3 with 42, d1.d with 4
derived d2{{}, {}, 4};     // initializes d2.b1 with 0, d2.b2 with 42,
                           //             d2.b3 with 42, d2.d with 4

```

#### Implicitly initialized elements

For a non-union aggregate, each element that is not an explicitly initialized element is initialized as follows:

|  |  |
| --- | --- |
| - If the element has a default member initializer, the element is initialized from that initializer. | (since C++11) |

- Otherwise, if the element is not a reference, the element is copy-initialized from an empty initializer list.
- Otherwise, the program is ill-formed.

```
struct S
{
    int a;
    const char* b;
    int c;
    int d = b[a];
};
 
// initializes ss.a with 1,
//             ss.b with "asdf",
//             ss.c with the value of an expression of the form int{} (that is, 0),
//         and ss.d with the value of ss.b[ss.a] (that is, 's')
S ss = {1, "asdf"};

```

If the aggregate is a union and the initializer list is empty, then

|  |  |
| --- | --- |
| - If any variant member has a default member initializer, that member is initialized from its default member initializer. | (since C++11) |

- Otherwise, the first member of the union (if any) is copy-initialized from an empty initializer list.

### Arrays with unknown bounds

The number of elements in an array of unknown bound initialized with a brace-enclosed initializer list is the number of explicitly initialized elements of the array. An array of unknown bound cannot be initialized with {}.

```
int x[] = {1, 3, 5}; // x has 3 elements
 
struct Y { int i, j, k; };
 
Y y[] = {1, 2, 3, 4, 5, 6}; // y has only 2 elements:
                            // 1, 2 and 3 appertain to y[0],
                            // 4, 5 and 6 appertain to y[1]
 
int z[] = {} // Error: cannot declare an array without any element

```

|  |  |
| --- | --- |
| Designated initializers The syntax forms (3,4) are known as designated initializers: each designator must name a direct non-static data member of T, and all designator ﻿s used in the expression must appear in the same order as the data members of T.   ```text struct A { int x; int y; int z; };   A a{.y = 2, .x = 1}; // error; designator order does not match declaration order A b{.x = 1, .z = 2}; // ok, b.y initialized to 0 ```   Each direct non-static data member named by the designated initializer is initialized from the corresponding brace-or-equals initializer that follows the designator. Narrowing conversions are prohibited.  Designated initializer can be used to initialize a union into the state other than the first. Only one initializer may be provided for a union.   ```text union u { int a; const char* b; };   u f = {.b = "asdf"};         // OK, active member of the union is b u g = {.a = 1, .b = "asdf"}; // Error, only one initializer may be provided ```   For a non-union aggregate, elements for which a designated initializer is not provided are initialized the same as described above for when the number of initializer clauses is less than the number of members (default member initializers where provided, empty list-initialization otherwise):   ```text struct A {     string str;     int n = 42;     int m = -1; };   A{.m = 21} // Initializes str with {}, which calls the default constructor            // then initializes n with = 42            // then initializes m with = 21 ```   If the aggregate that is initialized with a designated initializer clause has an anonymous union member, the corresponding designated initializer must name one of the members of that anonymous union.  Note: out-of-order designated initialization, nested designated initialization, mixing of designated initializers and regular initializers, and designated initialization of arrays are all supported in the C programming language, but are not allowed in C++.   ```text struct A { int x, y; }; struct B { struct A a; };   struct A a = {.y = 1, .x = 2}; // valid C, invalid C++ (out of order) int arr[3] = {[1] = 5};        // valid C, invalid C++ (array) struct B b = {.a.x = 0};       // valid C, invalid C++ (nested) struct A a = {.x = 1, 2};      // valid C, invalid C++ (mixed) ``` | (since C++20) |

### Character arrays

Arrays of ordinary character types (char, signed char, unsigned char), char8_t(since C++20), char16_t, char32_t(since C++11), or wchar_t can be initialized from ordinary string literals, UTF-8 string literals(since C++20), UTF-16 string literals, UTF-32 string literals(since C++11), or wide string literals, respectively, optionally enclosed in braces. Additionally, an array of char or unsigned char may be initialized by a UTF-8 string literal, optionally enclosed in braces(since C++20). Successive characters of the string literal (which includes the implicit terminating null character) initialize the elements of the array, with an integral conversion if necessary for the source and destination value(since C++20). If the size of the array is specified and it is larger than the number of characters in the string literal, the remaining characters are zero-initialized.

```
char a[] = "abc";
// equivalent to char a[4] = {'a', 'b', 'c', '\0'};
 
//  unsigned char b[3] = "abc"; // Error: initializer string too long
unsigned char b[5]{"abc"};
// equivalent to unsigned char b[5] = {'a', 'b', 'c', '\0', '\0'};
 
wchar_t c[] = {L"кошка"}; // optional braces
// equivalent to wchar_t c[6] = {L'к', L'о', L'ш', L'к', L'а', L'\0'};

```

### Notes

An aggregate class or array may include non-aggregate public bases(since C++17), members, or elements, which are initialized as described above (e.g. copy-initialization from the corresponding initializer clause).

Until C++11, narrowing conversions were permitted in aggregate initialization, but they are no longer allowed.

Until C++11, aggregate initialization could only be used in variable definition, and could not be used in a constructor initializer list, a new-expression, or temporary object creation due to syntax restrictions.

In C, character array of size one less than the size of the string literal may be initialized from a string literal; the resulting array is not null-terminated. This is not allowed in C++.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_aggregate_bases` | `201603L` | (C++17) | Aggregate classes with base classes |
| `__cpp_aggregate_nsdmi` | `201304L` | (C++14) | Aggregate classes with default member initializers |
| `__cpp_aggregate_paren_init` | `201902L` | (C++20) | Aggregate initialization in the form of direct initialization |
| `__cpp_char8_t` | `202207L` | (C++23) (DR20) | char8_t compatibility and portability fix (allow initialization of (unsigned char arrays from UTF-8 string literals) |
| `__cpp_designated_initializers` | `201707L` | (C++20) | Designated initializers |

### Example

Run this code

```
#include <array>
#include <cstdio>
#include <string>
 
struct S
{
    int x;
 
    struct Foo
    {
        int i;
        int j;
        int a[3];
    } b;
};
 
int main()
{
    S s1 = {1, {2, 3, {4, 5, 6}}};
    S s2 = {1, 2, 3, 4, 5, 6}; // same, but with brace elision
    S s3{1, {2, 3, {4, 5, 6}}}; // same, using direct-list-initialization syntax
    S s4{1, 2, 3, 4, 5, 6}; // error until CWG 1270:
                            // brace elision only allowed with equals sign
 
    int ar[] = {1, 2, 3}; // ar is int[3]
//  char cr[3] = {'a', 'b', 'c', 'd'}; // too many initializer clauses
    char cr[3] = {'a'}; // array initialized as {'a', '\0', '\0'}
 
    int ar2d1[2][2] = {{1, 2}, {3, 4}}; // fully-braced 2D array: {1, 2}
                                        //                        {3, 4}
    int ar2d2[2][2] = {1, 2, 3, 4}; // brace elision: {1, 2}
                                    //                {3, 4}
    int ar2d3[2][2] = {{1}, {2}};   // only first column: {1, 0}
                                    //                    {2, 0}
 
    std::array<int, 3> std_ar2{{1, 2, 3}};  // std::array is an aggregate
    std::array<int, 3> std_ar1 = {1, 2, 3}; // brace-elision okay
 
//  int ai[] = {1, 2.0}; // narrowing conversion from double to int:
                         // error in C++11, okay in C++03
 
    std::string ars[] = {std::string("one"), // copy-initialization
                         "two",              // conversion, then copy-initialization
                         {'t', 'h', 'r', 'e', 'e'}}; // list-initialization
    union U
    {
        int a;
        const char* b;
    };
    U u1 = {1};         // OK, first member of the union
//  U u2 = {0, "asdf"}; // error: too many initializers for union
//  U u3 = {"asdf"};    // error: invalid conversion to int
 
    [](...) { std::puts("Garbage collecting unused variables... Done."); }
    (
        s1, s2, s3, s4, ar, cr, ar2d1, ar2d2, ar2d3, std_ar2, std_ar1, u1
    );
}
 
// aggregate
struct base1 { int b1, b2 = 42; };
 
// non-aggregate
struct base2
{
    base2() : b3(42) {}
 
    int b3;
};
 
// aggregate in C++17
struct derived : base1, base2 { int d; };
 
derived d1{{1, 2}, {}, 4}; // d1.b1 = 1, d1.b2 = 2,  d1.b3 = 42, d1.d = 4
derived d2{{}, {}, 4};     // d2.b1 = 0, d2.b2 = 42, d2.b3 = 42, d2.d = 4

```

Output:

```
Garbage collecting unused variables... Done.

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 413 | C++98 | anonymous bit-fields were initialized in aggregate initialization | they are ignored |
| CWG 737 | C++98 | when a character array is initialized with a string literal having fewer characters than the array size, the character elements after the trailing '\0' was uninitialized | they are zero-initialized |
| CWG 1270 | C++11 | brace elision was only allowed to be used in copy-list-initialization | allowed elsewhere |
| CWG 1518 | C++11 | a class that declares an explicit default constructor or has inherited constructors should could be an aggregate | it is not an aggregate |
| CWG 1622 | C++98 | a union could not be initialized with {} | allowed |
| CWG 2149 (P3106R1) | C++98 | it was unclear whether brace elision is applicable during array size deduction | applicable |
| CWG 2272 | C++98 | a non-static reference member that is not explicitly initialized was copy-initialized from an empty initializer list | the program is ill- formed in this case |
| CWG 2610 | C++17 | aggregate types could not have private or protected indirect base classes | allowed |
| CWG 2619 | C++20 | the kind of the initialization from designated initializers was unclear | it depends on the kind of the initializer |
| P2513R4 | C++20 | a UTF-8 string literal could not initialize an array of char or unsigned char, which was incompatible with C or C++17 | such initialization is valid |

### See also

- copy elision
- initialization
  - constant initialization
  - list initialization
  - reference initialization
  - value initialization
  - zero initialization

|  |  |
| --- | --- |
| C documentation for Struct and union initialization | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/aggregate_initialization&oldid=179506>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 January 2025, at 13:11.