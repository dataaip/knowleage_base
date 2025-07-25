# std::tm

From cppreference.com
< cpp‎ | chrono‎ | c
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

Date and time library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Time point | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | time_point(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_time_conversion(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_cast(C++20) | | | | | |
| Duration | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration(C++11) | | | | | |
| Clocks | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

C-style date and time utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Time manipulation | | | | |
| difftime | | | | |
| time | | | | |
| clock | | | | |
| timespec_get(C++17) | | | | |
| Format conversions | | | | |
| asctime | | | | |
| ctime | | | | |
| strftime | | | | |
| wcsftime | | | | |
| gmtime | | | | |
| localtime | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| ****tm**** | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ctime>` |  |  |
| struct tm; |  |  |
|  |  |  |

Structure holding a calendar date and time broken down into its components.

### Member objects

|  |  |
| --- | --- |
| int tm_sec | seconds after the minute – `[`​0​`,`61`]`(until C++11) `[`​0​`,`60`]`(since C++11)[[note 1]](tm.html#cite_note-leapsecond-1)   (public member object) |
| int tm_min | minutes after the hour – `[`​0​`,`59`]`   (public member object) |
| int tm_hour | hours since midnight – `[`​0​`,`23`]`   (public member object) |
| int tm_mday | day of the month – `[`1`,`31`]`   (public member object) |
| int tm_mon | months since January – `[`​0​`,`11`]`   (public member object) |
| int tm_year | years since 1900   (public member object) |
| int tm_wday | days since Sunday – `[`​0​`,`6`]`   (public member object) |
| int tm_yday | days since January 1 – `[`​0​`,`365`]`   (public member object) |
| int tm_isdst | Daylight Saving Time flag. The value is positive if DST is in effect, zero if not and negative if no information is available.   (public member object) |

1. ↑ Range allows for a positive leap second. Two leap seconds in the same minute are not allowed (the range `[`​0​`,`61`]` was a defect introduced in C89 and corrected in C99).

### Notes

BSD, GNU and musl C library support two additional members, which are standardized in POSIX.1-2024.

|  |  |
| --- | --- |
| long tm_gmtoff | seconds east of UTC   (public member object) |
| const char\* tm_zone | timezone abbreviation   (public member object) |

### Example

Run this code

```
#include <ctime>
#include <iostream>
 
int main()
{
    std::tm tm{};
    tm.tm_year = 2022 - 1900;
    tm.tm_mday = 1;
    std::mktime(&tm);
 
    std::cout << std::asctime(&tm); // note implicit trailing '\n'
}

```

Possible output:

```
Sat Jan  1 00:00:00 2022

```

### See also

|  |  |
| --- | --- |
| localtime | converts time since epoch to calendar time expressed as local time   (function) |
| gmtime | converts time since epoch to calendar time expressed as Universal Coordinated Time   (function) |
| C documentation for tm | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/c/tm&oldid=174176>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 August 2024, at 01:52.