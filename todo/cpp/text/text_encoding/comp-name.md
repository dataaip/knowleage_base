# std::text_encoding::**comp-name**

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
| ****text_encoding::**comp-name****** | | | | |
| Non-member functions | | | | |
| operator==(std::text_encoding) | | | | |
| Member types | | | | |
| text_encoding::id | | | | |
| text_encoding::aliases_view | | | | |
| Helper classes | | | | |
| hash<std::text_encoding> | | | | |

|  |  |  |
| --- | --- | --- |
| static constexpr bool /\*comp-name\*/( std::string_view a, std::string_view b ); |  | (since C++26)  (exposition only\*) |
|  |  |  |

Compares two strings a and b encoded in ordinary literal encoding following the Unicode Charset Alias Matching rules.

Two strings are considered equal when comparing from left to right after:

- removing all non-alphanumeric characters,
- converting all letters to the same case, and
- removing any standalone sequences of '0' characters that do not immediately follow a numeric prefix. A numeric prefix consists of a non-zero digit ('1' through '9') optionally followed by one or more non-alphanumeric characters.

Here are the following examples:

```
static_assert(/*comp-name*/("UTF-8", "utf8") == true);
static_assert(/*comp-name*/("u.t.f-008", "utf8") == true);
static_assert(/*comp-name*/("ISO-8859-1", "iso88591") == true);
static_assert(/*comp-name*/("ut8", "utf8") == false);
static_assert(/*comp-name*/("utf-80", "utf8") == false);

```

### Parameters

|  |  |  |
| --- | --- | --- |
| a, b | - | strings to compare |

### Return value

true if two strings compare equal as described above; false otherwise.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/text/text_encoding/comp-name&oldid=179263>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 January 2025, at 17:48.