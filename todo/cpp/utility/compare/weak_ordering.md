# std::weak_ordering

From cppreference.com
< cpp‎ | utility
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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | ****weak_ordering****(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<compare>` |  |  |
| class weak_ordering; |  | (since C++20) |
|  |  |  |

The class type `std::weak_ordering` is the result type of a three-way comparison that:

- Admits all six relational operators (`==`, `!=`, `<`, `<=`, `>`, `>=`).

- Does not imply substitutability: if a is equivalent to b, f(a) may not be equivalent to f(b), where f denotes a function that reads only comparison-salient state that is accessible via the argument's public const members. In other words, equivalent values may be distinguishable.
- Does not allow incomparable values: exactly one of a < b, a == b, or a > b must be true.

### Constants

The type `std::weak_ordering` has three valid values, implemented as const static data members of its type:

|  |  |
| --- | --- |
| Name | Definition |
| inline constexpr std::weak_ordering less[static] | a valid value indicating less-than (ordered before) relationship   (public static member constant) |
| inline constexpr std::weak_ordering equivalent[static] | a valid value indicating equivalence (neither ordered before nor ordered after)   (public static member constant) |
| inline constexpr std::weak_ordering greater[static] | a valid value indicating greater-than (ordered after) relationship   (public static member constant) |

### Conversions

`std::weak_ordering` is implicitly-convertible to std::partial_ordering, while std::strong_ordering is implicitly-convertible to weak_ordering.

|  |  |
| --- | --- |
| ****operator partial_ordering**** | implicit conversion to std::partial_ordering   (public member function) |

## std::weak_ordering::operator partial_ordering

|  |  |  |
| --- | --- | --- |
| constexpr operator partial_ordering() const noexcept; |  |  |
|  |  |  |

### Return value

std::partial_ordering::less if `v` is `less`, std::partial_ordering::greater if `v` is `greater`,
std::partial_ordering::equivalent if `v` is `equivalent`.

### Comparisons

Comparison operators are defined between values of this type and literal ​0​. This supports the expressions a <=> b == 0 or a <=> b < 0 that can be used to convert the result of a three-way comparison operator to a boolean relationship; see std::is_eq, std::is_lt, etc.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::weak_ordering` is an associated class of the arguments.

The behavior of a program that attempts to compare a `weak_ordering` with anything other than the integer literal ​0​ is undefined.

|  |  |
| --- | --- |
| ****operator==operator<operator>operator<=operator>=operator<=>**** | compares with zero or a `weak_ordering`   (function) |

## operator==

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator==( weak_ordering v, /\*unspecified\*/ u ) noexcept; | (1) |  |
| friend constexpr bool operator==( weak_ordering v, weak_ordering w ) noexcept = default; | (2) |  |
|  |  |  |

### Parameters

|  |  |  |
| --- | --- | --- |
| v, w | - | `std::weak_ordering` values to check |
| u | - | an unused parameter of any type that accepts literal zero argument |

### Return value

1) true if `v` is `equivalent`, false if `v` is `less` or `greater`2) true if both parameters hold the same value, false otherwise

## operator<

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator<( weak_ordering v, /\*unspecified\*/ u ) noexcept; | (1) |  |
| friend constexpr bool operator<( /\*unspecified\*/ u, weak_ordering v ) noexcept; | (2) |  |
|  |  |  |

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | a `std::weak_ordering` value to check |
| u | - | an unused parameter of any type that accepts literal zero argument |

### Return value

1) true if `v` is `less`, and false if `v` is `greater` or `equivalent`2) true if `v` is `greater`, and false if `v` is `less` or `equivalent`

## operator<=

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator<=( weak_ordering v, /\*unspecified\*/ u ) noexcept; | (1) |  |
| friend constexpr bool operator<=( /\*unspecified\*/ u, weak_ordering v ) noexcept; | (2) |  |
|  |  |  |

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | a `std::weak_ordering` value to check |
| u | - | an unused parameter of any type that accepts literal zero argument |

### Return value

1) true if `v` is `less` or `equivalent`, and false if `v` is `greater`2) true if `v` is `greater` or `equivalent`, and false if `v` is `less`

## operator>

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator>( weak_ordering v, /\*unspecified\*/ u ) noexcept; | (1) |  |
| friend constexpr bool operator>( /\*unspecified\*/ u, weak_ordering v ) noexcept; | (2) |  |
|  |  |  |

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | a `std::weak_ordering` value to check |
| u | - | an unused parameter of any type that accepts literal zero argument |

### Return value

1) true if `v` is `greater`, and false if `v` is `less` or `equivalent`2) true if `v` is `less`, and false if `v` is `greater` or `equivalent`

## operator>=

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator>=( weak_ordering v, /\*unspecified\*/ u ) noexcept; | (1) |  |
| friend constexpr bool operator>=( /\*unspecified\*/ u, weak_ordering v ) noexcept; | (2) |  |
|  |  |  |

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | a `std::weak_ordering` value to check |
| u | - | an unused parameter of any type that accepts literal zero argument |

### Return value

1) true if `v` is `greater` or `equivalent`, and false if `v` is `less`2) true if `v` is `less` or `equivalent`, and false if `v` is `greater`

## operator<=>

|  |  |  |
| --- | --- | --- |
| friend constexpr weak_ordering operator<=>( weak_ordering v, /\*unspecified\*/ u ) noexcept; | (1) |  |
| friend constexpr weak_ordering operator<=>( /\*unspecified\*/ u, weak_ordering v ) noexcept; | (2) |  |
|  |  |  |

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | a `std::weak_ordering` value to check |
| u | - | an unused parameter of any type that accepts literal zero argument |

### Return value

1) v.2) `greater` if `v` is `less`, `less` if `v` is `greater`, otherwise `v`.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| strong_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators and is substitutable   (class) |
| partial_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators, is not substitutable, and allows incomparable values   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/compare/weak_ordering&oldid=173502>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 July 2024, at 05:00.