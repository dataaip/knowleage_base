# std::chrono::gps_clock

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****gps_clock****(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::gps_clock****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| gps_clock::now | | | | |
| gps_clock::to_utc | | | | |
| gps_clock::from_utc | | | | |
| Time point I/O | | | | |
| operator<< | | | | |
| formatter<std::chrono::gps_time> | | | | |
| from_stream | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| class gps_clock; |  | (since C++20) |
|  |  |  |

The clock `std::chrono::gps_clock` is a Clock that represents Global Positioning System (GPS) time. It measures time since 00:00:00, 6 January 1980 UTC.

Leap seconds are not inserted into GPS. Thus, every time a leap second is inserted into UTC, UTC falls another second behind GPS. As of December 2017, UTC is 18 seconds behind GPS, reflecting the 18 leap seconds inserted between 1980 and 2017. Thus, 2018-01-01 00:00:00 UTC is equivalent to 2018-01-01 00:00:18 GPS. GPS is a constant 19 seconds behind TAI.

`gps_clock` meets the Clock requirements. It does not meet the TrivialClock requirements unless the implementation can guarantee that now() does not throw an exception.

### Time point family

|  |  |  |
| --- | --- | --- |
| Defined in namespace `std::chrono` |  |  |
| template<class Duration>  using gps_time = std::chrono::time_point<std::chrono::gps_clock, Duration>; |  | (since C++20) |
| using gps_seconds = gps_time<std::chrono::seconds>; |  | (since C++20) |
|  |  |  |

|  |  |
| --- | --- |
| operator<<(std::chrono::gps_time)(C++20) | performs stream output on a `gps_time`   (function template) |
| from_stream(std::chrono::gps_time)(C++20) | parses a `gps_time` from a stream according to the provided format   (function template) |
| std::formatter<std::chrono::gps_time>(C++20) | formatting support for `gps_time`   (class template specialization) |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `rep` | signed arithmetic type representing the number of ticks in the clock's duration |
| `period` | a std::ratio type representing the tick period of the clock, in seconds |
| `duration` | std::chrono::duration<rep, period>, capable of representing negative durations |
| `time_point` | std::chrono::time_point<std::chrono::gps_clock> |

### Member constants

|  |  |
| --- | --- |
| constexpr bool is_steady[static] | true if the time between ticks is always constant, i.e. calls to now() return values that increase monotonically even in case of some external clock adjustment, otherwise false   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| now[static] | returns a std::chrono::time_point representing the current point in time   (public static member function) |
| to_utc[static] | converts a `gps_time` to `utc_time`   (public static member function) |
| from_utc[static] | converts a `utc_time` to `gps_time`   (public static member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/gps_clock&oldid=161585>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 October 2023, at 07:32.