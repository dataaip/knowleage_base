# std::chrono::weekday

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | time_point(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_time_conversion(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_cast(C++20) | | | | | |
| Duration | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration(C++11) | | | | | |
| Clocks | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | ****weekday****(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::weekday****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| weekday::weekday | | | | |
| weekday::operator++weekday::operator-- | | | | |
| weekday::operator+=weekday::operator-= | | | | |
| weekday::c_encodingweekday::iso_encoding | | | | |
| weekday::ok | | | | |
| [weekday::operator[]](weekday/operator_at.html "cpp/chrono/weekday/operator at") | | | | |
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
| Defined in header `<chrono>` |  |  |
| class weekday; |  | (since C++20) |
| inline constexpr std::chrono::weekday Sunday{0}; |  | (since C++20) |
| inline constexpr std::chrono::weekday Monday{1}; |  | (since C++20) |
| inline constexpr std::chrono::weekday Tuesday{2}; |  | (since C++20) |
| inline constexpr std::chrono::weekday Wednesday{3}; |  | (since C++20) |
| inline constexpr std::chrono::weekday Thursday{4}; |  | (since C++20) |
| inline constexpr std::chrono::weekday Friday{5}; |  | (since C++20) |
| inline constexpr std::chrono::weekday Saturday{6}; |  | (since C++20) |
|  |  |  |

The class `weekday` represent a day of the week in the proleptic Gregorian calendar. Its normal range is `[`​0​`,`6`]`, for Sunday through Saturday, but it can hold any value in the range `[`​0​`,`255`]`. Seven named constants are predefined in the `std::chrono` namespace for the seven days of the week.

`weekday` is a TriviallyCopyable StandardLayoutType.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `weekday`   (public member function) |
| operator++operator++(int)operator--operator--(int) | increments or decrements the weekday   (public member function) |
| operator+=operator-= | adds or subtracts a number of days   (public member function) |
| c_encodingiso_encoding | retrieves the stored weekday value retrieves ISO 8601 weekday value   (public member function) |
| ok | checks if the stored weekday value is valid   (public member function) |
| [operator[]](weekday/operator_at.html "cpp/chrono/weekday/operator at") | convenience syntax for constructing a weekday_indexed or weekday_last from this `weekday`   (public member function) |

### Nonmember functions

|  |  |
| --- | --- |
| operator==(C++20) | compares two `weekday` values   (function) |
| operator+operator-(C++20) | performs arithmetic on `weekday`s   (function) |
| operator<<(C++20) | outputs a `weekday` into a stream   (function template) |
| from_stream(C++20) | parses a `weekday` from a stream according to the provided format   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::formatter<std::chrono::weekday>(C++20) | formatting support for `weekday`   (class template specialization) |
| std::hash<std::chrono::weekday>(C++26) | hash support for ****std::chrono::weekday****   (class template specialization) |

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    std::chrono::weekday x{42 / 13};
    std::cout << x++ << '\n';
    std::cout << x << '\n';
    std::cout << ++x << '\n';
}

```

Output:

```
Wed
Thu
Fri

```

### See also

|  |  |
| --- | --- |
| weekday_indexed(C++20) | represents the nth ****weekday**** of a month   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/weekday&oldid=157857>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 September 2023, at 19:24.