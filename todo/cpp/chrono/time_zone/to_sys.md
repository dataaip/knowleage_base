# std::chrono::time_zone::to_sys

From cppreference.com
< cpp‎ | chrono‎ | time zone
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

std::chrono::time_zone

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| time_zone::name | | | | |
| time_zone::get_info | | | | |
| ****time_zone::to_sys**** | | | | |
| time_zone::to_local | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |

|  |  |  |
| --- | --- | --- |
| template< class Duration >  auto to_sys( const std::chrono::local_time<Duration>& tp ) const -> std::chrono::sys_time<std::common_type_t<Duration, std::chrono::seconds>>; | (1) | (since C++20) |
| template< class Duration >  auto to_sys( const std::chrono::local_time<Duration>& tp, std::chrono::choose z ) const -> std::chrono::sys_time<std::common_type_t<Duration, std::chrono::seconds>>; | (2) | (since C++20) |
|  |  |  |

Converts the local_time tp in this time zone to the corresponding sys_time.

1) Throws an exception if the conversion is ambiguous or if tp represents a nonexistent time.2) Resolves ambiguity according to the value of z:

- If z == std::chrono::choose::earliest, returns the earlier `sys_time`.
- If z == std::chrono::choose::latest, returns the later `sys_time`.
 If tp represents a nonexistent time between two UTC `time_point`s, those two `time_point`s will be the same, and that `time_point` will be returned.

### Return value

The UTC equivalent of tp according to the rules of this time zone.

### Exceptions

1) Throws:

- std::chrono::ambiguous_local_time if the conversion is ambiguous,
- std::chrono::nonexistent_local_time if tp represents a nonexistent time.

### Notes

The precision of the result is at least std::chrono::seconds, and will be finer if the argument has finer precision.

Ambiguous and nonexistent local times can occur as a result of time zone transitions (such as daylight saving time). For example, "2016-03-13 02:30:00" does not exist in the "America/New_York" time zone, while "2016-11-06 01:30:00" in that time zone can correspond to two UTC time points: 2016-11-06 05:30:00 UTC and 2016-11-06 06:30:00 UTC.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/time_zone/to_sys&oldid=169726>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 February 2024, at 05:53.