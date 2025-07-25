# std::hash<std::text_encoding>

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
| operator==(std::text_encoding) | | | | |
| Member types | | | | |
| text_encoding::id | | | | |
| text_encoding::aliases_view | | | | |
| Helper classes | | | | |
| ****hash<std::text_encoding>**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<text_encoding>` |  |  |
| template<> struct hash<std::text_encoding>; |  | (since C++26) |
|  |  |  |

The template specialization of std::hash for std::text_encoding allows users to obtain hashes of encoded id and name of type std::text_encoding.

`operator()` of this specialization is noexcept.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| hash(C++11) | hash function object   (class template) |
| std::hash<std::basic_stacktrace>(C++23) | hash support for std::basic_stacktrace   (class template specialization) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/text/text_encoding/hash&oldid=179086>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 20:53.