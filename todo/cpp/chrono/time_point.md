# std::chrono::time_point

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****time_point****(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_time_conversion(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clock_cast(C++20) | | | | | |
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

****std::chrono::time_point****

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
| template<  class Clock,      class Duration = typename Clock::duration > class time_point; |  | (since C++11) |
|  |  |  |

Class template `std::chrono::time_point` represents a point in time. It is implemented as if it stores a value of type `Duration` indicating the time interval from the start of the `Clock`'s epoch.

|  |  |
| --- | --- |
| `Clock` must meet the requirements for Clock or be std::chrono::local_t(since C++20). | (until C++23) |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `clock` | `Clock`, the clock on which this time point is measured |
| `duration` | `Duration`, a std::chrono::duration type used to measure the time since epoch |
| `rep` | `Rep`, an arithmetic type representing the number of ticks of the duration |
| `period` | `Period`, a std::ratio type representing the tick period of the duration |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new time point   (public member function) |
| time_since_epoch | returns the time point as duration since the start of its clock   (public member function) |
| operator+=operator-= | modifies the time point by the given duration   (public member function) |
| operator++operator++(int)operator--operator--(int)(C++20) | increments or decrements the duration   (public member function) |
| min[static] | returns the time point corresponding to the smallest duration   (public static member function) |
| max[static] | returns the time point corresponding to the largest duration   (public static member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator+operator-(C++11) | performs add and subtract operations involving a time point   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(C++11)(C++11)(C++11)(C++20) | compares two time points   (function template) |
| time_point_cast(C++11) | converts a time point to another time point on the same clock, with a different duration   (function template) |
| floor(std::chrono::time_point)(C++17) | converts a time_point to another, rounding down   (function template) |
| ceil(std::chrono::time_point)(C++17) | converts a time_point to another, rounding up   (function template) |
| round(std::chrono::time_point)(C++17) | converts a time_point to another, rounding to nearest, ties to even   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::common_type<std::chrono::time_point>(C++11) | specializes the std::common_type trait   (class template specialization) |
| std::hash<std::chrono::time_point>(C++26) | hash support for ****std::chrono::time_point****   (class template specialization) |

### Example

Run this code

```
#include <algorithm>
#include <chrono>
#include <ctime>
#include <iomanip>
#include <iostream>
 
void slow_motion()
{
    static int a[]{1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12};
    // Generate Γ(13) == 12! permutations:
    while (std::ranges::next_permutation(a).found) {}
}
 
int main()
{
    using namespace std::literals; // enables literal suffixes, e.g. 24h, 1ms, 1s.
 
    const std::chrono::time_point<std::chrono::system_clock> now =
        std::chrono::system_clock::now();
 
    const std::time_t t_c = std::chrono::system_clock::to_time_t(now - 24h);
    std::cout << "24 hours ago, the time was "
              << std::put_time(std::localtime(&t_c), "%F %T.\n") << std::flush;
 
    const std::chrono::time_point<std::chrono::steady_clock> start =
        std::chrono::steady_clock::now();
 
    std::cout << "Different clocks are not comparable: \n"
                 "  System time: " << now.time_since_epoch() << "\n"
                 "  Steady time: " << start.time_since_epoch() << '\n';
 
    slow_motion();
 
    const auto end = std::chrono::steady_clock::now();
    std::cout
        << "Slow calculations took "
        << std::chrono::duration_cast<std::chrono::microseconds>(end - start) << " ≈ "
        << (end - start) / 1ms << "ms ≈ " // almost equivalent form of the above, but
        << (end - start) / 1s << "s.\n";  // using milliseconds and seconds accordingly
}

```

Possible output:

```
24 hours ago, the time was 2021-02-15 18:28:52.
Different clocks are not comparable:
  System time: 1666497022681282572ns
  Steady time: 413668317434475ns
Slow calculations took 2090448µs ≈ 2090ms ≈ 2s.

```

### See also

|  |  |
| --- | --- |
| duration(C++11) | a time interval   (class template) |
| year_month_day(C++20) | represents a specific year, month, and day   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/time_point&oldid=157577>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 August 2023, at 08:23.