# std::chrono::weekday::operator++, std::chrono::weekday::operator--

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
| ****weekday::operator++weekday::operator--**** | | | | |
| weekday::operator+=weekday::operator-= | | | | |
| weekday::c_encodingweekday::iso_encoding | | | | |
| weekday::ok | | | | |
| [weekday::operator[]](operator_at.html "cpp/chrono/weekday/operator at") | | | | |
| Nonmember functions | | | | |
| operator== | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::weekday> | | | | |
| formatter<std::chrono::hash>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr std::chrono::weekday& operator++() noexcept; | (1) | (since C++20) |
| constexpr std::chrono::weekday operator++( int ) noexcept; | (2) | (since C++20) |
| constexpr std::chrono::weekday& operator--() noexcept; | (3) | (since C++20) |
| constexpr std::chrono::weekday operator--( int ) noexcept; | (4) | (since C++20) |
|  |  |  |

Adds or subtracts 1 from the weekday value, reducing the result modulo 7 to an integer in the range `[`​0​`,`6`]`.

1,2) Performs \*this += std::chrono::days{1};.3,4) Performs \*this -= std::chrono::days{1};.

### Parameters

(none)

### Return value

1,3) A reference to this `weekday` after modification.2,4) A copy of the `weekday` made before modification.

### Notes

After a call to one of these functions, `ok()` is always true.

### Example

Run this code

```
#include <cassert>
#include <chrono>
#include <iostream>
 
int main()
{
    std::cout << std::boolalpha;
 
    std::chrono::weekday wd{0}; // Sunday is 0 or 7
 
    --wd;
    std::cout << (wd == std::chrono::Saturday) << ' ';
 
    ++wd;
    std::cout << (wd == std::chrono::Sunday) << '\n';
 
    wd = std::chrono::weekday{13};
    assert(!wd.ok());
    wd++;
    assert(wd.ok());
}

```

Output:

```
true true

```

### See also

|  |  |
| --- | --- |
| operator+=operator-= | adds or subtracts a number of days   (public member function) |
| operator+operator-(C++20) | performs arithmetic on `weekday`s   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/weekday/operator_inc_dec&oldid=157511>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 08:28.