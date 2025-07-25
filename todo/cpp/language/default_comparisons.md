# Default comparisons (since C++20)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | ****Default comparisons**** (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Comparison operator functions can be explicitly defaulted to request the compiler to generate the corresponding default comparison for a class.

### Definition

A **defaulted comparison operator function** is a non-template comparison operator function (i.e. `<=>`, `==`, `!=`, `<`, `>`, `<=`, or `>=`) satisfying all following conditions:

- It is a non-static member or friend of some class `C`.
- It is defined as defaulted in `C` or in a context where `C` is complete.
- It has two parameters of type const C& or two parameters of type `C`, where the implicit object parameter (if any) is considered to be the first parameter.

Such a comparison operator function is termed a **defaulted comparison operator function for class `C`**.

```
struct X
{
    bool operator==(const X&) const = default; // OK
    bool operator==(const X&) = default;       // Error: the implicit object
                                               //        parameter type is X&
    bool operator==(this X, X) = default;      // OK
};
 
struct Y
{
    friend bool operator==(Y, Y) = default;        // OK
    friend bool operator==(Y, const Y&) = default; // Error: different parameter types
};
 
bool operator==(const Y&, const Y&) = default;     // Error: not a friend of Y

```

Name lookups and access checks in the implicit definition of a comparison operator function are performed from a context equivalent to its function body. A definition of a comparison operator function as defaulted that appears in a class must be the first declaration of that function.

### Default comparison order

Given a class `C`, a subobject list is formed by the following subjects in order:

- The direct base class subobjects of `C`, in declaration order.
- The non-static data members of `C`, in declaration order.

:   - If any member subobject is of array type, it is expanded to the sequence of its elements, in the order of increasing subscript. The expansion is recursive: array elements of array types will be expanded again until there is no subobject of array type.

For any object x of type `C`, in the following descriptions:

- Let n be the number of subobjects in the (expanded) subobject list for x.
- Let x_i be the ith subobject in the (expanded) subobject list for x, where x_i is formed by a sequence of derived-to-base conversions, class member access expressions, and array subscript expressions applied to x.

```
struct S {};
 
struct T : S
{
    int arr[2][2];
} t;
 
// The subobject list for “t” consists of the following 5 subobjects in order:
// (S)t → t[0][0] → t[0][1] → t[1][0] → t[1][1]

```

### Three-way comparison

An operator<=> for a class type can be defined as defaulted with any return type.

#### Comparison category types

There are three comparison category types:

- std::strong_ordering
- std::weak_ordering
- std::partial_ordering

| Type | Equivalent values are.. | Incomparable values are.. |
| --- | --- | --- |
| std::strong_ordering | indistinguishable | not allowed |
| std::weak_ordering | distinguishable | not allowed |
| std::partial_ordering | distinguishable | allowed |

#### Synthesized three-way comparison

The **synthesized three-way comparison** of type `T` between glvalues a and b of the same type is defined as follows:

- If the overload resolution for a <=> b results in a usable candidate, and can be explicitly converted to `T` using `static_cast`, the synthesized comparison is static_cast<T>(a <=> b).
- Otherwise, if any of the following condition is satisfied, the synthesized comparison is not defined:

:   - The overload resolution for a <=> b finds at least one viable candidate.
    - `T` is not a comparison category type.
    - The overload resolution for a == b does not result in a usable candidate.
    - The overload resolution for a < b does not result in a usable candidate.

- Otherwise, if `T` is std::strong_ordering, the synthesized comparison is

```
a == b ? std::strong_ordering::equal :
a < b  ? std::strong_ordering::less :
         std::strong_ordering::greater

```

- Otherwise, if `T` is std::weak_ordering, the synthesized comparison is

```
a == b ? std::weak_ordering::equivalent :
a < b  ? std::weak_ordering::less :
         std::weak_ordering::greater

```

- Otherwise (`T` is std::partial_ordering), the synthesized comparison is

```
a == b ? std::partial_ordering::equivalent :
a < b  ? std::partial_ordering::less :
b < a  ? std::partial_ordering::greater : 
         std::partial_ordering::unordered

```

#### Placeholder return type

If the declared return type of a defaulted three-way comparison operator function (operator<=>) for a class type `C` is auto, the return type is deduced from the return types of the three-way comparisons between the corresponding subobjects of an object x of type `C`.

For each subobject x_i in the (expanded) subobject list for x:

1. Perform overload resolution for x_i <=> x_i, if the overload resolution does not result in a usable candidate, the defaulted operator<=> is defined as deleted.
2. Denote the cv-unqualified version of the type of x_i <=> x_i as `R_i`, if `R_i` is not a comparison category type, the defaulted operator<=> is defined as deleted.

If the defaulted operator<=> is not defined as deleted, its return type is deduced as std::common_comparison_category_t<R_1, R_2, ..., R_n>.

#### Non-placeholder return type

If the declared return type of the defaulted operator<=> is not auto, it cannot contain any placeholder type (e.g. decltype(auto)).

If there is a subobject x_i in the (expanded) subobject list for x such that the synthesized three-way comparison of the declared return type between x_i and x_i is not defined, the defaulted operator<=> is defined as deleted.

#### Comparison result

Let x and y be the parameters of a defaulted operator<=>, denote each subobject in the (expanded) subobject list for x and y as x_i and y_i respectively. The default three-way comparison between x and y is performed by comparing corresponding subobjects x_i and y_i with increasing i order.

