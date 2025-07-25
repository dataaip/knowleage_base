# operator==, !=, <, <=, >, >=, <=>(std::optional)

From cppreference.com
< cpp‎ | utility‎ | optional
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

std::optional

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| optional::optional | | | | |
| optional::~optional | | | | |
| optional::operator= | | | | |
| Observers | | | | |
| optional::operator->optional::operator\* | | | | |
| optional::operator booloptional::has_value | | | | |
| optional::value | | | | |
| optional::value_or | | | | |
| Iterators | | | | |
| optional::begin(C++26) | | | | |
| optional::end(C++26) | | | | |
| Monadic operations | | | | |
| optional::and_then(C++23) | | | | |
| optional::transform(C++23) | | | | |
| optional::or_else(C++23) | | | | |
| Modifiers | | | | |
| optional::emplace | | | | |
| optional::swap | | | | |
| optional::reset | | | | |
| Non-member functions | | | | |
| ****operator==operator!=operator<operator<=operator>operator>=operator<=>****(C++20) | | | | |
| make_optional | | | | |
| swap(std::optional) | | | | |
| Deduction guides | | | | |
| Helper classes | | | | |
| hash<std::optional> | | | | |
| nullopt_t | | | | |
| in_place_t | | | | |
| bad_optional_access | | | | |
| Helper objects | | | | |
| nullopt | | | | |
| in_place | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<optional>` |  |  |
| Compare two `optional` objects |  |  |
| template< class T, class U >  constexpr bool operator==( const optional<T>& lhs, const optional<U>& rhs ); | (1) | (since C++17) |
| template< class T, class U >  constexpr bool operator!=( const optional<T>& lhs, const optional<U>& rhs ); | (2) | (since C++17) |
| template< class T, class U >  constexpr bool operator<( const optional<T>& lhs, const optional<U>& rhs ); | (3) | (since C++17) |
| template< class T, class U >  constexpr bool operator<=( const optional<T>& lhs, const optional<U>& rhs ); | (4) | (since C++17) |
| template< class T, class U >  constexpr bool operator>( const optional<T>& lhs, const optional<U>& rhs ); | (5) | (since C++17) |
| template< class T, class U >  constexpr bool operator>=( const optional<T>& lhs, const optional<U>& rhs ); | (6) | (since C++17) |
| template< class T, std::three_way_comparable_with<T> U >  constexpr std::compare_three_way_result_t<T, U>     operator<=>( const optional<T>& lhs, const optional<U>& rhs ); | (7) | (since C++20) |
| Compare an `optional` object with a `nullopt` |  |  |
| template< class T >  constexpr bool operator==( const optional<T>& opt, std::nullopt_t ) noexcept; | (8) | (since C++17) |
| template< class T >  constexpr bool operator==( std::nullopt_t, const optional<T>& opt ) noexcept; | (9) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator!=( const optional<T>& opt, std::nullopt_t ) noexcept; | (10) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator!=( std::nullopt_t, const optional<T>& opt ) noexcept; | (11) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator<( const optional<T>& opt, std::nullopt_t ) noexcept; | (12) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator<( std::nullopt_t, const optional<T>& opt ) noexcept; | (13) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator<=( const optional<T>& opt, std::nullopt_t ) noexcept; | (14) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator<=( std::nullopt_t, const optional<T>& opt ) noexcept; | (15) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator>( const optional<T>& opt, std::nullopt_t ) noexcept; | (16) | (since C++17)  (until C++20) |
| template< class T >  constexpr bool operator>( std::nullopt_t, const optional<T>& opt ) noexcept; | (17) | (since C++17)  (until C++20) |
| template< class T >   constexpr bool operator>=( const optional<T>& opt, std::nullopt_t ) noexcept; | (18) | (since C++17)  (until C++20) |
| template< class T >   constexpr bool operator>=( std::nullopt_t, const optional<T>& opt ) noexcept; | (19) | (since C++17)  (until C++20) |
| template< class T >  constexpr std::strong_ordering     operator<=>( const optional<T>& opt, std::nullopt_t ) noexcept; | (20) | (since C++20) |
| Compare an `optional` object with a value |  |  |
| template< class T, class U >  constexpr bool operator==( const optional<T>& opt, const U& value ); | (21) | (since C++17) |
| template< class U, class T >  constexpr bool operator==( const U& value, const optional<T>& opt ); | (22) | (since C++17) |
| template< class T, class U >  constexpr bool operator!=( const optional<T>& opt, const U& value ); | (23) | (since C++17) |
| template< class U, class T >  constexpr bool operator!=( const U& value, const optional<T>& opt ); | (24) | (since C++17) |
| template< class T, class U >  constexpr bool operator<( const optional<T>& opt, const U& value ); | (25) | (since C++17) |
| template< class U, class T >  constexpr bool operator<( const U& value, const optional<T>& opt ); | (26) | (since C++17) |
| template< class T, class U >  constexpr bool operator<=( const optional<T>& opt, const U& value ); | (27) | (since C++17) |
| template< class U, class T >  constexpr bool operator<=( const U& value, const optional<T>& opt ); | (28) | (since C++17) |
| template< class T, class U >  constexpr bool operator>( const optional<T>& opt, const U& value ); | (29) | (since C++17) |
| template< class U, class T >  constexpr bool operator>( const U& value, const optional<T>& opt ); | (30) | (since C++17) |
| template< class T, class U >  constexpr bool operator>=( const optional<T>& opt, const U& value ); | (31) | (since C++17) |
| template< class U, class T >  constexpr bool operator>=( const U& value, const optional<T>& opt ); | (32) | (since C++17) |
| template< class T, std::three_way_comparable_with<T> U >  constexpr std::compare_three_way_result_t<T, U>     operator<=>( const optional<T>& opt, const U& value ); | (33) | (since C++20) |
|  |  |  |

Performs comparison operations on `optional` objects.

1-7) Compares two `optional` objects, lhs and rhs. The contained values are compared (using the corresponding operator of `T`) only if both lhs and rhs contain values. Otherwise,

- lhs is considered **equal to** rhs if, and only if, both lhs and rhs do not contain a value.
- lhs is considered **less than** rhs if, and only if, rhs contains a value and lhs does not.
1-6) Let @ denote the corresponding comparison operator, for each of these functions:

|  |  |
| --- | --- |
| If the corresponding expression \*lhs @ \*rhs is ill-formed or its result is not convertible to bool, the program is ill-formed. | (until C++26) |
| This overload participates in overload resolution only if the corresponding expression \*lhs @ \*rhs is well-formed and its result is convertible to bool. | (since C++26) |

8-20) Compares opt with a `nullopt`. Equivalent to (1-6) when comparing to an `optional` that does not contain a value.

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

21-33) Compares opt with a value. The values are compared (using the corresponding operator of `T`) only if opt contains a value. Otherwise, opt is considered **less than** value.21-32) Let @ denote the corresponding comparison operator, for each of these functions:

|  |  |
| --- | --- |
| If the corresponding expression \*opt @ value or value @ \*opt (depending on the positions of the operands) is ill-formed or its result is not convertible to bool, the program is ill-formed. | (until C++26) |
| This overload participates in overload resolution only if all following conditions are satisfied:   - `U` is not a specialization of std::optional. - The corresponding expression \*opt @ value or value @ \*opt (depending on the positions of the operands) is well-formed and its result is convertible to bool. | (since C++26) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs, opt | - | an `optional` object to compare |
| value | - | value to compare to the contained value |

### Return value

1) lhs.has_value() != rhs.has_value() ? false :  
    (lhs.has_value() == false ? true : \*lhs == \*rhs)2) lhs.has_value() != rhs.has_value() ? true :  
    (lhs.has_value() == false ? false : \*lhs != \*rhs)3) !rhs ? false : (!lhs ? true : \*lhs < \*rhs)4) !lhs ? false : (!rhs ? true : \*lhs > \*rhs)5) !lhs ? true : (!rhs ? false : \*lhs <= \*rhs)6) !rhs ? true : (!lhs ? false : \*lhs >= \*rhs)7) lhs && rhs ? \*lhs <=> \*rhs : lhs.has_value() <=> rhs.has_value()8,9) !opt10,11) opt.has_value()12) false13) opt.has_value()14) !opt15) true16) opt.has_value()17) false18) true19) !opt20) opt.has_value() <=> false21) opt.has_value() ? \*opt == value : false22) opt.has_value() ? value == \*opt : false23) opt.has_value() ? \*opt != value : true24) opt.has_value() ? value != \*opt : true25) opt.has_value() ? \*opt < value  : true26) opt.has_value() ? value < \*opt  : false27) opt.has_value() ? \*opt <= value : true28) opt.has_value() ? value <= \*opt : false29) opt.has_value() ? \*opt > value  : false30) opt.has_value() ? value > \*opt  : true31) opt.has_value() ? \*opt >= value : false32) opt.has_value() ? value >= \*opt : true33) opt.has_value() ? \*opt <=> value : std::strong_ordering::less

### Exceptions

1-7) May throw implementation-defined exceptions.21-33) Throws when and what the comparison throws.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_constrained_equality` | `202403L` | (C++26) | constrained comparison operators for std::optional |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2945 | C++17 | order of template parameters inconsistent for compare-with-T cases | made consistent |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/optional/operator_cmp&oldid=179393>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 January 2025, at 18:55.