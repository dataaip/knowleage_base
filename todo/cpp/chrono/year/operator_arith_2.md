# std::chrono::operator+, std::chrono::operator- (std::chrono::year)

From cppreference.com
< cpp‎ | chrono‎ | year
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

std::chrono::year

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year::year | | | | |
| year::operator++year::operator-- | | | | |
| year::operator+=year::operator-= | | | | |
| year::operator+year::operator- | | | | |
| year::is_leap | | | | |
| year::operator int | | | | |
| year::ok | | | | |
| year::min | | | | |
| year::max | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| ****operator+operator-**** | | | | |
| operator<< | | | | |
| from_stream | | | | |
| operator""y | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year> | | | | |
| hash<std::chrono::year>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr std::chrono::year operator+( const std::chrono::year& y,                                         const std::chrono::years& ys ) noexcept; | (1) | (since C++20) |
| constexpr std::chrono::year operator+( const std::chrono::years& ys,                                         const std::chrono::year& y ) noexcept; | (2) | (since C++20) |
| constexpr std::chrono::year operator-( const std::chrono::year& y,                                         const std::chrono::years& ys ) noexcept; | (3) | (since C++20) |
| constexpr std::chrono::years operator-( const std::chrono::year& y1,                                           const std::chrono::year& y2 ) noexcept; | (4) | (since C++20) |
|  |  |  |

1,2) Adds ys.count() years to y.3) Subtracts ys.count() years from y.4) Returns the difference in years between y1 and y2.

### Return value

1,2) std::chrono::year(int(y) + ys.count())3) std::chrono::year(int(y) - ys.count())4) std::chrono::years(int(y1) - int(y2))

### Notes

If the resulting year value for (1-3) is outside the range `[`-32767`,`32767`]`, the actual value stored is unspecified.

The result of subtracting two `year` values is a duration of type std::chrono::years. This duration unit represents the length of the average Gregorian year, and the resulting duration bears no relationship to the number of days in the particular years represented by the operands. For example, the result of 2018y - 2017y is std::chrono::years(1), which represents 365.2425 days, not 365 days.

### Example

Run this code

```
#include <cassert>
#include <chrono>
 
int main()
{
    std::chrono::year y{2020};
 
    y = std::chrono::years(12) + y; // overload (2): duration + time point
    assert(y == std::chrono::year(2032));
 
    y = y - std::chrono::years(33); // overload (3): time point - duration
    assert(y == std::chrono::year(1999));
 
    // y = std::chrono::years(33) - y; // not supported: duration - time point
 
    using namespace std::chrono;
    constexpr std::chrono::years ys = 2025y - 2020y; // overload (4)
    static_assert(ys == std::chrono::years(5));
}

```

### See also

|  |  |
| --- | --- |
| operator++operator++(int)operator--operator--(int) | increments or decrements the month   (public member function of `std::chrono::month`) |
| operator+=operator-= | adds or subtracts a number of months   (public member function of `std::chrono::month`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year/operator_arith_2&oldid=157535>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 15:12.