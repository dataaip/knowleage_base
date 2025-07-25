# timespec

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
| gmtimegmtime_rgmtime_s(C23)(C11) | | | | |
| localtimelocaltime_rlocaltime_s(C23)(C11) | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| clock_t | | | | |
| ****timespec****(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<time.h>` |  |  |
| struct timespec; |  | (since C11) |
|  |  |  |

Structure holding an interval broken down into seconds and nanoseconds.

### Member objects

|  |  |
| --- | --- |
| Member | Description |
| time_t `tv_sec` | whole seconds (valid values are >= ​0​) |
| /\* see below \*/ `tv_nsec` | nanoseconds (valid values are `[`​0​`,`999999999`]`) |

|  |  |
| --- | --- |
| The type of `tv_nsec` is long. | (until C23) |
| The type of `tv_nsec` is an implementation-defined signed integer type that can represent integers in `[`​0​`,`999999999`]`. | (since C23) |

The declaration order of `tv_sec` and `tv_nsec` is unspecified. Implementation may add other members to struct timespec.

### Notes

The type of `tv_nsec` is long long on some platforms, which is conforming only since C23.

### Example

Run this code

```
#include <stdint.h>
#include <stdio.h>
#include <time.h>
 
int main(void)
{
    struct timespec ts;
    timespec_get(&ts, TIME_UTC);
    char buff[100];
    strftime(buff, sizeof buff, "%D %T", gmtime(&ts.tv_sec));
    printf("Current time: %s.%09ld UTC\n", buff, ts.tv_nsec);
    printf("Raw timespec.tv_sec: %jd\n", (intmax_t)ts.tv_sec);
    printf("Raw timespec.tv_nsec: %09ld\n", ts.tv_nsec);
}

```

Possible output:

```
Current time: 04/04/24 14:45:17.885909786 UTC
Raw timespec.tv_sec: 1712241917
Raw timespec.tv_nsec: 885909786

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.27.1/3 Components of time (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.27.1/3 Components of time (p: 284)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.27.1/3 Components of time (p: 388)

### See also

|  |  |
| --- | --- |
| timespec_get(C11) | returns the calendar time in seconds and nanoseconds based on a given time base   (function) |
| tm | calendar time type (struct) |
| C++ documentation for timespec | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono/timespec&oldid=180251>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 February 2025, at 18:28.