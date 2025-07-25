# std::chrono::operator+, std::chrono::operator- (std::chrono::weekday)

From cppreference.com
< cpp‎ | chrono‎ | weekday
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

std::chrono::weekday

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| weekday::weekday | | | | |
| weekday::operator++weekday::operator-- | | | | |
| weekday::operator+=weekday::operator-= | | | | |
| weekday::c_encodingweekday::iso_encoding | | | | |
| weekday::ok | | | | |
| [weekday::operator[]](operator_at.html "cpp/chrono/weekday/operator at") | | | | |
| Nonmember functions | | | | |
| operator== | | | | |
| ****operator+operator-**** | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::weekday> | | | | |
| formatter<std::chrono::hash>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| constexpr std::chrono::weekday operator+( const std::chrono::weekday& wd,                                            const std::chrono::days& d ) noexcept; | (1) | (since C++20) |
| constexpr std::chrono::weekday operator+( const std::chrono::days& d,                                            const std::chrono::weekday& wd ) noexcept; | (2) | (since C++20) |
| constexpr std::chrono::weekday operator-( const std::chrono::weekday& wd,                                            const std::chrono::days& d ) noexcept; | (3) | (since C++20) |
| constexpr std::chrono::days operator-( const std::chrono::weekday& wd1,                                         const std::chrono::weekday& wd2 ) noexcept; | (4) | (since C++20) |
|  |  |  |

1,2) Adds d.count() days to wd. The weekday value held in the result is computed by first evaluating static_cast<long long>(wd.c_encoding()) + d.count() and reducing it modulo 7 to an integer in the range `[`​0​`,`6`]`.3) Subtracts d.count() days from wd. Equivalent to return wd + -d;.4) If wd1.ok() and wd2.ok() are both true, returns a std::chrono::days value d such that d.count() is in the range `[`​0​`,`6`]` and wd2 + d == wd1. Otherwise the returned value is unspecified.

### Return value

1-3) A std::chrono::weekday holding a weekday value calculated as described above.4) A std::chrono::days representing the distance between wd1 and wd2.

### Notes

As long as the computation doesn't overflow, (1-3) always return a valid `weekday` even if wd.ok() is false.

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    std::cout << std::boolalpha;
 
    std::chrono::weekday wd{4};
    wd = wd + std::chrono::days(2);
    std::cout << (wd == std::chrono::weekday(6)) << ' '
              << (wd == std::chrono::Saturday) << ' ';
 
    wd = wd - std::chrono::days(3);
    std::cout << (wd == std::chrono::weekday(3)) << ' '
              << (wd == std::chrono::Wednesday) << ' ';
 
    wd = std::chrono::Tuesday;
    wd = wd + std::chrono::days{8}; // (((2 + 8) == 10) % 7) == 3;
    std::cout << (wd == std::chrono::Wednesday) << ' ';
 
    wd = wd + (std::chrono::Sunday - std::chrono::Thursday); // (3 + 3) == 6
    std::cout << (wd == std::chrono::Saturday) << '\n';
}

```

Output:

```
true true true true true true

```

### See also

|  |  |
| --- | --- |
| operator++operator++(int)operator--operator--(int) | increments or decrements the weekday   (public member function) |
| operator+=operator-= | adds or subtracts a number of days   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/weekday/operator_arith_2&oldid=157509>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 01:46.