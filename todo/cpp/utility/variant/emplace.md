# std::variant<Types...>::emplace

From cppreference.com
< cpp‎ | utility‎ | variant
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

std::variant

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| variant::variant | | | | |
| variant::~variant | | | | |
| variant::operator= | | | | |
| Observers | | | | |
| variant::index | | | | |
| variant::valueless_by_exception | | | | |
| Modifiers | | | | |
| ****variant::emplace**** | | | | |
| variant::swap | | | | |
| Visitation | | | | |
| variant::visit(C++26) | | | | |
| Non-member functions | | | | |
| visit(std::variant) | | | | |
| holds_alternative | | | | |
| get(std::variant) | | | | |
| get_if | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | | | | |
| swap(std::variant) | | | | |
| Helper classes | | | | |
| monostate | | | | |
| bad_variant_access | | | | |
| variant_size | | | | |
| variant_alternative | | | | |
| hash<std::variant> | | | | |
| Helper objects | | | | |
| variant_npos | | | | |

|  |  |  |
| --- | --- | --- |
| template< class T, class... Args >  T& emplace( Args&&... args ); | (1) | (since C++17)  (constexpr since C++20) |
| template< class T, class U, class... Args >  T& emplace( std::initializer_list<U> il, Args&&... args ); | (2) | (since C++17)  (constexpr since C++20) |
| template< std::size_t I, class... Args >  std::variant_alternative_t<I, variant>& emplace( Args&&... args ); | (3) | (since C++17)  (constexpr since C++20) |
| template< std::size_t I, class U, class... Args >  std::variant_alternative_t<I, variant>&     emplace( std::initializer_list<U> il, Args&&... args ); | (4) | (since C++17)  (constexpr since C++20) |
|  |  |  |

Creates a new value in-place, in an existing `variant` object

1) Equivalent to emplace<I>(std::forward<Args>(args)...), where `I` is the zero-based index of `T` in `Types...`.

- This overload participates in overload resolution only if std::is_constructible_v<T, Args...> is true, and `T` occurs exactly once in `Types...`.
2) Equivalent to emplace<I>(il, std::forward<Args>(args)...), where `I` is the zero-based index of `T` in `Types...`.

- This overload participates in overload resolution only if std::is_constructible_v<T, std::initializer_list<U>&, Args...> is true, and `T` occurs exactly once in `Types...`.
3) First, destroys the currently contained value (if any). Then direct-initializes the contained value as if constructing a value of type `T_I` with the arguments std::forward<Args>(args).... If an exception is thrown, \*this may become `valueless_by_exception`.

- This overload participates in overload resolution only if std::is_constructible_v<T_I, Args...> is true.
- It is a compile-time error if `I` is not less than sizeof...(Types).
4) First, destroys the currently contained value (if any). Then direct-initializes the contained value as if constructing a value of type `T_I` with the arguments il, std::forward<Args>(args).... If an exception is thrown, \*this may become `valueless_by_exception`.

- This overload participates in overload resolution only if std::is_constructible_v<T_I, std::initializer_list<U>&, Args...> is true.
- It is a compile-time error if `I` is not less than sizeof...(Types).

### Parameters

|  |  |  |
| --- | --- | --- |
| args | - | constructor arguments to use when constructing the new value |
| il | - | initializer_list argument to use when constructing the new value |

### Return value

A reference to the new contained value.

### Exceptions

1-4) Any exception thrown during the initialization of the contained value.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_variant` | `202106L` | (C++20) (DR) | Fully constexpr `std::variant` (1-4) |

### Example

Run this code

```
#include <iostream>
#include <string>
#include <variant>
 
int main()
{
    std::variant<std::string> v1;
    v1.emplace<0>("abc"); // OK
    std::cout << std::get<0>(v1) << '\n';
    v1.emplace<std::string>("def"); // OK
    std::cout << std::get<0>(v1) << '\n';
 
    std::variant<std::string, std::string> v2;
    v2.emplace<1>("ghi"); // OK
    std::cout << std::get<1>(v2) << '\n';
    // v2.emplace<std::string>("abc"); -> Error
}

```

Output:

```
abc
def
ghi

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2231R1 | C++20 | `emplace` was not constexpr while the required operations can be constexpr in C++20 | made constexpr |

### See also

|  |  |
| --- | --- |
| operator= | assigns a `variant`   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/variant/emplace&oldid=172839>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 June 2024, at 14:33.