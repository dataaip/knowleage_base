# std::basic_regex<CharT,Traits>::operator=

From cppreference.com
< cpp‎ | regex‎ | basic regex
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

std::basic_regex

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member Functions | | | | |
| basic_regex::basic_regex | | | | |
| basic_regex::~basic_regex | | | | |
| ****basic_regex::operator=**** | | | | |
| basic_regex::assign | | | | |
| Observers | | | | |
| basic_regex::mark_count | | | | |
| basic_regex::flags | | | | |
| Locale | | | | |
| basic_regex::getloc | | | | |
| basic_regex::imbue | | | | |
| Modifiers | | | | |
| basic_regex::swap | | | | |
| Constants | | | | |
| Non-member Functions | | | | |
| swap(std::basic_regex) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| basic_regex& operator=( const basic_regex& other ); | (1) | (since C++11) |
| basic_regex& operator=( basic_regex&& other ) noexcept; | (2) | (since C++11) |
| basic_regex& operator=( const CharT\* ptr ); | (3) | (since C++11) |
| basic_regex& operator=( std::initializer_list<CharT> il ); | (4) | (since C++11) |
| template< class ST, class SA >  basic_regex& operator=( const std::basic_string<CharT,ST,SA>& p ); | (5) | (since C++11) |
|  |  |  |

Assigns the contents.

1) Copy assignment operator. Assigns the contents of other. Equivalent to assign(other);.2) Move assignment operator. Assigns the contents of other using move semantics. other is in valid, but unspecified state after the operation. Equivalent to assign(other);.3) Assigns a null-terminated character string pointed to by ptr. Equivalent to assign(ptr);.4) Assigns characters contained in initializer list il. Equivalent to assign(il);.5) Assigns the contents of the string p. Equivalent to assign(p);.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another regex object |
| ptr | - | pointer to a null-terminated character string |
| il | - | initializer list containing characters to assign |
| p | - | string containing characters to assign |

### Return value

\*this

### Exceptions

1) May throw implementation-defined exceptions.3-5) std::regex_error if the supplied regular expression is not valid. The object is not modified in that case.

### See also

|  |  |
| --- | --- |
| assign | assigns the contents   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/basic_regex/operator%3D&oldid=161003>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 October 2023, at 23:01.