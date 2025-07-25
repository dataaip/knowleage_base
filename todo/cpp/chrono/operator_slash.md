# std::chrono::operator/(calendar)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | ****operator/****(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| `year_month` |  |  |
| constexpr auto operator/( const std::chrono::year& y,  const std::chrono::month& m ) noexcept -> std::chrono::year_month; | (1) | (since C++20) |
| constexpr auto operator/( const std::chrono::year& y, int m ) noexcept      -> std::chrono::year_month; | (2) | (since C++20) |
| `month_day` |  |  |
| constexpr auto operator/( const std::chrono::month& m,  const std::chrono::day& d ) noexcept -> std::chrono::month_day; | (3) | (since C++20) |
| constexpr auto operator/( const std::chrono::month& m, int d ) noexcept      -> std::chrono::month_day; | (4) | (since C++20) |
| constexpr auto operator/( int m, const std::chrono::day& d ) noexcept      -> std::chrono::month_day; | (5) | (since C++20) |
| constexpr auto operator/( const std::chrono::day& d,  const std::chrono::month& m ) noexcept -> std::chrono::month_day; | (6) | (since C++20) |
| constexpr auto operator/( const std::chrono::day& d, int m ) noexcept      -> std::chrono::month_day; | (7) | (since C++20) |
| `month_day_last` |  |  |
| constexpr auto operator/( const std::chrono::month& m,  std::chrono::last_spec ) noexcept -> std::chrono::month_day_last; | (8) | (since C++20) |
| constexpr auto operator/( int m, std::chrono::last_spec ) noexcept      -> std::chrono::month_day_last; | (9) | (since C++20) |
| constexpr auto operator/( std::chrono::last_spec,  const std::chrono::month& m ) noexcept -> std::chrono::month_day_last; | (10) | (since C++20) |
| constexpr auto operator/( std::chrono::last_spec, int m ) noexcept      -> std::chrono::month_day_last; | (11) | (since C++20) |
| `month_weekday` |  |  |
| constexpr auto operator/( const std::chrono::month& m,  const std::chrono::weekday_indexed& wdi ) noexcept -> std::chrono::month_weekday; | (12) | (since C++20) |
| constexpr auto operator/( int m, const std::chrono::weekday_indexed& wdi ) noexcept      -> std::chrono::month_weekday; | (13) | (since C++20) |
| constexpr auto operator/( const std::chrono::weekday_indexed& wdi,  const std::chrono::month& m ) noexcept -> std::chrono::month_weekday; | (14) | (since C++20) |
| constexpr auto operator/( const std::chrono::weekday_indexed& wdi, int m ) noexcept      -> std::chrono::month_weekday; | (15) | (since C++20) |
| `month_weekday_last` |  |  |
| constexpr auto operator/( const std::chrono::month& m,  const std::chrono::weekday_last& wdl ) noexcept -> std::chrono::month_weekday_last; | (16) | (since C++20) |
| constexpr auto operator/( int m, const std::chrono::weekday_last& wdl ) noexcept      -> std::chrono::month_weekday_last; | (17) | (since C++20) |
| constexpr auto operator/( const std::chrono::weekday_last& wdl,  const std::chrono::month& m ) noexcept -> std::chrono::month_weekday_last; | (18) | (since C++20) |
| constexpr auto operator/( const std::chrono::weekday_last& wdl, int m ) noexcept      -> std::chrono::month_weekday_last; | (19) | (since C++20) |
| `year_month_day` |  |  |
| constexpr auto operator/( const std::chrono::year_month& ym,  const std::chrono::day& d ) noexcept -> std::chrono::year_month_day; | (20) | (since C++20) |
| constexpr auto operator/( const std::chrono::year_month& ym, int d ) noexcept      -> std::chrono::year_month_day; | (21) | (since C++20) |
| constexpr auto operator/( const std::chrono::year& y,  const std::chrono::month_day& md ) noexcept -> std::chrono::year_month_day; | (22) | (since C++20) |
| constexpr auto operator/( int y, const std::chrono::month_day& md ) noexcept      -> std::chrono::year_month_day; | (23) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_day& md,  const std::chrono::year& y ) noexcept -> std::chrono::year_month_day; | (24) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_day& md, int y ) noexcept      -> std::chrono::year_month_day; | (25) | (since C++20) |
| `year_month_day_last` |  |  |
| constexpr auto operator/( const std::chrono::year_month& ym,  std::chrono::last_spec ) noexcept -> std::chrono::year_month_day_last; | (26) | (since C++20) |
| constexpr auto operator/( const std::chrono::year& y,  const std::chrono::month_day_last& mdl ) noexcept -> std::chrono::year_month_day_last; | (27) | (since C++20) |
| constexpr auto operator/( int y, const std::chrono::month_day_last& mdl ) noexcept      -> std::chrono::year_month_day_last; | (28) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_day_last& mdl,  const std::chrono::year& y ) noexcept -> std::chrono::year_month_day_last; | (29) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_day_last& mdl, int y ) noexcept      -> std::chrono::year_month_day_last; | (30) | (since C++20) |
| `year_month_weekday` |  |  |
| constexpr auto operator/( const std::chrono::year_month& ym,  const std::chrono::weekday_indexed& wdi ) noexcept -> std::chrono::year_month_weekday; | (31) | (since C++20) |
| constexpr auto operator/( const std::chrono::year& y,  const std::chrono::month_weekday& mwd ) noexcept -> std::chrono::year_month_weekday; | (32) | (since C++20) |
| constexpr auto operator/( int y, const std::chrono::month_weekday& mwd ) noexcept      -> std::chrono::year_month_weekday; | (33) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_weekday& mwd,  const std::chrono::year& y ) noexcept -> std::chrono::year_month_weekday; | (34) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_weekday& mwd, int y ) noexcept      -> std::chrono::year_month_weekday; | (35) | (since C++20) |
| `year_month_weekday_last` |  |  |
| constexpr auto operator/( const std::chrono::year_month& ym,  const std::chrono::weekday_last& wdl ) noexcept -> std::chrono::year_month_weekday_last; | (36) | (since C++20) |
| constexpr auto operator/( const std::chrono::year& y,  const std::chrono::month_weekday_last& mwdl ) noexcept -> std::chrono::year_month_weekday_last; | (37) | (since C++20) |
| constexpr auto operator/( int y, const std::chrono::month_weekday_last& mwdl ) noexcept      -> std::chrono::year_month_weekday_last; | (38) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_weekday_last& mwdl,  const std::chrono::year& y ) noexcept -> std::chrono::year_month_weekday_last; | (39) | (since C++20) |
| constexpr auto operator/( const std::chrono::month_weekday_last& mwdl, int y ) noexcept      -> std::chrono::year_month_weekday_last; | (40) | (since C++20) |
|  |  |  |

