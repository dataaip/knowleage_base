# _Complex_I

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex(C99) | | | | | | ****_Complex_I****(C99) | | | | | | CMPLX(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaginary(C99) | | | | | | _Imaginary_I(C99) | | | | | | I(C99) | | | | | |
| Manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cimag(C99) | | | | | | creal(C99) | | | | | | carg(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cabs(C99) | | | | | | conj(C99) | | | | | | cproj(C99) | | | | | |
| Power and exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | cexp(C99) | | | | | | clog(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cpow(C99) | | | | | | csqrt(C99) | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccos(C99) | | | | | | csin(C99) | | | | | | ctan(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacos(C99) | | | | | | casin(C99) | | | | | | catan(C99) | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ccosh(C99) | | | | | | csinh(C99) | | | | | | ctanh(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cacosh(C99) | | | | | | casinh(C99) | | | | | | catanh(C99) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex.h>` |  |  |
| #define _Complex_I /\* unspecified \*/ |  | (since C99) |
|  |  |  |

The `_Complex_I` macro expands to a value of type const float _Complex with the value of the imaginary unit.

### Notes

This macro may be used when I is not available, such as when it has been undefined by the application.

Unlike _Imaginary_I and CMPLX, use of this macro to construct a complex number may lose the sign of zero on the imaginary part.

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
#undef I
#define J _Complex_I // can be used to redefine I
 
int main(void)
{
    // can be used to construct a complex number
    double complex z = 1.0 + 2.0 * _Complex_I;
    printf("1.0 + 2.0 * _Complex_I = %.1f%+.1fi\n", creal(z), cimag(z));
 
    // sign of zero may not be preserved
    double complex z2 = 0.0 + -0.0 * _Complex_I;
    printf("0.0 + -0.0 * _Complex_I = %.1f%+.1fi\n", creal(z2), cimag(z2));
}

```

Possible output:

```
1.0 + 2.0 * _Complex_I = 1.0+2.0i
0.0 + -0.0 * _Complex_I = 0.0+0.0i

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.3.1/4 _Complex_I (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.3.1/4 _Complex_I (p: 136)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.1/4 _Complex_I (p: 188)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.1/2 _Complex_I (p: 170)

### See also

|  |  |
| --- | --- |
| _Imaginary_I(C99) | the imaginary unit constant i   (macro constant) |
| I(C99) | the complex or imaginary unit constant i   (macro constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/Complex_I&oldid=147475>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2023, at 12:04.