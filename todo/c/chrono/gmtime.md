# gmtime, gmtime_r, gmtime_s

From cppreference.com
< c‎ | chrono
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

 Date and time utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Time manipulation | | | | |
| difftime | | | | |
| time | | | | |
| clock | | | | |
| timespec_get(C11) | | | | |
| timespec_getres(C23) | | | | |
| Format conversions | | | | |
| asctimeasctime_s(deprecated in C23)(C11) | | | | |
| ctimectime_s(deprecated in C23)(C11) | | | | |
| strftime | | | | |
| wcsftime(C95) | | | | |
| ****gmtimegmtime_rgmtime_s****(C23)(C11) | | | | |
| localtimelocaltime_rlocaltime_s(C23)(C11) | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<time.h>` |  |  |
| struct tm\* gmtime  ( const time_t\* timer ); | (1) |  |
| struct tm\* gmtime_r( const time_t\* timer, struct tm\* buf ); | (2) | (since C23) |
| struct tm\* gmtime_s( const time_t\* restrict timer, struct tm\* restrict buf ); | (3) | (since C11) |
|  |  |  |

1) Converts given time since epoch (a time_t value pointed to by timer) into calendar time, expressed in Coordinated Universal Time (UTC) in the `struct tm` format. The result is stored in static storage and a pointer to that static storage is returned.2) Same as (1), except that the function uses user-provided storage buf for the result.3) Same as (1), except that the function uses user-provided storage buf for the result and that the following errors are detected at runtime and call the currently installed constraint handler function:

:   - timer or buf is a null pointer
:   As with all bounds-checked functions, `gmtime_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <time.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| timer | - | pointer to a time_t object to convert |
| buf | - | pointer to a struct tm object to store the result |

### Return value

1) pointer to a static internal tm object on success, or null pointer otherwise. The structure may be shared between `gmtime`, localtime, and ctime and may be overwritten on each invocation.2,3) copy of the buf pointer, or null pointer on error (which may be a runtime constraint violation or a failure to convert the specified time to UTC).

### Notes

`gmtime` may not be thread-safe.

POSIX requires that `gmtime` and `gmtime_r` set errno to EOVERFLOW if they fail because the argument is too large.

The implementation of `gmtime_s` in Microsoft CRT is incompatible with the C standard since it has reversed parameter order.

### Example

Run this code

```
#define __STDC_WANT_LIB_EXT1__ 1
#define _XOPEN_SOURCE // for putenv
#include <stdio.h>
#include <stdlib.h>   // for putenv
#include <time.h>
 
int main(void)
{
    time_t t = time(NULL);
    printf("UTC:       %s", asctime(gmtime(&t)));
    printf("local:     %s", asctime(localtime(&t)));
    // POSIX-specific
    putenv("TZ=Asia/Singapore");
    printf("Singapore: %s", asctime(localtime(&t)));
 
#ifdef __STDC_LIB_EXT1__
    struct tm buf;
    char str[26];
    asctime_s(str, sizeof str, gmtime_s(&t, &buf));
    printf("UTC:       %s", str);
    asctime_s(str, sizeof str, localtime_s(&t, &buf));
    printf("local:     %s", str);
#endif
}

```

Possible output:

```
UTC:       Fri Sep 15 14:22:05 2017
local:     Fri Sep 15 14:22:05 2017
Singapore: Fri Sep 15 22:22:05 2017
UTC:       Fri Sep 15 14:22:05 2017
local:     Fri Sep 15 14:22:05 2017

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.27.3.3 The gmtime function (p: TBD)

:   - K.3.8.2.3 The gmtime_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.27.3.3 The gmtime function (p: 288)

:   - K.3.8.2.3 The gmtime_s function (p: 454-455)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.27.3.3 The gmtime function (p: 393-394)

:   - K.3.8.2.3 The gmtime_s function (p: 626-627)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.23.3.3 The gmtime function (p: 343)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.12.3.3 The gmtime function

### See also

|  |  |
| --- | --- |
| localtimelocaltime_rlocaltime_s(C23)(C11) | converts time since epoch to calendar time expressed as local time   (function) |
| C++ documentation for gmtime | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono/gmtime&oldid=172290>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 June 2024, at 06:19.