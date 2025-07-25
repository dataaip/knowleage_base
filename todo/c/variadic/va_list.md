# va_list

From cppreference.com
< c‎ | variadic
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

 Variadic functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| va_start | | | | |
| va_arg | | | | |
| va_copy(C99) | | | | |
| va_end | | | | |
| ****va_list**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdarg.h>` |  |  |
| /\* unspecified \*/ va_list; |  |  |
|  |  |  |

`va_list` is a complete object type suitable for holding the information needed by the macros va_start, va_copy, va_arg, and va_end.

If a `va_list` instance is created, passed to another function, and used via va_arg in that function, then any subsequent use in the calling function should be preceded by a call to va_end.

It is legal to pass a pointer to a `va_list` object to another function and then use that object after the function returns.

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.16/3 Variable arguments <stdarg.h> (p: 269)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.15/3 Variable arguments <stdarg.h> (p: 249)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.8 VARIABLE ARGUMENTS <stdarg.h>

### See also

|  |  |
| --- | --- |
| va_arg | accesses the next variadic function argument   (function macro) |
| va_copy(C99) | makes a copy of the variadic function arguments   (function macro) |
| va_end | ends traversal of the variadic function arguments   (function macro) |
| va_start | enables access to variadic function arguments   (function macro) |
| C++ documentation for va_list | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/variadic/va_list&oldid=117386>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 March 2020, at 01:10.