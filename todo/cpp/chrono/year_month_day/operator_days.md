# std::chrono::year_month_day::operator sys_days, std::chrono::year_month_day::operator local_days

From cppreference.com
< cpp‎ | chrono‎ | year month day
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

std::chrono::year_month_day

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month_day::year_month_day | | | | |
| year_month_day::operator+=year_month_day::operator-= | | | | |
| year_month_day::yearyear_month_day::monthyear_month_day::day | | | | |
| ****year_month_day::operator sys_daysyear_month_day::operator local_days**** | | | | |
| year_month_day::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| formatter<std::chrono::year_month_day> | | | | |
| hash<std::chrono::year_month_day>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr operator std::chrono::sys_days() const noexcept; | (1) | (since C++20) |
| constexpr explicit operator std::chrono::local_days() const noexcept; | (2) | (since C++20) |
|  |  |  |

Converts \*this to a std::chrono::time_point representing the same date as this `year_month_day`.

1) If ok() is true, the return value holds a count of days from the std::chrono::system_clock epoch (1970-01-01) to \*this. The result is negative if \*this represent a date prior to it. Otherwise, if the stored year and month are valid (year().ok() && month().ok() is true), then the returned value is sys_days(year()/month()/1d) + (day() - 1d). Otherwise (if year().ok() && month().ok() is false), the return value is unspecified. A std::chrono::sys_days in the range [std::chrono::days{-12687428}, std::chrono::days{11248737}], when converted to `year_month_day` and back, yields the same value.2) Same as (1) but returns local_days instead. Equivalent to return local_days(sys_days(\*this).time_since_epoch());.

### Notes

Converting to std::chrono::sys_days and back can be used to normalize a `year_month_day` that contains an invalid day but a valid year and month:

```
using namespace std::chrono;
auto ymd = 2017y/January/0;
ymd = sys_days{ymd};
// ymd is now 2016y/December/31

```

Normalizing the year and month can be done by adding (or subtracting) zero std::chrono::months:

```
using namespace std::chrono;
constexpr year_month_day normalize(year_month_day ymd)
{
    ymd += months{0}; // normalizes year and month
    return sys_days{ymd}; // normalizes day
}
static_assert(normalize(2017y/33/59) == 2019y/10/29);

```

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    using namespace std::chrono;
    const auto today = sys_days{std::chrono::floor<days>(system_clock::now())};
    for (const year_month_day ymd : {{November/15/2020}, {November/15/2120}, today})
    {
        std::cout << ymd;
        const auto delta = (sys_days{ymd} - today).count();
        (delta < 0) ? std::cout << " was " << -delta << " day(s) ago\n" :
        (delta > 0) ? std::cout << " is " << delta << " day(s) from now\n"
                    : std::cout << " is today!\n";
    }
}

```

Possible output:

```
2020-11-15 was 1014 day(s) ago
2120-11-15 is 35510 day(s) from now
2023-08-26 is today!

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month_day/operator_days&oldid=157368>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 August 2023, at 05:18.