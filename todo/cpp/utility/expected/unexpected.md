# std::unexpected

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
| expected::operator= | | | | |
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
| ****unexpected**** | | | | |
| bad_expected_access | | | | |
| unexpect_tunexpect | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<expected>` |  |  |
| template< class E >  class unexpected; |  | (since C++23) |
|  |  |  |

The class template `std::unexpected` represents an unexpected value stored in std::expected. In particular, std::expected has constructors with `std::unexpected` as a single argument, which creates an `expected` object that contains an unexpected value.

A program is ill-formed if it instantiates an `unexpected` with a non-object type, an array type, a specialization of `std::unexpected`, or a cv-qualified type.

### Template parameters

|  |  |  |
| --- | --- | --- |
| E | - | the type of the unexpected value. The type must not be an array type, a non-object type, a specialization of `std::unexpected`, or a cv-qualified type. |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `unexpected` object   (public member function) |
| (destructor)(implicitly declared) | destroys the `unexpected` object, along with the stored value   (public member function) |
| operator=(implicitly declared) | assigns the stored value   (public member function) |
| error | accesses the stored value   (public member function) |
| swap | swaps the stored value   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==(C++23) | compares the stored value   (function template) |
| swap(std::unexpected)(C++23) | specializes the std::swap algorithm   (function template) |

## std::unexpected::unexpected

|  |  |  |
| --- | --- | --- |
| constexpr unexpected( const unexpected& ) = default; | (1) |  |
| constexpr unexpected( unexpected&& ) = default; | (2) |  |
| template< class Err = E >  constexpr explicit unexpected( Err&& e ); | (3) |  |
| template< class... Args >  constexpr explicit unexpected( std::in_place_t, Args&&... args ); | (4) |  |
| template< class U, class... Args >  constexpr explicit unexpected( std::in_place_t, std::initializer_list<U> il, Args&&... args ); | (5) |  |
|  |  |  |

Constructs a `std::unexpected` object.

1,2) Copy/move constructor. Copies or moves the stored value, respectively.3) Constructs the stored value, as if by direct-initializing a value of type `E` from std::forward<Err>(e).

- This overload participates in overload resolution only if
  - std::is_same_v<std::remove_cvref_t<Err>, unexpected> is false, and
  - std::is_same_v<std::remove_cvref_t<Err>, std::in_place_t> is false, and
  - std::is_constructible_v<E, Err> is true.
4) Constructs the stored value, as if by direct-initializing a value of type `E` from the arguments std::forward<Args>(args)....

- This overload participates in overload resolution only if std::is_constructible_v<E, Args...> is true.
5) Constructs the stored value, as if by direct-initializing a value of type `E` from the arguments il, std::forward<Args>(args)....

- This overload participates in overload resolution only if std::is_constructible_v<E, std::initializer_list<U>&, Args...> is true.

### Parameters

|  |  |  |
| --- | --- | --- |
| e | - | value with which to initialize the contained value |
| args... | - | arguments with which to initialize the contained value |
| il | - | initializer list with which to initialize the contained value |

### Exceptions

Throws any exception thrown by the constructor of `E`.

## std::unexpected::error

|  |  |  |
| --- | --- | --- |
| constexpr const E& error() const& noexcept;  constexpr E& error() & noexcept;  constexpr const E&& error() const&& noexcept; constexpr E&& error() && noexcept; |  |  |
|  |  |  |

Returns a reference to the stored value.

## std::unexpected::swap

|  |  |  |
| --- | --- | --- |
| constexpr void swap( unexpected& other ) noexcept(std::is_nothrow_swappable_v<E>); |  |  |
|  |  |  |

Swaps the stored values, as if by using std::swap; swap(error(), other.error());.

The program is ill-formed if std::is_swappable_v<E> is false.

## operator==(std::unexpected)

|  |  |  |
| --- | --- | --- |
| template< class E2 >  friend constexpr bool operator==( unexpected& x, std::unexpected<E2>& y ); |  |  |
|  |  |  |

Compares the stored values, as if by return x.error() == y.error().

If the expression x.error() == e.error() is not well-formed, or if its result is not convertible to bool, the program is ill-formed.

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when std::unexpected<E> is an associated class of the arguments.

## swap(std::unexpected)

|  |  |  |
| --- | --- | --- |
| friend constexpr void  swap( unexpected& x, unexpected& y ) noexcept(noexcept(x.swap(y))); |  |  |
|  |  |  |

Equivalent to x.swap(y).

This overload participates in overload resolution only if std::is_swappable_v<E> is true.

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when std::unexpected<E> is an associated class of the arguments.

### Deduction guides

|  |  |  |
| --- | --- | --- |
| template< class E >  unexpected(E) -> unexpected<E>; |  | (since C++23) |
|  |  |  |

The deduction guide is provided for unexpected to allow deduction from the constructor argument.

### Notes

Prior to C++17, the name std::unexpected denoted the function called by the C++ runtime when a dynamic exception specification was violated.

### Example

Run this code

```
#include <expected>
#include <iostream>
 
enum class error
{
    compile_time_error,
    runtime_error
};
 
[[nodiscard]] auto unexpected_runtime_error() -> std::expected<int, error>
{
    return std::unexpected(error::runtime_error);
}
 
int main()
{
    std::expected<double, int> ex = std::unexpected(3);
 
    if (!ex)
        std::cout << "ex contains an error value\n";
 
    if (ex == std::unexpected(3))
        std::cout << "The error value is equal to 3\n";
 
    const auto e = unexpected_runtime_error();
 
    e.and_then([](const auto& e) -> std::expected<int, error>
    {
        std::cout << "and_then: " << int(e); // not printed
        return {};
    })
    .or_else([](const auto& e) -> std::expected<int, error>
    {
        std::cout << "or_else: " << int(e); // prints this line
        return {};
    });
}

```

Output:

```
ex contains an error value
The error value is equal to 3
or_else: 1

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs the `expected` object   (public member function) |
| operator==(C++23) | compares `expected` objects   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/expected/unexpected&oldid=177369>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 October 2024, at 14:26.