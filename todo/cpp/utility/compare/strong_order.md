# std::strong_order

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | ****strong_order****(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<compare>` |  |  |
| inline namespace /\* unspecified \*/ {  inline constexpr /\* unspecified \*/ strong_order = /\* unspecified \*/; } |  | (since C++20) |
| Call signature |  |  |
| template< class T, class U >      requires /\* see below \*/ constexpr std::strong_ordering strong_order( T&& t, U&& u ) noexcept(/\* see below \*/); |  |  |
|  |  |  |

Compares two values using 3-way comparison and produces a result of type `std::strong_ordering`.

Let t and u be expressions and `T` and `U` denote decltype((t)) and decltype((u)) respectively, std::strong_order(t, u) is expression-equivalent to:

- If std::is_same_v<std::decay_t<T>, std::decay_t<U>> is true:
  - std::strong_ordering(strong_order(t, u)), if it is a well-formed expression with overload resolution performed in a context that does not include a declaration of `std::strong_order`,
  - otherwise, if `T` is a floating-point type:
    - if std::numeric_limits<T>::is_iec559 is true, performs the ISO/IEC/IEEE 60559 **totalOrder** comparison of floating-point values and returns that result as a value of type std::strong_ordering (note: this comparison can distinguish between the positive and negative zero and between the NaNs with different representations),
    - otherwise, yields a value of type std::strong_ordering that is consistent with the ordering observed by `T`'s comparison operators,
  - otherwise, std::strong_ordering(std::compare_three_way()(t, u)) if it is well-formed.
- In all other cases, the expression is ill-formed, which can result in substitution failure when it appears in the immediate context of a template instantiation.

### Customization point objects

The name `std::strong_order` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__strong_order_fn`.

All instances of `__strong_order_fn` are equal. The effects of invoking different instances of type `__strong_order_fn` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `std::strong_order` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `std::strong_order` above, `__strong_order_fn` models

- std::invocable<__strong_order_fn, Args...>,
- std::invocable<const __strong_order_fn, Args...>,
- std::invocable<__strong_order_fn&, Args...>, and
- std::invocable<const __strong_order_fn&, Args...>.

Otherwise, no function call operator of `__strong_order_fn` participates in overload resolution.

#### Strict total order of IEEE floating-point types

Let x and y be values of same IEEE floating-point type, and total_order_less(x, y) be the boolean result indicating if x precedes y in the strict total order defined by **totalOrder** in ISO/IEC/IEEE 60559.

(total_order_less(x, y) || total_order_less(y, x)) == false if and only if x and y have the same bit pattern.

- if neither x nor y is NaN:
  - if x < y, then total_order_less(x, y) == true;
  - if x > y, then total_order_less(x, y) == false;
  - if x == y,
    - if x is negative zero and y is positive zero, total_order_less(x, y) == true,
    - if x is not zero and x's exponent field is less than y's, then total_order_less(x, y) == (x > 0) (only meaningful for decimal floating-point number);
- if either x or y is NaN:
  - if x is negative NaN and y is not negative NaN, then total_order_less(x, y) == true,
  - if x is not positive NaN and y is positive NaN, then total_order_less(x, y) == true,
  - if both x and y are NaNs with the same sign and x's mantissa field is less than y's, then total_order_less(x, y) == !std::signbit(x).

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| strong_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators and is substitutable   (class) |
| weak_order(C++20) | performs 3-way comparison and produces a result of type `std::weak_ordering` (customization point object) |
| partial_order(C++20) | performs 3-way comparison and produces a result of type `std::partial_ordering` (customization point object) |
| compare_strong_order_fallback(C++20) | performs 3-way comparison and produces a result of type `std::strong_ordering`, even if operator<=> is unavailable (customization point object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/compare/strong_order&oldid=150890>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 April 2023, at 19:02.