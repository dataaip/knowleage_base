# Error numbers

From cppreference.com
< c‎ | error
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

 Error handling

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Error codes | | | | |
| ****Error codes**** | | | | |
| errno | | | | |
| Assertions | | | | |
| assert | | | | |
| static_assert(C11)(removed in C23) | | | | |
| Bounds checking | | | | |
| set_constraint_handler_s(C11) | | | | |
| abort_handler_s(C11) | | | | |
| ignore_handler_s(C11) | | | | |

Each of the macros defined in <errno.h> expands to an integer constant expression with type int and with a unique positive value. The following constants are defined by ISO C. The implementation may define more, as long as they begin with 'E' followed by digits or uppercase letters.

|  |  |
| --- | --- |
| Defined in header `<errno.h>` | |
| EDOM | Mathematics argument out of domain of function   (macro constant) |
| EILSEQ(C95) | Illegal byte sequence   (macro constant) |
| ERANGE | Result too large   (macro constant) |

### Notes

Many additional errno constants are defined by POSIX and by the C++ standard library, and individual implementations may define even more, e.g. errno(3) on Linux or intro(2) on BSD and OS X.

### Example

Run this code

```
#include <errno.h>
#include <math.h>
#include <stdio.h>
#include <string.h>
 
int main(void)
{
    errno = 0;
    printf("log(-1.0) = %f\n", log(-1.0));
    printf("%s\n\n", strerror(errno));
 
    errno = 0;
    printf("log(0.0)  = %f\n", log(0.0));
    printf("%s\n", strerror(errno));
}

```

Possible output:

```
log(-1.0) = nan
Numerical argument out of domain
 
log(0.0)  = -inf
Numerical result out of range

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.5/2 Errors <errno.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.5/2 Errors <errno.h> (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.5/2 Errors <errno.h> (p: 205)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.5/2 Errors <errno.h> (p: 186)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.1.3 Errors <errno.h>

### See also

|  |  |
| --- | --- |
| errno | macro which expands to POSIX-compatible thread-local error number variable (macro variable) |
| perror | displays a character string corresponding of the current error to stderr   (function) |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | returns a text version of a given error code   (function) |
| C++ documentation for Error numbers | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/error/errno_macros&oldid=180046>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 February 2025, at 23:14.