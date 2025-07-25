# std::chrono::operator+, std::chrono::operator- (std::chrono::year_month)

From cppreference.com
< cpp‎ | chrono‎ | year month
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

std::chrono::year_month

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month::year_month | | | | |
| year_month::yearyear_month::month | | | | |
| year_month::operator+=year_month::operator-= | | | | |
| year_month::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| ****operator+operator-**** | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month> | | | | |
| hash<std::chrono::year_month>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr std::chrono::year_month operator+( const std::chrono::year_month& ym,                                               const std::chrono::years& dy ) noexcept; | (1) | (since C++20) |
| constexpr std::chrono::year_month operator+( const std::chrono::years& dy,                                               const std::chrono::year_month& ym ) noexcept; | (2) | (since C++20) |
| constexpr std::chrono::year_month operator+( const std::chrono::year_month& ym,                                               const std::chrono::months& dm ) noexcept; | (3) | (since C++20) |
| constexpr std::chrono::year_month operator+( const std::chrono::months& dm,                                               const std::chrono::year_month& ym ) noexcept; | (4) | (since C++20) |
| constexpr std::chrono::year_month operator-( const std::chrono::year_month& ym,                                               const std::chrono::years& dy ) noexcept; | (5) | (since C++20) |
| constexpr std::chrono::year_month operator-( const std::chrono::year_month& ym,                                               const std::chrono::months& dm ) noexcept; | (6) | (since C++20) |
| constexpr std::chrono::months operator-( const std::chrono::year_month& ym1,                                           const std::chrono::year_month& ym2 ) noexcept; | (7) | (since C++20) |
|  |  |  |

1,2) Adds dy.count() years to ym.3,4) Adds dm.count() months to ym.5) Subtracts dy.count() years from ym.6) Subtracts dm.count() months from ym.7) Returns the difference in months between the two time points represented by ym1 and ym2.

For durations that are convertible to both std::chrono::years and std::chrono::months, the `years` overloads (1,2,5) are preferred if the call would otherwise be ambiguous.

### Return value

1,2) std::chrono::year_month(ym.year() + dy, ym.month())3,4) A `year_month` value `z` such that z - ym == dm and z.ok() == true.5) ym + -dy6) ym + -dm7)   
ym1.year() - ym2.year() + std::chrono::months(int(unsigned(ym1.month())) -  
int(unsigned(ym2.month())))

### Notes

The result of subtracting two `year_month` values is a duration of type std::chrono::months. This duration unit represents the length of the average Gregorian month (30.436875 days), and the resulting duration bears no relationship to the actual number of days in the time period at issue. For example, the result of 2017y/3 - 2017y/2 is std::chrono::months(1), even though February 2017 only contains 28 days.

### Example

Run this code

```
#include <cassert>
#include <chrono>
 
int main()
{
    auto ym{std::chrono::year(2021)/std::chrono::July};
 
    ym = ym + std::chrono::months(14);
    assert(ym.month() == std::chrono::September);
    assert(ym.year() == std::chrono::year(2022));
 
    ym = ym - std::chrono::years(3);
    assert(ym.month() == std::chrono::month(9));
    assert(ym.year() == std::chrono::year(2019));
 
    ym = ym + (std::chrono::September - std::chrono::month(2));
    assert(ym.month() == std::chrono::April);
    assert(ym.year() == std::chrono::year(2020));
}

```

### See also

|  |  |
| --- | --- |
| operator+=operator-= | modifies the `year_month` by some number of months or years   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month/operator_arith_2&oldid=157414>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 August 2023, at 12:14.