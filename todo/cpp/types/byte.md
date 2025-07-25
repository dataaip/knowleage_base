# std::byte

From cppreference.com
< cpp‎ | types
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

Type support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic types | | | | |
| Fixed width integer types (C++11) | | | | |
| Fixed width floating-point types (C++23) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ptrdiff_t | | | | | | size_t | | | | | | max_align_t(C++11) | | | | | | ****byte****(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nullptr_t(C++11) | | | | | | offsetof | | | | | | NULL | | | | | |  | | | | | |
| Numeric limits | | | | |
| numeric_limits | | | | |
| C numeric limits interface | | | | |
| Runtime type information | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | type_info | | | | | | type_index(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bad_typeid | | | | | | bad_cast | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstddef>` |  |  |
| enum class byte : unsigned char {}; |  | (since C++17) |
|  |  |  |

`std::byte` is a distinct type that implements the concept of byte as specified in the C++ language definition.

Like unsigned char, it can be used to access raw memory occupied by other objects (object representation), but unlike unsigned char, it is not a character type and is not an arithmetic type. `std::byte` models a mere collection of bits, supporting only bitshift operations with an integer, and bitwise and comparison operations with another `std::byte`.

### Non-member functions

## std::to_integer

|  |  |  |
| --- | --- | --- |
| template< class IntegerType >  constexpr IntegerType to_integer( std::byte b ) noexcept; |  | (since C++17) |
|  |  |  |

Equivalent to: return IntegerType(b);
This overload participates in overload resolution only if std::is_integral_v<IntegerType> is true.

## std::operator<<=,operator>>=

|  |  |  |
| --- | --- | --- |
| template< class IntegerType >  constexpr std::byte& operator<<=( std::byte& b, IntegerType shift ) noexcept; | (1) | (since C++17) |
| template< class IntegerType >  constexpr std::byte& operator>>=( std::byte& b, IntegerType shift ) noexcept; | (2) | (since C++17) |
|  |  |  |

1) Equivalent to: return b = b << shift;
This overload participates in overload resolution only if std::is_integral_v<IntegerType> is true.2) Equivalent to: return b = b >> shift;

This overload participates in overload resolution only if std::is_integral_v<IntegerType> is true.

## std::operator<<,operator>>

|  |  |  |
| --- | --- | --- |
| template< class IntegerType >  constexpr std::byte operator<<( std::byte b, IntegerType shift ) noexcept; | (1) | (since C++17) |
| template< class IntegerType >  constexpr std::byte operator>>( std::byte b, IntegerType shift ) noexcept; | (2) | (since C++17) |
|  |  |  |

1) Equivalent to: return std::byte(static_cast<unsigned int>(b) << shift);
This overload participates in overload resolution only if std::is_integral_v<IntegerType> is true.2) Equivalent to: return std::byte(static_cast<unsigned int>(b) >> shift);

This overload participates in overload resolution only if std::is_integral_v<IntegerType> is true.

## std::operator|=,operator&=,operator^=

|  |  |  |
| --- | --- | --- |
| constexpr std::byte& operator|=( std::byte& l, std::byte r ) noexcept; | (1) | (since C++17) |
| constexpr std::byte& operator&=( std::byte& l, std::byte r ) noexcept; | (2) | (since C++17) |
| constexpr std::byte& operator^=( std::byte& l, std::byte r ) noexcept; | (3) | (since C++17) |
|  |  |  |

1) Equivalent to: return l = l | r;.2) Equivalent to: return l = l & r;.3) Equivalent to: return l = l ^ r;.

## std::operator|,operator&,operator^,operator~

|  |  |  |
| --- | --- | --- |
| constexpr std::byte operator|( std::byte l, std::byte r ) noexcept; | (1) | (since C++17) |
| constexpr std::byte operator&( std::byte l, std::byte r ) noexcept; | (2) | (since C++17) |
| constexpr std::byte operator^( std::byte l, std::byte r ) noexcept; | (3) | (since C++17) |
| constexpr std::byte operator~( std::byte b ) noexcept; | (4) | (since C++17) |
|  |  |  |

1) Equivalent to: return std::byte(static_cast<unsigned int>(l) | static_cast<unsigned int>(r));.2) Equivalent to: return std::byte(static_cast<unsigned int>(l) & static_cast<unsigned int>(r));.3) Equivalent to: return std::byte(static_cast<unsigned int>(l) ^ static_cast<unsigned int>(r));.4) Equivalent to: return std::byte(~static_cast<unsigned int>(b));

### Notes

A numeric value n can be converted to a byte value using std::byte{n}, due to C++17 relaxed enum class initialization rules.

A byte can be converted to a numeric value (such as to produce an integer hash of an object) the usual way with an explicit conversion or alternatively with `std::to_integer`.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_byte` | `201603L` | (C++17) | `std::byte` |

### Example

Run this code

```
#include <bitset>
#include <cassert>
#include <cstddef>
#include <iostream>
#include <utility>
 
std::ostream& operator<<(std::ostream& os, std::byte b)
{
    return os << std::bitset<8>(std::to_integer<int>(b));
}
 
int main()
{
    // std::byte y = 1; // Error: cannot convert int to byte.
    std::byte y{1}; // OK
 
    // if (y == 13) {} // Error: cannot be compared.
    if (y == std::byte{13}) {} // OK, bytes are comparable
 
    int arr[]{1, 2, 3};
    // int c = a[y]; // Error: array subscript is not an integer
    [[maybe_unused]] int i = arr[std::to_integer<int>(y)]; // OK
    [[maybe_unused]] int j = arr[std::to_underlying(y)];   // OK
 
    auto to_int = [](std::byte b) { return std::to_integer<int>(b); };
 
    std::byte b{42};
    assert(to_int(b) == 0b00101010);
    std::cout << b << '\n';
 
    // b *= 2; // Error: b is not of arithmetic type
    b <<= 1;
    assert(to_int(b) == 0b01010100);
 
    b >>= 1;
    assert(to_int(b) == 0b00101010);
 
    assert(to_int(b << 1) == 0b01010100);
    assert(to_int(b >> 1) == 0b00010101);
 
    b |= std::byte{0b11110000};
    assert(to_int(b) == 0b11111010);
 
    b &= std::byte{0b11110000};
    assert(to_int(b) == 0b11110000);
 
    b ^= std::byte{0b11111111};
    assert(to_int(b) == 0b00001111);
}

```

Output:

```
00101010

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/byte&oldid=173341>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 July 2024, at 10:45.