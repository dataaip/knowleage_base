# C Standard Library headers

From cppreference.com
< c
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| ****Headers**** | | | | |
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

 ****Standard Library headers**** 

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | <assert.h> | | | | | | <complex.h> (C99) | | | | | | <ctype.h> | | | | | | <errno.h> | | | | | | <fenv.h> (C99) | | | | | | <float.h> | | | | | | <inttypes.h> (C99) | | | | | | <iso646.h> (C95) | | | | | | <limits.h> | | | | | | <locale.h> | | | | | | <math.h> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | <setjmp.h> | | | | | | <signal.h> | | | | | | <stdalign.h> (C11\*) | | | | | | <stdarg.h> | | | | | | <stdatomic.h> (C11) | | | | | | <stdbit.h> (C23) | | | | | | <stdbool.h> (C99\*) | | | | | | <stdckdint.h> (C23) | | | | | | <stddef.h> | | | | | | <stdint.h> (C99) | | | | | | <stdio.h> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | <stdlib.h> | | | | | | <stdnoreturn.h> (C11\*) | | | | | | <string.h> | | | | | | <tgmath.h> (C99) | | | | | | <threads.h> (C11) | | | | | | <time.h> | | | | | | <uchar.h> (C11) | | | | | | <wchar.h> (C95) | | | | | | <wctype.h> (C95) | | | | | |  | | | | | |  | | | | | |

The interface of C standard library is defined by the following collection of headers.

|  |  |
| --- | --- |
| <assert.h> | Conditionally compiled macro that compares its argument to zero |
| <complex.h> (since C99) | Complex number arithmetic |
| <ctype.h> | Functions to determine the type contained in character data |
| <errno.h> | Macros reporting error conditions |
| <fenv.h> (since C99) | Floating-point environment |
| <float.h> | Limits of floating-point types |
| <inttypes.h> (since C99) | Format conversion of integer types |
| <iso646.h> (since C95) | Alternative operator spellings |
| <limits.h> | Ranges of integer types |
| <locale.h> | Localization utilities |
| <math.h> | Common mathematics functions |
| <setjmp.h> | Nonlocal jumps |
| <signal.h> | Signal handling |
| <stdalign.h> (since C11)(deprecated in C23) | `alignas` and `alignof` convenience macros |
| <stdarg.h> | Variable arguments |
| <stdatomic.h> (since C11) | Atomic operations |
| <stdbit.h> (since C23) | Macros to work with the byte and bit representations of types |
| <stdbool.h> (since C99)(deprecated in C23) | Macros for boolean type |
| <stdckdint.h> (since C23) | Macros for performing checked integer arithmetic |
| <stddef.h> | Common macro definitions |
| <stdint.h> (since C99) | Fixed-width integer types |
| <stdio.h> | Input/output |
| <stdlib.h> | General utilities: memory management, program utilities, string conversions, random numbers, algorithms |
| <stdmchar.h> (since C29) | Text transcode |
| <stdnoreturn.h> (since C11)(deprecated in C23) | noreturn convenience macro |
| <string.h> | String handling |
| <tgmath.h> (since C99) | Type-generic math (macros wrapping math.h and complex.h) |
| <threads.h> (since C11) | Thread library |
| <time.h> | Time/date utilities |
| <uchar.h> (since C11) | UTF-16 and UTF-32 character utilities |
| <wchar.h> (since C95) | Extended multibyte and wide character utilities |
| <wctype.h> (since C95) | Functions to determine the type contained in wide character data |

### Feature test macros (since C23)

Feature test macros are defined in corresponding headers respectively since C23. Note that not all headers contain such a macro.

| # | Header | Macro name | Value |
| --- | --- | --- | --- |
| 1 | <assert.h> | __STDC_VERSION_ASSERT_H__ | 202311L |
| 2 | <complex.h> | __STDC_VERSION_COMPLEX_H__ | 202311L |
| 3 | <ctype.h> | N/A | |
| 4 | <errno.h> | N/A | |
| 5 | <fenv.h> | __STDC_VERSION_FENV_H__ | 202311L |
| 6 | <float.h> | __STDC_VERSION_FLOAT_H__ | 202311L |
| 7 | <inttypes.h> | __STDC_VERSION_INTTYPES_H__ | 202311L |
| 8 | <iso646.h> | N/A | |
| 9 | <limits.h> | __STDC_VERSION_LIMITS_H__ | 202311L |
| 10 | <locale.h> | N/A | |
| 11 | <math.h> | __STDC_VERSION_MATH_H__ | 202311L |
| 12 | <setjmp.h> | __STDC_VERSION_SETJMP_H__ | 202311L |
| 13 | <signal.h> | N/A | |
| 14 | <stdalign.h> | N/A | |
| 15 | <stdarg.h> | __STDC_VERSION_STDARG_H__ | 202311L |
| 16 | <stdatomic.h> | __STDC_VERSION_STDATOMIC_H__ | 202311L |
| 17 | <stdbit.h> | __STDC_VERSION_STDBIT_H__ | 202311L |
| 18 | <stdbool.h> | N/A | |
| 19 | <stdckdint.h> | __STDC_VERSION_STDCKDINT_H__ | 202311L |
| 20 | <stddef.h> | __STDC_VERSION_STDDEF_H__ | 202311L |
| 21 | <stdint.h> | __STDC_VERSION_STDINT_H__ | 202311L |
| 22 | <stdio.h> | __STDC_VERSION_STDIO_H__ | 202311L |
| 23 | <stdlib.h> | __STDC_VERSION_STDLIB_H__ | 202311L |
| 24 | <stdnoreturn.h> | N/A | |
| 25 | <string.h> | __STDC_VERSION_STRING_H__ | 202311L |
| 26 | <tgmath.h> | __STDC_VERSION_TGMATH_H__ | 202311L |
| 27 | <threads.h> | N/A | |
| 28 | <time.h> | __STDC_VERSION_TIME_H__ | 202311L |
| 29 | <uchar.h> | __STDC_VERSION_UCHAR_H__ | 202311L |
| 30 | <wchar.h> | __STDC_VERSION_WCHAR_H__ | 202311L |
| 31 | <wctype.h> | N/A | |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.1.2 Standard headers

- C17 standard (ISO/IEC 9899:2018):

:   - 7.1.2 Standard headers (p: 131-132)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.1.2 Standard headers (p: 181-182)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.1.2 Standard headers (p: 165)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.1.2 Standard headers

### See also

|  |  |
| --- | --- |
| C++ documentation for C++ Standard Library headers | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/header&oldid=180234>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 February 2025, at 13:59.