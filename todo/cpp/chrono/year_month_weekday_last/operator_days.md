# std::chrono::year_month_weekday_last::operator sys_days, std::chrono::year_month_weekday_last::operator local_days

From cppreference.com
< cpp‎ | chrono‎ | year month weekday last
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

std::chrono::year_month_weekday_last

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month_weekday_last::year_month_weekday_last | | | | |
| year_month_weekday_last::operator+=year_month_weekday_last::operator-= | | | | |
| year_month_weekday_last::yearyear_month_weekday_last::monthyear_month_weekday_last::weekdayyear_month_weekday_last::weekday_last | | | | |
| ****year_month_weekday_last::operator sys_daysyear_month_weekday_last::operator local_days**** | | | | |
| year_month_weekday_last::ok | | | | |
| Nonmember functions | | | | |
| operator== | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_weekday_last> | | | | |
| hash<std::chrono::year_month_weekday_last>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr operator std::chrono::sys_days() const noexcept; | (1) | (since C++20) |
| constexpr explicit operator std::chrono::local_days() const noexcept; | (2) | (since C++20) |
|  |  |  |

Converts \*this to a std::chrono::time_point representing the same date as this `year_month_weekday_last`.

1) If `ok()` is true, returns a `sys_days` that represents the last `weekday()` of the `year()` and `month()`. Otherwise, the returned value is unspecified.2) Same as (1), but returns `local_days` instead of `sys_days`. Equivalent to local_days(sys_days(\*this).time_since_epoch()).

### Example

Run this code

```
#include <chrono>
#include <iostream>
using namespace std::chrono;
 
int main()
{
    constexpr auto ymwdl{Tuesday[last]/11/2021};
    static_assert(static_cast<local_days>(ymwdl) ==
                  static_cast<local_days>(November/30/2021));
    // convert from field-based to serial-based to add days
    constexpr auto sd = static_cast<sys_days>(ymwdl);
    constexpr year_month_day ymd{sd + days(42)};
    std::cout << ymd << '\n';
}

```

Output:

```
2022-01-11

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_weekday_last/operator_days&oldid=160403>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 October 2023, at 10:36.