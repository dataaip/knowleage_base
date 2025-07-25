# std::chrono::day

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****day****(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::day****

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
| operator""d | | | | |
| Helper classes | | | | |
| formatter<std::chrono::day> | | | | |
| hash<std::chrono::day>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| class day; |  | (since C++20) |
|  |  |  |

The class `day` represents a day in a month. Its normal range is `[`1`,`31`]`, but it may hold any number in `[`​0​`,`255`]`.

`day` is a TriviallyCopyable StandardLayoutType.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `day`   (public member function) |
| operator++operator++(int)operator--operator--(int) | increments or decrements the day   (public member function) |
| operator+=operator-= | adds or subtracts a number of days   (public member function) |
| operator unsigned | retrieves the stored day value   (public member function) |
| ok | checks if the stored day value is in the normal range   (public member function) |

### Nonmember functions

|  |  |
| --- | --- |
| operator==operator<=>(C++20) | compares two `day` values   (function) |
| operator+operator-(C++20) | adds or subtracts a number of days and a `day`, or find the difference between two `day`s   (function) |
| operator<<(C++20) | outputs a `day` into a stream   (function template) |
| from_stream(C++20) | parses a `day` from a stream according to the provided format   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::formatter<std::chrono::day>(C++20) | formatting support for `day`   (class template specialization) |
| std::hash<std::chrono::day>(C++26) | hash support for ****std::chrono::day****   (class template specialization) |

### Literals

|  |  |
| --- | --- |
| Defined in inline namespace `std::literals::chrono_literals` | |
| operator""d(C++20) | a std::chrono::day literal representing a day of a month   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/day&oldid=157848>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 September 2023, at 18:28.