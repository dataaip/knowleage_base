# std::strftime

From cppreference.com
< cpp‎ | chrono‎ | c
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

C-style date and time utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Time manipulation | | | | |
| difftime | | | | |
| time | | | | |
| clock | | | | |
| timespec_get(C++17) | | | | |
| Format conversions | | | | |
| asctime | | | | |
| ctime | | | | |
| ****strftime**** | | | | |
| wcsftime | | | | |
| gmtime | | | | |
| localtime | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| clock_t | | | | |
| timespec(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ctime>` |  |  |
| std::size_t strftime( char\* str, std::size_t count, const char\* format, const std::tm\* tp ); |  |  |
|  |  |  |

Converts the date and time information from a given calendar time tp to a null-terminated multibyte character string str according to format string format. Up to count bytes are written.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the first element of the char array for output |
| count | - | maximum number of bytes to write |
| format | - | pointer to a null-terminated multibyte character string specifying the format of conversion |
| tp | - | pointer to the object containing date and time information to be converted |

### Format string

The format string consists of zero or more conversion specifiers and ordinary characters (except `%`). All ordinary characters, including the terminating null character, are copied to the output string without modification. Each conversion specification begins with `%` character, optionally followed by `E` or `O` modifier (ignored if unsupported by the locale), followed by the character that determines the behavior of the specifier. The following format specifiers are available:

| Conversion  specifier | Explanation | Used fields |
| --- | --- | --- |
| `%` | writes literal `%`. The full conversion specification must be `%%`. |  |
| `n` (C++11) | writes newline character |  |
| `t` (C++11) | writes horizontal tab character |  |
| Year | | |
| `Y` | writes ****year**** as a decimal number, e.g. 2017 | `tm_year` |
| `EY` (C++11) | writes ****year**** in the alternative representation, e.g.平成23年 (year Heisei 23) instead of 2011年 (year 2011) in ja_JP locale | `tm_year` |
| `y` | writes last 2 digits of ****year**** as a decimal number (range `[00,99]`) | `tm_year` |
| `Oy` (C++11) | writes last 2 digits of ****year**** using the alternative numeric system, e.g. 十一 instead of 11 in ja_JP locale | `tm_year` |
| `Ey` (C++11) | writes ****year**** as offset from locale's alternative calendar period `%EC` (locale-dependent) | `tm_year` |
| `C` (C++11) | writes first 2 digits of ****year**** as a decimal number (range `[00,99]`) | `tm_year` |
| `EC` (C++11) | writes name of the ****base year (period)**** in the locale's alternative representation, e.g. 平成 (Heisei era) in ja_JP | `tm_year` |
| `G` (C++11) | writes ****ISO 8601 week-based year****, i.e. the year that contains the specified week. In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | `tm_year`, `tm_wday`, `tm_yday` |
| `g` (C++11) | writes last 2 digits of ****ISO 8601 week-based year****, i.e. the year that contains the specified week (range `[00,99]`). In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | `tm_year`, `tm_wday`, `tm_yday` |
| Month | | |
| `b` | writes ****abbreviated month**** name, e.g. `Oct` (locale dependent) | `tm_mon` |
| `h` (C++11) | synonym of `b` | `tm_mon` |
| `B` | writes ****full month**** name, e.g. `October` (locale dependent) | `tm_mon` |
| `m` | writes ****month**** as a decimal number (range `[01,12]`) | `tm_mon` |
| `Om` (C++11) | writes ****month**** using the alternative numeric system, e.g. 十二 instead of 12 in ja_JP locale | `tm_mon` |
| Week | | |
| `U` | writes ****week of the year**** as a decimal number (Sunday is the first day of the week) (range `[00,53]`) | `tm_year`, `tm_wday`, `tm_yday` |
| `OU` (C++11) | writes ****week of the year****, as by `%U`, using the alternative numeric system, e.g. 五十二 instead of 52 in ja_JP locale | `tm_year`, `tm_wday`, `tm_yday` |
| `W` | writes ****week of the year**** as a decimal number (Monday is the first day of the week) (range `[00,53]`) | `tm_year`, `tm_wday`, `tm_yday` |
| `OW` (C++11) | writes ****week of the year****, as by `%W`, using the alternative numeric system, e.g. 五十二 instead of 52 in ja_JP locale | `tm_year`, `tm_wday`, `tm_yday` |
| `V` (C++11) | writes ****ISO 8601 week of the year**** (range `[01,53]`). In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | `tm_year`, `tm_wday`, `tm_yday` |
| `OV` (C++11) | writes ****week of the year****, as by `%V`, using the alternative numeric system, e.g. 五十二 instead of 52 in ja_JP locale | `tm_year`, `tm_wday`, `tm_yday` |
| Day of the year/month | | |
| `j` | writes ****day of the year**** as a decimal number (range `[001,366]`) | `tm_yday` |
| `d` | writes ****day of the month**** as a decimal number (range `[01,31]`) | `tm_mday` |
| `Od` (C++11) | writes zero-based ****day of the month**** using the alternative numeric system, e.g. 二十七 instead of 27 in ja_JP locale Single character is preceded by a space. | `tm_mday` |
| `e` (C++11) | writes ****day of the month**** as a decimal number (range `[1,31]`). Single digit is preceded by a space. | `tm_mday` |
| `Oe` (C++11) | writes one-based ****day of the month**** using the alternative numeric system, e.g. 二十七 instead of 27 in ja_JP locale Single character is preceded by a space. | `tm_mday` |
| Day of the week | | |
| `a` | writes ****abbreviated weekday**** name, e.g. `Fri` (locale dependent) | `tm_wday` |
| `A` | writes ****full weekday**** name, e.g. `Friday` (locale dependent) | `tm_wday` |
| `w` | writes ****weekday**** as a decimal number, where Sunday is `0` (range `[0-6]`) | `tm_wday` |
| `Ow` (C++11) | writes ****weekday****, where Sunday is `0`, using the alternative numeric system, e.g. 二 instead of 2 in ja_JP locale | `tm_wday` |
| `u` (C++11) | writes ****weekday**** as a decimal number, where Monday is `1` (ISO 8601 format) (range `[1-7]`) | `tm_wday` |
| `Ou` (C++11) | writes ****weekday****, where Monday is `1`, using the alternative numeric system, e.g. 二 instead of 2 in ja_JP locale | `tm_wday` |
| Hour, minute, second | | |
| `H` | writes ****hour**** as a decimal number, 24 hour clock (range `[00-23]`) | `tm_hour` |
| `OH` (C++11) | writes ****hour**** from 24-hour clock using the alternative numeric system, e.g. 十八 instead of 18 in ja_JP locale | `tm_hour` |
| `I` | writes ****hour**** as a decimal number, 12 hour clock (range `[01,12]`) | `tm_hour` |
| `OI` (C++11) | writes ****hour**** from 12-hour clock using the alternative numeric system, e.g. 六 instead of 06 in ja_JP locale | `tm_hour` |
| `M` | writes ****minute**** as a decimal number (range `[00,59]`) | `tm_min` |
| `OM` (C++11) | writes ****minute**** using the alternative numeric system, e.g. 二十五 instead of 25 in ja_JP locale | `tm_min` |
| `S` | writes ****second**** as a decimal number (range `[00,60]`) | `tm_sec` |
| `OS` (C++11) | writes ****second**** using the alternative numeric system, e.g. 二十四 instead of 24 in ja_JP locale | `tm_sec` |
| Other | | |
| `c` | writes ****standard date and time string****, e.g. `Sun Oct 17 04:41:13 2010` (locale dependent) | all |
| `Ec` (C++11) | writes ****alternative date and time string****, e.g. using 平成23年 (year Heisei 23) instead of 2011年 (year 2011) in ja_JP locale | all |
| `x` | writes localized ****date representation**** (locale dependent) | all |
| `Ex` (C++11) | writes ****alternative date representation****, e.g. using 平成23年 (year Heisei 23) instead of 2011年 (year 2011) in ja_JP locale | all |
| `X` | writes localized ****time representation****, e.g. 18:40:20 or 6:40:20 PM (locale dependent) | all |
| `EX` (C++11) | writes ****alternative time representation**** (locale dependent) | all |
| `D` (C++11) | equivalent to ****"%m/%d/%y"**** | `tm_mon`, `tm_mday`, `tm_year` |
| `F` (C++11) | equivalent to ****"%Y-%m-%d"**** (the ISO 8601 date format) | `tm_mon`, `tm_mday`, `tm_year` |
| `r` (C++11) | writes localized ****12-hour clock**** time (locale dependent) | `tm_hour`, `tm_min`, `tm_sec` |
| `R` (C++11) | equivalent to ****"%H:%M"**** | `tm_hour`, `tm_min` |
| `T` (C++11) | equivalent to ****"%H:%M:%S"**** (the ISO 8601 time format) | `tm_hour`, `tm_min`, `tm_sec` |
| `p` | writes localized ****a.m. or p.m.**** (locale dependent) | `tm_hour` |
| `z` (C++11) | writes ****offset from UTC**** in the ISO 8601 format (e.g. `-0430`), or no characters if the time zone information is not available | `tm_isdst` |
| `Z` | writes locale-dependent ****time zone name or abbreviation****, or no characters if the time zone information is not available | `tm_isdst` |

### Return value

The number of bytes written into the character array pointed to by str not including the terminating '\0' on success. If count was reached before the entire string could be stored, ​0​ is returned and the contents are indeterminate.

### Example

Run this code

```
#include <ctime>
#include <iostream>
#include <iterator>
#include <locale>
 
void utcExample()
{
    // Example of the very popular RFC 3339 format UTC time
    std::time_t time = std::time({});
    char timeString[std::size("yyyy-mm-ddThh:mm:ssZ")];
    std::strftime(std::data(timeString), std::size(timeString),
                  "%FT%TZ", std::gmtime(&time));
    std::cout << timeString << '\n';
}
 
int main()
{
    std::time_t t = std::time(nullptr);
    char mbstr[100];
 
    if (std::strftime(mbstr, sizeof(mbstr), "%A %c", std::localtime(&t)))
        std::cout << mbstr << '\n';
 
    std::locale::global(std::locale("ja_JP.utf8"));
    if (std::strftime(mbstr, sizeof(mbstr), "%A %c", std::localtime(&t)))
        std::cout << mbstr << '\n';
 
    utcExample();
}

```

Possible output:

```
Tuesday Tue Sep  7 19:40:35 2021
火曜日 2021年09月07日 19時40分35秒
2021-09-07T19:40:35Z

```

### See also

|  |  |
| --- | --- |
| asctime | converts a std::tm object to a textual representation   (function) |
| ctime | converts a std::time_t object to a textual representation   (function) |
| wcsftime | converts a std::tm object to custom wide string textual representation   (function) |
| put_time(C++11) | formats and outputs a date/time value according to the specified format   (function template) |
| std::formatter<std::chrono::hh_mm_ss>(C++20) | formatting support for `hh_mm_ss`   (class template specialization) |
| C documentation for strftime | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/c/strftime&oldid=161518>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 October 2023, at 00:53.