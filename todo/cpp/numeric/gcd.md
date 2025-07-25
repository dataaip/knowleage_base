# std::gcd

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****gcd****(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lcm(C++17) | | | | | |
| Interpolations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | midpoint(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lerp(C++20) | | | | | |
| Saturation arithmetic | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<numeric>` |  |  |
| template< class M, class N >  constexpr std::common_type_t<M, N> gcd( M m, N n ); |  | (since C++17) |
|  |  |  |

Computes the greatest common divisor of the integers m and n.

If either `M` or `N` is not an integer type, or if either is (possibly cv-qualified) bool, the program is ill-formed.

If either |m| or |n| is not representable as a value of type std::common_type_t<M, N>, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| m, n | - | integer values |

### Return value

If both m and n are zero, returns zero. Otherwise, returns the greatest common divisor of |m| and |n|.

### Exceptions

Throws no exceptions.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_gcd_lcm` | `201606L` | (C++17) | `std::gcd`, std::lcm |

### Example

Run this code

```
#include <numeric>
 
int main()
{
    constexpr int p{2 * 2 * 3};
    constexpr int q{2 * 3 * 3};
    static_assert(2 * 3 == std::gcd(p, q));
 
    static_assert(std::gcd( 6,  10) == 2);
    static_assert(std::gcd( 6, -10) == 2);
    static_assert(std::gcd(-6, -10) == 2);
 
    static_assert(std::gcd( 24, 0) == 24);
    static_assert(std::gcd(-24, 0) == 24);
}

```

### See also

|  |  |
| --- | --- |
| lcm(C++17) | computes the least common multiple of two integers   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/gcd&oldid=162783>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 November 2023, at 06:33.