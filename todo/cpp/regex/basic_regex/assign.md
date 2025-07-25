# std::basic_regex<CharT,Traits>::assign

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
| basic_regex::operator= | | | | |
| ****basic_regex::assign**** | | | | |
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
| basic_regex& assign( const basic_regex& other ); | (1) | (since C++11) |
| basic_regex& assign( basic_regex&& other ) noexcept; | (2) | (since C++11) |
| basic_regex& assign( const CharT\* s,                       flag_type f = std::regex_constants::ECMAScript ); | (3) | (since C++11) |
| basic_regex& assign( const CharT\* ptr, std::size_t count,                       flag_type f = std::regex_constants::ECMAScript ); | (4) | (since C++11) |
| template< class ST, class SA >  basic_regex& assign( const std::basic_string<CharT,ST,SA>& str,                      flag_type f = std::regex_constants::ECMAScript ); | (5) | (since C++11) |
| template< class InputIt >  basic_regex& assign( InputIt first, InputIt last,                      flag_type f = std::regex_constants::ECMAScript ); | (6) | (since C++11) |
| basic_regex& assign( std::initializer_list<CharT> ilist,                       flag_type f = std::regex_constants::ECMAScript ); | (7) | (since C++11) |
|  |  |  |

Assigns the contents to the regular expression.

1) Assigns the contents of other. flags() and mark_count() are equivalent to the values of other.flags() and other.mark_count() after the call.2) Assigns the contents of other using move semantics. flags() and mark_count() are equivalent to the values of other.flags() and other.mark_count() before the assignment. After the call, other is in a valid, but unspecified state.3-7) Assigns a sequence of characters to the regular expression. The syntax flags are set to `f`. mark_count() returns the number of marked subexpressions within the resulting subexpression after the call.3) Assigns a null-terminated string pointed to by s.4) Assigns a sequence of count characters, pointed to by s.5) Assigns the string str.6) Assigns the characters in the range ``first`,`last`)`.7) Assigns the characters in the initializer list ilist.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another regular expression to assign |
| s | - | pointer to a character sequence to assign |
| str | - | string to assign |
| first, last | - | the range of characters to assign |
| ilist | - | initializer list containing characters to assign |
| Type requirements | | |
| -`InputIt` must meet the requirements of [LegacyInputIterator. | | |

### Return value

\*this

### Exceptions

1) May throw implementation-defined exceptions.3-7) std::regex_error if the supplied regular expression is not valid. The object is not modified in that case.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| operator= | assigns the contents   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/basic_regex/assign&oldid=160993>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 October 2023, at 13:15.