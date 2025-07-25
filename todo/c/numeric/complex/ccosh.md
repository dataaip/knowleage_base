# ccoshf, ccosh, ccoshl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****ccosh****(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       ccoshf( float complex z ); | (1) | (since C99) |
| double complex      ccosh( double complex z ); | (2) | (since C99) |
| long double complex ccoshl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define cosh( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex hyperbolic cosine of `z`.4) Type-generic macro: If `z` has type long double complex, `ccoshl` is called. if `z` has type double complex, `ccosh` is called, if `z` has type float complex, `ccoshf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (coshf, cosh, coshl). If `z` is imaginary, then the macro invokes the corresponding real version of the function cos, implementing the formula cosh(iy) = cos(y), and the return type is real.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, complex hyperbolic cosine of `z` is returned

### Error handling and special values

Errors are reported consistent with math_errhandling

If the implementation supports IEEE floating-point arithmetic,

- ccosh(conj(z)) == conj(ccosh(z))
- ccosh(z) == ccosh(-z)
- If `z` is `+0+0i`, the result is `1+0i`
- If `z` is `+0+∞i`, the result is `NaN±0i` (the sign of the imaginary part is unspecified) and FE_INVALID is raised
- If `z` is `+0+NaNi`, the result is `NaN±0i` (the sign of the imaginary part is unspecified)
- If `z` is `x+∞i` (for any finite non-zero x), the result is `NaN+NaNi` and FE_INVALID is raised
- If `z` is `x+NaNi` (for any finite non-zero x), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `+∞+0i`, the result is `+∞+0i`
- If `z` is `+∞+yi` (for any finite non-zero y), the result is `+∞cis(y)`
- If `z` is `+∞+∞i`, the result is `±∞+NaNi` (the sign of the real part is unspecified) and FE_INVALID is raised
- If `z` is `+∞+NaN`, the result is `+∞+NaN`
- If `z` is `NaN+0i`, the result is `NaN±0i` (the sign of the imaginary part is unspecified)
- If `z` is `NaN+yi` (for any finite non-zero y), the result is `NaN+NaNi` and FE_INVALID may be raised
- If `z` is `NaN+NaNi`, the result is `NaN+NaNi`

where cis(y) is cos(y) + i sin(y)

### Notes

Mathematical definition of hyperbolic cosine is cosh z = 

|  |
| --- |
| ez +e-z |
| 2 |

Hyperbolic cosine is an entire function in the complex plane and has no branch cuts. It is periodic with respect to the imaginary component, with period 2πi

### Example

Run this code

```
#include <stdio.h>
#include <math.h>
#include <complex.h>
 
int main(void)
{
    double complex z = ccosh(1);  // behaves like real cosh along the real line
    printf("cosh(1+0i) = %f%+fi (cosh(1)=%f)\n", creal(z), cimag(z), cosh(1));
 
    double complex z2 = ccosh(I); // behaves like real cosine along the imaginary line
    printf("cosh(0+1i) = %f%+fi ( cos(1)=%f)\n", creal(z2), cimag(z2), cos(1));
}

```

Output:

```
cosh(1+0i) = 1.543081+0.000000i (cosh(1)=1.543081)
cosh(0+1i) = 0.540302+0.000000i ( cos(1)=0.540302)

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.6.4 The ccosh functions (p: 193)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.6.2.4 The ccosh functions (p: 541)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.6.4 The ccosh functions (p: 175)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.6.2.4 The ccosh functions (p: 476)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| csinhcsinhfcsinhl(C99)(C99)(C99) | computes the complex hyperbolic sine   (function) |
| ctanhctanhfctanhl(C99)(C99)(C99) | computes the complex hyperbolic tangent   (function) |
| cacoshcacoshfcacoshl(C99)(C99)(C99) | computes the complex arc hyperbolic cosine   (function) |
| coshcoshfcoshl(C99)(C99) | computes hyperbolic cosine (\({\small\cosh{x} }\)cosh(x))   (function) |
| C++ documentation for cosh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/ccosh&oldid=96399>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 October 2017, at 19:16.