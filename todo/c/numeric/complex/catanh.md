# catanhf, catanh, catanhl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | clog(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cpow(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | ****catanh****(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       catanhf( float complex z ); | (1) | (since C99) |
| double complex      catanh( double complex z ); | (2) | (since C99) |
| long double complex catanhl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define atanh( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex arc hyperbolic tangent of `z` with branch cuts outside the interval [−1; +1] along the real axis.4) Type-generic macro: If `z` has type long double complex, `catanhl` is called. if `z` has type double complex, `catanh` is called, if `z` has type float complex, `catanhf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (atanhf, atanh, atanhl). If `z` is imaginary, then the macro invokes the corresponding real version of atan, implementing the formula atanh(iy) = i atan(y), and the return type is imaginary.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, the complex arc hyperbolic tangent of `z` is returned, in the range of a half-strip mathematically unbounded along the real axis and in the interval [−iπ/2; +iπ/2] along the imaginary axis.

### Error handling and special values

Errors are reported consistent with math_errhandling

If the implementation supports IEEE floating-point arithmetic,

- catanh(conj(z)) == conj(catanh(z))
- catanh(-z) == -catanh(z)
- If `z` is `+0+0i`, the result is `+0+0i`
- If `z` is `+0+NaNi`, the result is `+0+NaNi`
- If `z` is `+1+0i`, the result is `+∞+0i` and FE_DIVBYZERO is raised
- If `z` is `x+∞i` (for any finite positive x), the result is `+0+iπ/2`
- If `z` is `x+NaNi` (for any finite nonzero x), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `+∞+yi` (for any finite positive y), the result is `+0+iπ/2`
- If `z` is `+∞+∞i`, the result is `+0+iπ/2`
- If `z` is `+∞+NaNi`, the result is `+0+NaNi`
- If `z` is `NaN+yi` (for any finite y), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `NaN+∞i`, the result is `±0+iπ/2` (the sign of the real part is unspecified)
- If `z` is `NaN+NaNi`, the result is `NaN+NaNi`

### Notes

Although the C standard names this function "complex arc hyperbolic tangent", the inverse functions of the hyperbolic functions are the area functions. Their argument is the area of a hyperbolic sector, not an arc. The correct name is "complex inverse hyperbolic tangent", and, less common, "complex area hyperbolic tangent".

Inverse hyperbolic tangent is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segmentd (-∞,-1] and +1,+∞) of the real axis.

The mathematical definition of the principal value of the inverse hyperbolic tangent is atanh z = 

|  |
| --- |
| ln(1+z)-ln(z-1) |
| 2 |

.For any z, atanh(z) = 

|  |
| --- |
| atan(iz) |
| i |

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
int main(void)
{
    double complex z = catanh(2);
    printf("catanh(+2+0i) = %f%+fi\n", creal(z), cimag(z));
 
    double complex z2 = catanh(conj(2)); // or catanh(CMPLX(2, -0.0)) in C11
    printf("catanh(+2-0i) (the other side of the cut) = %f%+fi\n", creal(z2), cimag(z2));
 
    // for any z, atanh(z) = atan(iz)/i
    double complex z3 = catanh(1+2*I);
    printf("catanh(1+2i) = %f%+fi\n", creal(z3), cimag(z3));
    double complex z4 = catan((1+2*I)*I)/I;
    printf("catan(i * (1+2i))/i = %f%+fi\n", creal(z4), cimag(z4));
}

```

Output:

```
catanh(+2+0i) = 0.549306+1.570796i
catanh(+2-0i) (the other side of the cut) = 0.549306-1.570796i
catanh(1+2i) = 0.173287+1.178097i
catan(i * (1+2i))/i = 0.173287+1.178097i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.6.3 The catanh functions (p: 193)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.6.2.3 The catanh functions (p: 540-541)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.6.3 The catanh functions (p: 175)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.6.2.3 The catanh functions (p: 475-476)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| [casinhcasinhfcasinhl(C99)(C99)(C99) | computes the complex arc hyperbolic sine   (function) |
| cacoshcacoshfcacoshl(C99)(C99)(C99) | computes the complex arc hyperbolic cosine   (function) |
| ctanhctanhfctanhl(C99)(C99)(C99) | computes the complex hyperbolic tangent   (function) |
| atanhatanhfatanhl(C99)(C99)(C99) | computes inverse hyperbolic tangent (\({\small\operatorname{artanh}{x} }\)artanh(x))   (function) |
| C++ documentation for atanh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/catanh&oldid=96166>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 October 2017, at 21:14.