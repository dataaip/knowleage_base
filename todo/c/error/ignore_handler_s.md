# ignore_handler_s

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
| errno | | | | |
| Assertions | | | | |
| assert | | | | |
| static_assert(C11)(removed in C23) | | | | |
| Bounds checking | | | | |
| set_constraint_handler_s(C11) | | | | |
| abort_handler_s(C11) | | | | |
| ****ignore_handler_s****(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
| void ignore_handler_s( const char \* restrict msg,  void \* restrict ptr,                         errno_t error ); |  | (since C11) |
|  |  |  |

The function simply returns to the caller without performing any other action.

A pointer to this function can be passed to set_constraint_handler_s to establish a runtime constraints violation handler that does nothing.

:   As with all bounds-checked functions, `ignore_handler_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including `<stdlib.h>`.

### Parameters

|  |  |  |
| --- | --- | --- |
| msg | - | pointer to character string that describes the error |
| ptr | - | pointer to an implementation-defined object or a null pointer. Examples of implementation-defined objects are objects that give the name of the function that detected the violation and the line number when the violation was detected |
| error | - | the error about to be returned by the calling function, if it happens to be one of the functions that return errno_t |

### Return value

(none)

### Notes

If `ignore_handler_s` is used as a the runtime constraints handler, the violations may be detected by examining the results of the bounds-checked function calls, which may be different for different functions (non-zero errno_t, null character written to the first byte of the output string, etc)

If `set_constraint_handler_s` is never called, the default handler is implementation-defined: it may be abort_handler_s, ignore_handler_s, or some other implementation-defined handler.

### Example

Run this code

```
#define __STDC_WANT_LIB_EXT1__ 1
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
#ifdef __STDC_LIB_EXT1__
    char dst[2];
    set_constraint_handler_s(ignore_handler_s);
    int r = strcpy_s(dst, sizeof dst, "Too long!");
    printf("dst = \"%s\", r = %d\n", dst, r);
    set_constraint_handler_s(abort_handler_s);
    r = strcpy_s(dst, sizeof dst, "Too long!");
    printf("dst = \"%s\", r = %d\n", dst, r);
#endif
}

```

Possible output:

```
dst = "", r = 22
abort_handler_s was called in response to a runtime-constraint violation.
 
The runtime-constraint violation was caused by the following expression in strcpy_s:
(s1max <= (s2_len=strnlen_s(s2, s1max)) ) (in string_s.c:62)
 
Note to end users: This program was terminated as a result
of a bug present in the software. Please reach out to your
software's vendor to get more help.
Aborted

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - K.3.6.1.3 The ignore_handler_s function (p: 606)

### See also

|  |  |
| --- | --- |
| abort_handler_s(C11) | abort callback for the bounds-checked functions   (function) |
| set_constraint_handler_s(C11) | set the error callback for bounds-checked functions   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/error/ignore_handler_s&oldid=78580>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 May 2015, at 18:11.