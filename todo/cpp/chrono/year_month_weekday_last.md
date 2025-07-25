# std::chrono::year_month_weekday_last

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | ****year_month_weekday_last****(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

****std::chrono::year_month_weekday_last****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month_weekday_last::year_month_weekday_last | | | | |
| year_month_weekday_last::operator+=year_month_weekday_last::operator-= | | | | |
| year_month_weekday_last::yearyear_month_weekday_last::monthyear_month_weekday_last::weekdayyear_month_weekday_last::weekday_last | | | | |
| year_month_weekday_last::operator sys_daysyear_month_weekday_last::operator local_days | | | | |
| year_month_weekday_last::ok | | | | |
| Nonmember functions | | | | |
| operator== | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_weekday_last> | | | | |
| hash<std::chrono::year_month_weekday_last>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| class year_month_weekday_last; |  | (since C++20) |
|  |  |  |

The class `year_month_weekday_last` represents the last weekday of a specific year and month. It is a field-based time point, with a resolution of std::chrono::days, except that it is limited to pointing to the last weekday of a year and month. std::chrono::years- and std::chrono::months-oriented arithmetic are supported directly. An implicit conversion to std::chrono::sys_days allows std::chrono::days-oriented arithmetic to be performed efficiently.

`year_month_weekday_last` is a TriviallyCopyable StandardLayoutType.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `year_month_weekday_last`   (public member function) |
| operator+=operator-= | modifies the time point by some number of months or years   (public member function) |
| yearmonthweekdayweekday_last | accesses the fields of this object   (public member function) |
| operator sys_daysoperator local_days | converts to a std::chrono::time_point   (public member function) |
| ok | checks whether this object represents a valid date   (public member function) |

### Nonmember functions

|  |  |
| --- | --- |
| operator==(C++20) | compares two `year_month_weekday_last` values   (function) |
| operator+operator-(C++20) | adds or subtracts a `year_month_weekday_last` and some number of years or months   (function) |
| operator<<(C++20) | outputs a `year_month_weekday_last` into a stream   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::formatter<std::chrono::year_month_weekday_last>(C++20) | formatting support for `year_month_weekday_last`   (class template specialization) |
| std::hash<std::chrono::year_month_weekday_last>(C++26) | hash support for ****std::chrono::year_month_weekday_last****   (class template specialization) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_weekday_last&oldid=157933>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2023, at 05:52.