# std::regex_iterator<BidirIt,CharT,Traits>::operator\*,operator->

From cppreference.com
< cpp‎ | regex‎ | regex iterator
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

std::regex_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| regex_iterator::regex_iterator | | | | |
| regex_iterator::operator= | | | | |
| Comparisons | | | | |
| regex_iterator::operator==regex_iterator::operator!=(until C++20) | | | | |
| Observers | | | | |
| ****regex_iterator::operator\*regex_iterator::operator->**** | | | | |
| Modifiers | | | | |
| regex_iterator::operator++regex_iterator::operator++(int) | | | | |

|  |  |  |
| --- | --- | --- |
| const value_type& operator\*() const; | (1) | (since C++11) |
| const value_type\* operator->() const; | (2) | (since C++11) |
|  |  |  |

Extracts the current std::match_results from a `regex_iterator`.

### Return value

1) Returns a reference to the current std::match_results.2) Returns a pointer to the current std::match_results.

### Example

Run this code

```
#include <iostream>
#include <regex>
#include <string>
 
int main()
{
    std::string hay{"1.1a2b3cjk34"};
    std::regex needle("[1234]");
    using Ri = std::regex_iterator<std::string::iterator>;
    for (Ri it{hay.begin(), hay.end(), needle}, last{}; it != last; ++it)
        std::cout << it->str();
    std::cout << '\n';
}

```

Output:

```
112334

```

Retrieved from "https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_iterator/operator\*&oldid=161421"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 October 2023, at 06:51.