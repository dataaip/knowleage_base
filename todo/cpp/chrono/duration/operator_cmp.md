# operator==,!=,<,<=,>,>=,<=>(std::chrono::duration)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator% | | | | | | ****operator==operator!=operator<operator<=operator>operator>=operator<=>****(until C++20)(C++20) | | | | | | operator<<(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration_cast | | | | | | floor(C++17) | | | | | | ceil(C++17) | | | | | | round(C++17) | | | | | | abs(C++17) | | | | | | operator""h(C++14) | | | | | | operator""min(C++14) | | | | | | operator""s(C++14) | | | | | | operator""ms(C++14) | | | | | | operator""us(C++14) | | | | | | operator""ns(C++14) | | | | | | from_stream(C++20) | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_type | | | | | | treat_as_floating_point | | | | | | duration_values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::chrono::duration>(C++20) | | | | | | hash<std::chrono::duration>(C++26) | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| template< class Rep1, class Period1, class Rep2, class Period2 >  constexpr bool operator==( const std::chrono::duration<Rep1, Period1>& lhs, const std::chrono::duration<Rep2, Period2>& rhs ); | (1) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  constexpr bool operator!=( const std::chrono::duration<Rep1, Period1>& lhs, const std::chrono::duration<Rep2, Period2>& rhs ); | (2) | (since C++11)  (until C++20) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  constexpr bool operator<( const std::chrono::duration<Rep1, Period1>& lhs, const std::chrono::duration<Rep2, Period2>& rhs ); | (3) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  constexpr bool operator<=( const std::chrono::duration<Rep1, Period1>& lhs, const std::chrono::duration<Rep2, Period2>& rhs ); | (4) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  constexpr bool operator>( const std::chrono::duration<Rep1, Period1>& lhs, const std::chrono::duration<Rep2, Period2>& rhs ); | (5) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >  constexpr bool operator>=( const std::chrono::duration<Rep1, Period1>& lhs, const std::chrono::duration<Rep2, Period2>& rhs ); | (6) | (since C++11) |
| template< class Rep1, class Period1, class Rep2, class Period2 >      requires std::three_way_comparable<std::common_type_t<Rep1, Rep2>>  constexpr auto operator<=>( const std::chrono::duration<Rep1, Period1>& lhs, const std::chrono::duration<Rep2, Period2>& rhs ); | (7) | (since C++20) |
|  |  |  |

Compares two durations. Let `CT` be std::common_type<std::chrono::duration<Rep1, Period1>, std::chrono::duration<Rep2, Period2>>::type:

1,2) Checks if lhs and rhs are equal, i.e. the number of ticks for the type common to both durations are equal.3-6) Compares lhs to rhs, i.e. compares the number of ticks for the type common to both durations.7) Compares lhs to rhs, i.e. compares the number of ticks for the type common to both durations. The return type is deduced from CT(lhs).count() <=> CT(rhs).count().

|  |  |
| --- | --- |
| The `!=` operator is synthesized from `operator==`. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs | - | duration on the left-hand side of the operator |
| rhs | - | duration on the right-hand side of the operator |

### Return value

1) CT(lhs).count() == CT(rhs).count()2) !(lhs == rhs)3) CT(lhs).count() < CT(rhs).count()4) !(rhs < lhs)5) rhs < lhs6) !(lhs < rhs)7) CT(lhs).count() <=> CT(rhs).count()

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    constexpr auto t1 = std::chrono::seconds(2);
    constexpr auto t2 = std::chrono::milliseconds(2000);
 
    if constexpr (t1 == t2)
        std::cout << t1 << " == " << t2 << '\n';
    else
        std::cout << t1 << " != " << t2 << '\n';
 
    constexpr auto t3 = std::chrono::seconds(61);
    constexpr auto t4 = std::chrono::minutes(1);
 
    if constexpr (t3 > t4)
        std::cout << t3 << " > " << t4 << '\n';
    else
        std::cout << t3 << " <= " << t4 << '\n';
 
    using namespace std::chrono_literals;
 
    static_assert(1h == 60min);
    static_assert(1min == 60s);
    static_assert(1s == 1'000ms);
    static_assert(1ms == 1'000us);
    static_assert(1us == 1'000ns);
}

```

Output:

```
2s == 2000ms
61s > 1min

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/duration/operator_cmp&oldid=157498>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 August 2023, at 23:28.