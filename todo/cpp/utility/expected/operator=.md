# std::expected<T,E>::operator=

From cppreference.com
< cpp‎ | utility‎ | expected
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

std::expected

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| expected::expected | | | | |
| expected::~expected | | | | |
| ****expected::operator=**** | | | | |
| Observers | | | | |
| expected::operator->expected::operator\* | | | | |
| expected::operator boolexpected::has_value | | | | |
| expected::value | | | | |
| expected::error | | | | |
| expected::value_or | | | | |
| expected::error_or | | | | |
| Monadic operations | | | | |
| expected::and_then | | | | |
| expected::or_else | | | | |
| expected::transform | | | | |
| expected::transform_error | | | | |
| Modifiers | | | | |
| expected::emplace | | | | |
| expected::swap | | | | |
| Non-member functions | | | | |
| operator==(std::expected) | | | | |
| swap(std::expected) | | | | |
| Helper classes | | | | |
| unexpected | | | | |
| bad_expected_access | | | | |
| unexpect_tunexpect | | | | |

|  |  |  |
| --- | --- | --- |
| Primary template |  |  |
| constexpr expected& operator=( const expected& other ); | (1) | (since C++23) |
| constexpr expected& operator=( expected&& other )      noexcept(/\* see below \*/); | (2) | (since C++23) |
| template< class U = T >  constexpr expected& operator=( U&& v ); | (3) | (since C++23) |
| template< class G >  constexpr expected& operator=( const std::unexpected<G>& e ); | (4) | (since C++23) |
| template< class G >  constexpr expected& operator=( std::unexpected<G>&& e ); | (5) | (since C++23) |
| void partial specialization |  |  |
| constexpr expected& operator=( const expected& other ); | (6) | (since C++23) |
| constexpr expected& operator=( expected&& other )      noexcept(/\* see below \*/); | (7) | (since C++23) |
| template< class G >  constexpr expected& operator=( const std::unexpected<G>& e ); | (8) | (since C++23) |
| template< class G >  constexpr expected& operator=( std::unexpected<G>&& e ); | (9) | (since C++23) |
| Helper function template |  |  |
| template< class T, class U, class... Args >  constexpr void reinit-expected( T& newval, U& oldval, Args&&... args ) | (10) | (since C++23)  (exposition only\*) |
|  |  |  |

Assigns a new value to an existing `expected` object.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `expected` object whose contained value to assign |
| v | - | value to assign to the contained value |
| e | - | std::unexpected object whose contained value to assign |
| newval | - | the contained value to be constructed |
| oldval | - | the contained value to be destroyed |
| args | - | the arguments used as initializers of newval |

### Effects

#### Primary template assignment operators

1,2) Assigns the state of other to \*this. If `has_value()` and rhs.has_value() have different values (i.e. one of \*this and other contains an expected value `val` and the other contains an unexpected value `unex` ﻿), the exposition-only function template `reinit-expected` is called to safely update the state.1) The contained value is assigned as follows:

| Value of  `has_value()` | Value of other.has_value() | |
| --- | --- | --- |
| true | false |
| true | `val`= \*other; | `reinit-expected` (`unex`,`val`, other.error()); |
| false | `reinit-expected` (`val`,`unex`, \*other); | `unex`= other.error(); |

2) The contained value is assigned as follows:

| Value of  `has_value()` | Value of other.has_value() | |
| --- | --- | --- |
| true | false |
| true | `val`= std::move(\*other); | `reinit-expected` (`unex`,`val`, std::move(other.error())); |
| false | `reinit-expected` (`val`,`unex`, std::move(\*other)); | `unex`= std::move(other.error()); |

 Then, if no exception was thrown, executes `has_val`= other.has_value();.3) The expected value is assigned as follows:

| Value of  `has_value()` | Equivalent to |
| --- | --- |
| true | `val`= std::forward<U>(v); |
| false | `reinit-expected`(`val`,`unex`, std::forward<U>(v)); `has_val`= false; |

4,5) The unexpected value is assigned as follows:

| Overload | Value of  `has_value()` | Equivalent to |
| --- | --- | --- |
| (4) | true | `reinit-expected`(`val`,`unex`, std::forward<const G&>(e.error())); `has_val`= false; |
| false | `unex`= std::forward<const G&>(e.error()); |
| (5) | true | `reinit-expected`(`val`,`unex`, std::forward<G>(e.error())); `has_val`= false; |
| false | `unex`= std::forward<G>(e.error()); |

#### void partial specialization assignment operators

6) The unexpected value is assigned or destroyed as follows:

| Value of  `has_value()` | Value of other.has_value() | |
| --- | --- | --- |
| true | false |
| true | (no effects) | std::construct_at (std::addressof(`unex`), rhs.`unex`); `has_val`= false; |
| false | std::destroy_at(std::addressof(`unex`)); `has_val`= true; | `unex`= other.error(); |

7) The unexpected value is assigned or destroyed as follows:

| Value of  `has_value()` | Value of other.has_value() | |
| --- | --- | --- |
| true | false |
| true | (no effects) | std::construct_at (std::addressof(`unex`), std::move(rhs.`unex`)); `has_val`= false; |
| false | std::destroy_at(std::addressof(`unex`)); `has_val`= true; | `unex`= std::move(other.error()); |

8,9) The unexpected value is assigned as follows:

