# ilogb, ilogbf, ilogbl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Basic operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | abslabsllabsimaxabs(C99)(C99) | | | | | | fabs | | | | | | divldivlldivimaxdiv(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C99) | | | | | | remquo(C99) | | | | | | fma(C99) | | | | | | fdim(C99) | | | | | | nannanfnanlnand**N**(C99)(C99)(C99)(C23) | | | | | | | Maximum/minimum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmax(C99) | | | | | | fmin(C99) | | | | | | fmaximum")(C23) | | | | | | fminimum")(C23) | | | | | | fmaximum_mag")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmaximum_num")(C23) | | | | | | fminimum_mag")(C23) | | | | | | fminimum_num")(C23) | | | | | | fmaximum_mag_num")(C23) | | | | | | fminimum_mag_num")(C23) | | | | | | | Exponential functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | exp10")(C23) | | | | | | exp2(C99) | | | | | | expm1(C99) | | | | | | exp10m1")(C23) | | | | | | exp2m1")(C23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | log10 | | | | | | log2(C99) | | | | | | log1plogp1(C99)(C23) | | | | | | log10p1")(C23) | | | | | | log2p1")(C23) | | | | | | | Power functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | cbrt(C99) | | | | | | rootn")(C23) | | | | | | rsqrt")(C23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hypot(C99) | | | | | | compound")(C23) | | | | | | pow | | | | | | pown")(C23) | | | | | | powr")(C23) | | | | | | | Trigonometric and hyperbolic functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinpi(C23) | | | | | | cospi(C23) | | | | | | tanpi")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinpi")(C23) | | | | | | acospi")(C23) | | | | | | atanpi")(C23) | | | | | | atan2pi")(C23) | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | asinh(C99) | | | | | | acosh(C99) | | | | | | atanh(C99) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Nearest integer floating-point | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ceil | | | | | | floor | | | | | | roundlroundllround(C99)(C99)(C99) | | | | | | roundeven(C23) | | | | | | trunc(C99) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nearbyint(C99) | | | | | | rintlrintllrint(C99)(C99)(C99) | | | | | | fromfpfromfpxufromfpufromfpx")(C23)(C23)(C23)(C23) | | | | | | | Floating-point manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ldexp | | | | | | frexp | | | | | | scalbnscalbln(C99)(C99) | | | | | | ****ilogbllogb****(C99)(C23) | | | | | | logb(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | modf | | | | | | nextafternexttoward(C99)(C99) | | | | | | nextupnextdown")(C23)(C23) | | | | | | copysign(C99) | | | | | | canonicalize")(C23) | | | | | | | Narrowing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fadd")(C23) | | | | | | fsub")(C23) | | | | | | fmul")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fdiv")(C23) | | | | | | ffma")(C23) | | | | | | fsqrt")(C23) | | | | | | | Quantum and quantum exponent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | quantized**N**")(C23) | | | | | | quantumd**N**")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | samequantumd**N**")(C23) | | | | | | llquantexpd**N**")(C23) | | | | | | | Decimal re-encoding functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | encodedecd**N**")(C23) | | | | | | decodedecd**N**")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | encodebind**N**")(C23) | | | | | | decodebind**N**")(C23) | | | | | | | Total order and payload functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | totalorder")(C23) | | | | | | getpayload")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setpayload")(C23) | | | | | | setpayloadsig")(C23) | | | | | | | Classification | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fpclassify(C99) | | | | | | iscanonical")(C23) | | | | | | isfinite(C99) | | | | | | isinf(C99) | | | | | | isnan(C99) | | | | | | isnormal(C99) | | | | | | signbit(C99) | | | | | | issubnormal")(C23) | | | | | | iszero")(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isgreater(C99) | | | | | | isgreaterequal(C99) | | | | | | isless(C99) | | | | | | islessequal(C99) | | | | | | islessgreater(C99) | | | | | | isunordered(C99) | | | | | | issignaling")(C23) | | | | | | iseqsig")(C23) | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Error and gamma functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | erf(C99) | | | | | | erfc(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lgamma(C99) | | | | | | tgamma(C99) | | | | | | | Types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | div_tldiv_tlldiv_timaxdiv_t(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | float_tdouble_t(C99)(C99) | | | | | | _Decimal32_t_Decimal64_t")(C23)(C23) | | | | | | | Macro constants | | | | | | Special floating-point values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | HUGE_VALHUGE_VALFHUGE_VALLHUGE_VALD**N**(C99)(C99)(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | INFINITYDEC_INFINITY(C99)(C23) | | | | | | NANDEC_NAN(C99)(C23) | | | | | | | Arguments and return values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****FP_ILOGB0FP_ILOGBNAN****(C99)(C99) | | | | | | FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C99)(C99)(C99)(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****FP_LLOGB0FP_LLOGBNAN****(C23)(C23) | | | | | | FP_INT_UPWARDFP_INT_DOWNWARDFP_INT_TOWARDZEROFP_INT_TONEARESTFROMZEROFP_INT_TONEAREST")(C23)(C23)(C23)(C23)(C23) | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MATH_ERRNOMATH_ERRNOEXCEPT(C99)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | math_errhandling(C99) | | | | | |  | | | | | | | Fast operation indicators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_FAST_FMAFFP_FAST_FMA(C99)(C99) | | | | | | FP_FAST_FADDFP_FAST_FADDLFP_FAST_DADDLFP_FAST_D**M**ADDD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FMULFP_FAST_FMULLFP_FAST_DMULLFP_FAST_D**M**MULD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FFMAFP_FAST_FFMALFP_FAST_DFMALFP_FAST_D**M**FMAD**N**")(C23)(C23)(C23)(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FP_FAST_FMALFP_FAST_FMAD**N**(C99)(C23) | | | | | | FP_FAST_FSUBFP_FAST_FSUBLFP_FAST_DSUBLFP_FAST_D**M**SUBD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FDIVFP_FAST_FDIVLFP_FAST_DDIVLFP_FAST_D**M**DIVD**N**")(C23)(C23)(C23)(C23) | | | | | | FP_FAST_FSQRTFP_FAST_FSQRTLFP_FAST_DSQRTLFP_FAST_D**M**SQRTD**N**")(C23)(C23)(C23)(C23) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<math.h>` |  |  |
| int ilogbf( float arg ); | (1) | (since C99) |
| int ilogb( double arg ); | (2) | (since C99) |
| int ilogbl( long double arg ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define ilogb( arg ) | (4) | (since C99) |
| Defined in header `<math.h>` |  |  |
| #define FP_ILOGB0    /\* implementation-defined \*/ | (5) | (since C99) |
| #define FP_ILOGBNAN  /\* implementation-defined \*/ | (6) | (since C99) |
|  |  |  |

1-3) Extracts the value of the unbiased exponent from the floating-point argument arg, and returns it as a signed integer value.4) Type-generic macros: If arg has type long double, `ilogbl` is called. Otherwise, if arg has integer type or the type double, `ilogb` is called. Otherwise, `ilogbf` is called.5) Expands to integer constant expression whose value is either INT_MIN or -INT_MAX.6) Expands to integer constant expression whose value is either INT_MIN or +INT_MAX.

