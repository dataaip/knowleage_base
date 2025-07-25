# I

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex(C99) | | | | | | _Complex_I(C99) | | | | | | CMPLX(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaginary(C99) | | | | | | _Imaginary_I(C99) | | | | | | ****I****(C99) | | | | | |
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
| #define I /\* unspecified \*/ |  | (since C99) |
|  |  |  |

The `I` macro expands to either _Complex_I or _Imaginary_I. If the implementation does not support imaginary types, then the macro always expands to _Complex_I.

A program may undefine and perhaps then redefine the macro I.

### Notes

The macro is not named i, which is the name of the imaginary unit in mathematics, because the name `i` was already used in many C programs, e.g. as a loop counter variable.

The macro I is often used to form complex numbers, with expressions such as x + y\*I.
If `I` is defined as _Complex_I, then such expression may create a value with imaginary component `+0.0` even when `y` is `-0.0`, which is significant for complex number functions with branch cuts. The macro CMPLX provides a way to construct a complex number precisely.

GCC provides a non-portable extension that allows imaginary constants to be specified with the suffix `i` on integer literals: `1.0fi`, `1.0i`, and `1.0li` are imaginary units in GNU C. A similar approach is part of standard C++ as of C++14 (`1.0if`, `1.0i`, and `1.0il` are the imaginary units in C++)

### Example

Run this code

```
#include <stdio.h>
#include <complex.h>
 
int main(void)
{
    printf("I = %.1f%+.1fi\n", creal(I), cimag(I));
 
    double complex z1 = I * I;     // imaginary unit squared
    printf("I * I = %.1f%+.1fi\n", creal(z1), cimag(z1));
 
    double complex z = 1.0 + 2.0*I; // usual way to form a complex number pre-C11
    printf("z = %.1f%+.1fi\n", creal(z), cimag(z));
}

```

Output:

```
I = 0.0+1.0i
I * I = -1.0+0.0i
z = 1.0+2.0i

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.3.1/6 I (p: 188)

:   - G.6/1 I (p: 537)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.3.1/4 I (p: 170)

:   - G.6/1 I (p: 472)

### See also

|  |  |
| --- | --- |
| _Imaginary_I(C99) | the imaginary unit constant i   (macro constant) |
| _Complex_I(C99) | the complex unit constant i   (macro constant) |
| CMPLXCMPLXFCMPLXL(C11)(C11)(C11) | constructs a complex number from real and imaginary parts   (function macro) |
| C++ documentation for operator""i | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/complex/I&oldid=77426>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 March 2015, at 05:35.