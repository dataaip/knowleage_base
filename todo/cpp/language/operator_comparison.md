# Comparison operators

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

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | ****Comparison operators**** | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Compares the arguments.

| Operator name | Syntax | Overloadable | Prototype examples (for class T) | |
| --- | --- | --- | --- | --- |
| Inside class definition | Outside class definition |
| Equal to | `a == b` | Yes | bool T::operator==(const U& b) const; | bool operator==(const T& a, const U& b); |
| Not equal to | `a != b` | Yes | bool T::operator!=(const U& b) const; | bool operator!=(const T& a, const U& b); |
| Less than | `a < b` | Yes | bool T::operator<(const U& b) const; | bool operator<(const T& a, const U& b); |
| Greater than | `a > b` | Yes | bool T::operator>(const U& b) const; | bool operator>(const T& a, const U& b); |
| Less than or equal to | `a <= b` | Yes | bool T::operator<=(const U& b) const; | bool operator<=(const T& a, const U& b); |
| Greater than or equal to | `a >= b` | Yes | bool T::operator>=(const U& b) const; | bool operator>=(const T& a, const U& b); |
| Three-way comparison (C++20) | `a <=> b` | Yes | `R`T::operator<=>(const U& b) const;[[1]](operator_comparison.html#cite_note-R-1) | `R`operator<=>(const T& a, const U& b);[[1]](operator_comparison.html#cite_note-R-1) |
| ****Notes****   - Where built-in operators return bool, most user-defined overloads also return bool so that the user-defined operators can be used in the same manner as the built-ins. However, in a user-defined operator overload, any type can be used as return type (including void). - `U` can be any type including `T`.  1. ↑ 1.0 1.1 `R` is the return type of `operator<=>` (see below) | | | | |

### Two-way comparison

The two-way comparison operator expressions have the form

##### Relational operators

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `<` rhs | (1) |  |
|  | | | | | | | | | |
| lhs `>` rhs | (2) |  |
|  | | | | | | | | | |
| lhs `<=` rhs | (3) |  |
|  | | | | | | | | | |
| lhs `>=` rhs | (4) |  |
|  | | | | | | | | | |

##### Equality operators

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `==` rhs | (5) |  |
|  | | | | | | | | | |
| lhs `!=` rhs | (6) |  |
|  | | | | | | | | | |

1) Returns true if lhs is less than rhs, false otherwise.2) Returns true if lhs is greater than rhs, false otherwise.3) Returns true if lhs is less than or equal to rhs, false otherwise.4) Returns true if lhs is greater than or equal to rhs, false otherwise.5) Returns true if lhs is equal to rhs, false otherwise.6) Returns true if lhs is not equal to rhs, false otherwise.

#### Built-in two-way comparison operators

For built-in two-way comparison operators, lvalue-to-rvalue conversions, array-to-pointer conversions(until C++26) and function-to-pointer conversions are applied to lhs and rhs ﻿.

|  |  |
| --- | --- |
| The comparison is deprecated if both lhs and rhs have array type prior to the application of these conversions. | (since C++20) (until C++26) |
| For built-in relational operators, if one of the operands is a pointer, the array-to-pointer conversion is performed on the other operand.  For built-in equality operators, if one of the operands is a pointer or a null pointer constant, the array-to-pointer conversion is performed on the other operand. | (since C++26) |

For built-in two-way comparison operators, the result is a bool prvalue.

#### Built-in arithmetic comparison

If the converted operands both have arithmetic or enumeration type (scoped or unscoped), usual arithmetic conversions are performed on both operands. The values are compared after conversions:

Run this code

