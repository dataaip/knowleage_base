# Error handling

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
| ****Error handling**** | | | | |
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

 ****Error handling****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Error codes | | | | |
| Error codes | | | | |
| errno | | | | |
| Assertions | | | | |
| assert | | | | |
| static_assert(C11)(removed in C23) | | | | |
| Bounds checking | | | | |
| set_constraint_handler_s(C11) | | | | |
| abort_handler_s(C11) | | | | |
| ignore_handler_s(C11) | | | | |

### Error numbers

|  |  |
| --- | --- |
| Defined in header `<errno.h>` | |
| errno | macro which expands to POSIX-compatible thread-local error number variable (macro variable) |
| E2BIG, EACCES, ..., EXDEV | macros for standard POSIX-compatible error conditions   (macro constant) |

### Assertions

|  |  |
| --- | --- |
| Defined in header `<assert.h>` | |
| assert | aborts the program if the user-specified condition is not true. May be disabled for release builds   (function macro) |
| static_assert(C11)(removed in C23) | issues a compile-time diagnostic if the value of a constant expression is false   (keyword macro) |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Bounds checking The standard library provides bounds-checked versions of some existing functions (gets_s, fopen_s, printf_s, strcpy_s, wcscpy_s, mbstowcs_s, qsort_s, getenv_s, etc). This functionality is **optional** and is only available if __STDC_LIB_EXT1__ is defined. The following macros and functions support this functionality.   |  |  | | --- | --- | |  | | | Defined in header `<errno.h>` | | | Defined in header `<stdio.h>` | | | errno_t(C11) | a typedef for the type int, used to self-document functions that return errno values   (typedef) | |  | | | Defined in header `<stddef.h>` | | | Defined in header `<stdio.h>` | | | Defined in header `<stdlib.h>` | | | Defined in header `<string.h>` | | | Defined in header `<time.h>` | | | Defined in header `<wchar.h>` | | | rsize_t(C11) | a typedef for the same type as size_t, used to self-document functions that range-check their parameters at runtime   (typedef) | |  | | | Defined in header `<stdint.h>` | | | RSIZE_MAX(C11) | largest acceptable size for bounds-checked functions, expands to either constant or variable which may change at runtime (e.g. as the currently allocated memory size changes) (macro variable) | |  | | | Defined in header `<stdlib.h>` | | | set_constraint_handler_s(C11) | set the error callback for bounds-checked functions   (function) | | abort_handler_s(C11) | abort callback for the bounds-checked functions   (function) | | ignore_handler_s(C11) | ignore callback for the bounds-checked functions   (function) |   Note: implementations of bounds-checked functions are available as open-source libraries Safe C and Slibc, and as part of Watcom C. There is also an incompatible set of bounds-checked functions available in Visual Studio. | (since C11) |

### Notes

Since C23, static_assert is itself a keyword, which may also be a predefined macro, so `<assert.h>` no longer provides it.

### References

| Extended content |
| --- |
| - C23 standard (ISO/IEC 9899:2024):   - 7.2 Diagnostics <assert.h> (p: TBD)  - 7.5 Errors <errno.h> (p: TBD)  - 7.19 Common definitions <stddef.h> (p: TBD)  - 7.20 Integer types <stdint.h> (p: TBD)  - 7.21 Input/output <stdio.h> (p: TBD)  - 7.22 General utilities <stdlib.h> (p: TBD)  - K.3.1.3 Use of errno (p: TBD)  - K.3.2/2 errno_t (p: TBD)  - K.3.3/2 rsize_t (p: TBD)  - K.3.4/2 RSIZE_MAX (p: TBD)  - 7.31.3 Errors <errno.h> (p: TBD)  - 7.31.10 Integer types <stdint.h> (p: TBD)  - 7.31.11 Input/output <stdio.h> (p: TBD)  - 7.31.12 General utilities <stdlib.h> (p: TBD)   - C17 standard (ISO/IEC 9899:2018):   - 7.2 Diagnostics <assert.h> (p: TBD)  - 7.5 Errors <errno.h> (p: TBD)  - 7.19 Common definitions <stddef.h> (p: TBD)  - 7.20 Integer types <stdint.h> (p: TBD)  - 7.21 Input/output <stdio.h> (p: TBD)  - 7.22 General utilities <stdlib.h> (p: TBD)  - K.3.1.3 Use of errno (p: TBD)  - K.3.2/2 errno_t (p: TBD)  - K.3.3/2 rsize_t (p: TBD)  - K.3.4/2 RSIZE_MAX (p: TBD)  - 7.31.3 Errors <errno.h> (p: TBD)  - 7.31.10 Integer types <stdint.h> (p: TBD)  - 7.31.11 Input/output <stdio.h> (p: TBD)  - 7.31.12 General utilities <stdlib.h> (p: TBD)   - C11 standard (ISO/IEC 9899:2011):   - 7.2 Diagnostics <assert.h> (p: 186-187)  - 7.5 Errors <errno.h> (p: 205)  - 7.19 Common definitions <stddef.h> (p: 288)  - 7.20 Integer types <stdint.h> (p: 289-295)  - 7.21 Input/output <stdio.h> (p: 296-339)  - 7.22 General utilities <stdlib.h> (p: 340-360)  - K.3.1.3 Use of errno (p: 584)  - K.3.2/2 errno_t (p: 585)  - K.3.3/2 rsize_t (p: 585)  - K.3.4/2 RSIZE_MAX (p: 585)  - 7.31.3 Errors <errno.h> (p: 455)  - 7.31.10 Integer types <stdint.h> (p: 456)  - 7.31.11 Input/output <stdio.h> (p: 456)  - 7.31.12 General utilities <stdlib.h> (p: 456)   - C99 standard (ISO/IEC 9899:1999):   - 7.2 Diagnostics <assert.h> (p: 169)  - 7.5 Errors <errno.h> (p: 186)  - 7.26.3 Errors <errno.h> (p: 401)  - 7.26.8 Integer types <stdint.h> (p: 401)  - 7.26.9 Input/output <stdio.h> (p: 402)  - 7.26.10 General utilities <stdlib.h> (p: 402)   - C89/C90 standard (ISO/IEC 9899:1990):   - 4.2 DIAGNOSTICS <assert.h>  - 4.1.3 Errors <errno.h>  - 4.13.1 Errors <errno.h>  - 4.13.6 Input/output <stdio.h>  - 4.13.7 General utilities <stdlib.h> |

### See also

|  |  |
| --- | --- |
| math_errhandlingMATH_ERRNOMATH_ERREXCEPT(C99)(C99)(C99) | defines the error handling mechanism used by the common mathematical functions   (macro constant) |
| C++ documentation for Error handling | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/error&oldid=180038>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 February 2025, at 21:06.