| Overload | Value of  `has_value()` | Equivalent to |
| --- | --- | --- |
| (8) | true | std::construct_at(std::addressof(`unex`), std::forward<const G&>(e.error())); `has_val`= false; |
| false | `unex`= std::forward<const G&>(e.error()); |
| (9) | true | std::construct_at(std::addressof(`unex`), std::forward<G>(e.error())); `has_val`= false; |
| false | `unex`= std::forward<G>(e.error()); |

#### Helper function template

The exposition-only function template `reinit-expected` is “defined” as follows:

```
template<class NewType, class OldType, class... Args>
constexpr void reinit-expected(NewType& new_val, OldType& old_val, Args&&... args)
{
    // Case 1: the construction of “new_val” is non-throwing:
    // “new_val” can be directly constructed after destroying “old_val”
    if constexpr (std::is_nothrow_constructible_v<NewType, Args...>)
    {
        std::destroy_at(std::addressof(old_val));
        std::construct_at(std::addressof(new_val), std::forward<Args>(args)...);
    }
    // Case 2: the move construction of “new_val” is non-throwing:
    // constuct a temporary NewType object first
    // (“old_val” is left intact if an exception is thrown from this construction)
    else if constexpr (std::is_nothrow_move_constructible_v<NewType>)
    {
        NewType temp(std::forward<Args>(args)...); // may throw
        std::destroy_at(std::addressof(old_val));
        std::construct_at(std::addressof(new_val), std::move(temp));
    }
    // Case 3: the construction of “new_val” is potentially-throwing:
    // a backup of “old_val” is required in order to recover from an exception
    else
    {
        OldType temp(std::move(old_val)); // may throw
        std::destroy_at(std::addressof(old_val));
        try
        {
            std::construct_at(std::addressof(new_val),
                              std::forward<Args>(args)...); // may throw
        }
        catch (...)
        {
            std::construct_at(std::addressof(old_val), std::move(temp));
            throw;
        }
    }
}

```

This function template is called when the assignment is going to make \*this hold the alternative value (i.e. from expected value to unexpected value, or from unexpected value to expected value).

In this case, the old value oldval needs to be destroyed before constructing the new value newval. However, the construction of newval may throw an exception. In order to provide strong exception safety guarantee, the old value needs to be restored before rethrowing the exception so that \*this will have a valid state while the exception is being handled.

### Return value

1-9) \*this

### Constraints and supplement information

#### Primary template assignment operators

1) This overload is defined as deleted unless all following values are true:

- std::is_copy_assignable_v<T>
- std::is_copy_constructible_v<T>
- std::is_copy_assignable_v<E>
- std::is_copy_constructible_v<E>
- std::is_nothrow_move_constructible_v<T> || std::is_nothrow_move_constructible_v<E>
2) This overload participates in overload resolution only if all following values are true:

- std::is_move_assignable_v<T>
- std::is_move_constructible_v<T>
- std::is_move_assignable_v<E>
- std::is_move_constructible_v<E>
- std::is_nothrow_move_constructible_v<T> || std::is_nothrow_move_constructible_v<E>
3) This overload participates in overload resolution only if all following conditions are satisfied:

- std::is_same_v<expected, std::remove_cvref_t<U>> is false.
- std::remove_cvref_t<U> is not a specialization of `std::unexpected`.
- All following values are true:
  - std::is_constructible_v<T, U>
  - std::is_assignable_v<T&, U>
  - std::is_nothrow_constructible_v<T, U> || std::is_nothrow_move_constructible_v<T> ||  
    std::is_nothrow_move_constructible_v<E>
4) This overload participates in overload resolution only if all following values are true:

- std::is_constructible_v<E, const G&>
- std::is_assignable_v<E&, const G&>
- std::is_nothrow_constructible_v<E, const G&> || std::is_nothrow_move_constructible_v<T> ||  
  std::is_nothrow_move_constructible_v<E>
5) This overload participates in overload resolution only if all following values are true:

- std::is_constructible_v<E, G>
- std::is_assignable_v<E&, G>
- std::is_nothrow_constructible_v<E, G> || std::is_nothrow_move_constructible_v<T> ||  
  std::is_nothrow_move_constructible_v<E>

#### void partial specialization assignment operators

6) This overload is defined as deleted unless std::is_copy_assignable_v<E> and std::is_copy_constructible_v<E> are both true.7) This overload participates in overload resolution only if std::is_move_constructible_v<E> and std::is_move_assignable_v<E> are both true.8) This overload participates in overload resolution only if std::is_constructible_v<E, const G&> and std::is_assignable_v<E&, const G&> are both true.9) This overload participates in overload resolution only if std::is_constructible_v<E, G> and std::is_assignable_v<E&, G> are both true.

### Exceptions

2)noexcept specification:noexcept(  

std::is_nothrow_move_constructible_v<T> && std::is_nothrow_move_assignable_v<T> &&

std::is_nothrow_move_constructible_v<E> && std::is_nothrow_move_assignable_v<E>)7)noexcept specification:noexcept(std::is_nothrow_move_constructible_v<E> && std::is_nothrow_move_assignable_v<E>)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 4025 | C++23 | overload (7) was defined as deleted if `E` is not move constructible or not move assignable | it does not participate in overload resolution in this case |

### See also

|  |  |
| --- | --- |
| emplace | constructs the expected value in-place   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/expected/operator%3D&oldid=173291>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 July 2024, at 19:04.