```
#include <iostream>
 
int main()
{
    static_assert(sizeof(unsigned char) < sizeof(int),
                  "Cannot compare signed and smaller unsigned properly");
    int a = -1;
    int b = 1;
    unsigned int c = 1;
    unsigned char d = 1;
 
    std::cout << std::boolalpha
              << "Comparing two signed values:\n"
                 " -1 == 1 ? " << (a == b) << "\n"
                 " -1 <  1 ? " << (a <  b) << "\n"
                 " -1 >  1 ? " << (a >  b) << "\n"
                 "Comparing signed and unsigned:\n"
                 // may issue different-signedness warning:
                 " -1 == 1 ? " << (a == c) << "\n"
                 // may issue different-signedness warning:
                 " -1 <  1 ? " << (a <  c) << "\n"
                 // may issue different-signedness warning:
                 " -1 >  1 ? " << (a >  c) << "\n"
                 "Comparing signed and smaller unsigned:\n"
                 " -1 == 1 ? " << (a == d) << "\n"
                 " -1 <  1 ? " << (a <  d) << "\n"
                 " -1 >  1 ? " << (a >  d) << '\n';
}

```

Output:

```
Comparing two signed values:
 -1 == 1 ? false
 -1 <  1 ? true
 -1 >  1 ? false
Comparing signed and unsigned:
 -1 == 1 ? false
 -1 <  1 ? false
 -1 >  1 ? true
Comparing signed and smaller unsigned:
 -1 == 1 ? false
 -1 <  1 ? true
 -1 >  1 ? false

```

#### Built-in pointer equality comparison

The converted operands of equality operators `==` and `!=` can also have the type std::nullptr_t,(since C++11) pointer type or pointer-to-member type.

Built-in pointer equality comparison has three possible results: equal, unequal and unspecified. The values yielded by equality operators for built-in pointer equality comparison is listed below:

| Comparison result  of p and q | Value yielded by | |
| --- | --- | --- |
| p == q | p != q |
| equal | true | false |
| unequal | false | true |
| unspecified | unspecified bool value | |

If at least one of converted lhs and rhs is a pointer, pointer conversions, function pointer conversions(since C++17) and qualification conversions are performed on both converted operands to bring them to their composite pointer type. The two pointers of the composite pointer type are compared as follows:

- If one pointer represents the address of a complete object, and another pointer

:   - represents the address past the end of a different complete non-array object, or
    - represents the address one past the last element of a different complete array object,
:   the result of the comparison is unspecified.

- Otherwise, if the pointers are both null, both point to the same function, or both represent the same address (i.e., they point to or are past the end of the same object), they compare equal.
- Otherwise, the pointers compare unequal.

If at least one of converted lhs and rhs is a pointer to member, pointer-to-member conversions, function pointer conversions(since C++17) and qualification conversions are performed on both converted operands to bring them to their composite pointer type. The two pointers to members of the composite pointer type are compared as follows:

- If two pointers to members are both the null member pointer value, they compare equal.
- If only one of two pointers to members is the null member pointer value, they compare unequal.
- If either is a pointer to a virtual member function, the result is unspecified.
- If one refers to a member of class `C1` and the other refers to a member of a different class `C2`, where neither is a base class of the other, the result is unspecified.
- If both refer to (possibly different) members of the same union, they compare equal.
- Otherwise, two pointers to members compare equal if they would refer to the same member of the same most derived object or the same subobject if indirection with a hypothetical object of the associated class type were performed, otherwise they compare unequal.

```
struct P {};
struct Q : P { int x; };
struct R : P { int x; };
 
int P::*bx = (int(P::*)) &Q::x;
int P::*cx = (int(P::*)) &R::x;
 
bool b1 = (bx == cx); // unspecified
 
struct B
{
    int f();
};
struct L : B {};
struct R : B {};
struct D : L, R {};
 
int (B::*pb)() = &B::f;
int (L::*pl)() = pb;
int (R::*pr)() = pb;
int (D::*pdl)() = pl;
int (D::*pdr)() = pr;
 
bool x = (pdl == pdr); // false
bool y = (pb == pl);   // true

```

|  |  |
| --- | --- |
| Two operands of type std::nullptr_t or one operand of type std::nullptr_t and the other a null pointer constant compare equal. | (since C++11) |

#### Built-in pointer relational comparison

The converted operands of relational operators `>`, `<`, `>=` and `<=` can also have pointer type.

Built-in pointer relational comparison on unequal pointers p and q has three possible results: p is greater, q is greater and unspecified. The values yielded by relational operators for built-in pointer relational comparison is listed below:

