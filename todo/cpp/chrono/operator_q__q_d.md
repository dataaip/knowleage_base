# std::literals::chrono_literals::operator""d

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

std::chrono::day

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| day::day | | | | |
| day::operator++day::operator-- | | | | |
| day::operator+=day::operator-= | | | | |
| day::operator unsigned | | | | |
| day::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| from_stream | | | | |
| ****operator""d**** | | | | |
| Helper classes | | | | |
| formatter<std::chrono::day> | | | | |
| hash<std::chrono::day>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| constexpr std::chrono::day operator ""d( unsigned long long d ) noexcept; |  | (since C++20) |
|  |  |  |

Forms a std::chrono::day literal representing a day of the month in the calendar.

### Parameters

|  |  |  |
| --- | --- | --- |
| d | - | the day value |

### Return value

A std::chrono::day storing d. If d > 255, the stored value is unspecified.

### Possible implementation

|  |
| --- |
| ```text constexpr std::chrono::day operator ""d(unsigned long long d) noexcept {     return std::chrono::day(d); } ``` |

### Notes

This operator is declared in the namespace std::literals::chrono_literals, where both literals and chrono_literals are inline namespaces. Access to this operator can be gained with:

- using namespace std::literals,
- using namespace std::chrono_literals, or
- using namespace std::literals::chrono_literals.

In addition, within the namespace std::chrono, the directive using namespace literals::chrono_literals; is provided by the standard library, so that if a programmer uses using namespace std::chrono; to gain access to the classes in the chrono library, the corresponding literal operators become visible as well.

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    using namespace std::literals::chrono_literals;
 
    std::cout << static_cast<unsigned>(42d) << '\t' << 42d << '\n'
              << static_cast<unsigned>(256d) << '\t' << 256d << '\n' // unspecified
              << static_cast<unsigned>(298d) << '\t' << 298d << '\n'; // unspecified
}

```

Possible output:

```
42      42 is not a valid day
0       00 is not a valid day
42      42 is not a valid day

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `day`   (public member function of `std::chrono::day`) |
| operator unsigned | retrieves the stored day value   (public member function of `std::chrono::day`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/operator%22%22d&oldid=157624>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 August 2023, at 12:26.