These operator/ overloads provide a conventional syntax for the creation of Proleptic Gregorian calendar dates.

For creation of a full date, any of the following three orders are accepted:

- `year/month/day`,
- `month/day/year`,
- `day/month/year`.

In each case `day` can replaced with one of:

- std::chrono::last, for the last day of the month;
- `weekday[i]`, for the `i`th **weekday** of the month;
- `weekday[std::chrono::last]`, for the last **weekday** of the month.

A plain integer is accepted if its meaning is unambiguous from the types of other operands: 2005y/4/5 is allowed, but 5/April/2005 is not.

Partial-date types (`year_month`, `month_day`, etc.) can be created by not applying the second operator/ in any of the three orders.

### Return value

1) std::chrono::year_month(y, m)2) std::chrono::year_month(y, std::chrono::month(m))3,6) std::chrono::month_day(m, d)4) std::chrono::month_day(m, std::chrono::day(d))5,7) std::chrono::month_day(std::chrono::month(m), d)8,10) std::chrono::month_day_last(m)9,11) std::chrono::month_day_last(std::chrono::month(m))12,14) std::chrono::month_weekday(m, wdi)13,15) std::chrono::month_weekday(std::chrono::month(m), wdi)16,18) std::chrono::month_weekday_last(m, wdl)17,19) std::chrono::month_weekday_last(std::chrono::month(m), wdl)20) std::chrono::year_month_day(ym.year(), ym.month(), d)21) std::chrono::year_month_day(ym.year(), ym.month(), std::chrono::day(d))22,24) std::chrono::year_month_day(y, md.month(), md.day())23,25) std::chrono::year_month_day(std::chrono::year(y), md.month(), md.day())26) std::chrono::year_month_day_last(ym.year(), std::chrono::month_day_last(ym.month()))27,29) std::chrono::year_month_day_last(y, mdl)28,30) std::chrono::year_month_day_last(std::chrono::year(y), mdl)31) std::chrono::year_month_weekday(ym.year(), ym.month(), wdi)32,34) std::chrono::year_month_weekday(y, mwd.month(), mwd.weekday_indexed())33,35) std::chrono::year_month_weekday(std::chrono::year(y), mwd.month(), mwd.weekday_indexed())36) std::chrono::year_month_weekday_last(ym.year(), ym.month(), wdl)37,39) std::chrono::year_month_weekday_last(y, mwdl.month(), mwdl.weekday_last())38,40) std::chrono::year_month_weekday_last(std::chrono::year(y), mwdl.month(), mwdl.weekday_last())

### Example

Run this code

```
#include <chrono>
using namespace std::chrono;
 
constexpr auto ym{2021y/8};
static_assert(ym == year_month(year(2021), August));
 
constexpr auto md{9/15d};
static_assert(md == month_day(September, day(15)));
 
constexpr auto mdl{October/last};
static_assert(mdl == month_day_last(month(10)));
 
constexpr auto mw{11/Monday[3]};
static_assert(mw == month_weekday(November, Monday[3]));
 
constexpr auto mwdl{December/Sunday[last]};
static_assert(mwdl == month_weekday_last(month(12), weekday_last(Sunday)));
 
// Those 3 year/month/day orders that people actually use on this planet and beyond:
constexpr auto ymd{year(2021)/January/day(23)};
static_assert(ymd == month{1}/23/2021);
static_assert(ymd == day{23}/1/2021);
static_assert(ymd == year_month_day(2021y, month(January), 23d));
 
int main() {}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/operator_slash&oldid=157232>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 August 2023, at 10:29.