| Comparison result  of p and q | Value yielded by | | | |
| --- | --- | --- | --- | --- |
| p > q | p < q | p >= q | p <= q |
| equal | false | false | true | true |
| p is greater | true | false | true | false |
| q is greater | false | true | false | true |
| unspecified | unspecified bool value | | | |

If converted lhs and rhs are both pointers, pointer conversions, function pointer conversions(since C++17) and qualification conversions are performed on both converted operands to bring them to their composite pointer type. The two pointers of the composite pointer type are compared as follows:

- If the pointers compare equal or the equality comparison result is unspecified, the relational comparison result falls into the same category.
- Otherwise (the pointers compare unequal), if any of the pointers is not a pointer to object, the result is unspecified.
- Otherwise (both pointers point to objects), the result is defined in terms of a partial order consistent with the following rules:

:   - Given two different elements high and low of an array such than high has higher subscript than low, if one pointer points to high (or a subobject of high) and the other pointer points to low (or a subobject of low), the former compares greater than the latter.
    - If one pointer points to an element elem (or to a subobject of elem) of an array, and the other pointer is past the end of the same array, the past-the-end pointer compares greater than the other pointer.
    - If one pointer points to a complete object, a base class subobject or a member subobject obj (or to a subobject of obj), and the other pointer is past the end of obj, the past-the-end pointer compares greater than the other pointer.

:   - If the pointers point to different non-zero-sized(since C++20) non-static data members with the same member access(until C++23) of the same object of a non-union class type, or to subobjects of such members, recursively, the pointer to the later declared member compares greater than the other pointer.
    - Otherwise, the result is unspecified.

#### Pointer total order

There exists an **implementation-defined strict total order over pointers** in each program. The strict total order is consistent with the partial order described above: unspecified results become implementation-defined, while other results stay the same.

Pointer comparison with the strict total order is applied in the following cases:

- Calling the operator() of the pointer type specializations of std::less, std::greater, std::less_equal, and std::greater_equal.

|  |  |
| --- | --- |
| - Calling built-in operators comparing pointers from the operator() of specializations std::less<void>, std::greater<void>, std::less_equal<void>, and std::greater_equal<void>. | (since C++14) |
| - Calling built-in operator<=> comparing pointers from the operator() of std::compare_three_way. - Calling built-in operator== comparing pointers from the operator() of std::ranges::equal_to and std::ranges::not_equal_to. - Calling built-in operator< comparing pointers from the operator() of std::ranges::less, std::ranges::greater, std::ranges::less_equal, and std::ranges::greater_equal. | (since C++20) |

#### Overloads

In overload resolution against user-defined operators, for every pair of promoted arithmetic types `L` and `R`, including enumeration types, the following function signatures participate in overload resolution:

|  |  |  |
| --- | --- | --- |
| bool operator<(L, R); |  |  |
| bool operator>(L, R); |  |  |
| bool operator<=(L, R); |  |  |
| bool operator>=(L, R); |  |  |
| bool operator==(L, R); |  |  |
| bool operator!=(L, R); |  |  |
|  |  |  |

For every type `P` which is either pointer to object or pointer to function, the following function signatures participate in overload resolution:

|  |  |  |
| --- | --- | --- |
| bool operator<(P, P); |  |  |
| bool operator>(P, P); |  |  |
| bool operator<=(P, P); |  |  |
| bool operator>=(P, P); |  |  |
| bool operator==(P, P); |  |  |
| bool operator!=(P, P); |  |  |
|  |  |  |

For every type `MP` that is a pointer to member object or pointer to member function or std::nullptr_t(since C++11), the following function signatures participate in overload resolution:

|  |  |  |
| --- | --- | --- |
| bool operator==(MP, MP); |  |  |
| bool operator!=(MP, MP); |  |  |
|  |  |  |

Run this code

