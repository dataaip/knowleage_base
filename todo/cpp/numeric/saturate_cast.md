# std::saturate_cast

From cppreference.com
< cpp‎ | numeric
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

Numerics library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Mathematical special functions (C++17) | | | | |
| Mathematical constants (C++20) | | | | |
| Basic linear algebra algorithms (C++26) | | | | |
| Data-parallel types (SIMD) (C++26) | | | | |
| Floating-point environment (C++11) | | | | |
| Complex numbers | | | | |
| Numeric array (`valarray`) | | | | |
| Pseudo-random number generation | | | | |
| Bit manipulation (C++20) | | | | |
| Factor operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | gcd(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lcm(C++17) | | | | | |
| Interpolations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | midpoint(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lerp(C++20) | | | | | |
| Saturation arithmetic | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | ****saturate_cast****(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<numeric>` |  |  |
| template< class T, class U >  constexpr T saturate_cast( U x ) noexcept; |  | (since C++26) |
|  |  |  |

Converts the value x to a value of type `T`, clamping x between the minimum and maximum values of type `T`.

The program is ill-formed if either `T` or `U` is not a signed or unsigned integer type (including standard integer type and extended integer type).

### Parameters

|  |  |  |
| --- | --- | --- |
| x | - | an integer value |

### Return value

- x, if x is representable as a value of type `T`. Otherwise,
- either the largest or smallest representable value of type `T`, whichever is closer to the value of x.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_saturation_arithmetic` | `202311L` | (C++26) | Saturation arithmetic |

### Possible implementation

See libstdc++ (GCC).

### Example

Can be previewed on Compiler Explorer.

Run this code

```
#include <cstdint>
#include <limits>
#include <numeric>
 
int main()
{
    constexpr std::int16_t x1{696};
 
    constexpr std::int8_t x2 = std::saturate_cast<std::int8_t>(x1);
    static_assert(x2 == std::numeric_limits<std::int8_t>::max());
 
    constexpr std::uint8_t x3 = std::saturate_cast<std::uint8_t>(x1);
    static_assert(x3 == std::numeric_limits<std::uint8_t>::max());
 
    constexpr std::int16_t y1{-696};
 
    constexpr std::int8_t y2 = std::saturate_cast<std::int8_t>(y1);
    static_assert(y2 == std::numeric_limits<std::int8_t>::min());
 
    constexpr std::uint8_t y3 = std::saturate_cast<std::uint8_t>(y1);
    static_assert(y3 == 0);
}

```

### See also

|  |  |
| --- | --- |
| bit_cast(C++20) | reinterpret the object representation of one type as that of another   (function template) |
| clamp(C++17) | clamps a value between a pair of boundary values   (function template) |
| in_range(C++20) | checks if an integer value is in the range of a given integer type   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/saturate_cast&oldid=175283>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 August 2024, at 11:49.