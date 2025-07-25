# tm

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
| ****tm**** | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<time.h>` |  |  |
| struct tm; |  |  |
|  |  |  |

Structure holding a calendar date and time broken down into its components.

### Member objects

|  |  |
| --- | --- |
| int tm_sec | seconds after the minute – `[`​0​`,`61`]`(until C99)`[`​0​`,`60`]`(since C99)[[note 1]](tm.html#cite_note-leapsecond-1)   (public member object) |
| int tm_min | minutes after the hour – `[`​0​`,`59`]`   (public member object) |
| int tm_hour | hours since midnight – `[`​0​`,`23`]`   (public member object) |
| int tm_mday | day of the month – `[`1`,`31`]`   (public member object) |
| int tm_mon | months since January – `[`​0​`,`11`]`   (public member object) |
| int tm_year | years since 1900   (public member object) |
| int tm_wday | days since Sunday – `[`​0​`,`6`]`   (public member object) |
| int tm_yday | days since January 1 – `[`​0​`,`365`]`   (public member object) |
| int tm_isdst | Daylight Saving Time flag. The value is positive if DST is in effect, zero if not and negative if no information is available   (public member object) |

###### Notes

The Standard mandates only the presence of the aforementioned members in either order. The implementations usually add more data-members to this structure.

1. ↑ Range allows for a positive leap second. Two leap seconds in the same minute are not allowed (the C89 range 0..61 was a defect)

### Example

Run this code

```
#include <stdio.h>
#include <time.h>
 
int main(void)
{
    struct tm start = {.tm_year = 2022 - 1900, .tm_mday = 1};
    mktime(&start);
    printf("%s", asctime(&start)); // note implicit trailing '\n'
}

```

Output:

```
Sat Jan  1 00:00:00 2022

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.27.1/3 Components of time (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.27.1/3 Components of time (p: 284)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.27.1/3 Components of time (p: 388)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.23.1/3 Components of time (p: 338)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.12.1 Components of time

### See also

|  |  |
| --- | --- |
| localtimelocaltime_rlocaltime_s(C23)(C11) | converts time since epoch to calendar time expressed as local time   (function) |
| gmtimegmtime_rgmtime_s(C23)(C11) | converts time since epoch to calendar time expressed as Coordinated Universal Time (UTC)   (function) |
| C++ documentation for tm | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono/tm&oldid=172469>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 June 2024, at 17:03.