```
#include <iostream>
 
struct Foo
{
    int n1;
    int n2;
};
 
union Union
{
    int n;
    double d;
};
 
int main()
{
    std::cout << std::boolalpha;
 
    char a[4] = "abc";
    char* p1 = &a[1];
    char* p2 = &a[2];
    std::cout << "Pointers to array elements:\n"
              << "p1 == p2? " << (p1 == p2) << '\n'
              << "p1 <  p2? " << (p1 <  p2) << '\n';
 
    Foo f;
    int* p3 = &f.n1;
    int* p4 = &f.n2;
    std::cout << "Pointers to members of a class:\n"
              << "p3 == p4? " << (p3 == p4) << '\n'
              << "p3 <  p4? " << (p3 <  p4) << '\n';
 
    Union u;
    int* p5 = &u.n;
    double* p6 = &u.d;
    std::cout << "Pointers to members of a union:\n"
              << "p5 == (void*)p6? " << (p5 == (void*)p6) << '\n'
              << "p5 <  (void*)p6? " << (p5 <  (void*)p6) << '\n';
}

```

Output:

```
Pointers to array elements:
p1 == p2? false
p1 <  p2? true
Pointers to members of a class:
p3 == p4? false
p3 <  p4? true
Pointers to members of a union:
p5 == (void*)p6? true
p5 <  (void*)p6? false

```

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Three-way comparison The three-way comparison operator expressions have the form   |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | |  | | | | | | | | | | | a `<=>` b |  |  | |  | | | | | | | | | |   The expression returns an object such that   - (a <=> b) < 0 if a < b, - (a <=> b) > 0 if a > b, - (a <=> b) == 0 if a and b are equal/equivalent.   If one of the operands is of type bool and the other is not, the program is ill-formed.  If both operands have arithmetic types, or if one operand has unscoped enumeration type and the other has integral type, the usual arithmetic conversions are applied to the operands, and then   - If a narrowing conversion is required, other than from an integral type to a floating point type, the program is ill-formed. - Otherwise, if the operands have integral type, the operator yields a prvalue of type std::strong_ordering:   - std::strong_ordering::equal if both operands are arithmetically equal, - std::strong_ordering::less if the first operand is arithmetically less than the second, - std::strong_ordering::greater otherwise.   - Otherwise, the operands have floating-point type, and the operator yields a prvalue of type std::partial_ordering. The expression a <=> b yields   - std::partial_ordering::less if a is less than b, - std::partial_ordering::greater if a is greater than b, - std::partial_ordering::equivalent if a is equivalent to b (-0 <=> +0 is equivalent), - std::partial_ordering::unordered (NaN <=> anything is unordered).  If both operands have the same enumeration type `E`, the operator yields the result of converting the operands to the underlying type of E and applying <=> to the converted operands.  If at least one of the operands is a pointer to object or pointer to member, array-to-pointer conversions, pointer conversions and qualification conversions are applied to both operands to bring them to their composite pointer type.  For converted pointer operands p and q, p <=> q returns a prvalue of type std::strong_ordering:   - std::strong_ordering::equal if they compare equal, - std::strong_ordering::less if q compares greater than p, - std::strong_ordering::greater if p compares greater than q, - unspecified result if the two-way comparison result is unspecified.   Otherwise, the program is ill-formed.   Overloads In overload resolution against user-defined operators, for pointer or enumeration type `T`, the following function signature participates in overload resolution:   |  |  |  | | --- | --- | --- | | R operator<=>(T, T); |  |  | |  |  |  |   Where `R` is the ordering category type defined above. Run this code  ```text #include <compare> #include <iostream>   int main() {     double foo = -0.0;     double bar = 0.0;       auto res = foo <=> bar;       if (res < 0)         std::cout << "-0 is less than 0";     else if (res > 0)         std::cout << "-0 is greater than 0";     else if (res == 0)         std::cout << "-0 and 0 are equal";     else         std::cout << "-0 and 0 are unordered"; } ```   Output:   ```text -0 and 0 are equal ``` | (since C++20) |

### Notes

Because comparison operators group left-to-right, the expression a < b < c is parsed (a < b) < c, and not a < (b < c) or (a < b) && (b < c).

Run this code

