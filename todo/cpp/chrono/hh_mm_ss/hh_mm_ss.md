# std::chrono::hh_mm_ss<Duration>::hh_mm_ss

From cppreference.com
< cpp‎ | chrono‎ | hh mm ss
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

std::chrono::hh_mm_ss

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****hh_mm_ss::hh_mm_ss**** | | | | |
| hh_mm_ss::is_negativehh_mm_ss::hourshh_mm_ss::minuteshh_mm_ss::secondshh_mm_ss::subseconds | | | | |
| hh_mm_ss::operator precisionhh_mm_ss::to_duration | | | | |
| Non-member functions | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| formatter<std::chrono::hh_mm_ss> | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr hh_mm_ss() noexcept : hh_mm_ss{Duration::zero()} {} | (1) |  |
| constexpr explicit hh_mm_ss( Duration d ); | (2) |  |
|  |  |  |

Constructs a `hh_mm_ss` object.

1) Constructs a `hh_mm_ss` object corresponding to `Duration::zero()`.2) Constructs a `hh_mm_ss` object corresponding to d:

- is_negative() returns d < Duration::zero().
- hours() returns std::chrono::duration_cast<std::chrono::hours>(abs(d)).
- minutes() returns std::chrono::duration_cast<std::chrono::minutes>(abs(d) - hours()).
- seconds() returns  
  std::chrono::duration_cast<std::chrono::seconds>(abs(d) - hours() - minutes()).
- subseconds() returns abs(d) - hours() - minutes() - seconds() if std::chrono::treat_as_floating_point_v<precision::rep> is true; otherwise it returns std::chrono::duration_cast<precision>(abs(d) - hours() - minutes() - seconds()).

### Parameters

|  |  |  |
| --- | --- | --- |
| d | - | the duration to be broken down |

### Example

Run this code

```
#include <chrono>
#include <print>
 
int main()
{
    std::println("Default constructor: {}", std::chrono::hh_mm_ss<std::chrono::minutes>{});
 
    std::chrono::time_point now = std::chrono::system_clock::now();
    std::chrono::hh_mm_ss time_of_day{now - std::chrono::floor<std::chrono::days>(now)};
    std::println("The time of day is: {}", time_of_day);
}

```

Possible output:

```
Default constructor: 00:00:00
The time of day is: 12:13:14.151617189

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/hh_mm_ss/hh_mm_ss&oldid=171252>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 April 2024, at 05:21.