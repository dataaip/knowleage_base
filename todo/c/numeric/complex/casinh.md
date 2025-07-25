# casinhf, casinh, casinhl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | ****casinh****(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       casinhf( float complex z ); | (1) | (since C99) |
| double complex      casinh( double complex z ); | (2) | (since C99) |
| long double complex casinhl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define asinh( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex arc hyperbolic sine of `z` with branch cuts outside the interval [−i; +i] along the imaginary axis.4) Type-generic macro: If `z` has type long double complex, `casinhl` is called. if `z` has type double complex, `casinh` is called, if `z` has type float complex, `casinhf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (asinhf, asinh, asinhl). If `z` is imaginary, then the macro invokes the corresponding real version of the function asin, implementing the formula asinh(iy) = i asin(y), and the return type is imaginary.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, the complex arc hyperbolic sine of `z` is returned, in the range of a strip mathematically unbounded along the real axis and in the interval [−iπ/2; +iπ/2] along the imaginary axis.

### Error handling and special values

Errors are reported consistent with math_errhandling

If the implementation supports IEEE floating-point arithmetic,

- casinh(conj(z)) == conj(casinh(z))
- casinh(-z) == -casinh(z)
- If `z` is `+0+0i`, the result is `+0+0i`
- If `z` is `x+∞i` (for any positive finite x), the result is `+∞+π/2`
- If `z` is `x+NaNi` (for any finite x), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `+∞+yi` (for any positive finite y), the result is `+∞+0i`
- If `z` is `+∞+∞i`, the result is `+∞+iπ/4`
- If `z` is `+∞+NaNi`, the result is `+∞+NaNi`
- If `z` is `NaN+0i`, the result is `NaN+0i`
- If `z` is `NaN+yi` (for any finite nonzero y), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `NaN+∞i`, the result is `±∞+NaNi` (the sign of the real part is unspecified)
- If `z` is `NaN+NaNi`, the result is `NaN+NaNi`

### Notes

Although the C standard names this function "complex arc hyperbolic sine", the inverse functions of the hyperbolic functions are the area functions. Their argument is the area of a hyperbolic sector, not an arc. The correct name is "complex inverse hyperbolic sine", and, less common, "complex area hyperbolic sine".

Inverse hyperbolic sine is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segments (-**i**∞,-**i**) and (**i**,**i**∞) of the imaginary axis.

The mathematical definition of the principal value of the inverse hyperbolic sine is asinh z = ln(z + √1+z2  
)

For any z, asinh(z) = 

|  |
| --- |
| asin(iz) |
| i |

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
int main(void)
{
    double complex z = casinh(0+2*I);
    printf("casinh(+0+2i) = %f%+fi\n", creal(z), cimag(z));
 
    double complex z2 = casinh(-conj(2*I)); // or casinh(CMPLX(-0.0, 2)) in C11
    printf("casinh(-0+2i) (the other side of the cut) = %f%+fi\n", creal(z2), cimag(z2));
 
    // for any z, asinh(z) = asin(iz)/i
    double complex z3 = casinh(1+2*I);
    printf("casinh(1+2i) = %f%+fi\n", creal(z3), cimag(z3));
    double complex z4 = casin((1+2*I)*I)/I;
    printf("casin(i * (1+2i))/i = %f%+fi\n", creal(z4), cimag(z4));
}

```

Output:

```
casinh(+0+2i) = 1.316958+1.570796i
casinh(-0+2i) (the other side of the cut) = -1.316958+1.570796i
casinh(1+2i) = 1.469352+1.063440i
casin(i * (1+2i))/i =  1.469352+1.063440i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.6.2 The casinh functions (p: 192-193)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.6.2.2 The casinh functions (p: 540)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.6.2 The casinh functions (p: 174-175)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.6.2.2 The casinh functions (p: 475)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| cacoshcacoshfcacoshl(C99)(C99)(C99) | computes the complex arc hyperbolic cosine   (function) |
| catanhcatanhfcatanhl(C99)(C99)(C99) | computes the complex arc hyperbolic tangent   (function) |
| csinhcsinhfcsinhl(C99)(C99)(C99) | computes the complex hyperbolic sine   (function) |
| asinhasinhfasinhl(C99)(C99)(C99) | computes inverse hyperbolic sine (\({\small\operatorname{arsinh}{x} }\)arsinh(x))   (function) |
| C++ documentation for asinh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/casinh&oldid=77475>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 March 2015, at 06:22.