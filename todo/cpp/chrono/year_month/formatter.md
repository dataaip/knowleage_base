# std::formatter<std::chrono::year_month>

From cppreference.com
< cpp‎ | chrono‎ | year month
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

std::chrono::year_month

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| year_month::year_month | | | | |
| year_month::yearyear_month::month | | | | |
| year_month::operator+=year_month::operator-= | | | | |
| year_month::ok | | | | |
| Nonmember functions | | | | |
| operator==operator<=> | | | | |
| operator+operator- | | | | |
| operator<< | | | | |
| from_stream | | | | |
| Helper classes | | | | |
| ****formatter<std::chrono::year_month>**** | | | | |
| hash<std::chrono::year_month>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class CharT >  struct formatter<std::chrono::year_month, CharT>; |  | (since C++20) |
|  |  |  |

Specialization of std::formatter that defines formatting rules for std::chrono::year_month.

The std::formatter specialization is usually not directly accessed, but is used through formatting functions.

### Format specification

The format specification has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| fill-and-align ﻿(optional) width ﻿(optional) precision ﻿(optional) `L`(optional) chrono-spec ﻿(optional) |  |  |
|  | | | | | | | | | |

fill-and-align, width, and precision have the same meaning as in standard format specification. precision is valid only for std::chrono::duration types where the representation type `Rep` is a floating-point type, otherwise std::format_error is thrown.

The locale used for formatting is determined as follows:

- the default "C" locale if `L` is not present in the format specification,
- otherwise, the locale denoted by the std::locale passed to the formatting function, if any,
- otherwise (`L` is present but no std::locale is passed to the formatting function), the global locale.

If the (ordinary or wide) string literal encoding is a Unicode encoding form and the locale is among an implementation-defined set of locales, each replacement that depends on the locale is performed as if the replacement character sequence is converted to the literal encoding.

The chrono-spec consists of one or more conversion specifiers and ordinary characters (other than `{`, `}`, and `%`). A chrono-spec must start with a conversion specifier. All ordinary characters are written to the output without modification. Each unmodified conversion specifier begins with a `%` character followed by a character that determines the behavior of the specifier. Some conversion specifiers have a modified form in which an `E` or `O` modifier character is inserted after the `%` character. Each conversion specifier is replaced by appropriate characters in the output as described below.

If the chrono-spec is empty, the chrono object is formatted as if by streaming it to an object `os` of type std::basic_ostringstream<CharT> with the formatting locale (one of std::locale::classic(), the passed std::locale object, and std::locale::global()) imbued and copying os.str() to the output buffer with additional padding and adjustments as per format specifiers.

The following format specifiers are available:

| Conversion  specifier | Explanation |
| --- | --- |
| `%%` | Writes a literal `%` character. |
| `%n` | Writes a newline character. |
| `%t` | Writes a horizontal tab character. |
| Year | | |
| `%C`   `%EC` | Writes the year divided by 100 using floored division. If the result is a single decimal digit, it is prefixed with 0. The modified command `%EC` writes the locale's alternative representation of the century. |
| `%y`   `%Oy`   `%Ey` | Writes the last two decimal digits of the year. If the result is a single digit it is prefixed by 0. The modified command `%Oy` writes the locale's alternative representation.  The modified command `%Ey` writes the locale's alternative representation of offset from `%EC` (year only). |
| `%Y`   `%EY` | Writes the year as a decimal number. If the result is less than four digits it is left-padded with 0 to four digits. The modified command `%EY` writes the locale's alternative full year representation. |
| Month | | |
| `%b` `%h` | Writes the locale's abbreviated month name. |
| `%B` | Writes the locale's full month name. |
| `%m` `%Om` | Writes the month as a decimal number (January is `01`). If the result is a single digit, it is prefixed with 0. The modified command `%Om` writes the locale's alternative representation. |

The following specifiers are recognized, but will cause std::format_error to be thrown:

