# std::chrono::year_month_day::operator+=, std::chrono::year_month_day::operator-=

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
| ****year_month_day::operator+=year_month_day::operator-=**** | | | | |
| year_month_day::yearyear_month_day::monthyear_month_day::day | | | | |
| year_month_day::operator sys_daysyear_month_day::operator local_days | | | | |
| year_month_day::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_day> | | | | |
| hash<std::chrono::year_month_day>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr std::chrono::year_month_day&      operator+=( const std::chrono::years& dy ) const noexcept; | (1) | (since C++20) |
| constexpr std::chrono::year_month_day&      operator+=( const std::chrono::months& dm ) const noexcept; | (2) | (since C++20) |
| constexpr std::chrono::year_month_day&      operator-=( const std::chrono::years& dy ) const noexcept; | (3) | (since C++20) |
| constexpr std::chrono::year_month_day&      operator-=( const std::chrono::months& dm ) const noexcept; | (4) | (since C++20) |
|  |  |  |

Modifies the time point \*this represents by the duration dy or dm.

1) Equivalent to \*this = \*this + dy;.2) Equivalent to \*this = \*this + dm;.3) Equivalent to \*this = \*this - dy;.4) Equivalent to \*this = \*this - dm;.

For durations that are convertible to both std::chrono::years and std::chrono::months, the `years` overloads (1,3) are preferred if the call would otherwise be ambiguous.

### Example

Run this code

```
#include <cassert>
#include <chrono>
#include <iostream>
 
int main()
{
    constexpr auto monthsInYear{12};
    auto ymd{std::chrono::day(1)/std::chrono::July/2020};
    std::cout << "#1 " << ymd << '\n';
 
    ymd -= std::chrono::years(10);
    std::cout << "#2 " << ymd << '\n';
    assert(ymd.month() == std::chrono::July);
    assert(ymd.year() == std::chrono::year(2010));
 
    ymd += std::chrono::months(10 * monthsInYear + 11);
    std::cout << "#3 " << ymd << '\n';
    assert(ymd.month() == std::chrono::month(6));
    assert(ymd.year() == std::chrono::year(2021));
 
    // Handling the ymd += months "overflow" case.
    ymd = std::chrono::May/31/2021; // ok
    std::cout << "#4 " << ymd << '\n';
    assert(ymd.ok());
 
    ymd += std::chrono::months{1}; // bad date: June has only 30 days
    std::cout << "#5 " << ymd << '\n';
    assert(not ymd.ok());
    assert(ymd == std::chrono::June/31/2021);
 
    // Snap to the last day of the month, June 30:
    const auto ymd1 = ymd.year()/ymd.month()/std::chrono::last;
    std::cout << "#6 " << ymd1 << '\n';
    assert(ymd1.ok());
    assert(ymd1 == std::chrono::June/30/2021);
 
    // Overflow into the next month, July 1 (via converting to/from sys_days):
    const std::chrono::year_month_day ymd2 = std::chrono::sys_days{ymd};
    std::cout << "#7 " << ymd2 << '\n';
    assert(ymd2.ok());
    assert(ymd2 == std::chrono::July/1/2021);
}

```

Output:

```
#1 2020-07-01
#2 2010-07-01
#3 2021-06-01
#4 2021-05-31
#5 2021-06-31 is not a valid date
#6 2021/Jun/last
#7 2021-07-01

```

### See also

|  |  |
| --- | --- |
| operator+operator-(C++20) | adds or subtracts a `year_month_day` and some number of years or months   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_day/operator_arith&oldid=157364>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 August 2023, at 23:30.