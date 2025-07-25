# std::chrono::abs(std::chrono::duration)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator% | | | | | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | | | operator<<(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration_cast | | | | | | floor(C++17) | | | | | | ceil(C++17) | | | | | | round(C++17) | | | | | | ****abs****(C++17) | | | | | | operator""h(C++14) | | | | | | operator""min(C++14) | | | | | | operator""s(C++14) | | | | | | operator""ms(C++14) | | | | | | operator""us(C++14) | | | | | | operator""ns(C++14) | | | | | | from_stream(C++20) | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_type | | | | | | treat_as_floating_point | | | | | | duration_values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::chrono::duration>(C++20) | | | | | | hash<std::chrono::duration>(C++26) | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class Rep, class Period >  constexpr std::chrono::duration<Rep, Period> abs( std::chrono::duration<Rep, Period> d ); |  | (since C++17) |
|  |  |  |

Returns the absolute value of the duration d. Specifically, if d >= d.zero(), return d, otherwise return -d.

The function does not participate in the overload resolution unless std::numeric_limits<Rep>::is_signed is true.

### Parameters

|  |  |  |
| --- | --- | --- |
| d | - | duration |

### Return value

Absolute value of d.

### Possible implementation

|  |
| --- |
| ```text template<class Rep, class Period,     class = std::enable_if_t<std::numeric_limits<Rep>::is_signed>> constexpr std::chrono::duration<Rep, Period> abs(std::chrono::duration<Rep, Period> d) {     return d >= d.zero() ? +d : -d; } ``` |

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    using namespace std::chrono;
 
    static_assert(abs(-42s) == std::chrono::abs(42s));
 
    std::cout << "abs(+3min) = " << abs(3min).count() << '\n'
              << "abs(-3min) = " << abs(-3min).count() << '\n';
}

```

Output:

```
abs(+3min) = 3
abs(-3min) = 3

```

### See also

|  |  |
| --- | --- |
| operator+operator- | implements unary + and unary -   (public member function) |
| abs(int)labsllabs(C++11) | computes absolute value of an integral value (\(\small{|x|}\)|x|)   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/duration/abs&oldid=158855>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2023, at 00:16.