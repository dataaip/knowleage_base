# operator==(std::text_encoding)

From cppreference.com
< cpp‎ | text‎ | text encoding
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

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

std::text_encoding

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| Creation | | | | |
| text_encoding::text_encoding") | | | | |
| text_encoding::literal | | | | |
| text_encoding::environment | | | | |
| Observers | | | | |
| text_encoding::mib | | | | |
| text_encoding::name | | | | |
| text_encoding::aliases | | | | |
| text_encoding::environment_is | | | | |
| Helpers | | | | |
| text_encoding::**comp-name** | | | | |
| Non-member functions | | | | |
| ****operator==(std::text_encoding)**** | | | | |
| Member types | | | | |
| text_encoding::id | | | | |
| text_encoding::aliases_view | | | | |
| Helper classes | | | | |
| hash<std::text_encoding> | | | | |

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator==( const text_encoding& a,                                     const text_encoding& b ) noexcept; | (1) | (since C++26) |
| friend constexpr bool operator==( const text_encoding& a, id i ) noexcept; | (2) | (since C++26) |
|  |  |  |

Performs comparison operations on `text_encoding` objects.

1) Compares two `text_encoding` objects. The objects compare equal if and only if `comp-name` (a.name(), b.name()) is true when both a.mib() and b.mib() are equal to id::other, or a.mib() is equal to b.mib().2) Compare `text_encoding` object with a MIBenum value. The objects compare equal if and only if a.mib() is equal to i.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::text_encoding` is an associated class of the arguments.

The `!=` operator is synthesized from `operator==`.

### Parameters

|  |  |  |
| --- | --- | --- |
| a, b | - | `text_encoding` objects to compare |
| i | - | `id` value to compare with the MIBenum value contained in a |

### Return value

1) a.mib() == id::other && b.mib() == id::other  
?`comp-name` (a.name(), b.name())  
: a.mib() == b.mib().2) a.mib() == i.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| operator==operator!=(removed in C++20) | equality comparison between locale objects   (public member function of `std::locale`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/text/text_encoding/operator_eq&oldid=179269>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 January 2025, at 22:01.