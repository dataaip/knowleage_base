# std::chrono::duration_cast

From cppreference.com
< cpp‎ | chrono‎ | duration
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

std::chrono::duration

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration::duration | | | | | | duration::operator= | | | | | | duration::count | | | | | | duration::zero | | | | | | duration::min | | | | | | duration::max | | | | | | duration::operator+duration::operator- | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration::operator++duration::operator-- | | | | | | duration::operator+=duration::operator-=duration::operator\*=duration::operator/=duration::operator%= | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator% | | | | | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | | | operator<<(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****duration_cast**** | | | | | | floor(C++17) | | | | | | ceil(C++17) | | | | | | round(C++17) | | | | | | abs(C++17) | | | | | | operator""h(C++14) | | | | | | operator""min(C++14) | | | | | | operator""s(C++14) | | | | | | operator""ms(C++14) | | | | | | operator""us(C++14) | | | | | | operator""ns(C++14) | | | | | | from_stream(C++20) | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_type | | | | | | treat_as_floating_point | | | | | | duration_values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::chrono::duration>(C++20) | | | | | | hash<std::chrono::duration>(C++26) | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class ToDuration, class Rep, class Period >  constexpr ToDuration duration_cast( const std::chrono::duration<Rep, Period>& d ); |  | (since C++11) |
|  |  |  |

Converts a std::chrono::duration to a duration of different type `ToDuration`.

The function only participate in overload resolution if `ToDuration` is a specialization of std::chrono::duration.

Let

- `ToRep` be typename ToDuration::rep,
- `ToPeriod` be typename ToDuration::period,
- `CF` be std::ratio_divide<Period, ToPeriod>,
- `CR` be std::common_type<Rep, ToRep, std::intmax_t>::type,
- cr_count be static_cast<CR>(d.count()),
- cr_num be static_cast<CR>(CF::num), and
- cr_den be static_cast<CR>(CF::den),

the result is:

|  | | CF::num | |
| --- | --- | --- | --- |
| 1 | not 1 |
| CF::den | 1 | ToDuration(static_cast<ToRep>                (d.count())) | ToDuration(static_cast<ToRep>                (cr_count \* cr_num)) |
| not 1 | ToDuration(static_cast<ToRep>                (cr_count / cr_den)) | ToDuration(static_cast<ToRep>                (cr_count \* cr_num / cr_den)) |

### Parameters

|  |  |  |
| --- | --- | --- |
| d | - | duration to convert |

### Return value

d converted to a duration of type `ToDuration`.

### Notes

No implicit conversions are used. Multiplications and divisions are avoided where possible, if it is known at compile time that one or more parameters are 1. Computations are done in the widest type available and converted, as if by static_cast, to the result type only when finished.

Casting between integer durations where the source period is exactly divisible by the target period (e.g. hours to minutes) or between floating-point durations can be performed with ordinary casts or implicitly via `std::chrono::duration` constructors, no `duration_cast` is needed.

Casting from a floating-point duration to an integer duration is subject to undefined behavior when the floating-point value is NaN, infinity, or too large to be representable by the target's integer type. Otherwise, casting to an integer duration is subject to truncation as with any static_cast to an integer type.

### Example

This example measures the execution time of a function.

Run this code

```
#include <chrono>
#include <iostream>
#include <ratio>
#include <thread>
 
void f()
{
    std::this_thread::sleep_for(std::chrono::seconds(1));
}
 
int main()
{
    const auto t1 = std::chrono::high_resolution_clock::now();
    f();
    const auto t2 = std::chrono::high_resolution_clock::now();
 
    // floating-point duration: no duration_cast needed
    const std::chrono::duration<double, std::milli> fp_ms = t2 - t1;
 
    // integral duration: requires duration_cast
    const auto int_ms = std::chrono::duration_cast<std::chrono::milliseconds>(t2 - t1);
 
    // converting integral duration to integral duration of
    // shorter divisible time unit: no duration_cast needed
    const std::chrono::duration<long, std::micro> int_usec = int_ms;
 
    std::cout << "f() took " << fp_ms << ", or "
              << int_ms << " (whole milliseconds), or "
              << int_usec << " (whole microseconds)\n";
}

```

Possible output:

```
f() took 1000.14ms, or 1000ms (whole milliseconds), or 1000000us (whole microseconds)

```

### See also

|  |  |
| --- | --- |
| duration(C++11) | a time interval   (class template) |
| time_point_cast(C++11) | converts a time point to another time point on the same clock, with a different duration   (function template) |
| floor(std::chrono::duration)(C++17) | converts a duration to another, rounding down   (function template) |
| ceil(std::chrono::duration)(C++17) | converts a duration to another, rounding up   (function template) |
| round(std::chrono::duration)(C++17) | converts a duration to another, rounding to nearest, ties to even   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/duration/duration_cast&oldid=175306>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 August 2024, at 18:25.