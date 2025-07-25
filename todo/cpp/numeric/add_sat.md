# std::add_sat

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****add_sat****(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<numeric>` |  |  |
| template< class T >  constexpr T add_sat( T x, T y ) noexcept; |  | (since C++26) |
|  |  |  |

Computes the saturating addition x + y. This operation (unlike built-in arithmetic operations on integers) behaves as-if it is a mathematical operation with an **infinite** range. Let `q` denote the result of such operation.
Returns:

- `q`, if `q` is representable as a value of type `T`. Otherwise,
- the largest or smallest value of type `T`, whichever is closer to the `q`.

This overload participates in overload resolution only if `T` is an integer type, that is: signed char, short, int, long, long long, an extended signed integer type, or an unsigned version of such types. In particular, `T` must not be (possibly cv-qualified) bool, char, wchar_t, char8_t, char16_t, and char32_t, as these types are not intended for arithmetic.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y | - | integer values |

### Return value

Saturated x + y.

### Notes

Unlike the built-in arithmetic operators on integers, the integral promotion does not apply to the x and y arguments.

If two arguments of different type are passed, the call fails to compile, i.e. the behavior relative to template argument deduction is the same as for std::min or std::max.

Most modern hardware architectures have efficient support for saturation arithmetic on SIMD vectors, including SSE2 for x86 and NEON for ARM.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_saturation_arithmetic` | `202311L` | (C++26) | Saturation arithmetic |

### Possible implementation

See libstdc++ (gcc).

### Example

Can be previewed on Compiler Explorer.

Run this code

```
#include <climits>
#include <limits>
#include <numeric>
 
static_assert(CHAR_BIT == 8);
static_assert(UCHAR_MAX == 255);
 
int main()
{
    constexpr int a = std::add_sat(3, 4); // no saturation occurs, T = int
    static_assert(a == 7);
 
    constexpr unsigned char b = std::add_sat<unsigned char>(UCHAR_MAX, 4); // saturated
    static_assert(b == UCHAR_MAX);
 
    constexpr unsigned char c = std::add_sat(UCHAR_MAX, 4); // not saturated, T = int
        // add_sat(int, int) returns int tmp == 259,
        // then assignment truncates 259 % 256 == 3
    static_assert(c == 3);
 
//  unsigned char d = std::add_sat(252, c); // Error: inconsistent deductions for T
 
    constexpr unsigned char e = std::add_sat<unsigned char>(251, a); // saturated
    static_assert(e == UCHAR_MAX);
        // 251 is of type T = unsigned char, `a` is converted to unsigned char value;
        // might yield an int -> unsigned char conversion warning for `a`
 
    constexpr signed char f = std::add_sat<signed char>(-123, -3); // not saturated
    static_assert(f == -126);
 
    constexpr signed char g = std::add_sat<signed char>(-123, -13); // saturated
    static_assert(g == std::numeric_limits<signed char>::min()); // g == -128
}

```

### See also

|  |  |
| --- | --- |
| sub_sat(C++26) | saturating subtraction operation on two integers   (function template) |
| mul_sat(C++26) | saturating multiplication operation on two integers   (function template) |
| div_sat(C++26) | saturating division operation on two integers   (function template) |
| saturate_cast(C++26) | returns an integer value clamped to the range of another integer type   (function template) |
| clamp(C++17) | clamps a value between a pair of boundary values   (function template) |
| in_range(C++20) | checks if an integer value is in the range of a given integer type   (function template) |
| min[static] | returns the smallest finite value of the given non-floating-point type, or the smallest positive normal value of the given floating-point type   (public static member function of `std::numeric_limits<T>`) |
| max[static] | returns the largest finite value of the given type   (public static member function of `std::numeric_limits<T>`) |

### External links

|  |  |
| --- | --- |
| 1. | A branch-free implementation of saturation arithmetic — Locklessinc.com, 2012 |
| 2. | C++ Weekly - Ep 459 - C++26's Saturating Math Operations — Youtube.com, 2024-12-16 |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/add_sat&oldid=169617>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 February 2024, at 22:20.