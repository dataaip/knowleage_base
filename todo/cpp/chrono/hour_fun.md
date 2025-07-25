# std::chrono::is_am, std::chrono::is_pm, std::chrono::make12, std::chrono::make24

From cppreference.com
< cpp‎ | chrono
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****is_amis_pm****(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****make12make24****(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| constexpr bool is_am( const std::chrono::hours& h ) noexcept; | (1) | (since C++20) |
| constexpr bool is_pm( const std::chrono::hours& h ) noexcept; | (2) | (since C++20) |
| constexpr std::chrono::hours make12( const std::chrono::hours& h ) noexcept; | (3) | (since C++20) |
| constexpr std::chrono::hours make24( const std::chrono::hours& h,                                       bool is_pm ) noexcept; | (4) | (since C++20) |
|  |  |  |

These functions aid in translating between a 12-hour format time of day, and a 24-hour format time of day.

1) Detects whether the 24-hour format time is a.m. (**ante meridiem**, before midday).2) Detects whether the 24-hour format time is p.m. (**post meridiem**, after midday).3) Returns the 12-hour equivalent of a 24-hour format time.4) Returns the 24-hour equivalent of a 12-hour format time h, where is_pm determines whether the time is p.m.

### Parameters

|  |  |  |
| --- | --- | --- |
| h | - | 12-hour or 24-hour format time to detect |
| is_pm | - | whether the 12-hour format time is p.m. |

### Return value

1) 0h <= h && h <= 11h2) 12h <= h && h <= 23h3) If h is in range `[`0h`,`23h`]`, returns the 12-hour equivalent in range `[`1h`,`12h`]`. Otherwise, the return value is unspecified.4) If h is in range `[`1h`,`12h`]`, returns the 24-hour equivalent in range `[`0h`,`11h`]` if is_pm is false, or in range `[`12h`,`23h`]` otherwise. Otherwise, the return value is unspecified.

### Example

Run this code

```
#include <chrono>
#include <iomanip>
#include <iostream>
#include <utility>
 
int main()
{
    using namespace std::chrono;
 
    static_assert(
        is_am(10h) &&  is_am(11h) && !is_am(12h) && !is_am(23h) &&
       !is_pm(10h) && !is_pm(11h) &&  is_pm(12h) &&  is_pm(23h)
    );
 
    std::cout << "make12():\n";
 
    for (const hours hh : {0h, 1h, 11h, 12h, 13h, 23h})
    {
        const hours am{make12(hh)};
        std::cout << std::setw(2) << hh.count() << "h == "
                  << std::setw(2) << am.count() << (is_am(hh) ? "h a.m.\n" : "h p.m.\n");
    }
 
    std::cout << "\nmake24():\n";
 
    using p = std::pair<hours, bool>;
 
    for (const auto& [hh, pm] : {p{1h, 0}, p{12h, 0}, p{1h, 1}, p{12h, 1}})
    {
        std::cout << std::setw(2) << hh.count()
                  << (pm ? "h p.m." : "h a.m.")
                  << " == " << std::setw(2)
                  << make24(hh, pm).count() << "h\n";
    }
}

```

Output:

```
make12():
 0h == 12h a.m.
 1h ==  1h a.m.
11h == 11h a.m.
12h == 12h p.m.
13h ==  1h p.m.
23h == 11h p.m.
 
make24():
 1h a.m. ==  1h
12h a.m. ==  0h
 1h p.m. == 13h
12h p.m. == 12h

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/hour_fun&oldid=159664>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 September 2023, at 11:04.