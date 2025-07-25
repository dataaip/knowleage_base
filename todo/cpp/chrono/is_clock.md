# std::chrono::is_clock

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | system_clock(C++11) | | | | | | steady_clock(C++11) | | | | | | ****is_clock****(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | utc_clock(C++20) | | | | | | tai_clock(C++20) | | | | | | high_resolution_clock(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | gps_clock(C++20) | | | | | | file_clock(C++20) | | | | | | local_t(C++20) | | | | | |
| Time of day | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_amis_pm(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make12make24(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hh_mm_ss(C++20) | | | | | |  | | | | | |
| Calendar | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | day(C++20) | | | | | | month(C++20) | | | | | | year(C++20) | | | | | | weekday(C++20) | | | | | | operator/(C++20) | | | | | | year_month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | year_month_day_last(C++20) | | | | | | year_month_weekday(C++20) | | | | | | year_month_weekday_last(C++20) | | | | | | weekday_indexed(C++20) | | | | | | weekday_last(C++20) | | | | | | month_day(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | month_day_last(C++20) | | | | | | month_weekday(C++20) | | | | | | month_weekday_last(C++20) | | | | | | year_month(C++20) | | | | | | last_speclast(C++20)(C++20) | | | | | |
| Time zone | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ambiguous_local_time(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| template< class T >  struct is_clock; |  | (since C++20) |
|  |  |  |

If `T` satisfies the Clock requirements, provides the member constant value equal true. For any other type, value is false.

For the purpose of this trait, the extent to which an implementation determines that a type cannot meet the Clock requirements is unspecified, except that a minimum `T` shall not qualify as a Clock unless it meets all following conditions:

- Each of the following qualified identifiers is valid and denotes a type:

:   - `T::rep`
    - `T::period`
    - `T::duration`
    - `T::time_point`

- Each of the following expressions is well-formed when treated as an unevaluated operand:

:   - `T::is_steady`
    - `T::now()`

If the program adds specializations for `std::is_clock` or `std::is_clock_v`, the behavior is undefined.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | a type to check |

### Helper variable template

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr bool is_clock_v = is_clock<T>::value; |  | (since C++20) |
|  |  |  |

## Inherited from std::integral_constant

### Member constants

|  |  |
| --- | --- |
| value[static] | true if `T` satisfies the Clock requirements, false otherwise   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| operator bool | converts the object to bool, returns value   (public member function) |
| operator()(C++14) | returns value   (public member function) |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `value_type` | bool |
| `type` | std::integral_constant<bool, value> |

### Possible implementation

|  |
| --- |
| ```text template<class> struct is_clock : std::false_type {};   template<class T>     requires         requires         {             typename T::rep;             typename T::period;             typename T::duration;             typename T::time_point;             T::is_steady; // type is not checked             T::now();     // return type is not checked         } struct is_clock<T> : std::true_type {}; ``` |

### Notes

If `T` otherwise meets the Clock requirements, but `T::is_steady` is not of type const bool, or `T::now()` is not of type T::time_point, the result of `is_clock_v<T>` is unspecified.

### Example

Run this code

```
#include <chrono>
#include <ratio>
 
static_assert
(
    std::chrono::is_clock_v<std::chrono::utc_clock> and
    not std::chrono::is_clock_v<std::chrono::duration<int, std::exa>>
);
 
int main() {}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/is_clock&oldid=176446>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 September 2024, at 08:31.