| Conversion  specifier | Explanation |
| --- | --- |
| Day | | |
| `%d` `%Od` | Writes the day of month as a decimal number. If the result is a single decimal digit, it is prefixed with 0. The modified command `%Od` writes the locale's alternative representation. |
| `%e` `%Oe` | Writes the day of month as a decimal number. If the result is a single decimal digit, it is prefixed with a space. The modified command `%Oe` writes the locale's alternative representation. |
| Day of the week | | |
| `%a` | Writes the locale's abbreviated weekday name. |
| `%A` | Writes the locale's full weekday name. |
| `%u` `%Ou` | Writes the ISO weekday as a decimal number (1-7), where Monday is `1`. The modified command `%Ou` writes the locale's alternative representation. |
| `%w` `%Ow` | Writes the weekday as a decimal number (0-6), where Sunday is `0`. The modified command `%Ow` writes the locale's alternative representation. |
| ISO 8601 week-based year | | |
| In ISO 8601 weeks begin with Monday and the first week of the year must satisfy the following requirements:   - Includes January 4 - Includes first Thursday of the year | | |
| `%g` | Writes the last two decimal digits of the ISO 8601 week-based year. If the result is a single digit it is prefixed by 0. |
| `%G` | Writes the ISO 8601 week-based year as a decimal number. If the result is less than four digits it is left-padded with 0 to four digits. |
| `%V` `%OV` | Writes the ISO 8601 week of the year as a decimal number. If the result is a single digit, it is prefixed with 0. The modified command `%OV` writes the locale's alternative representation. |
| Week/day of the year | | |
| `%j` | Writes the day of the year as a decimal number (January 1 is `001`). If the result is less than three digits, it is left-padded with 0 to three digits. |
| `%U` `%OU` | Writes the week number of the year as a decimal number. The first Sunday of the year is the first day of week 01. Days of the same year prior to that are in week 00. If the result is a single digit, it is prefixed with 0. The modified command `%OU` writes the locale's alternative representation. |
| `%W` `%OW` | Writes the week number of the year as a decimal number. The first Monday of the year is the first day of week 01. Days of the same year prior to that are in week 00. If the result is a single digit, it is prefixed with 0. The modified command `%OW` writes the locale's alternative representation. |
| Date | | |
| `%D` | Equivalent to `"%m/%d/%y"`. |
| `%F` | Equivalent to `"%Y-%m-%d"`. |
| `%x` `%Ex` | Writes the locale's date representation. The modified command `%Ex` produces the locale's alternate date representation. |
| Time of day | | |
| `%H` `%OH` | Writes the hour (24-hour clock) as a decimal number. If the result is a single digit, it is prefixed with 0. The modified command `%OH` writes the locale's alternative representation. |
| `%I` `%OI` | Writes the hour (12-hour clock) as a decimal number. If the result is a single digit, it is prefixed with 0. The modified command `%OI` writes the locale's alternative representation. |
| `%M` `%OM` | Writes the minute as a decimal number. If the result is a single digit, it is prefixed with 0. The modified command `%OM` writes the locale's alternative representation. |
| `%S` `%OS` | Writes the second as a decimal number. If the number of seconds is less than 10, the result is prefixed with 0. If the precision of the input cannot be exactly represented with seconds, then the format is a decimal floating-point number with a fixed format and a precision matching that of the precision of the input (or to a microseconds precision if the conversion to floating-point decimal seconds cannot be made within 18 fractional digits). The character for the decimal point is localized according to the locale.  The modified command `%OS` writes the locale's alternative representation. |
| `%p` | Writes the locale's equivalent of the AM/PM designations associated with a 12-hour clock. |
| `%R` | Equivalent to `"%H:%M"`. |
| `%T` | Equivalent to `"%H:%M:%S"`. |
| `%r` | Writes the locale's 12-hour clock time. |
| `%X` `%EX` | Writes the locale's time representation. The modified command `%EX` writes the locale's alternate time representation. |
| Duration count | | |
| `%Q` | Writes the count of ticks of the duration, i.e. the value obtained via count(). |
| `%q` | Writes the unit suffix of the duration, as specified in operator<<(). |
| Time zone | | |
| `%z` `%Ez` `%Oz` | Writes the offset from UTC in the ISO 8601 format. For example `-0430` refers to 4 hours 30 minutes behind UTC. If the offset is zero, `+0000` is used. The modified commands `%Ez` and `%Oz` insert a `:` between the hours and minutes (e.g., `-04:30`). |
| `%Z` | Writes the time zone abbreviation. |
| Miscellaneous | | |
| `%c` `%Ec` | Writes the locale's date and time representation. The modified command `%Ec` writes the locale's alternative date and time representation. |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2372R3 | C++20 | `formatter` used the global locale or passed locale | default "C" locale is used when `L` is absent |

### See also

|  |  |
| --- | --- |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/year_month/formatter&oldid=161689>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 October 2023, at 05:43.