Formally, the unbiased exponent is the integral part of logr|arg| as a signed integral value, for non-zero arg, where `r` is FLT_RADIX.

### Parameters

|  |  |  |
| --- | --- | --- |
| arg | - | floating-point value |

### Return value

If no errors occur, the unbiased exponent of arg is returned as a signed int value.

If arg is zero, FP_ILOGB0 is returned.

If arg is infinite, INT_MAX is returned.

If arg is a NaN, FP_ILOGBNAN is returned.

If the correct result is greater than INT_MAX or smaller than INT_MIN, the return value is unspecified and a domain error or range error may occur.

### Error handling

Errors are reported as specified in `math_errhandling`.

A domain error or range error may occur if arg is zero, infinite, or NaN.

If the correct result is greater than INT_MAX or smaller than INT_MIN, a domain error or a range error may occur

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- If the correct result is greater than INT_MAX or smaller than INT_MIN, FE_INVALID is raised.
- If arg is ±0, ±∞, or NaN, FE_INVALID is raised.
- In all other cases, the result is exact (FE_INEXACT is never raised) and the current rounding mode is ignored.

### Notes

If arg is not zero, infinite, or NaN, the value returned is exactly equivalent to (int)logb(arg).

POSIX requires that a domain error occurs if arg is zero, infinite, NaN, or if the correct result is outside of the range of int.

