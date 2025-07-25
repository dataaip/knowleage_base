# std::nearbyint, std::nearbyintf, std::nearbyintl

From cppreference.com
< cpp‎ | numeric‎ | math
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

Common mathematical functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Basic operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abs(int)labsllabsimaxabs(C++11) | | | | | | abs(float)fabs | | | | | | divldivlldivimaxdiv(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C++11) | | | | | | remquo(C++11) | | | | | | fma(C++11) | | | | | | fmax(C++11) | | | | | | fmin(C++11) | | | | | | fdim(C++11) | | | | | | nannanfnanl(C++11)(C++11)(C++11) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | exp2(C++11) | | | | | | expm1(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | log10 | | | | | | log1p(C++11) | | | | | | log2(C++11) | | | | | |
| Power functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | cbrt(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hypot(C++11) | | | | | | pow | | | | | |
| Trigonometric and  hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | |  | | | | | |
| Error and gamma functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erf(C++11) | | | | | | erfc(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lgamma(C++11) | | | | | | tgamma(C++11) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Nearest integer floating point operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ceil | | | | | | floor | | | | | | roundlroundllround(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | trunc(C++11) | | | | | | ****nearbyint****(C++11) | | | | | | rintlrintllrint(C++11)(C++11)(C++11) | | | | | |
| Floating point manipulation functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ldexp | | | | | | scalbnscalbln(C++11)(C++11) | | | | | | ilogb(C++11) | | | | | | logb(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | frexp | | | | | | modf | | | | | | nextafternexttoward(C++11)(C++11) | | | | | | copysign(C++11) | | | | | |
| Classification and comparison | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | fpclassify(C++11) | | | | | | isfinite(C++11) | | | | | | isinf(C++11) | | | | | | isnan(C++11) | | | | | | isnormal(C++11) | | | | | | signbit(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isgreater(C++11) | | | | | | isgreaterequal(C++11) | | | | | | isless(C++11) | | | | | | islessequal(C++11) | | | | | | islessgreater(C++11) | | | | | | isunordered(C++11) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | div_t | | | | | | ldiv_t | | | | | | lldiv_t(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaxdiv_t(C++11) | | | | | | float_t(C++11) | | | | | | double_t(C++11) | | | | | |
| Macro constants | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | HUGE_VALFHUGE_VALHUGE_VALL(C++11)(C++11) | | | | | | math_errhandlingMATH_ERRNOMATH_ERREXCEPT(C++11) | | | | | | INFINITY(C++11) | | | | | | NAN(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Classification | | | | | | FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C++11)(C++11)(C++11)(C++11)(C++11) | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       nearbyint ( float num );  double      nearbyint ( double num ); long double nearbyint ( long double num ); |  | (until C++23) |
| /\*floating-point-type\*/              nearbyint ( /\*floating-point-type\*/ num ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       nearbyintf( float num ); | (2) | (since C++11) |
| long double nearbyintl( long double num ); | (3) | (since C++11) |
| SIMD overload (since C++26) |  |  |
| Defined in header `<simd>` |  |  |
| template< /\*math-floating-point\*/ V >  constexpr /\*deduced-simd-t\*/<V>             nearbyint ( const V& v_num ); | (S) | (since C++26) |
| Additional overloads (since C++11) |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      nearbyint ( Integer num ); | (A) |  |
|  |  |  |

1-3) Rounds the floating-point argument num to an integer value in floating-point format, using the current rounding mode. The library provides overloads of `std::nearbyint` for all cv-unqualified floating-point types as the type of the parameter.(since C++23)

|  |  |
| --- | --- |
| S) The SIMD overload performs an element-wise `std::nearbyint` on v_num. (See **math-floating-point** and **deduced-simd-t** for their definitions.) | (since C++26) |

|  |  |
| --- | --- |
| A) Additional overloads are provided for all integer types, which are treated as double. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| num | - | floating-point or integer value |

### Return value

The nearest integer value to num, according to the current rounding mode, is returned.

### Error handling

This function is not subject to any of the errors specified in math_errhandling.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- FE_INEXACT is never raised.
- If num is ±∞, it is returned, unmodified.
- If num is ±0, it is returned, unmodified.
- If num is NaN, NaN is returned.

### Notes

The only difference between `std::nearbyint` and std::rint is that `std::nearbyint` never raises FE_INEXACT.

The largest representable floating-point values are exact integers in all standard floating-point formats, so `std::nearbyint` never overflows on its own; however the result may overflow any integer type (including std::intmax_t), when stored in an integer variable.

If the current rounding mode is FE_TONEAREST, this function rounds to even in halfway cases (like std::rint, but unlike std::round).

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their argument num of integer type, std::nearbyint(num) has the same effect as std::nearbyint(static_cast<double>(num)).

### Example

Run this code

```
#include <cfenv>
#include <cmath>
#include <iostream>
#pragma STDC FENV_ACCESS ON
 
int main()
{
    std::fesetround(FE_TONEAREST);
    std::cout << "rounding to nearest: \n"
              << "nearbyint(+2.3) = " << std::nearbyint(2.3)
              << "  nearbyint(+2.5) = " << std::nearbyint(2.5)
              << "  nearbyint(+3.5) = " << std::nearbyint(3.5) << '\n'
              << "nearbyint(-2.3) = " << std::nearbyint(-2.3)
              << "  nearbyint(-2.5) = " << std::nearbyint(-2.5)
              << "  nearbyint(-3.5) = " << std::nearbyint(-3.5) << '\n';
 
    std::fesetround(FE_DOWNWARD);
    std::cout << "rounding down:\n"
              << "nearbyint(+2.3) = " << std::nearbyint(2.3)
              << "  nearbyint(+2.5) = " << std::nearbyint(2.5)
              << "  nearbyint(+3.5) = " << std::nearbyint(3.5) << '\n'
              << "nearbyint(-2.3) = " << std::nearbyint(-2.3)
              << "  nearbyint(-2.5) = " << std::nearbyint(-2.5)
              << "  nearbyint(-3.5) = " << std::nearbyint(-3.5) << '\n';
 
    std::cout << "nearbyint(-0.0) = " << std::nearbyint(-0.0)  << '\n'
              << "nearbyint(-Inf) = " << std::nearbyint(-INFINITY) << '\n';
}

```

Output:

```
rounding to nearest: 
nearbyint(+2.3) = 2  nearbyint(+2.5) = 2  nearbyint(+3.5) = 4
nearbyint(-2.3) = -2  nearbyint(-2.5) = -2  nearbyint(-3.5) = -4
rounding down:
nearbyint(+2.3) = 2  nearbyint(+2.5) = 2  nearbyint(+3.5) = 3
nearbyint(-2.3) = -3  nearbyint(-2.5) = -3  nearbyint(-3.5) = -4
nearbyint(-0.0) = -0
nearbyint(-Inf) = -inf

```

### See also

|  |  |
| --- | --- |
| rintrintfrintllrintlrintflrintlllrintllrintfllrintl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer using current rounding mode with exception if the result differs   (function) |
| roundroundfroundllroundlroundflroundlllroundllroundfllroundl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer, rounding away from zero in halfway cases   (function) |
| fegetroundfesetround(C++11)(C++11) | gets or sets rounding direction   (function) |
| C documentation for nearbyint | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/nearbyint&oldid=160768>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 October 2023, at 21:39.