Let `R` be the (possibly-deduced) return type, the comparison result between x_i and y_i is the result of the synthesized three-way comparison of type `R` between x_i and y_i.

- During the default three-way comparison between x and y, if a subobject-wise comparison between x_i and y_i generates a result v_i such that contextually converting v_i != 0 to bool yields true, the return value is a copy of v_i (the remaining subobjects will not be compared).
- Otherwise, the return value is static_cast<R>(std::strong_ordering::equal).

Run this code

```
#include <compare>
#include <iostream>
#include <set>
 
struct Point
{
    int x;
    int y;
    auto operator<=>(const Point&) const = default;
    /* non-comparison functions */
};
 
int main()
{
    Point pt1{1, 1}, pt2{1, 2};
    std::set<Point> s; // OK
    s.insert(pt1);     // OK
 
    // two-way comparison operator functions are not required to be explicitly defined:
    // operator== is implicitly declared (see below)
    // the overload resolutions of other candidates will select rewritten candidates 
    std::cout << std::boolalpha
        << (pt1 == pt2) << ' '  // false
        << (pt1 != pt2) << ' '  // true
        << (pt1 <  pt2) << ' '  // true
        << (pt1 <= pt2) << ' '  // true
        << (pt1 >  pt2) << ' '  // false
        << (pt1 >= pt2) << ' '; // false
}

```

### Equality comparison

#### Explicit declaration

An operator== for a class type can be defined as defaulted with return type bool.

Given a class `C` and an object x of type `C`, if there is a subobject x_i in the (expanded) subobject list for x such that the overload resolution for x_i == x_i does not result in a usable candidate, the defaulted operator== is defined as deleted.

Let x and y be the parameters of a defaulted operator==, denote each subobject in the (expanded) subobject list for x and y as x_i and y_i respectively. The default equality comparison between x and y is performed by comparing corresponding subobjects x_i and y_i with increasing i order.

The comparison result between x_i and y_i is the result of x_i == y_i.

- During the default equality comparison between x and y, if a subobject-wise comparison between x_i and y_i generates a result v_i such that contextually converting v_i to bool yields false, the return value is false (the remaining subobjects will not be compared).
- Otherwise, the return value is true.

Run this code

```
#include <iostream>
 
struct Point
{
    int x;
    int y;
    bool operator==(const Point&) const = default;
    /* non-comparison functions */
};
 
int main()
{
    Point pt1{3, 5}, pt2{2, 5};
    std::cout << std::boolalpha
        << (pt1 != pt2) << '\n'  // true
        << (pt1 == pt1) << '\n'; // true
 
    struct [[maybe_unused]] { int x{}, y{}; } p, q;
    // if (p == q) {} // Error: operator== is not defined
}

```

#### Implicit declaration

If a class `C` does not explicitly declare any member or friend named operator==, an  operator function is declared implicitly for each operator<=> defined as defaulted. Each implicity-declared operator== have the same access and function definition and in the same class scope as the respective defaulted operator<=>, with the following changes:

- The declarator identifier is replaced with operator==.
- The return type is replaced with bool.

```
template<typename T>
struct X
{
    friend constexpr std::partial_ordering operator<=>(X, X)
        requires (sizeof(T) != 1) = default;
    // implicitly declares: friend constexpr bool operator==(X, X)
    //                          requires (sizeof(T) != 1) = default;
 
    [[nodiscard]] virtual std::strong_ordering operator<=>(const X&) const = default;
    // implicitly declares: [[nodiscard]] virtual bool
    //                          operator==(const X&) const = default;
};

```

### Secondary comparison

A secondary comparison operator function (`!=`, `<`, `>`, `<=`, or `>=`) for a class type can be defined as defaulted with return type bool.

Let `@` be one of the five secondary comparison operators, for each defaulted operator@ with parameters x and y, up to two overloads resolutions are performed (not considering the defaulted operator@ as a candidate) to determine whether it is defined as deleted.

- The first overload resolution is performed for x @ y. If the overload resolution does not result in a usable candidate, or the selected candidate is not a rewritten candidate, the defaulted operator@ is defined as deleted. There is no second overload resolution in these cases.
- The second overload resolution is performed for the selected rewritten candidate of x @ y. If the overload resolution does not result in a usable candidate, the defaulted operator@ is defined as deleted.

If is x @ y cannot be implicitly converted to bool, the defaulted operator@ is defined as deleted.

If the defaulted operator@ is not defined as deleted, it yields x @ y.

```
struct HasNoRelational {};
 
struct C
{
    friend HasNoRelational operator<=>(const C&, const C&);
    bool operator<(const C&) const = default; // OK, function is defaulted
};

```

### Keywords

default

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2539 | C++20 | the synthesized three-way comparison would choose static_cast even if the explicit conversion is not available | does not choose static_cast in this case |
| CWG 2546 | C++20 | the defaulted secondary operator@ was not defined as deleted if the overload resolution of x @ y selects a non-usable rewritten candidate | defined as deleted in this case |
| CWG 2547 | C++20 | it was unclear whether comparison operator functions for non-classes can be defaulted | they cannot be defaulted |
| CWG 2568 | C++20 | the implicit definition of comparison operator functions might violate member access rules | access checks are performed from a context equivalent to their function bodies |

### See also

- overload resolution in a call to an overloaded operator
- Built-in three-way comparison operator
- Operator overloading for comparison operators
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/default_comparisons&oldid=175305>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 August 2024, at 17:33.