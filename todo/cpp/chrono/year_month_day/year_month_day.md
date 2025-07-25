# std::chrono::year_month_day::year_month_day

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
| ****year_month_day::year_month_day**** | | | | |
| year_month_day::operator+=year_month_day::operator-= | | | | |
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
| year_month_day() = default; | (1) | (since C++20) |
| constexpr year_month_day( const std::chrono::year& y,  const std::chrono::month& m, const std::chrono::day& d ) noexcept; | (2) | (since C++20) |
| constexpr year_month_day( const std::chrono::year_month_day_last& ymdl ) noexcept; | (3) | (since C++20) |
| constexpr year_month_day( const std::chrono::sys_days& dp ) noexcept; | (4) | (since C++20) |
| constexpr explicit year_month_day( const std::chrono::local_days& dp ) noexcept; | (5) | (since C++20) |
|  |  |  |

Constructs a `year_month_day` object.

1) Default constructor leaves the date uninitialized.2) Constructs a `year_month_day` object that stores the year y, month m and day d.3) Constructs a `year_month_day` object that stores the year ymdl.year(), month ymdl.month() and day ymdl.day().4) Constructs a `year_month_day` object that represent the same date as the one represented by dp.5) Constructs a `year_month_day` object that represent the same date as the one represented by dp, as if by year_month_day(sys_days(dp.time_since_epoch())).

Constructors (3,4) define implicit conversions from std::chrono::year_month_day_last and std::chrono::sys_days, respectively.

For any `year_month_day` object `ymd` representing a valid date (ymd.ok() == true), converting `ymd` to sys_days and back yields the same value.

### Notes

A `year_month_day` can also be created by combining one of the partial-date types std::chrono::year_month and std::chrono::month_day with the missing component (day and year, respectively) using operator/.

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    using namespace std::chrono;
 
    constexpr auto ymd2 = std::chrono::year_month_day(
        2020y, std::chrono::January, 31d // overload (2)
    );
    std::cout << "ymd2: " << ymd2 << '\n';
 
    constexpr auto ymd3 = std::chrono::year_month_day(
        std::chrono::April / std::chrono::Monday[last] / 2023y // overload (3)
    );
    std::cout << "ymd3: " << ymd3 << '\n';
 
    const auto now = std::chrono::system_clock::now();
    const auto ymd4 = std::chrono::year_month_day(
        std::chrono::floor<std::chrono::days>(now) // overload (4)
    );
    std::cout << "ymd4: " << ymd4 << '\n';
}

```

Possible output:

```
ymd2: 2020-01-31
ymd3: 2023-04-24
ymd4: 2023-08-30

```

### See also

|  |  |
| --- | --- |
| operator/(C++20) | conventional syntax for Gregorian calendar date creation   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_day/year_month_day&oldid=157576>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 August 2023, at 07:26.