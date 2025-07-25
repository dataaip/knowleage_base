# CMPLXF, CMPLX, CMPLXL

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex(C99) | | | | | | _Complex_I(C99) | | | | | | ****CMPLX****(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaginary(C99) | | | | | | _Imaginary_I(C99) | | | | | | I(C99) | | | | | |
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
| float complex       CMPLXF( float real, float imag ); |  | (since C11) |
| double complex      CMPLX( double real, double imag ); |  | (since C11) |
| long double complex CMPLXL( long double real, long double imag ); |  | (since C11) |
|  |  |  |

Each of these macros expands to an expression that evaluates to the value of the specified complex type, with the real part having the value of `real` (converted to the specified argument type) and the imaginary part having the value of `imag` (converted to the specified argument type)

The expressions are suitable for use as initializers for objects with static or thread storage duration, as long as the expressions `real` and `imag` are also suitable.

### Parameters

|  |  |  |
| --- | --- | --- |
| real | - | the real part of the complex number to return |
| imag | - | the imaginary part of the complex number to return |

### Return value

A complex number composed of `real` and `imag` as the real and imaginary parts.

### Notes

These macros are implemented as if the imaginary types are supported (even if they are otherwise not supported and _Imaginary_I is actually undefined) and as if defined as follows:

```
#define CMPLX(x, y) ((double complex)((double)(x) + _Imaginary_I * (double)(y)))
#define CMPLXF(x, y) ((float complex)((float)(x) + _Imaginary_I * (float)(y)))
#define CMPLXL(x, y) ((long double complex)((long double)(x) + \
                      _Imaginary_I * (long double)(y)))

```

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
int main(void)
{
    double complex z = CMPLX(0.0, -0.0);
    printf("z = %.1f%+.1fi\n", creal(z), cimag(z));
}

```

Output:

```
z = 0.0-0.0i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.9.3 The CMPLX macros (p: 197)

### See also

|  |  |
| --- | --- |
| _Imaginary_I(C99) | the imaginary unit constant i   (macro constant) |
| C++ documentation for complex | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/CMPLX&oldid=77485>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 March 2015, at 09:33.