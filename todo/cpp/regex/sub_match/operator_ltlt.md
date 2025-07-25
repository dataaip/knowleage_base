# operator<<(std::sub_match)

From cppreference.com
< cpp‎ | regex‎ | sub match
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

std::sub_match

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| sub_match::sub_match | | | | |
| sub_match::length | | | | |
| sub_match::strsub_match::operator string_type | | | | |
| sub_match::compare | | | | |
| sub_match::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| ****operator<<**** | | | | |

|  |  |  |
| --- | --- | --- |
| template< class CharT, class Traits, class BidirIt >  std::basic_ostream<CharT,Traits>&     operator<<( std::basic_ostream<CharT,Traits>& os, const sub_match<BidirIt>& m ); |  | (since C++11) |
|  |  |  |

Writes the representation of the matched subsequence m to the output stream os.
Equivalent to os << m.str().

### Parameters

|  |  |  |
| --- | --- | --- |
| os | - | output stream to write the representation to |
| m | - | a sub-match object to output |

### Return value

os

### Example

Run this code

```
#include <iostream>
#include <regex>
#include <string>
 
int main()
{
    std::string sentence{"Quick red fox jumped over a lazy hare."};
    const std::regex re{"([A-z]+) ([a-z]+) ([a-z]+)"};
    std::smatch words;
    std::regex_search(sentence, words, re);
    for (const auto& m : words)
        // m has type `const std::sub_match<std::string::const_iterator>&`
        std::cout << '[' << m << "] ";
    std::cout << '\n';
}

```

Output:

```
[Quick red fox] [Quick] [red] [fox]

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/sub_match/operator_ltlt&oldid=178383>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 December 2024, at 11:56.