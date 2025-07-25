# std::optional<T>::operator=

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
| ****optional::operator=**** | | | | |
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
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | | | | |
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
| optional& operator=( std::nullopt_t ) noexcept; | (1) | (since C++17)  (constexpr since C++20) |
| constexpr optional& operator=( const optional& other ); | (2) | (since C++17) |
| constexpr optional& operator=( optional&& other ) noexcept(/\* see below \*/); | (3) | (since C++17) |
| template< class U = T >  optional& operator=( U&& value ); | (4) | (since C++17)  (constexpr since C++20) |
| template< class U >  optional& operator=( const optional<U>& other ); | (5) | (since C++17)  (constexpr since C++20) |
| template< class U >  optional& operator=( optional<U>&& other ); | (6) | (since C++17)  (constexpr since C++20) |
|  |  |  |

Replaces contents of \*this with the contents of other.

1) If \*this contains a value before the call, the contained value is destroyed by calling its destructor as if by value().T::~T(). \*this does not contain a value after this call.2,3) Assigns the state of other.  

- If both \*this and other do not contain a value, the function has no effect.
- If \*this contains a value, but other does not, then the contained value is destroyed by calling its destructor. \*this does not contain a value after the call.
- If other contains a value, then depending on whether \*this contains a value, the contained value is either direct-initialized or assigned from \*other (2) or std::move(\*other) (3). Note that a moved-from optional still **contains a value**.
- Overload (2) is deleted when either std::is_copy_constructible_v<T> or std::is_copy_assignable_v<T> is false. It is trivial if std::is_trivially_copy_constructible_v<T>, std::is_trivially_copy_assignable_v<T> and std::is_trivially_destructible_v<T> are all true.
- Overload (3) does not participate in overload resolution when either std::is_move_constructible_v<T> or std::is_move_assignable_v<T> is false. It is trivial if std::is_trivially_move_constructible_v<T>, std::is_trivially_move_assignable_v<T> and std::is_trivially_destructible_v<T> are all true.
4) Perfect-forwarded assignment: depending on whether \*this contains a value before the call, the contained value is either direct-initialized from std::forward<U>(value) or assigned from std::forward<U>(value). The function does not participate in overload resolution unless std::decay_t<U>(until C++20)std::remove_cvref_t<U>(since C++20) is not std::optional<T>, std::is_constructible_v<T, U> is true, std::is_assignable_v<T&, U> is true, and at least one of the following is true:  

- `T` is not a scalar type;
- std::decay_t<U> is not `T`.
5,6) Assigns the state of other.  

- If both \*this and other do not contain a value, the function has no effect.
- If \*this contains a value, but other does not, then the contained value is destroyed by calling its destructor. \*this does not contain a value after the call.
- If other contains a value, then depending on whether \*this contains a value, the contained value is either direct-initialized or assigned from \*other (5) or std::move(\*other) (6). Note that a moved-from optional still **contains a value**.
- These overloads do not participate in overload resolution unless the following conditions are met:
  - `T` is not constructible, convertible, or assignable from any expression of type (possibly const) std::optional<U>, i.e., the following 12 type traits are all false:
    - std::is_constructible_v<T, std::optional<U>&>
    - std::is_constructible_v<T, const std::optional<U>&>
    - std::is_constructible_v<T, std::optional<U>&&>
    - std::is_constructible_v<T, const std::optional<U>&&>
    - std::is_convertible_v<std::optional<U>&, T>
    - std::is_convertible_v<const std::optional<U>&, T>
    - std::is_convertible_v<std::optional<U>&&, T>
    - std::is_convertible_v<const std::optional<U>&&, T>
    - std::is_assignable_v<T&, std::optional<U>&>
    - std::is_assignable_v<T&, const std::optional<U>&>
    - std::is_assignable_v<T&, std::optional<U>&&>
    - std::is_assignable_v<T&, const std::optional<U>&&>
  - For overload (5), std::is_constructible_v<T, const U&> and std::is_assignable_v<T&, const U&> are both true.
  - For overload (6), std::is_constructible_v<T, U> and std::is_assignable_v<T&, U> are both true.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `optional` object whose contained value to assign |
| value | - | value to assign to the contained value |

### Return value

\*this

### Exceptions

2-6) Throws any exception thrown by the constructor or assignment operator of `T`. If an exception is thrown, the initialization state of \*this (and of other in case of (2,3) and (5,6)) is unchanged, i.e. if the object contained a value, it still contains a value, and the other way round. The contents of value and the contained values of \*this and other depend on the exception safety guarantees of the operation from which the exception originates (copy-constructor, move-assignment, etc.).3) Has followingnoexcept specification:noexcept(std::is_nothrow_move_assignable_v<T> && std::is_nothrow_move_constructible_v<T>)

### Notes

An optional object `op` may be turned into an empty optional with both op = {}; and op = nullopt;. The first expression constructs an empty optional object with {} and assigns it to `op`.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_optional` | `202106L` | (C++20) (DR20) | Fully constexpr (1), (4-6) |

### Example

Run this code

```
#include <iostream>
#include <optional>
 
int main()
{
    std::optional<const char*> s1 = "abc", s2; // constructor
    s2 = s1; // assignment
    s1 = "def"; // decaying assignment (U = char[4], T = const char*)
    std::cout << *s2 << ' ' << *s1 << '\n';
}

```

Output:

```
abc def

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P0602R4 | C++17 | copy/move assignment operator may not be trivial even if underlying operations are trivial | required to propagate triviality |
| P2231R1 | C++20 | converting assignment operators (1) and (4-6) were not constexpr while the required operations can be in C++20 | made constexpr |

### See also

|  |  |
| --- | --- |
| emplace | constructs the contained value in-place   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/optional/operator%3D&oldid=172854>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 June 2024, at 18:26.