```
#include <iostream>
 
int main()
{
    int a = 3, b = 2, c = 1;
 
    std::cout << std::boolalpha
        << (a < b < c) << '\n' // true; maybe warning
        << ((a < b) < c) << '\n' // true
        << (a < (b < c)) << '\n' // false
        << ((a < b) && (b < c)) << '\n'; // false
}

```

A common requirement for user-defined operator< is strict weak ordering. In particular, this is required by the standard algorithms and containers that work with Compare types: std::sort, std::max_element, std::map, etc.

The comparison result of pointers to different non-static data members of the same class implies that non-static data members in each of the three member access modes(until C++23) are positioned in memory in order of declaration.

Although the results of comparing pointers of random origin (e.g. not all pointing to members of the same array) is unspecified, many implementations provide strict total ordering of pointers, e.g. if they are implemented as addresses within continuous virtual address space. Those implementations that do not (e.g. where not all bits of the pointer are part of a memory address and have to be ignored for comparison, or an additional calculation is required or otherwise pointer and integer is not a 1 to 1 relationship), provide a specialization of std::less for pointers that has that guarantee. This makes it possible to use all pointers of random origin as keys in standard associative containers such as std::set or std::map.

For the types that are both EqualityComparable and LessThanComparable, the C++ standard library makes a distinction between **equality**, which is the value of the expression a == b and **equivalence**, which is the value of the expression !(a < b) && !(b < a).

Comparison between pointers and null pointer constants was removed by the resolution of CWG issue 583 included in N3624:

Run this code

```
void f(char* p)
{
    if (p > 0) { /*...*/ } // Error with N3624, compiled before N3624
    if (p > nullptr) { /*...*/ } // Error with N3624, compiled before N3624
}
 
int main() {}

```

Three-way comparison can be automatically generated for class types, see default comparisons.

If both of the operands are arrays, three-way comparison is ill-formed.

```
unsigned int i = 1;
auto r = -1 < i;    // existing pitfall: returns ‘false’
auto r2 = -1 <=> i; // Error: narrowing conversion required

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_impl_three_way_comparison` | `201907L` | (C++20) | Three-way comparison (compiler support) |
| `__cpp_lib_three_way_comparison` | `201907L` | (C++20) | Three-way comparison (library support); adding three-way comparison to the library |

### Standard library

Comparison operators are overloaded for many classes in the standard library.

|  |  |
| --- | --- |
| operator==operator!=(removed in C++20) | checks whether the objects refer to the same type   (public member function of `std::type_info`) |
| operator==operator!=operator<operator<=>(removed in C++20)(removed in C++20)(C++20) | compares two `error_code`s   (function) |
| operator==operator!=operator<operator<=>(removed in C++20)(removed in C++20)(C++20) | compares `error_condition`s and `error_code`s   (function) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values in the `pair`   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values in the tuple   (function template) |
| operator==operator!=(removed in C++20) | compares the contents   (public member function of `std::bitset<N>`) |
| operator==operator!=(removed in C++20) | compares two allocator instances   (public member function of `std::allocator<T>`) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(C++20) | compares to another `unique_ptr` or with nullptr   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | compares with another `shared_ptr` or with nullptr   (function template) |
| operator==operator!=(removed in C++20) | compares a std::function with nullptr   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(C++11)(C++11)(C++11)(C++20) | compares two durations   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(C++11)(C++11)(C++11)(C++20) | compares two time points   (function template) |
| operator==operator!=(removed in C++20) | compares two `scoped_allocator_adaptor` objects   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(C++20) | compares the underlying std::type_info objects   (public member function of `std::type_index`) |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares two strings   (function template) |
| operator==operator!=(removed in C++20) | equality comparison between locale objects   (public member function of `std::locale`) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++20) | lexicographically compares the values of two `array`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `deque`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++20) | lexicographically compares the values of two `forward_list`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `list`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `vector`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `map`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `multimap`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `set`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `multiset`s   (function template) |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the values in the unordered_map   (function template) |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the values in the unordered_multimap   (function template) |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the values in the unordered_set   (function template) |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the values in the unordered_multiset   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | lexicographically compares the values of two `queue`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | lexicographically compares the values of two `stack`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | compares the underlying iterators   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(C++11)(C++11)(C++11)(C++20) | compares the underlying iterators   (function template) |
| operator==operator!=(removed in C++20) | compares two `istream_iterator`s   (function template) |
| operator==operator!=(removed in C++20) | compares two `istreambuf_iterator`s   (function template) |
| operator==operator!=(removed in C++20) | compares two complex numbers or a complex and a scalar   (function template) |
| operator==operator!=operator<operator<=operator>operator>= | compares two valarrays or a valarray with a value   (function template) |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the internal states of two pseudo-random number engines   (function) |
|  |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares two distribution objects   (function) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | compares a `sub_match` with another `sub_match`, a string, or a character   (function template) |
| operator==operator!=(removed in C++20) | lexicographically compares the values in the two match result   (function template) |
| operator==operator!=(removed in C++20) | compares two `regex_iterator`s   (public member function of `std::regex_iterator<BidirIt,CharT,Traits>`) |
| operator==operator!=(removed in C++20) | compares two `regex_token_iterator`s   (public member function of `std::regex_token_iterator<BidirIt,CharT,Traits>`) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | compares two `thread::id` objects   (function) |

