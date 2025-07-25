# std::chrono::year_month_day_last::year_month_day_last

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
| ****year_month_day_last::year_month_day_last**** | | | | |
| year_month_day_last::operator+=year_month_day_last::operator-= | | | | |
| year_month_day_last::yearyear_month_day_last::monthyear_month_day_last::dayyear_month_day_last::month_day_last | | | | |
| year_month_day_last::operator sys_daysyear_month_day_last::operator local_days | | | | |
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
| constexpr year_month_day_last( const std::chrono::year& y,                                 const std::chrono::month_day_last& mdl ) noexcept; |  | (since C++20) |
|  |  |  |

Constructs a `year_month_day_last` object storing the year y and the month mdl.month(). The constructed object represents the last day of that year and month.

### Notes

A `year_month_day_last` can also be created by combining a std::chrono::year_month with std::chrono::last using operator/.

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    std::cout << "All last days of months of a given year:\n";
 
    constexpr std::chrono::year year{2021};
 
    for (int i{1}; i <= 12; ++i)
    {
        const std::chrono::month_day_last mdl{std::chrono::month(i) / std::chrono::last};
        const std::chrono::year_month_day_last ymdl{year, mdl};
        std::cout << ymdl << " day: " << ymdl.day() << '\n';
    }
}

```

Possible output:

```
All last days of months of a given year: 
2021/Jan/last day: 31
2021/Feb/last day: 28
2021/Mar/last day: 31
2021/Apr/last day: 30
2021/May/last day: 31
2021/Jun/last day: 30
2021/Jul/last day: 31
2021/Aug/last day: 31
2021/Sep/last day: 30
2021/Oct/last day: 31
2021/Nov/last day: 30
2021/Dec/last day: 31

```

### See also

|  |  |
| --- | --- |
| operator/(C++20) | conventional syntax for Gregorian calendar date creation   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_day_last/year_month_day_last&oldid=159690>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 September 2023, at 23:30.