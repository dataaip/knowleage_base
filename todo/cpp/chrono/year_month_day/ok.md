# std::chrono::year_month_day::ok

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
| ****year_month_day::ok**** | | | | |
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
| constexpr bool ok() const noexcept; |  | (since C++20) |
|  |  |  |

Checks if this `year_month_day` object represents a valid calendar date.

### Return value

true if this `year_month_day` object represents a valid calendar date, that is, the stored year, month, and day values are all valid and the stored day value is within the number of days in the given year and month. Otherwise false.

### Possible implementation

|  |
| --- |
| ```text constexpr bool std::chrono::year_month_day::ok() const noexcept {     return year().ok() && month().ok() && day().ok() &&         day() <= (year()/month()/std::chrono::last).day(); } ``` |

### Example

Run this code

```
#include <chrono>
 
int main()
{
    constexpr auto ymd1 {std::chrono::day(1)/std::chrono::July/2020};
    static_assert(ymd1.ok());
 
    constexpr auto ymd2 {std::chrono::year(2020)/7/42};
    static_assert(not ymd2.ok());
 
    constexpr auto ymd3 {std::chrono::February/29/2020}; // ok, leap year
    static_assert(ymd3.ok());
 
    constexpr auto ymd4 = ymd3 + std::chrono::years{1}; // bad, not a leap year
    static_assert(ymd4 == std::chrono::February/29/2021 and not ymd4.ok());
 
    // to fix the bad date we may want to snap to the last day of the month:
    if constexpr (!ymd4.ok())
    {
        constexpr auto ymd = ymd4.year()/ymd4.month()/std::chrono::last;
        static_assert(ymd == std::chrono::February/28/2021 and ymd.ok());
    }
 
    // or we may want to overflow to the next month:
    if constexpr (!ymd4.ok())
    {
        constexpr auto st = std::chrono::sys_time<std::chrono::days>{ymd4};
        constexpr auto ymd = std::chrono::year_month_day{st};
        static_assert(ymd == std::chrono::March/1/2021 and ymd.ok());
    }
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_day/ok&oldid=161691>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 October 2023, at 05:49.