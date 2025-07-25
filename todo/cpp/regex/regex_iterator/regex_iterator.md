# std::regex_iterator<BidirIt,CharT,Traits>::regex_iterator

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
| ****regex_iterator::regex_iterator**** | | | | |
| regex_iterator::operator= | | | | |
| Comparisons | | | | |
| regex_iterator::operator==regex_iterator::operator!=(until C++20) | | | | |
| Observers | | | | |
| regex_iterator::operator\*regex_iterator::operator-> | | | | |
| Modifiers | | | | |
| regex_iterator::operator++regex_iterator::operator++(int) | | | | |

|  |  |  |
| --- | --- | --- |
| regex_iterator(); | (1) | (since C++11) |
| regex_iterator( BidirIt a, BidirIt b,  const regex_type& re,                  std::regex_constants::match_flag_type m = std::regex_constants::match_default ); | (2) | (since C++11) |
| regex_iterator( const regex_iterator& ); | (3) | (since C++11) |
| regex_iterator( BidirIt, BidirIt,  const regex_type&&,                  std::regex_constants::match_flag_type = std::regex_constants::match_default ) = delete; | (4) | (since C++11) |
|  |  |  |

Constructs a new `regex_iterator`:

1) Default constructor. Constructs an end-of-sequence iterator.2) Constructs a `regex_iterator` from the sequence of characters ``a`,`b`)`, the regular expression re, and a flag m that governs matching behavior. This constructor performs an initial call to [std::regex_search with this data. If the result of this initial call is false, \*this is set to an end-of-sequence iterator.3) Copies a `regex_iterator`.4) The overload (2) is not allowed to be called with a temporary regex, since the returned iterator would be immediately invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| a | - | LegacyBidirectionalIterator to the beginning of the target character sequence |
| b | - | LegacyBidirectionalIterator to the end of the target character sequence |
| re | - | regular expression used to search the target character sequence |
| m | - | flags that govern the behavior of re |

### Example

Run this code

```
#include <iostream>
#include <regex>
#include <string_view>
 
int main()
{
    constexpr std::string_view str{R"(
        #ONE: *p = &Mass;
        #Two: MOV %rd, 42
    )"};
    const std::regex re("[a-w]");
 
    // create regex_iterator, overload (2)
    auto it = std::regex_iterator<std::string_view::iterator>
    {
        str.cbegin(), str.cend(),
        re // re is lvalue; if an immediate expression was used
           // instead, e.g. std::regex{"[a-z]"}, this would
           // produce an error since overload (4) is deleted
    };
 
    for (decltype(it) last /* overload (1) */; it != last; ++it)
        std::cout << (*it).str();
    std::cout << '\n';
}

```

Output:

```
password

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2332 | C++11 | a `regex_iterator` constructed from a temporary `basic_regex` became invalid immediately | such construction is disallowed via a deleted overload |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_iterator/regex_iterator&oldid=161422>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 October 2023, at 06:59.