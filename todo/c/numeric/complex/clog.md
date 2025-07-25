# clogf, clog, clogl

From cppreference.com
< c‎ | numeric‎ | complex
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

 Complex number arithmetic

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and the imaginary constant | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex(C99) | | | | | | _Complex_I(C99) | | | | | | CMPLX(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaginary(C99) | | | | | | _Imaginary_I(C99) | | | | | | I(C99) | | | | | |
| Manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cimag(C99) | | | | | | creal(C99) | | | | | | carg(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cabs(C99) | | | | | | conj(C99) | | | | | | cproj(C99) | | | | | |
| Power and exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | ****clog****(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cpow(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       clogf( float complex z ); | (1) | (since C99) |
| double complex      clog( double complex z ); | (2) | (since C99) |
| long double complex clogl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define log( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex natural (base-**e**) logarithm of `z` with branch cut along the negative real axis.4) Type-generic macro: If `z` has type long double complex, `clogl` is called. if `z` has type double complex, `clog` is called, if `z` has type float complex, `clogf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (logf, log, logl). If `z` is imaginary, the corresponding complex number version is called.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, the complex natural logarithm of `z` is returned, in the range of a strip in the interval [−iπ, +iπ] along the imaginary axis and mathematically unbounded along the real axis.

### Error handling and special values

Errors are reported consistent with math_errhandling

If the implementation supports IEEE floating-point arithmetic,

- The function is continuous onto the branch cut taking into account the sign of imaginary part
- clog(conj(z)) == conj(clog(z))
- If `z` is `-0+0i`, the result is `-∞+πi` and FE_DIVBYZERO is raised
- If `z` is `+0+0i`, the result is `-∞+0i` and FE_DIVBYZERO is raised
- If `z` is `x+∞i` (for any finite x), the result is `+∞+πi/2`
- If `z` is `x+NaNi` (for any finite x), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `-∞+yi` (for any finite positive y), the result is `+∞+πi`
- If `z` is `+∞+yi` (for any finite positive y), the result is `+∞+0i`
- If `z` is `-∞+∞i`, the result is `+∞+3πi/4`
- If `z` is `+∞+∞i`, the result is `+∞+πi/4`
- If `z` is `±∞+NaNi`, the result is `+∞+NaNi`
- If `z` is `NaN+yi` (for any finite y), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `NaN+∞i`, the result is `+∞+NaNi`
- If `z` is `NaN+NaNi`, the result is `NaN+NaNi`

### Notes

The natural logarithm of a complex number z with polar coordinate components (r,θ) equals ln r + i(θ+2nπ), with the principal value ln r + iθ

### Example

Run this code

```
#include <stdio.h>
#include <math.h>
#include <complex.h>
 
int main(void)
{
    double complex z = clog(I); // r = 1, θ = pi/2
    printf("2*log(i) = %.1f%+fi\n", creal(2*z), cimag(2*z));
 
    double complex z2 = clog(sqrt(2)/2 + sqrt(2)/2*I); // r = 1, θ = pi/4
    printf("4*log(sqrt(2)/2+sqrt(2)i/2) = %.1f%+fi\n", creal(4*z2), cimag(4*z2));
 
    double complex z3 = clog(-1); // r = 1, θ = pi
    printf("log(-1+0i) = %.1f%+fi\n", creal(z3), cimag(z3));
 
    double complex z4 = clog(conj(-1)); // or clog(CMPLX(-1, -0.0)) in C11
    printf("log(-1-0i) (the other side of the cut) = %.1f%+fi\n", creal(z4), cimag(z4));
}

```

Output:

```
2*log(i) = 0.0+3.141593i
4*log(sqrt(2)/2+sqrt(2)i/2) = 0.0+3.141593i
log(-1+0i) = 0.0+3.141593i
log(-1-0i) (the other side of the cut) = 0.0-3.141593i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.7.2 The clog functions (p: 195)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.6.3.2 The clog functions (p: 543-544)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.7.2 The clog functions (p: 176-177)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.6.3.2 The clog functions (p: 478-479)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| cexpcexpfcexpl(C99)(C99)(C99) | computes the complex base-e exponential   (function) |
| loglogflogl(C99)(C99) | computes natural (base-**e**) logarithm (\({\small \ln{x} }\)ln(x))   (function) |
| C++ documentation for log | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/clog&oldid=96195>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 October 2017, at 23:25.