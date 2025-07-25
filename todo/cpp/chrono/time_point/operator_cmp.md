# operator==,!=,<,<=,>,>=,<=>(std::chrono::time_point)

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
| ****operator==operator!=operator<operator<=operator>operator>=operator<=>****(until C++20)(C++20) | | | | |
| time_point_cast | | | | |
| floor(C++17) | | | | |
| ceil(C++17) | | | | |
| round(C++17) | | | | |
| Helper classes | | | | |
| common_type | | | | |
| hash<std::chrono::time_point>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class Clock, class Dur1, class Dur2 >  bool operator==( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++11)  (until C++14) |
| template< class Clock, class Dur1, class Dur2 >  constexpr bool operator==( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class Clock, class Dur1, class Dur2 >  bool operator!=( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++11)  (until C++14) |
| template< class Clock, class Dur1, class Dur2 >  constexpr bool operator!=( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++14)  (until C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class Clock, class Dur1, class Dur2 >  bool operator<( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++11)  (until C++14) |
| template< class Clock, class Dur1, class Dur2 >  constexpr bool operator<( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class Clock, class Dur1, class Dur2 >  bool operator<=( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++11)  (until C++14) |
| template< class Clock, class Dur1, class Dur2 >  constexpr bool operator<=( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (5) |  |
| template< class Clock, class Dur1, class Dur2 >  bool operator>( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++11)  (until C++14) |
| template< class Clock, class Dur1, class Dur2 >  constexpr bool operator>( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (6) |  |
| template< class Clock, class Dur1, class Dur2 >  bool operator>=( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++11)  (until C++14) |
| template< class Clock, class Dur1, class Dur2 >  constexpr bool operator>=( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
| template< class Clock, class Dur1, std::three_way_comparable_with<Dur1> Dur2 >  constexpr auto operator<=>( const std::chrono::time_point<Clock,Dur1>& lhs, const std::chrono::time_point<Clock,Dur2>& rhs ); | (7) | (since C++20) |
|  |  |  |

Compares two time points. The comparison is done by comparing the results time_since_epoch() for the time points.

1,2) Checks if the time points lhs and rhs refer to the same time point for the given clock.3-6) Compares the time points lhs and rhs.7) Compares the time points lhs and rhs. The return type is deduced from lhs.time_since_epoch() <=> rhs.time_since_epoch(), and hence the three-way comparison result type of `Dur1` and `Dur2`.

|  |  |
| --- | --- |
| The `!=` operator is synthesized from `operator==`. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | time points to compare |

### Return value

1) true if the lhs and rhs refer to the same time point, false otherwise.2) true if the lhs and rhs refer to different time points, false otherwise.3) true if the lhs refers to time point **before** rhs, false otherwise.4) true if the lhs refers to time point **before** rhs, or to the same time point as rhs, false otherwise.5) true if the lhs refers to time point **after** rhs, false otherwise.6) true if the lhs refers to time point **after** rhs, or to the same time point as rhs, false otherwise.7) lhs.time_since_epoch() <=> rhs.time_since_epoch().

### Exceptions

May throw implementation-defined exceptions.

### Notes

Two-way comparison operators of `time_point` were not constexpr in C++11, this was corrected in C++14.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/time_point/operator_cmp&oldid=157508>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 01:43.