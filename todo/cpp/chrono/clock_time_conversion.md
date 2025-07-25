# std::chrono::clock_time_conversion

From cppreference.com
< cpp‎ | chrono
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | time_point(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****clock_time_conversion****(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_cast(C++20) | | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class Dest, class Source >  struct clock_time_conversion {}; |  | (since C++20) |
|  |  |  |

`std::chrono::clock_time_conversion` is a trait that specifies how to convert a std::chrono::time_point of the `Source` clock to that of the `Dest` clock. It does so by providing a const-callable `operator()` that accepts an argument of type std::chrono::time_point<Source, Duration> and returns a std::chrono::time_point<Dest, OtherDuration> that represents an equivalent point in time. The duration of the returned time point is computed from the source duration in a manner that varies for each specialization. `clock_time_conversion` is normally only used indirectly, via std::chrono::clock_cast.

A program may specialize `clock_time_conversion` if at least one of the template parameters is a user-defined clock type.

The primary template is an empty struct. The standard defines the following specializations:

|  |  |  |
| --- | --- | --- |
| template< class Clock >  struct clock_time_conversion<Clock, Clock>; | (1) | (since C++20) |
| template<>  struct clock_time_conversion<std::chrono::system_clock, std::chrono::system_clock>; | (2) | (since C++20) |
| template<>  struct clock_time_conversion<std::chrono::utc_clock, std::chrono::utc_clock>; | (3) | (since C++20) |
| template<>  struct clock_time_conversion<std::chrono::system_clock, std::chrono::utc_clock>; | (4) | (since C++20) |
| template<>  struct clock_time_conversion<std::chrono::utc_clock, std::chrono::system_clock>; | (5) | (since C++20) |
| template< class Clock >  struct clock_time_conversion<Clock, std::chrono::system_clock>; | (6) | (since C++20) |
| template< class Clock >  struct clock_time_conversion<std::chrono::system_clock, Clock>; | (7) | (since C++20) |
| template< class Clock >  struct clock_time_conversion<Clock, std::chrono::utc_clock>; | (8) | (since C++20) |
| template< class Clock >  struct clock_time_conversion<std::chrono::utc_clock, Clock>; | (9) | (since C++20) |
|  |  |  |

1-3) Identity conversion: `operator()` returns a copy of the argument.4,5) Conversions between std::chrono::sys_time and std::chrono::utc_time: `operator()` calls std::chrono::utc_clock::to_sys and std::chrono::utc_clock::from_sys, respectively.6,7) Conversions to and from std::chrono::sys_time when `Clock` supports `from_sys` and `to_sys`: `operator()` calls Clock::to_sys and Clock::from_sys, respectively.8,9) Conversions to and from std::chrono::utc_time when `Clock` supports `from_utc` and `to_utc`: `operator()` calls Clock::to_utc and Clock::from_utc, respectively.

### Member functions

Each specialization has an implicitly-declared default constructor, copy constructor, move constructor, copy assignment operator, move assignment operator, and destructor.

## std::chrono::clock_time_conversion::operator()

|  |  |  |
| --- | --- | --- |
| template< class Duration >  std::chrono::time_point<Clock, Duration>     operator()( const std::chrono::time_point<Clock, Duration>& t ) const; | (1) | (member of specialization (1)) |
| template< class Duration >  std::chrono::sys_time<Duration>     operator()( const std::chrono::sys_time<Duration> & t ) const; | (2) | (member of specialization (2)) |
| template< class Duration >  std::chrono::utc_time<Duration>     operator()( const std::chrono::utc_time<Duration>& t ) const; | (3) | (member of specialization (3)) |
| template< class Duration >  std::chrono::sys_time<Duration>     operator()( const std::chrono::utc_time<Duration>& t ) const; | (4) | (member of specialization (4)) |
| template< class Duration >  std::chrono::utc_time<Duration>     operator()( const std::chrono::sys_time<Duration>& t ) const; | (5) | (member of specialization (5)) |
| template< class Duration >  auto operator()( const std::chrono::sys_time<Duration>& t ) const -> decltype(Clock::from_sys(t)); | (6) | (member of specialization (6)) |
| template< class Duration >  auto operator()( const std::chrono::time_point<SourceClock, Duration>& t ) const -> decltype(Clock::to_sys(t)); | (7) | (member of specialization (7)) |
| template< class Duration >  auto operator()( const std::chrono::utc_time<Duration>& t ) const -> decltype(Clock::from_utc(t)); | (8) | (member of specialization (8)) |
| template< class Duration >  auto operator()( const std::chrono::time_point<Clock, Duration>& t ) const -> decltype(Clock::to_utc(t)); | (9) | (member of specialization (9)) |
|  |  |  |

Converts the argument std::chrono::time_point to the destination clock.

1-3) Identity conversion. Returns `t` unchanged.4) Returns std::chrono::utc_clock::to_sys(t).5) Returns std::chrono::utc_clock::from_sys(t).6) Returns Clock::from_sys(t). This overload participates in overload resolution only if the expression Clock::from_sys(t) is well-formed. The program is ill-formed if Clock::from_sys(t) does not return std::chrono::time_point<Clock, Duration> where `Duration` is some valid specialization of std::chrono::duration.7) Returns Clock::to_sys(t). This overload participates in overload resolution only if the expression Clock::to_sys(t) is well-formed. The program is ill-formed if Clock::to_sys(t) does not return std::chrono::sys_time<Duration> where `Duration` is some valid specialization of std::chrono::duration.8) Returns Clock::from_utc(t). This overload participates in overload resolution only if the expression Clock::from_utc(t) is well-formed. The program is ill-formed if Clock::from_utc(t) does not return std::chrono::time_point<Clock, Duration> where `Duration` is some valid specialization of std::chrono::duration.9) Returns Clock::to_utc(t). This overload participates in overload resolution only if the expression Clock::to_utc(t) is well-formed. The program is ill-formed if Clock::to_utc(t) does not return std::chrono::utc_time<Duration> where `Duration` is some valid specialization of std::chrono::duration.

### Parameters

|  |  |  |
| --- | --- | --- |
| t | - | time point to convert |

### Return value

The result of the conversion as described above:

1-3) t.4) std::chrono::utc_clock::to_sys(t).5) std::chrono::utc_clock::from_sys(t).6) Clock::from_sys(t).7) Clock::to_sys(t).8) Clock::from_utc(t).9) Clock::to_utc(t).

### See also

|  |  |
| --- | --- |
| clock_cast(C++20) | convert time points of one clock to another   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/clock_time_conversion&oldid=157493>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 August 2023, at 22:43.