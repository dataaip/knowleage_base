# std::chrono::system_clock

From cppreference.com
< cpp‎ | chrono
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****system_clock****(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::system_clock****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| system_clock::now | | | | |
| system_clock::to_time_t | | | | |
| system_clock::from_time_t | | | | |
| Time point I/O | | | | |
| operator<< | | | | |
| formatter<std::chrono::sys_time> | | | | |
| from_stream | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| class system_clock; |  | (since C++11) |
|  |  |  |

Class `std::chrono::system_clock` represents the system-wide real time wall clock.

It may not be monotonic: on most systems, the system time can be adjusted at any moment. It is the only C++ clock that has the ability to map its time points to C-style time.

`std::chrono::system_clock` meets the requirements of TrivialClock.

|  |  |
| --- | --- |
| The epoch of `system_clock` is unspecified, but most implementations use Unix Time (i.e., time since 00:00:00 Coordinated Universal Time (UTC), Thursday, 1 January 1970, not counting leap seconds). | (until C++20) |
| `system_clock` measures Unix Time (i.e., time since 00:00:00 Coordinated Universal Time (UTC), Thursday, 1 January 1970, not counting leap seconds). | (since C++20) |

### Time point family

|  |  |  |
| --- | --- | --- |
| Defined in namespace `std::chrono` |  |  |
| template<class Duration>  using sys_time = std::chrono::time_point<std::chrono::system_clock, Duration>; |  | (since C++20) |
| using sys_seconds = sys_time<std::chrono::seconds>; |  | (since C++20) |
| using sys_days = sys_time<std::chrono::days>; |  | (since C++20) |
|  |  |  |

|  |  |
| --- | --- |
| operator<<(std::chrono::sys_time)(C++20) | performs stream output on a `sys_time`   (function template) |
| from_stream(std::chrono::sys_time)(C++20) | parses a `sys_time` from a stream according to the provided format   (function template) |
| std::formatter<std::chrono::sys_time>(C++20) | formatting support for `sys_time`   (class template specialization) |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `rep` | signed arithmetic type representing the number of ticks in the clock's duration |
| `period` | a std::ratio type representing the tick period of the clock, in seconds |
| `duration` | std::chrono::duration<rep, period>, capable of representing negative durations |
| `time_point` | std::chrono::time_point<std::chrono::system_clock> |

### Member constants

|  |  |
| --- | --- |
| constexpr bool is_steady[static] | true if the time between ticks is always constant, i.e. calls to now() return values that increase monotonically even in case of some external clock adjustment, otherwise false   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| now[static] | returns a std::chrono::time_point representing the current point in time   (public static member function) |
| to_time_t[static] | converts a system clock time point to std::time_t   (public static member function) |
| from_time_t[static] | converts std::time_t to a system clock time point   (public static member function) |

### Notes

The `system_clock`'s time value can be internally adjusted at any time by the operating system, for example due to NTP synchronization or the user changing the system's clock. Daylight Saving Time and time zone changes, however, do not affect it since it is based on the UTC time-zone.

### See also

|  |  |
| --- | --- |
| steady_clock(C++11) | monotonic clock that will never be adjusted   (class) |
| high_resolution_clock(C++11) | the clock with the shortest tick period available   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/system_clock&oldid=154231>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 June 2023, at 09:26.