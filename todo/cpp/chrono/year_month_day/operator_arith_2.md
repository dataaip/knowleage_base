# std::chrono::operator+, std::chrono::operator- (std::chrono::year_month_day)

From cppreference.com
< cpp‎ | chrono‎ | year month day
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

std::chrono::year_month_day

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month_day::year_month_day | | | | |
| year_month_day::operator+=year_month_day::operator-= | | | | |
| year_month_day::yearyear_month_day::monthyear_month_day::day | | | | |
| year_month_day::operator sys_daysyear_month_day::operator local_days | | | | |
| year_month_day::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| ****operator+operator-**** | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_day> | | | | |
| hash<std::chrono::year_month_day>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| constexpr std::chrono::year_month_day operator+( const std::chrono::year_month_day& ymd,  const std::chrono::months& dm ) noexcept; |  | (since C++20) |
| constexpr std::chrono::year_month_day operator+( const std::chrono::months& dm,  const std::chrono::year_month_day& ymd ) noexcept; |  | (since C++20) |
| constexpr std::chrono::year_month_day operator+( const std::chrono::year_month_day& ymd,  const std::chrono::years& dy ) noexcept; |  | (since C++20) |
| constexpr std::chrono::year_month_day operator+( const std::chrono::years& dy,  const std::chrono::year_month_day& ymd ) noexcept; |  | (since C++20) |
| constexpr std::chrono::year_month_day operator-( const std::chrono::year_month_day& ymd,  const std::chrono::months& dm ) noexcept; |  | (since C++20) |
| constexpr std::chrono::year_month_day operator-( const std::chrono::year_month_day& ymd,  const std::chrono::years& dy ) noexcept; |  | (since C++20) |
|  |  |  |

1,2) Adds dm.count() months to the date represented by ymd. The result has the same day() as ymd and the same year() and month() as std::chrono::year_month(ymd.year(), ymd.month()) + dm.3,4) Adds dy.count() years to the date represented by ymd. The result is equivalent to std::chrono::year_month_day(ymd.year() + dy, ymd.month(), ymd.day().5) Subtracts dm.count() months from the date represented by ymd. Equivalent to ymd + -dm.6) Subtracts dy.count() years from the date represented by ymd. Equivalent to ymd + -dy.

For durations that are convertible to both std::chrono::years and std::chrono::months, the `years` overloads (3,4,6) are preferred if the call would otherwise be ambiguous.

### Notes

Even if ymd.ok() is true, the resulting `year_month_day` may not represent a valid date if ymd.day() is 29, 30, or 31.

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    std::cout << std::boolalpha;
 
    auto ymd{std::chrono::day(1)/std::chrono::July/2021};
 
    ymd = ymd + std::chrono::months(4);
    std::cout << (ymd.month() == std::chrono::November) << ' '
              << (ymd.year() == std::chrono::year(2021)) << ' ';
 
    ymd = ymd - std::chrono::years(10);
    std::cout << (ymd.month() == std::chrono::month(11)) << ' '
              << (ymd.year() == std::chrono::year(2011)) << '\n';
}

```

Output:

```
true true true true

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_day/operator_arith_2&oldid=157547>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 23:12.