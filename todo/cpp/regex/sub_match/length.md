# std::sub_match<BidirIt>::length

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
| ****sub_match::length**** | | | | |
| sub_match::strsub_match::operator string_type | | | | |
| sub_match::compare | | | | |
| sub_match::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| operator<< | | | | |

|  |  |  |
| --- | --- | --- |
| difference_type length() const; |  |  |
|  |  |  |

Returns the number of characters in the match.

### Return value

std::distance(first, second) if the match is valid, ​0​ otherwise.

### Complexity

Constant.

### Example

Run this code

```
#include <iostream>
#include <regex>
#include <string>
 
int main()
{
    std::string sentence{"Quick red fox jumped over a lazy cow."};
    const std::regex re{"([A-z]+) ([a-z]+) ([a-z]+) ([a-z]+)"};
    std::smatch words;
    std::regex_search(sentence, words, re);
    for (const auto& m : words)
        std::cout << '[' << m << "], length = " << m.length() << '\n';
}

```

Output:

```
[Quick red fox jumped], length = 20
[Quick], length = 5
[red], length = 3
[fox], length = 3
[jumped], length = 6

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/sub_match/length&oldid=178382>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 December 2024, at 11:53.