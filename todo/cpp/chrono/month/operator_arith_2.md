# std::chrono::operator+, std::chrono::operator- (std::chrono::month)

From cppreference.com
< cpp‎ | chrono‎ | month
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

std::chrono::month

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| month::month | | | | |
| month::operator++month::operator-- | | | | |
| month::operator+=month::operator-= | | | | |
| month::operator unsigned | | | | |
| month::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| ****operator+operator-**** | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::month> | | | | |
| hash<std::chrono::month>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| constexpr std::chrono::month operator+( const std::chrono::month& m,                                          const std::chrono::months& ms ) noexcept; | (1) | (since C++20) |
| constexpr std::chrono::month operator+( const std::chrono::months& ms,                                          const std::chrono::month& m ) noexcept; | (2) | (since C++20) |
| constexpr std::chrono::month operator-( const std::chrono::month& m,                                           const std::chrono::months& ms ) noexcept; | (3) | (since C++20) |
| constexpr std::chrono::months operator-( const std::chrono::month& m1,                                            const std::chrono::month& m2 ) noexcept; | (4) | (since C++20) |
|  |  |  |

1,2) Adds ms.count() months to m. The month value held in the result is computed by first evaluating static_cast<long long>(unsigned(m)) + (ms.count() - 1), reducing it modulo 12 to an integer in the range `[`​0​`,`11`]`, and then adding 1.3) Subtracts ms.count() months from m and returns the result. Equivalent to return m + -ms;.4) If m1.ok() and m2.ok() are both true, returns a std::chrono::months value m such that m.count() is in the range `[`​0​`,`11`]` and m2 + m == m1. Otherwise the returned value is unspecified.

### Return value

1-3) A std::chrono::month holding a month value calculated as described above.4) A std::chrono::months representing the distance between m1 and m2.

### Notes

As long as the computation doesn't overflow, (1-3) always return a valid month even if m.ok() is false.

The result of subtracting two `month` values is a duration of type std::chrono::months. That duration unit represents the length of the average Gregorian month, and the resulting duration bears no relationship to the number of days in the particular months represented by the operands. For example, std::chrono::seconds(std::chrono::April - std::chrono::March) is not the number of seconds in March (2678400s), but 2629746s (30.436875 days).

### Example

Run this code

```
#include <cassert>
#include <chrono>
 
int main()
{
    std::chrono::month m{6};
 
    m = m + std::chrono::months(2);
    assert(m == std::chrono::month(8));
 
    m = m - std::chrono::months(3);
    assert(m == std::chrono::month(5));
 
    constexpr std::chrono::months ms = std::chrono::month(8) - std::chrono::month(6);
    static_assert(ms == std::chrono::months(2));
}

```

### See also

|  |  |
| --- | --- |
| operator++operator++(int)operator--operator--(int) | increments or decrements the month   (public member function) |
| operator+=operator-= | adds or subtracts a number of months   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/month/operator_arith_2&oldid=157501>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 00:34.