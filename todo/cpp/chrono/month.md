# std::chrono::month

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | ****month****(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::month****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| month::month | | | | |
| month::operator++month::operator-- | | | | |
| month::operator+=month::operator-= | | | | |
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
| Defined in header `<chrono>` |  |  |
| class month; |  | (since C++20) |
| inline constexpr std::chrono::month January{1}; |  | (since C++20) |
| inline constexpr std::chrono::month February{2}; |  | (since C++20) |
| inline constexpr std::chrono::month March{3}; |  | (since C++20) |
| inline constexpr std::chrono::month April{4}; |  | (since C++20) |
| inline constexpr std::chrono::month May{5}; |  | (since C++20) |
| inline constexpr std::chrono::month June{6}; |  | (since C++20) |
| inline constexpr std::chrono::month July{7}; |  | (since C++20) |
| inline constexpr std::chrono::month August{8}; |  | (since C++20) |
| inline constexpr std::chrono::month September{9}; |  | (since C++20) |
| inline constexpr std::chrono::month October{10}; |  | (since C++20) |
| inline constexpr std::chrono::month November{11}; |  | (since C++20) |
| inline constexpr std::chrono::month December{12}; |  | (since C++20) |
|  |  |  |

The class `month` represents a month in a year. Its normal range is `[`1`,`12`]`, but it may hold any number in `[`​0​`,`255`]`. Twelve named constants are predefined in the `std::chrono` namespace for the twelve months of the year.

`month` is a TriviallyCopyable StandardLayoutType.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `month`   (public member function) |
| operator++operator++(int)operator--operator--(int) | increments or decrements the month   (public member function) |
| operator+=operator-= | adds or subtracts a number of months   (public member function) |
| operator unsigned | retrieves the stored month value   (public member function) |
| ok | checks if the stored month value is in the normal range   (public member function) |

### Nonmember functions

|  |  |
| --- | --- |
| operator==operator<=>(C++20) | compares two `month` values   (function) |
| operator+operator-(C++20) | performs arithmetic on `month`s   (function) |
| operator<<(C++20) | outputs a `month` into a stream   (function template) |
| from_stream(C++20) | parses a `month` from a stream according to the provided format   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::formatter<std::chrono::month>(C++20) | formatting support for `month`   (class template specialization) |
| std::hash<std::chrono::month>(C++26) | hash support for ****std::chrono::month****   (class template specialization) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/month&oldid=157851>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 September 2023, at 18:44.