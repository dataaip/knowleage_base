# std::ceil, std::ceilf, std::ceill

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****ceil**** | | | | | | floor | | | | | | roundlroundllround(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | trunc(C++11) | | | | | | nearbyint(C++11) | | | | | | rintlrintllrint(C++11)(C++11)(C++11) | | | | | |
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
| float       ceil ( float num );  double      ceil ( double num ); long double ceil ( long double num ); |  | (until C++23) |
| constexpr /\*floating-point-type\*/              ceil ( /\*floating-point-type\*/ num ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       ceilf( float num ); | (2) | (since C++11)  (constexpr since C++23) |
| long double ceill( long double num ); | (3) | (since C++11)  (constexpr since C++23) |
| SIMD overload (since C++26) |  |  |
| Defined in header `<simd>` |  |  |
| template< /\*math-floating-point\*/ V >  constexpr /\*deduced-simd-t\*/<V>             ceil ( const V& v_num ); | (S) | (since C++26) |
| Additional overloads (since C++11) |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      ceil ( Integer num ); | (A) | (constexpr since C++23) |
|  |  |  |

1-3) Computes the least integer value not less than num. The library provides overloads of `std::ceil` for all cv-unqualified floating-point types as the type of the parameter.(since C++23)

|  |  |
| --- | --- |
| S) The SIMD overload performs an element-wise `std::ceil` on v_num. (See **math-floating-point** and **deduced-simd-t** for their definitions.) | (since C++26) |

|  |  |
| --- | --- |
| A) Additional overloads are provided for all integer types, which are treated as double. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| num | - | floating point or integer value |

### Return value

If no errors occur, the smallest integer value not less than num, that is ⌈num⌉, is returned.

Return value!math-ceil.svgnum

### Error handling

Errors are reported as specified in math_errhandling.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- The current rounding mode has no effect.
- If num is ±∞, it is returned unmodified.
- If num is ±0, it is returned, unmodified.
- If num is NaN, NaN is returned.

### Notes

FE_INEXACT may be (but is not required to be) raised when rounding a non-integer finite value.

The largest representable floating-point values are exact integers in all standard floating-point formats, so this function never overflows on its own; however the result may overflow any integer type (including std::intmax_t), when stored in an integer variable. It is for this reason that the return type is floating-point not integral.

This function (for double argument) behaves as if (except for the freedom to not raise FE_INEXACT) implemented by the following code:

```
#include <cfenv>
#include <cmath>
#pragma STDC FENV_ACCESS ON
 
double ceil(double x)
{
    int save_round = std::fegetround();
    std::fesetround(FE_UPWARD);
    double result = std::rint(x); // or std::nearbyint
    std::fesetround(save_round);
    return result;
}

```

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their argument num of integer type, std::ceil(num) has the same effect as std::ceil(static_cast<double>(num)).

### Example

Run this code

```
#include <cmath>
#include <iostream>
 
int main()
{
    std::cout << std::fixed
              << "ceil(+2.4) = " << std::ceil(+2.4) << '\n'
              << "ceil(-2.4) = " << std::ceil(-2.4) << '\n'
              << "ceil(-0.0) = " << std::ceil(-0.0) << '\n'
              << "ceil(-Inf) = " << std::ceil(-INFINITY) << '\n';
}

```

Output:

```
ceil(+2.4) = 3.000000
ceil(-2.4) = -2.000000
ceil(-0.0) = -0.000000
ceil(-Inf) = -inf

```

### See also

|  |  |
| --- | --- |
| floorfloorffloorl(C++11)(C++11) | nearest integer not greater than the given value   (function) |
| trunctruncftruncl(C++11)(C++11)(C++11) | nearest integer not greater in magnitude than the given value   (function) |
| roundroundfroundllroundlroundflroundlllroundllroundfllroundl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer, rounding away from zero in halfway cases   (function) |
| nearbyintnearbyintfnearbyintl(C++11)(C++11)(C++11) | nearest integer using current rounding mode   (function) |
| rintrintfrintllrintlrintflrintlllrintllrintfllrintl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer using current rounding mode with exception if the result differs   (function) |
| C documentation for ceil | |

### External links

|  |
| --- |
| Fast ceiling of an integer division — StackOverflow |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/ceil&oldid=160766>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 October 2023, at 21:28.