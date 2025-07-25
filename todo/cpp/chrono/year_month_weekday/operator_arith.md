# std::chrono::year_month_weekday::operator+=, std::chrono::year_month_weekday::operator-=

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
| ****year_month_weekday::operator+=year_month_weekday::operator-=**** | | | | |
| year_month_weekday::yearyear_month_weekday::monthyear_month_weekday::weekdayyear_month_weekday::indexyear_month_weekday::weekday_indexed | | | | |
| year_month_weekday::operator sys_daysyear_month_weekday::operator local_days | | | | |
| year_month_weekday::ok | | | | |
| Nonmember functions | | | | |
| operator== | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_weekday> | | | | |
| hash<std::chrono::year_month_weekday>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr std::chrono::year_month_weekday&      operator+=( const std::chrono::years& dy ) const noexcept; | (1) | (since C++20) |
| constexpr std::chrono::year_month_weekday&      operator+=( const std::chrono::months& dm ) const noexcept; | (2) | (since C++20) |
| constexpr std::chrono::year_month_weekday&      operator-=( const std::chrono::years& dy ) const noexcept; | (3) | (since C++20) |
| constexpr std::chrono::year_month_weekday&      operator-=( const std::chrono::months& dm ) const noexcept; | (4) | (since C++20) |
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
    auto ymwi{1/std::chrono::Wednesday[2]/2021};
    std::cout << ymwi << '\n';
 
    ymwi += std::chrono::years(5);
    std::cout << ymwi << '\n';
    assert(static_cast<std::chrono::year_month_day>(ymwi) ==
                       std::chrono::year(2026)/1/14);
 
    ymwi -= std::chrono::months(1);
    std::cout << ymwi << '\n';
    assert(static_cast<std::chrono::year_month_day>(ymwi) == 
                       std::chrono::day(10)/12/2025);
}

```

Output:

```
2021/Jan/Wed[2]
2026/Jan/Wed[2]
2025/Dec/Wed[2]

```

### See also

|  |  |
| --- | --- |
| operator+operator-(C++20) | adds or subtracts a `year_month_weekday` and some number of years or months   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_weekday/operator_arith&oldid=157409>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 August 2023, at 11:47.