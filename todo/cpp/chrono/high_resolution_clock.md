# std::chrono::high_resolution_clock

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | is_clock(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | ****high_resolution_clock****(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::high_resolution_clock****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| high_resolution_clock::now | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| class high_resolution_clock; |  | (since C++11) |
|  |  |  |

Class `std::chrono::high_resolution_clock` represents the clock with the smallest tick period provided by the implementation. It may be an alias of std::chrono::system_clock or std::chrono::steady_clock, or a third, independent clock.

`std::chrono::high_resolution_clock` meets the requirements of TrivialClock.

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `rep` | arithmetic type representing the number of ticks in the clock's duration |
| `period` | a std::ratio type representing the tick period of the clock, in seconds |
| `duration` | std::chrono::duration<rep, period> |
| `time_point` | std::chrono::time_point<std::chrono::high_resolution_clock> |

### Member constants

|  |  |
| --- | --- |
| constexpr bool is_steady[static] | true if the time between ticks is always constant, i.e. calls to now() return values that increase monotonically even in case of some external clock adjustment, otherwise false   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| now[static] | returns a std::chrono::time_point representing the current value of the clock   (public static member function) |

### Notes

There has been some controversy around the use of `high_resolution_clock`. Howard Hinnant, who claims to have introduced `high_resolution_clock` to the language, stated in 2016 on the ISO C++ Standard - Discussion mailing list that he was in favor of deprecating it. His rationale was that, because the standard allows for it to be an alias for std::chrono::steady_clock or std::chrono::system_clock, its use adds uncertainty to a program without benefit. However, other participants in the thread spoke out its favor, for instance on the basis that, because neither std::chrono::steady_clock nor std::chrono::system_clock come with any particular resolution guarantees, `high_resolution_clock` serves a useful role by giving the vendor an opportunity to supply the platform's highest-resolution clock, when neither its std::chrono::steady_clock nor its std::chrono::system_clock would be that.

It is often just an alias for std::chrono::steady_clock or std::chrono::system_clock, but which one it is depends on the library or configuration. When it is a `system_clock`, it is not monotonic (e.g., the time can go backwards). For example, as of 2023, libstdc++ has it aliased to `system_clock` "until higher-than-nanosecond definitions become feasible"[[1]](high_resolution_clock.html#cite_note-1), MSVC has it as `steady_clock`[[2]](high_resolution_clock.html#cite_note-2), and libc++ uses `steady_clock` when the C++ standard library implementation supports a monotonic clock and `system_clock` otherwise[[3]](high_resolution_clock.html#cite_note-3).

### See also

|  |  |
| --- | --- |
| system_clock(C++11) | wall clock time from the system-wide realtime clock   (class) |
| steady_clock(C++11) | monotonic clock that will never be adjusted   (class) |

### External links

|  |
| --- |
| 1. ↑ libstdc++ `<chrono.h>` 2. ↑ MSVC `high_resolution_clock` 3. ↑ libc++ `<high_resolution_clock.h>` |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/high_resolution_clock&oldid=178562>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 13:23.