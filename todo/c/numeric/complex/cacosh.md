# cacoshf, cacosh, cacoshl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****cacosh****(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       cacoshf( float complex z ); | (1) | (since C99) |
| double complex      cacosh( double complex z ); | (2) | (since C99) |
| long double complex cacoshl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define acosh( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes complex arc hyperbolic cosine of a complex value `z` with branch cut at values less than 1 along the real axis.4) Type-generic macro: If `z` has type long double complex, `cacoshl` is called. if `z` has type double complex, `cacosh` is called, if `z` has type float complex, `cacoshf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (acoshf, acosh, acoshl). If `z` is imaginary, then the macro invokes the corresponding complex number version and the return type is complex.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

The complex arc hyperbolic cosine of `z` in the interval [0; ∞) along the real axis and in the interval [−iπ; +iπ] along the imaginary axis.

### Error handling and special values

Errors are reported consistent with math_errhandling

If the implementation supports IEEE floating-point arithmetic,

- cacosh(conj(z)) == conj(cacosh(z))
- If `z` is `±0+0i`, the result is `+0+iπ/2`
- If `z` is `+x+∞i` (for any finite x), the result is `+∞+iπ/2`
- If `z` is `+x+NaNi` (for non-zero finite x), the result is `NaN+NaNi` and FE_INVALID may be raised.
- If `z` is `0+NaNi`, the result is `NaN±iπ/2`, where the sign of the imaginary part is unspecified
- If `z` is `-∞+yi` (for any positive finite y), the result is `+∞+iπ`
- If `z` is `+∞+yi` (for any positive finite y), the result is `+∞+0i`
- If `z` is `-∞+∞i`, the result is `+∞+3iπ/4`
- If `z` is `+∞+∞i`, the result is `+∞+iπ/4`
- If `z` is `±∞+NaNi`, the result is `+∞+NaNi`
- If `z` is `NaN+yi` (for any finite y), the result is `NaN+NaNi` and FE_INVALID may be raised.
- If `z` is `NaN+∞i`, the result is `+∞+NaNi`
- If `z` is `NaN+NaNi`, the result is `NaN+NaNi`

### Notes

Although the C standard names this function "complex arc hyperbolic cosine", the inverse functions of the hyperbolic functions are the area functions. Their argument is the area of a hyperbolic sector, not an arc. The correct name is "complex inverse hyperbolic cosine", and, less common, "complex area hyperbolic cosine".

Inverse hyperbolic cosine is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segment (-∞,+1) of the real axis.

The mathematical definition of the principal value of the inverse hyperbolic cosine is acosh z = ln(z + √z+1 √z-1)

For any z, acosh(z) = 

|  |
| --- |
| √z-1 |
| √1-z |

 acos(z), or simply i acos(z) in the upper half of the complex plane.

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
int main(void)
{
    double complex z = cacosh(0.5);
    printf("cacosh(+0.5+0i) = %f%+fi\n", creal(z), cimag(z));
 
    double complex z2 = conj(0.5); // or cacosh(CMPLX(0.5, -0.0)) in C11
    printf("cacosh(+0.5-0i) (the other side of the cut) = %f%+fi\n", creal(z2), cimag(z2));
 
    // in upper half-plane, acosh(z) = i*acos(z) 
    double complex z3 = casinh(1+I);
    printf("casinh(1+1i) = %f%+fi\n", creal(z3), cimag(z3));
    double complex z4 = I*casin(1+I);
    printf("I*asin(1+1i) = %f%+fi\n", creal(z4), cimag(z4));
}

```

Output:

```
cacosh(+0.5+0i) = 0.000000-1.047198i
cacosh(+0.5-0i) (the other side of the cut) = 0.500000-0.000000i
casinh(1+1i) = 1.061275+0.666239i
I*asin(1+1i) = -1.061275+0.666239i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.6.1 The cacosh functions (p: 192)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.6.2.1 The cacosh functions (p: 539-540)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.6.1 The cacosh functions (p: 174)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.6.2.1 The cacosh functions (p: 474-475)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| cacoscacosfcacosl(C99)(C99)(C99) | computes the complex arc cosine   (function) |
| casinhcasinhfcasinhl(C99)(C99)(C99) | computes the complex arc hyperbolic sine   (function) |
| catanhcatanhfcatanhl(C99)(C99)(C99) | computes the complex arc hyperbolic tangent   (function) |
| ccoshccoshfccoshl(C99)(C99)(C99) | computes the complex hyperbolic cosine   (function) |
| acoshacoshfacoshl(C99)(C99)(C99) | computes inverse hyperbolic cosine (\({\small\operatorname{arcosh}{x} }\)arcosh(x))   (function) |
| C++ documentation for acosh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/cacosh&oldid=121959>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 August 2020, at 04:04.