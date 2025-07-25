# std::text_encoding::environment

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
| ****text_encoding::environment**** | | | | |
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
| hash<std::text_encoding> | | | | |

|  |  |  |
| --- | --- | --- |
| static text_encoding environment(); |  | (since C++26) |
|  |  |  |

Constructs a new `text_encoding` object representing the environment encoding that refers to the implementation-defined character encoding scheme of the execution environment. The execution environment at runtime is the environment in which the program is run.

The environment encoding in the execution environment is distinct from the encoding of execution character set which is locale-specific. In other words, the environment encoding remains locale-independent, that is, the value returned by environment() is not affected by calls to the functions (e.g. std::setlocale and POSIX function `setenv()`) which can modify the environment.

This function is deleted unless the CHAR_BIT is 8.

### Parameters

(none)

### Return value

The object holding the representation of the environment character encoding.

### Notes

The environment encoding may differ from the global locale-associated encoding that is accessible via std::locale().encoding().

On Windows platforms, the environment encoding can be determined by `GetACP()` and then mapped to MIBenum values.

On POSIX platforms, the environment encoding is associated with the POSIX locale "" which can be implemented to correspond to a value of `nl_langinfo_l()` when the environment locale "" is set before the global C++ locale is set to "C" at program startup.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| encoding(C++26) | returns the character encoding scheme associated with the locale   (public member function of `std::locale`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/text/text_encoding/environment&oldid=179259>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 January 2025, at 00:06.