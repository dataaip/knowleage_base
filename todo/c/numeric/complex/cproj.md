# cprojf, cproj, cprojl

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cimag(C99) | | | | | | creal(C99) | | | | | | carg(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cabs(C99) | | | | | | conj(C99) | | | | | | ****cproj****(C99) | | | | | |
| Power and exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | clog(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cpow(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| float complex       cprojf( float complex z ); | (1) | (since C99) |
| double complex      cproj( double complex z ); | (2) | (since C99) |
| long double complex cprojl( long double complex z ); | (3) | (since C99) |
| Defined in header `<tgmath.h>` |  |  |
| #define cproj( z ) | (4) | (since C99) |
|  |  |  |

1-3) Computes the projection of `z` on the Riemann sphere.4) Type-generic macro: if `z` has type long double complex, long double imaginary, or long double, `cprojl` is called. If `z` has type float complex, float imaginary, or float, `cprojf` is called. If `z` has type double complex, double imaginary, double, or any integer type, `cproj` is called.

For most `z`, cproj(z)==z, but all complex infinities, even the numbers where one component is infinite and the other is NaN, become positive real infinity, INFINITY+0.0\*I or INFINITY-0.0\*I. The sign of the imaginary (zero) component is the sign of cimag(z).

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex argument |

### Return value

The projection of `z` on the Riemann sphere.

This function is fully specified for all possible inputs and is not subject to any errors described in math_errhandling

### Notes

The `cproj` function helps model the Riemann sphere by mapping all infinities to one (give or take the sign of the imaginary zero), and should be used just before any operation, especially comparisons, that might give spurious results for any of the other infinities.

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
#include <math.h>
 
int main(void)
{
    double complex z1 = cproj(1 + 2*I);
    printf("cproj(1+2i) = %.1f%+.1fi\n", creal(z1),cimag(z1));
 
    double complex z2 = cproj(INFINITY+2.0*I);
    printf("cproj(Inf+2i) = %.1f%+.1fi\n", creal(z2),cimag(z2));
 
    double complex z3 = cproj(INFINITY-2.0*I);
    printf("cproj(Inf-2i) = %.1f%+.1fi\n", creal(z3),cimag(z3));
}

```

Output:

```
cproj(1+2i) = 1.0+2.0i
cproj(Inf+2i) = inf+0.0i
cproj(Inf-2i) = inf-0.0i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.9.5 The cproj functions (p: 198)

:   - 7.25 Type-generic math <tgmath.h> (p: 373-375)

:   - G.7 Type-generic math <tgmath.h> (p: 545)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.9.4 The cproj functions (p: 179)

:   - 7.22 Type-generic math <tgmath.h> (p: 335-337)

:   - G.7 Type-generic math <tgmath.h> (p: 480)

### See also

|  |  |
| --- | --- |
| C++ documentation for proj | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/cproj&oldid=119329>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 May 2020, at 04:18.