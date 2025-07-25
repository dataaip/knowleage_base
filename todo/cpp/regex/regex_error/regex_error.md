# std::regex_error::regex_error

From cppreference.com
< cpp‎ | regex‎ | regex error
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

Regular expressions library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_regex(C++11) | | | | |
| sub_match(C++11) | | | | |
| match_results(C++11) | | | | |
| Algorithms | | | | |
| regex_match(C++11) | | | | |
| regex_search(C++11) | | | | |
| regex_replace(C++11) | | | | |
| Iterators | | | | |
| regex_iterator(C++11) | | | | |
| regex_token_iterator(C++11) | | | | |
| Exceptions | | | | |
| regex_error(C++11) | | | | |
| Traits | | | | |
| regex_traits(C++11) | | | | |
| Constants | | | | |
| syntax_option_type(C++11) | | | | |
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

std::regex_error

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****regex_error::regex_error**** | | | | |
| regex_error::operator= | | | | |
| regex_error::code | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| regex_error( std::regex_constants::error_type ecode ); | (1) | (since C++11) |
| regex_error( const regex_error& other ); | (2) | (since C++11) |
|  |  |  |

1) Constructs a `regex_error` with a given ecode of type std::regex_constants::error_type.2) Copy constructor. Initializes the contents with those of other. If \*this and other both have dynamic type `std::regex_error` then std::strcmp(what(), other.what()) == 0.

### Parameters

|  |  |  |
| --- | --- | --- |
| ecode | - | error code indicating the error raised in regular expression parsing |
| other | - | another `regex_error` object to copy |

### See also

|  |  |
| --- | --- |
| error_type(C++11) | describes different types of matching errors   (typedef) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_error/regex_error&oldid=160537>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 October 2023, at 09:59.