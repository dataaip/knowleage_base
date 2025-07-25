# lgamma, lgammaf, lgammal

From cppreference.com
< c‎ | numeric‎ | math
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Numerics

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Floating-point environment (C99) | | | | |
| Pseudo-random number generation | | | | |
| Complex number arithmetic (C99) | | | | |
| Type-generic math (C99) | | | | |
| Bit manipulation (C23) | | | | |
| Checked integer arithmetic (C23) | | | | |

 Common mathematical functions

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Basic operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | abslabsllabsimaxabs(C99)(C99) | | | | | | fabs | | | | | | divldivlldivimaxdiv(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C99) | | | | | | remquo(C99) | | | | | | fma(C99) | | | | | | fdim(C99) | | | | | | nannanfnanlnand**N**(C99)(C99)(C99)(C23) | | | | | | | Maximum/minimum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmax(C99) | | | | | | fmin(C99) | | | | | | fmaximum")(C23) | | | | | | fminimum")(C23) | | | | | | fmaximum_mag")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmaximum_num")(C23) | | | | | | fminimum_mag")(C23) | | | | | | fminimum_num")(C23) | | | | | | fmaximum_mag_num")(C23) | | | | | | fminimum_mag_num")(C23) | | | | | | | Exponential functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | exp10")(C23) | | | | | | exp2(C99) | | | | | | expm1(C99) | | | | | | exp10m1")(C23) | | | | | | exp2m1")(C23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | log10 | | | | | | log2(C99) | | | | | | log1plogp1(C99)(C23) | | | | | | log10p1")(C23) | | | | | | log2p1")(C23) | | | | | | | Power functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | cbrt(C99) | | | | | | rootn")(C23) | | | | | | rsqrt")(C23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hypot(C99) | | | | | | compound")(C23) | | | | | | pow | | | | | | pown")(C23) | | | | | | powr")(C23) | | | | | | | Trigonometric and hyperbolic functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinpi(C23) | | | | | | cospi(C23) | | | | | | tanpi")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinpi")(C23) | | | | | | acospi")(C23) | | | | | | atanpi")(C23) | | | | | | atan2pi")(C23) | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | asinh(C99) | | | | | | acosh(C99) | | | | | | atanh(C99) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Nearest integer floating-point | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ceil | | | | | | floor | | | | | | roundlroundllround(C99)(C99)(C99) | | | | | | roundeven(C23) | | | | | | trunc(C99) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nearbyint(C99) | | | | | | rintlrintllrint(C99)(C99)(C99) | | | | | | fromfpfromfpxufromfpufromfpx")(C23)(C23)(C23)(C23) | | | | | | | Floating-point manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ldexp | | | | | | frexp | | | | | | scalbnscalbln(C99)(C99) | | | | | | ilogbllogb(C99)(C23) | | | | | | logb(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | modf | | | | | | nextafternexttoward(C99)(C99) | | | | | | nextupnextdown")(C23)(C23) | | | | | | copysign(C99) | | | | | | canonicalize")(C23) | | | | | | | Narrowing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fadd")(C23) | | | | | | fsub")(C23) | | | | | | fmul")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fdiv")(C23) | | | | | | ffma")(C23) | | | | | | fsqrt")(C23) | | | | | | | Quantum and quantum exponent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | quantized**N**")(C23) | | | | | | quantumd**N**")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | samequantumd**N**")(C23) | | | | | | llquantexpd**N**")(C23) | | | | | | | Decimal re-encoding functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | encodedecd**N**")(C23) | | | | | | decodedecd**N**")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | encodebind**N**")(C23) | | | | | | decodebind**N**")(C23) | | | | | | | Total order and payload functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | totalorder")(C23) | | | | | | getpayload")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setpayload")(C23) | | | | | | setpayloadsig")(C23) | | | | | | | Classification | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fpclassify(C99) | | | | | | iscanonical")(C23) | | | | | | isfinite(C99) | | | | | | isinf(C99) | | | | | | isnan(C99) | | | | | | isnormal(C99) | | | | | | signbit(C99) | | | | | | issubnormal")(C23) | | | | | | iszero")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isgreater(C99) | | | | | | isgreaterequal(C99) | | | | | | isless(C99) | | | | | | islessequal(C99) | | | | | | islessgreater(C99) | | | | | | isunordered(C99) | | | | | | issignaling")(C23) | | | | | | iseqsig")(C23) | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Error and gamma functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | erf(C99) | | | | | | erfc(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****lgamma****(C99) | | | | | | tgamma(C99) | | | | | | | Types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | div_tldiv_tlldiv_timaxdiv_t(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | float_tdouble_t(C99)(C99) | | | | | | _Decimal32_t_Decimal64_t")(C23)(C23) | | | | | | | Macro constants | | | | | | Special floating-point values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | HUGE_VALHUGE_VALFHUGE_VALLHUGE_VALD**N**(C99)(C99)(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | INFINITYDEC_INFINITY(C99)(C23) | | | | | | NANDEC_NAN(C99)(C23) | | | | | | | Arguments and return values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_ILOGB0FP_ILOGBNAN(C99)(C99) | | | | | | FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C99)(C99)(C99)(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_LLOGB0FP_LLOGBNAN(C23)(C23) | | | | | | FP_INT_UPWARDFP_INT_DOWNWARDFP_INT_TOWARDZEROFP_INT_TONEARESTFROMZEROFP_INT_TONEAREST")(C23)(C23)(C23)(C23)(C23) | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MATH_ERRNOMATH_ERRNOEXCEPT(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | math_errhandling(C99) | | | | | |  | | | | | | | Fast operation indicators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_FAST_FMAFFP_FAST_FMA(C99)(C99) | | | | | | FP_FAST_FADDFP_FAST_FADDLFP_FAST_DADDLFP_FAST_D**M**ADDD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FMULFP_FAST_FMULLFP_FAST_DMULLFP_FAST_D**M**MULD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FFMAFP_FAST_FFMALFP_FAST_DFMALFP_FAST_D**M**FMAD**N**")(C23)(C23)(C23)(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_FAST_FMALFP_FAST_FMAD**N**(C99)(C23) | | | | | | FP_FAST_FSUBFP_FAST_FSUBLFP_FAST_DSUBLFP_FAST_D**M**SUBD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FDIVFP_FAST_FDIVLFP_FAST_DDIVLFP_FAST_D**M**DIVD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FSQRTFP_FAST_FSQRTLFP_FAST_DSQRTLFP_FAST_D**M**SQRTD**N**")(C23)(C23)(C23)(C23) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<math.h>` |  |  |
| float       lgammaf( float arg ); | (1) | (since C99) |
| double      lgamma( double arg ); | (2) | (since C99) |
| long double lgammal( long double arg ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define lgamma( arg ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the natural logarithm of the absolute value of the gamma function of arg.4) Type-generic macro: If arg has type long double, `lgammal` is called. Otherwise, if arg has integer type or the type double, `lgamma` is called. Otherwise, `lgammaf` is called.

### Parameters

|  |  |  |
| --- | --- | --- |
| arg | - | floating-point value |

### Return value

If no errors occur, the value of the logarithm of the gamma function of arg, that is \(\log_{e}|{\int_0^\infty t^{arg-1} e^{-t} \mathsf{d}t}|\)loge|∫∞  
0**t**arg-1  
 **e**-t d**t**|, is returned.

If a pole error occurs, +HUGE_VAL, `+HUGE_VALF`, or `+HUGE_VALL` is returned.

If a range error due to overflow occurs, ±HUGE_VAL, `±HUGE_VALF`, or `±HUGE_VALL` is returned.

### Error handling

Errors are reported as specified in `math_errhandling`.

If arg is zero or is an integer less than zero, a pole error may occur.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- If the argument is 1, +0 is returned.
- If the argument is 2, +0 is returned.
- If the argument is ±0, +∞ is returned and FE_DIVBYZERO is raised.
- If the argument is a negative integer, +∞ is returned and FE_DIVBYZERO is raised.
- If the argument is ±∞, +∞ is returned.
- If the argument is NaN, NaN is returned.

### Notes

If arg is a natural number, lgamma(arg) is the logarithm of the factorial of arg - 1.

The POSIX version of `lgamma` is not thread-safe: each execution of the function stores the sign of the gamma function of arg in the static external variable `signgam`. Some implementations provide `lgamma_r`, which takes a pointer to user-provided storage for singgam as the second parameter, and is thread-safe.

There is a non-standard function named `gamma` in various implementations, but its definition is inconsistent. For example, glibc and 4.2BSD version of `gamma` executes `lgamma`, but 4.4BSD version of `gamma` executes `tgamma`.

### Example

Run this code

```
#include <errno.h>
#include <fenv.h>
#include <float.h>
#include <math.h>
#include <stdio.h>
// #pragma STDC FENV_ACCESS ON
 
int main(void)
{
    printf("lgamma(10) = %f, log(9!) = %f\n", lgamma(10),
                                              log(2 * 3 * 4 * 5 * 6 * 7 * 8 * 9));
    const double pi = acos(-1);
    printf("lgamma(0.5) = %f, log(sqrt(pi)) = %f\n", log(sqrt(pi)), lgamma(0.5));
    // special values
    printf("lgamma(1) = %f\n", lgamma(1));
    printf("lgamma(+Inf) = %f\n", lgamma(INFINITY));
 
    // error handling
    errno = 0; feclearexcept(FE_ALL_EXCEPT);
    printf("lgamma(0) = %f\n", lgamma(0));
    if (errno == ERANGE)
        perror("    errno == ERANGE");
    if (fetestexcept(FE_DIVBYZERO))
        puts("    FE_DIVBYZERO raised");
}

```

Possible output:

```
lgamma(10) = 12.801827, log(9!) = 12.801827
lgamma(0.5) = 0.572365, log(sqrt(pi)) = 0.572365
lgamma(1) = 0.000000
lgamma(+Inf) = inf
lgamma(0) = inf
    errno == ERANGE: Numerical result out of range
    FE_DIVBYZERO raised

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.12.8.3 The lgamma functions (p: TBD)

:   - 7.25 Type-generic math <tgmath.h> (p: TBD)

:   - F.10.5.3 The lgamma functions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.12.8.3 The lgamma functions (p: 182)

:   - 7.25 Type-generic math <tgmath.h> (p: 272-273)

:   - F.10.5.3 The lgamma functions (p: 383)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.12.8.3 The lgamma functions (p: 250)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - F.10.5.3 The lgamma functions (p: 525)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.12.8.3 The lgamma functions (p: 231)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - F.9.5.3 The lgamma functions (p: 462)

### See also

|  |  |
| --- | --- |
| tgammatgammaftgammal(C99)(C99)(C99) | computes gamma function   (function) |
| C++ documentation for lgamma | |

### External links

|  |
| --- |
| Weisstein, Eric W. "Log Gamma Function." From MathWorld — A Wolfram Web Resource. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/math/lgamma&oldid=172041>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 May 2024, at 07:29.