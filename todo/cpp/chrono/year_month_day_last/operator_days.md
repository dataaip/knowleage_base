# std::chrono::year_month_day_last::operator sys_days, std::chrono::year_month_day_last::operator local_days

From cppreference.com
< cpp‎ | chrono‎ | year month day last
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

std::chrono::year_month_day_last

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month_day_last::year_month_day_last | | | | |
| year_month_day_last::operator+=year_month_day_last::operator-= | | | | |
| year_month_day_last::yearyear_month_day_last::monthyear_month_day_last::dayyear_month_day_last::month_day_last | | | | |
| ****year_month_day_last::operator sys_daysyear_month_day_last::operator local_days**** | | | | |
| year_month_day_last::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_day_last> | | | | |
| hash<std::chrono::year_month_day_last>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr operator std::chrono::sys_days() const noexcept; | (1) | (since C++20) |
| constexpr explicit operator std::chrono::local_days() const noexcept; | (2) | (since C++20) |
|  |  |  |

Converts \*this to a std::chrono::time_point representing the same date as this `year_month_day_last`. This is equivalent to composing a `year_month_day` from `year()`, `month()` and `day()` and converting that `year_month_day` to the destination type.

1) Equivalent to std::chrono::sys_days(year()/month()/day()).2) Equivalent to std::chrono::local_days(year()/month()/day()).

### Example

Run this code

```
#include <array>
#include <chrono>
#include <iostream>
#include <string_view>
using namespace std::chrono;
using namespace std::literals;
 
int main()
{
    constexpr std::chrono::year y{2023y};
    constexpr std::array quarters{"1st"sv, "2nd"sv, "3rd"sv, "4th"sv};
    constexpr auto mq{12 / 4}; // months per quarter        
 
    std::cout << "In year " << static_cast<int>(y) << '\n';
    for (auto q = 1; q < 5; ++q)
    {
        const auto ls = y / std::chrono::month(q * mq) / Sunday[last];
        const auto ld = y / std::chrono::month(q * mq) / last;
        // subtract last Sunday from last day for day of week
        const auto index = (sys_days(ld) - sys_days(ls)).count();
        std::cout << "The " << quarters[q - 1] << " quarter ends on a "  
                  << std::chrono::weekday(index) << '\n';
    }
}

```

Output:

```
In year 2023
The 1st quarter ends on a Fri
The 2nd quarter ends on a Fri
The 3rd quarter ends on a Sat
The 4th quarter ends on a Sun

```

### See also

|  |  |
| --- | --- |
| operator sys_daysoperator local_days | converts to a std::chrono::time_point   (public member function of `std::chrono::year_month_day`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_day_last/operator_days&oldid=159959>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 October 2023, at 14:02.