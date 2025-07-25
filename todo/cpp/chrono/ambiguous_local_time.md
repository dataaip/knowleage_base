# std::chrono::ambiguous_local_time

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tzdb(C++20) | | | | | | tzdb_list(C++20) | | | | | | get_tzdbget_tzdb_listreload_tzdbremote_version(C++20)(C++20)(C++20)(C++20) | | | | | | sys_info(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | local_info(C++20) | | | | | | nonexistent_local_time(C++20) | | | | | | ****ambiguous_local_time****(C++20) | | | | | | locate_zone(C++20) | | | | | | current_zone(C++20) | | | | | | time_zone(C++20) | | | | | | choose(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | zoned_traits(C++20) | | | | | | zoned_time(C++20) | | | | | | time_zone_link(C++20) | | | | | | leap_second(C++20) | | | | | | leap_second_info(C++20) | | | | | | get_leap_second_info(C++20) | | | | | |  | | | | | |
| `chrono` I/O | | | | |
| parse(C++20) | | | | |
| C-style date and time | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<chrono>` |  |  |
| class ambiguous_local_time; |  | (since C++20) |
|  |  |  |

Defines a type of object to be thrown as exception to report that an attempt was made to convert an ambiguous std::chrono::local_time to a std::chrono::sys_time without specifying a std::chrono::choose (such as `choose::earliest` or `choose::latest`).

This exception is thrown by std::chrono::time_zone::to_sys and functions that call it (such as the constructors of std::chrono::zoned_time that take a std::chrono::local_time).

!std-chrono-ambiguous local time-inheritance.svg

Inheritance diagram

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the exception object   (public member function) |
| operator= | replaces the exception object   (public member function) |
| what | returns the explanatory string   (public member function) |

## std::chrono::ambiguous_local_time::ambiguous_local_time

|  |  |  |
| --- | --- | --- |
| template< class Duration >  ambiguous_local_time( const std::chrono::local_time<Duration>& tp, const std::chrono::local_info& i ); | (1) | (since C++20) |
| ambiguous_local_time( const ambiguous_local_time& other ) noexcept; | (2) | (since C++20) |
|  |  |  |

Constructs the exception object.

1) The explanatory string returned by what() is equivalent to that produced by os.str() after the following code:

```
std::ostringstream os;
os << tp << " is ambiguous.  It could be\n"
   << tp << ' ' << i.first.abbrev << " == "
   << tp - i.first.offset << " UTC or\n"
   << tp << ' ' << i.second.abbrev  << " == "
   << tp - i.second.offset  << " UTC";

```

 The behavior is undefined if i.result != std::chrono::local_info::ambiguous.2) Copy constructor. If \*this and `other` both have dynamic type `std::chrono::ambiguous_local_time` then std::strcmp(what(), other.what()) == 0.

### Parameters

|  |  |  |
| --- | --- | --- |
| tp | - | the time point for which conversion was attempted |
| i | - | a std::chrono::local_info describing the result of the conversion attempt |
| other | - | another `ambiguous_local_time` to copy |

### Exceptions

May throw std::bad_alloc

### Notes

Because copying a standard library class derived from std::exception is not permitted to throw exceptions, this message is typically stored internally as a separately-allocated reference-counted string.

## std::chrono::ambiguous_locale_time::operator=

|  |  |  |
| --- | --- | --- |
| ambiguous_locale_time& operator=( const ambiguous_locale_time& other ) noexcept; |  | (since C++20) |
|  |  |  |

Assigns the contents with those of other.If \*this and other both have dynamic type `std::chrono::ambiguous_locale_time` then std::strcmp(what(), other.what()) == 0 after assignment.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another exception object to assign with |

### Return value

\*this

## std::chrono::ambiguous_locale_time::what

|  |  |  |
| --- | --- | --- |
| virtual const char\* what() const noexcept; |  | (since C++20) |
|  |  |  |

Returns the explanatory string.

### Return value

Pointer to an implementation-defined null-terminated string with explanatory information. The string is suitable for conversion and display as a std::wstring. The pointer is guaranteed to be valid at least until the exception object from which it is obtained is destroyed, or until a non-const member function (e.g. copy assignment operator) on the exception object is called.

|  |  |
| --- | --- |
| The returned string is encoded with the ordinary literal encoding during constant evaluation. | (since C++26) |

### Notes

Implementations are allowed but not required to override `what()`.

## Inherited from std::runtime_error

## Inherited from std::exception

### Member functions

|  |  |
| --- | --- |
| (destructor)[virtual] | destroys the exception object   (virtual public member function of `std::exception`) |
| what[virtual] | returns an explanatory string   (virtual public member function of `std::exception`) |

### See also

|  |  |
| --- | --- |
| nonexistent_local_time(C++20) | exception thrown to report that a local time is nonexistent   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/chrono/ambiguous_local_time&oldid=154389>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 June 2023, at 12:08.