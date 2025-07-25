# std::chrono::operator<<(std::chrono::year)

From cppreference.com
< cpp‎ | chrono‎ | year
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

std::chrono::year

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year::year | | | | |
| year::operator++year::operator-- | | | | |
| year::operator+=year::operator-= | | | | |
| year::operator+year::operator- | | | | |
| year::is_leap | | | | |
| year::operator int | | | | |
| year::ok | | | | |
| year::min | | | | |
| year::max | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| operator+operator- | | | | |
| ****operator<<**** | | | | |
| from_stream | | | | |
| operator""y | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year> | | | | |
| hash<std::chrono::year>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class CharT, class Traits >  std::basic_ostream<CharT, Traits>&     operator<<( std::basic_ostream<CharT, Traits>& os, const std::chrono::year& y ); |  | (since C++20) |
|  |  |  |

Forms a std::basic_string<CharT> s consisting of the year value stored in y formatted as a decimal number, left-padded with ​0​ to four digits if the result would otherwise be less than four digits. Then, if !y.ok(), append " is not a valid year" to the formatted string. Inserts that string into os.

Equivalent to

return os << (y.ok() ?  
    std::format(STATICALLY_WIDEN<CharT>("{:%Y}"), y) :  
    std::format(STATICALLY_WIDEN<CharT>("{:%Y} is not a valid year"), y));

where STATICALLY_WIDEN<CharT>("...") is "..." if `CharT` is `char`, and L"..." if `CharT` is `wchar_t`.

### Return value

os

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    constexpr std::chrono::year y1{2020}, y2{-020}, y3{98304};
    std::cout << y1 << '\n'
              << y2 << '\n'
              << y3 << '\n';
}

```

Possible output:

```
2020
-0016
-32768 is not a valid year

```

### See also

|  |  |
| --- | --- |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |
| std::formatter<std::chrono::year>(C++20) | formatting support for `year`   (class template specialization) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year/operator_ltlt&oldid=161685>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 October 2023, at 05:32.