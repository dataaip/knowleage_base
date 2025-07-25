# std::chrono::round(std::chrono::time_point)

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
| time_point::min | | | | |
| time_point::max | | | | |
| Non-member functions | | | | |
| operator+operator- | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | |
| time_point_cast | | | | |
| floor(C++17) | | | | |
| ceil(C++17) | | | | |
| ****round****(C++17) | | | | |
| Helper classes | | | | |
| common_type | | | | |
| hash<std::chrono::time_point>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class ToDuration, class Clock, class Duration >  constexpr std::chrono::time_point<Clock, ToDuration>     round( const std::chrono::time_point<Clock, Duration>& tp ); |  | (since C++17) |
|  |  |  |

Returns the nearest time point to tp representable in `ToDuration`, rounding to even in halfway cases.

The function does not participate in the overload resolution unless `ToDuration` is a specialization of std::chrono::duration and std::chrono::treat_as_floating_point_v<typename ToDuration::rep> is false.

### Parameters

|  |  |  |
| --- | --- | --- |
| tp | - | time point to round to nearest |

### Return value

tp rounded to nearest time point using duration of type `ToDuration`, rounding to even in halfway cases.

### Possible implementation

|  |
| --- |
| ```text namespace detail {     template<class> inline constexpr bool is_duration_v = false;     template<class Rep, class Period> inline constexpr bool is_duration_v<         std::chrono::duration<Rep, Period>> = true; }   template<class To, class Clock, class FromDuration,          class = std::enable_if_t<detail::is_duration_v<To> &&                 !std::chrono::treat_as_floating_point_v<typename To::rep>>> constexpr std::chrono::time_point<Clock, To> round(     const std::chrono::time_point<Clock, FromDuration>& tp) {     return std::chrono::time_point<Clock, To>{         std::chrono::round<To>(tp.time_since_epoch())}; } ``` |

### Example

Run this code

```
#include <chrono>
#include <iostream>
#include <string>
 
template<typename TimePoint>
std::string to_string(const TimePoint& time_point)
{
    return std::to_string(time_point.time_since_epoch().count());
}
 
int main()
{
    using namespace std::literals::chrono_literals;
    using Sec = std::chrono::seconds;
 
    std::cout << "Time point\t" "Cast\t" "Floor\t" "Round\t" "Ceil\n";
    std::cout << "(ms)\t\t"     "(s)\t"  "(s)\t"   "(s)\t"   "(s)\n";
    for (const auto value_ms : {5432ms, 5678ms})
    {
        std::chrono::time_point<std::chrono::system_clock, std::chrono::milliseconds>
            time_point_ms(value_ms);
 
        std::cout
            << to_string(time_point_ms) << "\t\t"
            << to_string(std::chrono::time_point_cast<Sec>(time_point_ms)) << '\t'
            << to_string(std::chrono::floor<Sec>(time_point_ms)) << '\t'
            << to_string(std::chrono::round<Sec>(time_point_ms)) << '\t'
            << to_string(std::chrono::ceil<Sec>(time_point_ms)) << '\n';
    }
}

```

Output:

```
Time point	Cast	Floor	Round	Ceil
(ms)		(s)	(s)	(s)	(s)
5432		5	5	5	6
5678		5	5	6	6

```

### See also

|  |  |
| --- | --- |
| time_point_cast(C++11) | converts a time point to another time point on the same clock, with a different duration   (function template) |
| ceil(std::chrono::time_point)(C++17) | converts a time_point to another, rounding up   (function template) |
| floor(std::chrono::time_point)(C++17) | converts a time_point to another, rounding down   (function template) |
| round(std::chrono::duration)(C++17) | converts a duration to another, rounding to nearest, ties to even   (function template) |
| roundroundfroundllroundlroundflroundlllroundllroundfllroundl(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | nearest integer, rounding away from zero in halfway cases   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/time_point/round&oldid=159670>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 September 2023, at 11:26.