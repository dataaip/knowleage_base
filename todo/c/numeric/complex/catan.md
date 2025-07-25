# catanf, catan, catanl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | ****catan****(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       catanf( float complex z ); | (1) | (since C99) |
| double complex      catan( double complex z ); | (2) | (since C99) |
| long double complex catanl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define atan( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the complex arc tangent of `z` with branch cuts outside the interval [−i,+i] along the imaginary axis.4) Type-generic macro: If `z` has type long double complex, `catanl` is called. if `z` has type double complex, `catan` is called, if `z` has type float complex, `catanf` is called. If `z` is real or integer, then the macro invokes the corresponding real function (atanf, atan, atanl). If `z` is imaginary, then the macro invokes the corresponding real version of the function atanh, implementing the formula atan(iy) = i atanh(y), and the return type of the macro is imaginary.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

If no errors occur, complex arc tangent of `z` is returned, in the range of a strip unbounded along the imaginary axis and in the interval [−π/2; +π/2] along the real axis.

Errors and special cases are handled as if the operation is implemented by -I \* catanh(I\*z).

### Notes

Inverse tangent (or arc tangent) is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segments (-∞i,-i) and (+i,+∞i) of the imaginary axis.

The mathematical definition of the principal value of inverse tangent is atan z = -

|  |
| --- |
| 1 |
| 2 |

 i [ln(1 - iz) - ln (1 + iz]

### Example

Run this code

```
#include <stdio.h>
#include <float.h>
#include <complex.h>
 
int main(void)
{
    double complex z = catan(2*I);
    printf("catan(+0+2i) = %f%+fi\n", creal(z), cimag(z));
 
    double complex z2 = catan(-conj(2*I)); // or CMPLX(-0.0, 2)
    printf("catan(-0+2i) (the other side of the cut) = %f%+fi\n", creal(z2), cimag(z2));
 
    double complex z3 = 2*catan(2*I*DBL_MAX); // or CMPLX(0, INFINITY)
    printf("2*catan(+0+i*Inf) = %f%+fi\n", creal(z3), cimag(z3));
}

```

Output:

```
catan(+0+2i) = 1.570796+0.549306i
catan(-0+2i) (the other side of the cut) = -1.570796+0.549306i
2*catan(+0+i*Inf) = 3.141593+0.000000i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.5.3 The catan functions (p: 191)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.5.3 The catan functions (p: 173)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| casincasinfcasinl(C99)(C99)(C99) | computes the complex arc sine   (function) |
| cacoscacosfcacosl(C99)(C99)(C99) | computes the complex arc cosine   (function) |
| ctanctanfctanl(C99)(C99)(C99) | computes the complex tangent   (function) |
| atanatanfatanl(C99)(C99) | computes arc tangent (\({\small\arctan{x} }\)arctan(x))   (function) |
| C++ documentation for atan | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/catan&oldid=77471>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 March 2015, at 06:16.