The namespace std::rel_ops provides generic operators !=, >, <=, and >=:

|  |  |
| --- | --- |
| Defined in header `<utility>` | |
| Defined in namespace `std::rel_ops` | |
| operator!=operator>operator<=operator>=(deprecated in C++20) | automatically generates comparison operators based on user-defined operator== and operator<   (function template) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 583 (N3624) | C++98 | all six comparison operators could be used to compare a pointer with a null pointer constant | only equality operators are allowed |
| CWG 661 | C++98 | the actual semantics of arithmetic comparisons (e.g. whether 1 < 2 yields true or false) were unspecified | specification added |
| CWG 879 | C++98 | pointers to function types and pointers to void did not have built-in comparisons | added comparison specification for these pointers |
| CWG 1596 | C++98 | non-array objects were considered to belong to arrays with one element only for the purpose of pointer arithmetic | the rule is also applied to comparison |
| CWG 1598 | C++98 | two pointers to members of classes that are different and neither is the base class of the other did not compare equal even if the offsets of the pointed members can be the same | the result is unspecified in this case |
| CWG 1858 | C++98 | it was not clear whether two pointers to members that refer to different members of the same union compare equal as if they refer to the same member | they compare equal in this case |
| CWG 2419 | C++98 | a pointer to non-array object was only treated as a pointer to the first element of an array with size 1 in pointer comparison if the pointer is obtained by `&` | applies to all pointers to non-array objects |
| CWG 2526 | C++98 | the definition of relational comparison (`>`, `>=`, `<` and `<=`) of pointers to void and function pointers were removed by N3624 | restored |
| CWG 2796 | C++17 | function pointer conversions were not performed on the converted pointer operands during built-in pointer relational comparisons | performs these conversions in this case |

### See also

- Operator precedence
- Operator overloading
- Compare (named requirements)

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | increment decrement | arithmetic | logical | ****comparison**** | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b  a <=> b | a[...]  \*a  &a  a->b  a.b  a->\*b  a.\*b | function call  a(...) |
| comma  a, b |
| conditional  a ? b : c |
| Special operators | | | | | | |
| static_cast converts one type to another related type  dynamic_cast converts within inheritance hierarchies  const_cast adds or removes cv-qualifiers  reinterpret_cast converts type to unrelated type  C-style cast converts one type to another by a mix of static_cast, const_cast, and reinterpret_cast  new creates objects with dynamic storage duration  delete destructs objects previously created by the new expression and releases obtained memory area  sizeof queries the size of a type  sizeof... queries the size of a pack (since C++11)  typeid queries the type information of a type  noexcept checks if an expression can throw an exception (since C++11)  alignof queries alignment requirements of a type (since C++11) | | | | | | |

|  |  |
| --- | --- |
| C documentation for Comparison operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/operator_comparison&oldid=177936>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 22:28.