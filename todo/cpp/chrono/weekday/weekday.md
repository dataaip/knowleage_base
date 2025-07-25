# std::chrono::weekday::weekday

From cppreference.com
< cpp‎ | chrono‎ | weekday
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

std::chrono::weekday

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****weekday::weekday**** | | | | |
| weekday::operator++weekday::operator-- | | | | |
| weekday::operator+=weekday::operator-= | | | | |
| weekday::c_encodingweekday::iso_encoding | | | | |
| weekday::ok | | | | |
| [weekday::operator[]](operator_at.html "cpp/chrono/weekday/operator at") | | | | |
| Nonmember functions | | | | |
| operator== | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::weekday> | | | | |
| formatter<std::chrono::hash>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| weekday() = default; | (1) | (since C++20) |
| constexpr explicit weekday( unsigned wd ) noexcept; | (2) | (since C++20) |
| constexpr weekday( const std::chrono::sys_days& sd ) noexcept; | (3) | (since C++20) |
| constexpr explicit weekday( const std::chrono::local_days& ld ) noexcept; | (4) | (since C++20) |
|  |  |  |

Constructs a `weekday` object.

1) Default constructor leaves the weekday value uninitialized.2) Constructs a `weekday` object holding the weekday value wd. If wd == 7, the value held is ​0​. If wd > 255, the value held is unspecified.3) Constructs a `weekday` object representing the day of the week sd corresponds to. This constructor defines an implicit conversion from std::chrono::sys_days to `weekday`.4) Constructs a `weekday` object representing the day of the week ld corresponds to, as if by weekday(std::chrono::sys_days(ld.time_since_epoch())).

### Parameters

|  |  |  |
| --- | --- | --- |
| wd | - | a weekday value |
| sd | - | a system days object |
| ld | - | a local days object |

### Example

Run this code

```
#include <chrono>
#include <iomanip>
#include <iostream>
 
int main()
{
    constexpr std::chrono::weekday friday{5}; // uses overload (2)
    static_assert(friday == std::chrono::Friday);
 
    for (int y{2020}; y <= 2024; ++y)
    {
        const std::chrono::year cur_year{y};
        for (int cur_month{1}; cur_month != 13; ++cur_month)
        {
            const std::chrono::year_month_day ymd{cur_year/cur_month/13};
            const std::chrono::weekday cur_weekday{std::chrono::sys_days(ymd)}; // (3)
            if (cur_weekday == friday)
                std::cout << ymd << " is " << friday << '\n';
        }
    }
}

```

Output:

```
2020-03-13 is Fri
2020-11-13 is Fri
2021-08-13 is Fri
2022-05-13 is Fri
2023-01-13 is Fri
2023-10-13 is Fri
2024-09-13 is Fri
2024-12-13 is Fri

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/weekday/weekday&oldid=176093>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2024, at 12:41.