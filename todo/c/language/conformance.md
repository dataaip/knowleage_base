# Conformance

From cppreference.com
< c‎ | language
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

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

**Conformance** has a three-fold definition:

- **strictly conforming program** - uses only well-defined language constructs, that is constructs with a single behavior. It excludes unspecified, undefined, or implementation-defined behavior, and does not exceed any minimum implementation limit.
- **conforming program** - acceptable to a conforming implementation.
- **conforming implementation** -
  - A conforming hosted implementation shall accept any strictly conforming program.
  - A conforming freestanding implementation shall accept any strictly conforming program in which the use of the features specified in the library clause (clause 7) is confined to the contents of the freestanding standard library headers (see below).
  - A conforming implementation may have extensions (including additional library functions), provided they do not alter the behavior of any strictly conforming program.

### Explanation

The standard does not define any minimum implementation limit on translation units. A hosted environment has an operating system; a freestanding environment does not. A program running in a hosted environment may use all features described in the library clause (clause 7); a program running in a freestanding environment may use a subset of library features required by clause 4.

#### Freestanding standard library headers

All standard library features in every fully freestanding header are required to be provided by a freestanding implementation.

|  |  |
| --- | --- |
| Some standard library headers are conditionally freestanding.   - If the implementation predefines the macro `__STDC_IEC_60559_BFP__` or `__STDC_IEC_60559_DFP__`, then <math.h> and <fenv.h> are fully freestanding headers. However, the behavior of functions in these headers is required to be well-defined in a freestanding environment only if a program does not set the state of the FENV_ACCESS pragma to `ON`.   Some standard library headers are partially freestanding.   - In <stdlib.h>, memalignment is freestanding. Additionally, when `__STDC_IEC_60559_BFP__` or `__STDC_IEC_60559_DFP__` are predefined, numeric conversion functions (`atoX`, `strtoX`, and `strfromX`) are also freestanding, while their behavior is required to be well-defined in a freestanding environment only if a program does not set the state of the FENV_ACCESS pragma to `ON`. No other component in <stdlib.h> is required to be to be provided by a freestanding implementation. - In <string.h>, strdup, strndup, strcoll, strxfrm, strtok, and strerror are not required to be provided by a freestanding implementation. | (since C23) |

|  |  |
| --- | --- |
| Fully freestanding standard library headers | |
| <float.h> | Limits of floating-point types |
| <iso646.h> (since C95) | Alternative operator spellings |
| <limits.h> | Ranges of integer types |
| <stdalign.h> (since C11) | `alignas` and `alignof` convenience macros |
| <stdarg.h> | Variable arguments |
| <stdbool.h> (since C99) | Macros for boolean type |
| <stddef.h> | Common macro definitions |
| <stdint.h> (since C99) | Fixed-width integer types |
| <stdnoreturn.h> (since C11) | noreturn convenience macro |
| <stdbit.h> (since C23) | Macros to work with the byte and bit representations of types |
| Conditionally fully freestanding standard library headers | |
| <fenv.h> (since C23) | Floating-point environment |
| <math.h> (since C23) | Common mathematics functions |
| Partially freestanding standard library headers | |
| <stdlib.h> (since C23) | General utilities: memory management, program utilities, string conversions, random numbers, algorithms |
| <string.h> (since C23) | String handling |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 4 Conformance (p: 9-10)

- C17 standard (ISO/IEC 9899:2018):

:   - 4 Conformance (p: 4)

- C11 standard (ISO/IEC 9899:2011):

:   - 4 Conformance (p: 8-9)

- C99 standard (ISO/IEC 9899:1999):

:   - 4 Conformance (p: 7-8)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 1.7 Compliance

### See also

|  |  |
| --- | --- |
| C++ documentation for Freestanding and hosted implementation | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/conformance&oldid=177001>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 October 2024, at 17:50.