# errno

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
| Error codes | | | | |
| ****errno**** | | | | |
| Assertions | | | | |
| assert | | | | |
| static_assert(C11)(removed in C23) | | | | |
| Bounds checking | | | | |
| set_constraint_handler_s(C11) | | | | |
| abort_handler_s(C11) | | | | |
| ignore_handler_s(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<errno.h>` |  |  |
| #define errno /\* implementation-defined \*/ |  |  |
|  |  |  |

`errno` is a preprocessor macro (but see note below) that expands to a thread-local(since C11) modifiable lvalue of type int. Several standard library functions indicate errors by writing positive integers to `errno`. Typically, the value of `errno` is set to one of the error codes listed in <errno.h> as macro constants beginning with the letter `E` followed by uppercase letters or digits.

The value of `errno` is ​0​ at program startup, and although library functions are allowed to write positive integers to `errno` whether or not an error occurred, library functions never store ​0​ in `errno`.

Library functions perror and strerror can be used to obtain textual descriptions of the error conditions that correspond to the current `errno` value.

Note: Until C11, the C standards had contradictory requirements, in that they said that `errno` is a macro but **also** that "it is unspecified whether `errno` is a macro or an identifier declared with external linkage". C11 fixes this, requiring that it be defined as a macro (see also WG14 N1338).

### Example

Run this code

```
#include <errno.h>
#include <math.h>
#include <stdio.h>
 
void show_errno(void)
{
    const char *err_info = "unknown error";
    switch (errno)
    {
        case EDOM:
            err_info = "domain error";
            break;
        case EILSEQ:
            err_info = "illegal sequence";
            break;
        case ERANGE:
            err_info = "pole or range error";
            break;
        case 0:
            err_info = "no error";
    }
    fputs(err_info, stdout);
    puts(" occurred");
}
 
int main(void)
{
    fputs("MATH_ERRNO is ", stdout);
    puts(math_errhandling & MATH_ERRNO ? "set" : "not set");
 
    errno = 0;
    (void)(1.0 / 0.0);
    show_errno();
 
    errno = 0;
    (void)acos(+1.1);
    show_errno();
 
    errno = 0;
    (void)log(0.0);
    show_errno();
 
    errno = 0;
    (void)sin(0.0);
    show_errno();
}

```

Possible output:

```
MATH_ERRNO is set
no error occurred
domain error occurred
pole or range error occurred
no error occurred

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.5 Errors <errno.h> (p: TBD)

:   - K.3.1.3 Use of errno (p: TBD)

:   - K.3.2 Errors <errno.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.5 Errors <errno.h> (p: TBD)

:   - K.3.1.3 Use of errno (p: TBD)

:   - K.3.2 Errors <errno.h> (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.5 Errors <errno.h> (p: 205)

:   - K.3.1.3 Use of errno (p: 584)

:   - K.3.2 Errors <errno.h> (p: 585)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.5 Errors <errno.h> (p: 186)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.1.3 Errors <errno.h>

### See also

|  |  |
| --- | --- |
| E2BIG, EACCES, ..., EXDEV | macros for standard POSIX-compatible error conditions   (macro constant) |
| perror | displays a character string corresponding of the current error to stderr   (function) |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | returns a text version of a given error code   (function) |
| math_errhandlingMATH_ERRNOMATH_ERREXCEPT(C99)(C99)(C99) | defines the error handling mechanism used by the common mathematical functions   (macro constant) |
| C++ documentation for errno | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/error/errno&oldid=180045>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 February 2025, at 23:12.