# std::literals::chrono_literals::operator""us

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

std::chrono::duration

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration::duration | | | | | | duration::operator= | | | | | | duration::count | | | | | | duration::zero | | | | | | duration::min | | | | | | duration::max | | | | | | duration::operator+duration::operator- | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration::operator++duration::operator-- | | | | | | duration::operator+=duration::operator-=duration::operator\*=duration::operator/=duration::operator%= | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator-operator\*operator/operator% | | | | | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(C++20) | | | | | | operator<<(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | duration_cast | | | | | | floor(C++17) | | | | | | ceil(C++17) | | | | | | round(C++17) | | | | | | abs(C++17) | | | | | | operator""h(C++14) | | | | | | operator""min(C++14) | | | | | | operator""s(C++14) | | | | | | operator""ms(C++14) | | | | | | ****operator""us****(C++14) | | | | | | operator""ns(C++14) | | | | | | from_stream(C++20) | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_type | | | | | | treat_as_floating_point | | | | | | duration_values | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::chrono::duration>(C++20) | | | | | | hash<std::chrono::duration>(C++26) | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| constexpr std::chrono::microseconds      operator""us( unsigned long long us ); | (1) | (since C++14) |
| constexpr std::chrono::duration</\*unspecified\*/, std::micro>      operator""us( long double us ); | (2) | (since C++14) |
|  |  |  |

Forms a std::chrono::duration literal representing microseconds.

1) Integer literal, returns exactly std::chrono::microseconds(us).2) Floating-point literal, returns a floating-point duration equivalent to std::chrono::microseconds.

### Parameters

|  |  |  |
| --- | --- | --- |
| us | - | the number of microseconds |

### Return value

The std::chrono::duration literal.

### Possible implementation

|  |
| --- |
| ```text constexpr std::chrono::microseconds operator""us(unsigned long long us) {     return std::chrono::microseconds(us); } constexpr std::chrono::duration<long double, std::micro> operator""us(long double us) {     return std::chrono::duration<long double, std::micro>(us); } ``` |

### Notes

This operator is declared in the namespace std::literals::chrono_literals, where both literals and chrono_literals are inline namespaces. Access to this operator can be gained with:

- using namespace std::literals,
- using namespace std::chrono_literals, or
- using namespace std::literals::chrono_literals.

In addition, within the namespace std::chrono, the directive using namespace literals::chrono_literals; is provided by the standard library, so that if a programmer uses using namespace std::chrono; to gain access to the classes in the chrono library, the corresponding literal operators become visible as well.

### Example

Run this code

```
#include <chrono>
#include <iostream>
 
int main()
{
    using namespace std::chrono_literals;
    auto d1 = 250us;
    std::chrono::microseconds d2 = 1ms;
    std::cout << d1 << " = " << d1.count() << " microseconds\n"
              << 1ms << " = " << d2.count() << " microseconds\n";
}

```

Output:

```
250us = 250 microseconds
1ms = 1000 microseconds

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs new duration   (public member function of `std::chrono::duration<Rep,Period>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/operator%22%22us&oldid=157229>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 August 2023, at 10:21.