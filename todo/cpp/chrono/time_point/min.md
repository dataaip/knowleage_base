# std::chrono::time_point<Clock,Duration>::min

From cppreference.com
< cpp‎ | chrono‎ | time point
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

std::chrono::time_point

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| time_point::time_point | | | | |
| time_point::time_since_epoch | | | | |
| time_point::operator+=time_point::operator-= | | | | |
| time_point::operator++time_point::operator--(C++20)(C++20) | | | | |
| ****time_point::min**** | | | | |
| time_point::max | | | | |
| Non-member functions | | | | |
| operator+operator- | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | |
| time_point_cast | | | | |
| floor(C++17) | | | | |
| ceil(C++17) | | | | |
| round(C++17) | | | | |
| Helper classes | | | | |
| common_type | | | | |
| hash<std::chrono::time_point>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| static constexpr time_point min(); |  | (until C++20) |
| static constexpr time_point min() noexcept; |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Returns a `time_point` with the smallest possible duration, i.e. time_point(duration::min()).

### Parameters

(none)

### Return value

The smallest possible `time_point`.

### Example

Run this code

```
#include <chrono>
#include <iomanip>
#include <iostream>
#include <ratio>
#include <string>
 
constexpr auto steady_min = std::chrono::steady_clock::time_point::min();
 
void animate_frame_at_time_offset(double game_time)
{
    std::cout << std::string(static_cast<int>(game_time) % 10 + 1, '*') << '\n';
}
 
int main()
{
    auto last_frame = steady_min;
    std::chrono::duration<double, std::micro> game_time{0.0};
 
    for (int n = 0; n < 5; ++n)
    {
        const auto current_frame = std::chrono::steady_clock::now();
        // initialize timer if first frame ever:
        if (last_frame == steady_min)
            last_frame = current_frame;
        game_time += current_frame - last_frame;
        std::cout << "Drawing frame at " << std::setprecision(10)
                  << std::setw(8) << game_time.count() << " μs ";
        animate_frame_at_time_offset(game_time.count());
    }
}

```

Possible output:

```
Drawing frame at        0 μs *
Drawing frame at  134.499 μs *****
Drawing frame at  274.337 μs *****
Drawing frame at  416.571 μs *******
Drawing frame at  561.124 μs **

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/time_point/min&oldid=175496>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 August 2024, at 05:47.