POSIX also requires that, on XSI-conformant systems, the value returned when the correct result is greater than INT_MAX is INT_MAX and the value returned when the correct result is less than INT_MIN is INT_MIN.

The correct result can be represented as int on all known implementations. For overflow to occur, INT_MAX must be less than LDBL_MAX_EXP \* log2(FLT_RADIX) or INT_MIN must be greater than LDBL_MIN_EXP - LDBL_MANT_DIG) \* log2(FLT_RADIX).

The value of the exponent returned by `ilogb` is always 1 less than the exponent retuned by frexp because of the different normalization requirements: for the exponent `e` returned by `ilogb`, |arg\*r-e  
| is between 1 and `r` (typically between 1 and 2), but for the exponent `e` returned by frexp, |arg\*2-e  
| is between 0.5 and 1.

### Example

Run this code

```
#include <fenv.h>
#include <float.h>
#include <math.h>
#include <stdio.h>
// #pragma STDC FENV_ACCESS ON
 
int main(void)
{
    double f = 123.45;
    printf("Given the number %.2f or %a in hex,\n", f, f);
 
    double f3;
    double f2 = modf(f, &f3);
    printf("modf() makes %.0f + %.2f\n", f3, f2);
 
    int i;
    f2 = frexp(f, &i);
    printf("frexp() makes %f * 2^%d\n", f2, i);
 
    i = ilogb(f);
    printf("logb()/ilogb() make %f * %d^%d\n", f/scalbn(1.0, i), FLT_RADIX, i);
 
    // error handling
    feclearexcept(FE_ALL_EXCEPT);
    printf("ilogb(0) = %d\n", ilogb(0));
    if (fetestexcept(FE_INVALID))
        puts("    FE_INVALID raised");
}

```

Possible output:

```
Given the number 123.45 or 0x1.edccccccccccdp+6 in hex,
modf() makes 123 + 0.45
frexp() makes 0.964453 * 2^7
logb()/ilogb() make 1.92891 * 2^6
ilogb(0) = -2147483648
    FE_INVALID raised

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.12/8 Mathematics <math.h> (p: TBD)

:   - 7.12.6.5 The ilogb functions (p: TBD)

:   - 7.25 Type-generic math <tgmath.h> (p: TBD)

:   - F.10.3.5 The ilogb functions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.12/8 Mathematics <math.h> (p: TBD)

:   - 7.12.6.5 The ilogb functions (p: TBD)

:   - 7.25 Type-generic math <tgmath.h> (p: TBD)

:   - F.10.3.5 The ilogb functions (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.12/8 Mathematics <math.h> (p: 232)

:   - 7.12.6.5 The ilogb functions (p: 244)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - F.10.3.5 The ilogb functions (p: 521)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.12/8 Mathematics <math.h> (p: 213)

:   - 7.12.6.5 The ilogb functions (p: 224-225)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - F.9.3.5 The ilogb functions (p: 458)

### See also

|  |  |
| --- | --- |
| frexpfrexpffrexpl(C99)(C99) | breaks a number into significand and a power of 2   (function) |
| logblogbflogbl(C99)(C99)(C99) | extracts exponent of the given number   (function) |
| scalbnscalbnfscalbnlscalblnscalblnfscalblnl(C99)(C99)(C99)(C99)(C99)(C99) | computes efficiently a number times FLT_RADIX raised to a power   (function) |
| C++ documentation for ilogb | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/math/ilogb&oldid=172026>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 May 2024, at 04:36.