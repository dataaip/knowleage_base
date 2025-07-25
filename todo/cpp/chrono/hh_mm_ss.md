# std::chrono::hh_mm_ss

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****hh_mm_ss****(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::hh_mm_ss****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| hh_mm_ss::hh_mm_ss | | | | |
| hh_mm_ss::is_negativehh_mm_ss::hourshh_mm_ss::minuteshh_mm_ss::secondshh_mm_ss::subseconds | | | | |
| hh_mm_ss::operator precisionhh_mm_ss::to_duration | | | | |
| Non-member functions | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| formatter<std::chrono::hh_mm_ss> | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class Duration >  class hh_mm_ss; |  | (since C++20) |
|  |  |  |

The class template `hh_mm_ss` splits a std::chrono::duration into a "broken down" time such as **hours**:**minutes**:**seconds**, with the precision of the split determined by the `Duration` template parameter. It is primarily a formatting tool.

`Duration` must be a specialization of std::chrono::duration, otherwise the program is ill-formed.

### Member constants

|  |  |
| --- | --- |
| constexpr unsigned fractional_width[static] | the smallest possible integer in the range `[`​0​`,`18`]` such that `precision` (see below) will exactly represent the value of Duration{1}, or 6 if there's no such integer   (public static member constant) |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `precision` | std::chrono::duration<std::common_type_t<Duration::rep, std::chrono::seconds::rep>,                       std::ratio<1, 10`fractional_width`>> |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `hh_mm_ss`   (public member function) |
| is_negativehoursminutessecondssubseconds | obtains components of the broken-down time   (public member function) |
| operator precisionto_duration | obtains the stored std::chrono::duration   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator<<(C++20) | outputs a `hh_mm_ss` into a stream   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::formatter<std::chrono::hh_mm_ss>(C++20) | formatting support for `hh_mm_ss`   (class template specialization) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/hh_mm_ss&oldid=161589>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 October 2023, at 07:45.