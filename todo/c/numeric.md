# Numerics

From cppreference.com
< c
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
| ****Numerics**** | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 ****Numerics****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Floating-point environment (C99) | | | | |
| Pseudo-random number generation | | | | |
| Complex number arithmetic (C99) | | | | |
| Type-generic math (C99) | | | | |
| Bit manipulation (C23) | | | | |
| Checked integer arithmetic (C23) | | | | |

The C numerics library includes common mathematical functions and types, as well as support for random number generation.

### Common mathematical functions

The header <math.h> provides standard C library mathematical functions such as fabs, sqrt, and sin.

### Floating-point environment

The header <fenv.h> defines flags and functions related to exceptional floating-point state, such as overflow and division by zero.

### Pseudo-random number generation

The header <stdlib.h> also includes C-style random number generation via srand and rand.

### Complex number arithmetic

The header <complex.h> provides types and functions to work with complex numbers.

### Type-generic math

The header <tgmath.h> provides some macros for a function which names XXX:

- real function:

:   - float variant `XXXf`
    - double variant `XXX`
    - long double variant `XXXl`

- complex function:

:   - float variant `cXXXf`
    - double variant `cXXX`
    - long double variant `cXXXl`

### Bit manipulation (since C23)

The header <stdbit.h> provides macros and functions to work with the byte ordering and byte and bit representation of C objects.

### Checked integer arithmetic (since C23)

Provides some type-generic macros for checked integer arithmetic:

|  |  |
| --- | --- |
| Defined in header `<stdckdint.h>` | |
| ckd_add(C23) | checked addition operation on two integers (type-generic function macro) |
| ckd_sub(C23) | checked subtraction operation on two integers (type-generic function macro) |
| ckd_mul(C23) | checked multiplication operation on two integers (type-generic function macro) |

### See also

|  |  |
| --- | --- |
| C++ documentation for Numerics library | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric&oldid=180191>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 February 2025, at 22:26.