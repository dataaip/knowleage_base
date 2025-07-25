# std::chrono::duration<Rep,Period>::duration

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****duration::duration**** | | | | | | duration::operator= | | | | | | duration::count | | | | | | duration::zero | | | | | | duration::min | | | | | | duration::max | | | | | | duration::operator+duration::operator- | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration::operator++duration::operator-- | | | | | | duration::operator+=duration::operator-=duration::operator\*=duration::operator/=duration::operator%= | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator% | | | | | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | | | operator<<(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration_cast | | | | | | floor(C++17) | | | | | | ceil(C++17) | | | | | | round(C++17) | | | | | | abs(C++17) | | | | | | operator""h(C++14) | | | | | | operator""min(C++14) | | | | | | operator""s(C++14) | | | | | | operator""ms(C++14) | | | | | | operator""us(C++14) | | | | | | operator""ns(C++14) | | | | | | from_stream(C++20) | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_type | | | | | | treat_as_floating_point | | | | | | duration_values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::chrono::duration>(C++20) | | | | | | hash<std::chrono::duration>(C++26) | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr duration() = default; | (1) | (since C++11) |
| duration( const duration& ) = default; | (2) | (since C++11) |
| template< class Rep2 >  constexpr explicit duration( const Rep2& r ); | (3) | (since C++11) |
| template< class Rep2, class Period2 >  constexpr duration( const duration<Rep2, Period2>& d ); | (4) | (since C++11) |
|  |  |  |

Constructs a new `duration` from one of several optional data sources.

1) The default constructor.2) The copy constructor.3) Constructs a duration with r ticks. This overload participates in overload resolution only if all following conditions are satisfied:

- is_convertible<const Rep2&, Rep>::value is true.
- Any of the following conditions is satisfied:[[1]](duration.html#cite_note-1)

:   - std::chrono::treat_as_floating_point<Rep>::value is true.
    - std::chrono::treat_as_floating_point<Rep2>::value is false.

4) Constructs a duration by converting d to an appropriate period and tick count, as if by std::chrono::duration_cast<duration>(d).count(). This overload participates in overload resolution only if no overflow is induced in the conversion, and any of the following conditions is satisfied:[[2]](duration.html#cite_note-2)

- std::chrono::treat_as_floating_point<Rep>::value is true.
- All following conditions are satisfied:

:   - std::ratio_divide<Period2, Period>::den is 1.
    - std::chrono::treat_as_floating_point<Rep2>::value is false.

1. ↑ That is, a duration with an integer tick count cannot be constructed from a floating-point value, but a duration with a floating-point tick count can be constructed from an integer value.
2. ↑ That is, either the duration uses floating-point ticks, or `Period2` is exactly divisible by `Period`.

### Parameters

|  |  |  |
| --- | --- | --- |
| r | - | a tick count |
| d | - | a duration to copy from |

### Example

The following code shows several examples (both valid and invalid) of how to construct durations:

Run this code

```
#include <chrono>
 
int main()
{
    std::chrono::hours h(1); // one hour
    std::chrono::milliseconds ms{3}; // 3 milliseconds
    std::chrono::duration<int, std::kilo> ks(3); // 3000 seconds
 
    // error: treat_as_floating_point<int>::value == false,
    // This duration allows whole tick counts only
//  std::chrono::duration<int, std::kilo> d3(3.5);
 
    // 30Hz clock using fractional ticks
    std::chrono::duration<double, std::ratio<1, 30>> hz30(3.5);
 
    // 3000 microseconds constructed from 3 milliseconds
    std::chrono::microseconds us = ms;
    // error: 1/1000000 is not divisible by 1/1000
//  std::chrono::milliseconds ms2 = us
    std::chrono::duration<double, std::milli> ms2 = us; // 3.0 milliseconds
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2094 | C++11 | for overload (4), std::ratio_divide<Period2, period>::num might overflow when evaluating std::ratio_divide<Period2, period>::den | overload (4) does not participate in overload resolution in this case |
| LWG 3050 | C++11 | convertibility constraint used non-const xvalue | use const lvalues instead |

### See also

|  |  |
| --- | --- |
| operator= | assigns the contents   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/duration/duration&oldid=169900>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 February 2024, at 21:54.