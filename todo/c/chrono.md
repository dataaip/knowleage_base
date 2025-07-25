# Date and time utilities

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
| Numerics | | | | |
| ****Date and time utilities**** | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 ****Date and time utilities****

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
| gmtimegmtime_rgmtime_s(C23)(C11) | | | | |
| localtimelocaltime_rlocaltime_s(C23)(C11) | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C11) | | | | |

### Functions

|  |  |
| --- | --- |
| Time manipulation | |
| Defined in header `<time.h>` | |
| difftime | computes the difference between times   (function) |
| time | returns the current calendar time of the system as time since epoch   (function) |
| clock | returns raw processor clock time since the program is started   (function) |
| timespec_get(C11) | returns the calendar time in seconds and nanoseconds based on a given time base   (function) |
| timespec_getres(C23) | returns the resolution of calendar time based on a given time base   (function) |
| Format conversions | |
| Defined in header `<time.h>` | |
| asctimeasctime_s(deprecated in C23)(C11) | converts a tm object to a textual representation   (function) |
| ctimectime_s(deprecated in C23)(C11) | converts a time_t object to a textual representation   (function) |
| strftime | converts a tm object to custom textual representation   (function) |
| Defined in header `<wchar.h>` | |
| wcsftime(C95) | converts a tm object to custom wide string textual representation   (function) |
| Defined in header `<time.h>` | |
| gmtimegmtime_rgmtime_s(C23)(C11) | converts time since epoch to calendar time expressed as Coordinated Universal Time (UTC)   (function) |
| localtimelocaltime_rlocaltime_s(C23)(C11) | converts time since epoch to calendar time expressed as local time   (function) |
| mktime | converts calendar time to time since epoch   (function) |

### Constants

|  |  |
| --- | --- |
| Defined in header `<time.h>` | |
| CLOCKS_PER_SEC | number of processor clock ticks per second   (macro constant) |

### Types

|  |  |
| --- | --- |
| Defined in header `<time.h>` | |
| tm | calendar time type (struct) |
| time_t | calendar time since epoch type   (typedef) |
| clock_t | processor time since era type   (typedef) |
| timespec(C11) | time in seconds and nanoseconds  (struct) |

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.27 Date and time <time.h> (p: 284-291)

:   - 7.29.5.1 The wcsftime function (p: 320-321)

:   - 7.31.14 Date and time <time.h> (p: 333)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.27 Date and time <time.h> (p: 388-397)

:   - 7.29.5.1 The wcsftime function (p: 439-440)

:   - 7.31.14 Date and time <time.h> (p: 456)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.23 Date and time <time.h> (p: 338-347)

:   - 7.24.5.1 The wcsftime function (p: 385-386)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.12 DATE AND TIME <time.h>

### See also

|  |  |
| --- | --- |
| C++ documentation for C Date and time utilities | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono&oldid=143967>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 October 2022, at 05:04.