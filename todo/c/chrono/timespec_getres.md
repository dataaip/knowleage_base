# timespec_getres

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
| ****timespec_getres****(C23) | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<time.h>` |  |  |
| int timespec_getres( struct timespec \*ts, int base ); |  | (since C23) |
|  |  |  |

If `ts` is non-null and `base` is supported by timespec_get, modifies \*ts to hold the resolution of time provided by timespec_get for `base`. For each supported `base`, multiple calls to `timespec_getres` during the same program execution have identical results.

### Parameters

|  |  |  |
| --- | --- | --- |
| ts | - | pointer to an object of type struct timespec |
| base | - | TIME_UTC or another nonzero integer value indicating the time base |

### Return value

The value of `base` if `base` is supported, zero otherwise.

### Notes

The POSIX function `clock_getres(clock_id, ts)` may also be used to populate a timespec with the resolution of time identified by `clock_id`.

### Example

Run this code

```
#include <stdio.h>
#include <time.h>
 
int main(void)
{
    char buff[128];
    struct timespec ts;
    const int res = timespec_getres(&ts, TIME_UTC);
    if (res == TIME_UTC) {
        struct tm timer;
        strftime(buff, sizeof buff, "%D %T", gmtime_r(&ts.tv_sec, &timer));
        printf("Time resolution info: %s.%09ld UTC\n", buff, ts.tv_nsec);
    } else {
        printf("TIME_UTC base is not supported.");
    }
}

```

Possible output:

```
Time resolution info: 01/01/70 00:00:00.000000001 UTC

```

### See also

|  |  |
| --- | --- |
| timespec(C11) | time in seconds and nanoseconds  (struct) |
| timespec_get(C11) | returns the calendar time in seconds and nanoseconds based on a given time base   (function) |
| time | returns the current calendar time of the system as time since epoch   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono/timespec_getres&oldid=125006>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 December 2020, at 04:30.