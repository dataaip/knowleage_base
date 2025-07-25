# std::common_type<std::chrono::duration>

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator% | | | | | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | | | operator<<(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration_cast | | | | | | floor(C++17) | | | | | | ceil(C++17) | | | | | | round(C++17) | | | | | | abs(C++17) | | | | | | operator""h(C++14) | | | | | | operator""min(C++14) | | | | | | operator""s(C++14) | | | | | | operator""ms(C++14) | | | | | | operator""us(C++14) | | | | | | operator""ns(C++14) | | | | | | from_stream(C++20) | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****common_type**** | | | | | | treat_as_floating_point | | | | | | duration_values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::chrono::duration>(C++20) | | | | | | hash<std::chrono::duration>(C++26) | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class Rep1, class Period1, class Rep2, class Period2 >  struct common_type<std::chrono::duration<Rep1, Period1>, std::chrono::duration<Rep2, Period2>>; |  | (since C++11) |
|  |  |  |

Exposes the type named `type`, which is the common type of two std::chrono::durations, whose period is the greatest common divisor of `Period1` and `Period2`.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `type` | std::chrono::duration<typename std::common_type<Rep1, Rep2>::type, /\* see note \*/> |

### Note

The period of the resulting duration can be computed by forming a ratio of the greatest common divisor of Period1::num and Period2::num and the least common multiple of Period1::den and Period2::den.

### Example

Run this code

```
#include <chrono>
#include <iostream>
#include <type_traits>
 
// std::chrono already finds the greatest common divisor,
// likely using std::common_type<>. We make the type
// deduction externally. 
 
template<typename T,typename S>
constexpr auto durationDiff(const T& t, const S& s)
    -> typename std::common_type<T,S>::type
{
    typedef typename std::common_type<T,S>::type Common;
    return Common(t) - Common(s);
}
 
int main() 
{
    using namespace std::literals;
 
    constexpr auto ms = 30ms;
    constexpr auto us = 1100us;
    constexpr auto diff = durationDiff(ms, us);
 
    std::cout << ms << " - " << us << " = " << diff << '\n';
}

```

Output:

```
30ms - 1100us = 28900us

```

### See also

|  |  |
| --- | --- |
| std::common_type<std::chrono::time_point>(C++11) | specializes the std::common_type trait   (class template specialization) |
| common_type(C++11) | determines the common type of a group of types   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/duration/common_type&oldid=175510>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 August 2024, at 06:02.