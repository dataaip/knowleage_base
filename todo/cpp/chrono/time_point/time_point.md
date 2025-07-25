# std::chrono::time_point<Clock,Duration>::time_point

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
| ****time_point::time_point**** | | | | |
| time_point::time_since_epoch | | | | |
| time_point::operator+=time_point::operator-= | | | | |
| time_point::operator++time_point::operator--(C++20)(C++20) | | | | |
| time_point::min | | | | |
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
|  | (1) |  |
| time_point(); |  | (since C++11)  (constexpr since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| explicit time_point( const duration& d ); |  | (since C++11)  (constexpr since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class Duration2 >  time_point( const time_point<Clock, Duration2>& t ); |  | (since C++11)  (constexpr since C++14) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Constructs a new `time_point` from one of several optional data sources.

1) Default constructor, creates a `time_point` representing the `Clock`'s epoch (i.e., time_since_epoch() is zero).2) Constructs a `time_point` at `Clock`'s epoch plus d.3) Constructs a `time_point` by converting t to `duration`. This constructor only participates in overload resolution if `Duration2` is implicitly convertible to `duration`.

### Parameters

|  |  |  |
| --- | --- | --- |
| d | - | a `duration` to copy from |
| t | - | a `time_point` to convert from |

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
using Clock = std::chrono::steady_clock;
using TimePoint = std::chrono::time_point<Clock>;
 
void print_ms(const TimePoint& point) 
{
    using Ms = std::chrono::milliseconds;
    const Clock::duration since_epoch = point.time_since_epoch();
    std::cout << std::chrono::duration_cast<Ms>(since_epoch) << '\n';
}
 
int main() 
{
    const TimePoint default_value = TimePoint(); // (1)
    print_ms(default_value); // 0ms
 
    const Clock::duration duration_4_seconds = std::chrono::seconds(4);
    const TimePoint time_point_4_seconds(duration_4_seconds); // (2)
    // 4 seconds from start of epoch
    print_ms(time_point_4_seconds); // 4000ms
 
    const TimePoint time_point_now = Clock::now(); // (3)
    print_ms(time_point_now); // 212178842ms
}

```

Possible output:

```
0ms
4000ms
212178842ms

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs new duration   (public member function of `std::chrono::duration<Rep,Period>`) |
| duration_cast(C++11) | converts a duration to another, with a different tick interval   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/time_point/time_point&oldid=161649>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 October 2023, at 15:35.