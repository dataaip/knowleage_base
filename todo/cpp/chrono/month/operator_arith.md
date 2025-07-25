# std::chrono::month::operator+=, std::chrono::month::operator-=

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
| ****month::operator+=month::operator-=**** | | | | |
| month::operator unsigned | | | | |
| month::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::month> | | | | |
| hash<std::chrono::month>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr std::chrono::month& operator+=( const std::chrono::months& m ) noexcept; | (1) | (since C++20) |
| constexpr std::chrono::month& operator-=( const std::chrono::months& m ) noexcept; | (2) | (since C++20) |
|  |  |  |

Adds or subtracts m.count() from the month value, reducing the result modulo 12 to an integer in the range `[`1`,`12`]`.

1) Performs \*this = \*this + m;.2) Performs \*this = \*this - m;.

### Return value

A reference to this `month` after modification.

### Notes

After a call to one of these functions, `ok()` is always true if no overflow occurred during the operation.

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    std::cout << std::boolalpha;
 
    std::chrono::month m{6};
    m += std::chrono::months(2);
    std::cout << (m == std::chrono::month(8)) << ' '
              << (m == std::chrono::August) << ' ';
 
    m -= std::chrono::months(3);
    std::cout << (m == std::chrono::month(5)) << ' '
              << (m == std::chrono::May) << ' ';
 
    m = std::chrono::October;
    m += std::chrono::months{8}; // ((10 += 8 == 18) % 12) == 6;
    std::cout << (m == std::chrono::June) << ' ';
 
    m -= std::chrono::months{std::chrono::December - std::chrono::February}; // -= 10
    // (6 -= 10) == -4; -4 % 12 == (12 - 4) == 8
    std::cout << (m == std::chrono::August) << '\n';
}

```

Output:

```
true true true true true true

```

### See also

|  |  |
| --- | --- |
| operator++operator++(int)operator--operator--(int) | increments or decrements the month   (public member function) |
| operator+operator-(C++20) | performs arithmetic on `month`s   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/month/operator_arith&oldid=157580>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 August 2023, at 09:27.