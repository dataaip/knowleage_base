# std::chrono::operator+, std::chrono::operator- (std::chrono::year_month_weekday)

From cppreference.com
< cpp‎ | chrono‎ | year month weekday
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

std::chrono::year_month_weekday

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month_weekday::year_month_weekday | | | | |
| year_month_weekday::operator+=year_month_weekday::operator-= | | | | |
| year_month_weekday::yearyear_month_weekday::monthyear_month_weekday::weekdayyear_month_weekday::indexyear_month_weekday::weekday_indexed | | | | |
| year_month_weekday::operator sys_daysyear_month_weekday::operator local_days | | | | |
| year_month_weekday::ok | | | | |
| Nonmember functions | | | | |
| operator== | | | | |
| ****operator+operator-**** | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_weekday> | | | | |
| hash<std::chrono::year_month_weekday>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr std::chrono::year_month_weekday       operator+( const std::chrono::year_month_weekday& ymwd, const std::chrono::months& dm ) noexcept; | (1) | (since C++20) |
| constexpr std::chrono::year_month_weekday       operator+( const std::chrono::months& dm, const std::chrono::year_month_weekday& ymwd ) noexcept; | (2) | (since C++20) |
| constexpr std::chrono::year_month_weekday       operator+( const std::chrono::year_month_weekday& ymwd, const std::chrono::years& dy ) noexcept; | (3) | (since C++20) |
| constexpr std::chrono::year_month_weekday       operator+( const std::chrono::years& dy, const std::chrono::year_month_weekday& ymwd ) noexcept; | (4) | (since C++20) |
| constexpr std::chrono::year_month_weekday      operator-( const std::chrono::year_month_weekday& ymwd, const std::chrono::months& dm ) noexcept; | (5) | (since C++20) |
| constexpr std::chrono::year_month_weekday       operator-( const std::chrono::year_month_weekday& ymwd, const std::chrono::years& dy ) noexcept; | (6) | (since C++20) |
|  |  |  |

1,2) Adds dm.count() months to the date represented by ymwd. The result has the same `year()` and `month()` as std::chrono::year_month(ymwd.year(), ymwd.month()) + dm and the same `weekday()` and `index()` as ymwd.3,4) Adds dy.count() years to the date represented by ymwd. The result is equivalent to std::chrono::year_month_weekday(ymwd.year() + dy, ymwd.month(), ymwd.weekday_indexed()).5) Subtracts dm.count() months from the date represented by ymwd. Equivalent to ymwd + -dm.6) Subtracts dy.count() years from the date represented by ymwd. Equivalent to ymwd + -dy.

For durations that are convertible to both std::chrono::years and std::chrono::months, the `years` overloads (3,4,6) are preferred if the call would otherwise be ambiguous.

### Notes

Even if ymwd.ok() is true, the resulting `year_month_weekday` may not represent a valid date if ymwd.index() is 5.

### Example

Run this code

```
#include <cassert>
#include <chrono>
#include <iostream>
 
int main()
{
    auto ymwdi{1/std::chrono::Wednesday[1]/2021};
    std::cout << ymwdi << '\n';
 
    ymwdi = std::chrono::years(5) + ymwdi;
    // First Wednesday in January, 2026
    std::cout << ymwdi << '\n';
    assert(static_cast<std::chrono::year_month_day>(ymwdi) ==
           std::chrono::January/7/2026);
 
    ymwdi = ymwdi - std::chrono::months(6);
    // First Wednesday in July, 2025
    std::cout << ymwdi << '\n';
    assert(static_cast<std::chrono::year_month_day>(ymwdi) ==
           std::chrono::July/2/2025);
}

```

Output:

```
2021/Jan/Wed[1]
2026/Jan/Wed[1]
2025/Jul/Wed[1]

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_weekday/operator_arith_2&oldid=161710>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 October 2023, at 10:11.