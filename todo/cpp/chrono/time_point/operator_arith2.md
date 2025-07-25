# operator+, operator-(std::chrono::time_point)

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
| ****operator+operator-**** | | | | |
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
| Defined in header `<chrono>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class C, class D1, class R2, class P2 >  time_point<C, typename std::common_type<D1, duration<R2,P2>>::type>      operator+( const time_point<C,D1>& pt, const duration<R2,P2>& d ); |  | (since C++11)  (until C++14) |
| template< class C, class D1, class R2, class P2 >  constexpr time_point<C, std::common_type_t<D1, duration<R2,P2>>>      operator+( const time_point<C,D1>& pt, const duration<R2,P2>& d ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class R1, class P1, class C, class D2 >  time_point<C, typename std::common_type<duration<R1,P1>,D2>::type>      operator+( const duration<R1,P1>& d, const time_point<C,D2>& pt ); |  | (since C++11)  (until C++14) |
| template< class R1, class P1, class C, class D2 >  constexpr time_point<C, std::common_type_t<duration<R1,P1>,D2>>      operator+( const duration<R1,P1>& d, const time_point<C,D2>& pt ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class C, class D1, class R2, class P2 >  time_point<C, typename std::common_type<D1, duration<R2,P2>>::type>      operator-( const time_point<C,D1>& pt, const duration<R2,P2>& d ); |  | (since C++11)  (until C++14) |
| template< class C, class D1, class R2, class P2 >  constexpr time_point<C, std::common_type_t<D1, duration<R2,P2>>>      operator-( const time_point<C,D1>& pt, const duration<R2,P2>& d ); |  | (since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class C, class D1, class D2 >  typename std::common_type<D1,D2>::type      operator-( const time_point<C,D1>& pt_lhs, const time_point<C,D2>& pt_rhs ); |  | (since C++11)  (until C++14) |
| template< class C, class D1, class D2 >  constexpr std::common_type_t<D1,D2>      operator-( const time_point<C,D1>& pt_lhs, const time_point<C,D2>& pt_rhs ); |  | (since C++14) |
|  |  |  |

Performs add and subtract operations involving a `time_point`.

1,2) Applies the offset d to pt. Effectively returns CT(pt.time_since_epoch() + d), where `CT` is the return type.3) Applies the offset d to pt in negative direction. Effectively returns CT(pt.time_since_epoch() - d), where `CT` is the return type.4) Computes the difference between pt_lhs and pt_rhs.

### Parameters

|  |  |  |
| --- | --- | --- |
| pt | - | a time point to apply the offset to |
| d | - | a time offset |
| pt_lhs, pt_rhs | - | time points to extract difference from |

### Return value

1-3) The time point that resulted from applying the offset d.4) The duration between the time points.

### Exceptions

May throw implementation-defined exceptions.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2739 | C++11 | pt - d behaved erratically for unsigned `duration`s | behavior corrected |

### See also

|  |  |
| --- | --- |
| operator+=operator-= | modifies the time point by the given duration   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/time_point/operator_arith2&oldid=157504>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 01:03.