# std::sub_match<BidirIt>::swap

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
| ****sub_match::swap**** | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| operator<< | | | | |

|  |  |  |
| --- | --- | --- |
| void swap( sub_match& s ) noexcept(/\* see below \*/); |  | (since C++11) |
|  |  |  |

Exchanges the contents of two sub-match objects. Equivalent to

this->pair<BidirIt, BidirIt>::swap(s);  
std::swap(matched, s.matched);

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | a `sub_match` to swap with |
| Type requirements | | |
| -`BidirIt` must meet the requirements of LegacySwappable"). | | |

### Exceptions

noexcept specification:noexcept(std::is_nothrow_swappable_v<BidirIt>)

### Example

Run this code

```
#include <cassert>
#include <iostream>
#include <regex>
 
int main()
{
    const char* s = "Quick red cat";
    std::sub_match<const char*> x, y;
 
    x.first = &s[0];
    x.second = &s[5];
    x.matched = false;
 
    y.first = &s[012];
    y.second = &s[13];
    y.matched = true;
 
    std::cout << "Before swap:\n";
    std::cout << "x.str() = [" << x.str() << "]\n";
    std::cout << "y.str() = [" << y.str() << "]\n";
    assert(!x.matched and y.matched);
 
    x.swap(y);
 
    std::cout << "After swap:\n";
    std::cout << "x.str() = [" << x.str() << "]\n";
    std::cout << "y.str() = [" << y.str() << "]\n";
    assert(x.matched and !y.matched);
}

```

Output:

```
Before swap:
x.str() = []
y.str() = [cat]
After swap:
x.str() = [cat]
y.str() = []

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3204 | C++11 | std::sub_match used inherited std::pair::swap(pair&) which led to a slicing | std::sub_match::swap(sub_match&) is added |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/sub_match/swap&oldid=178372>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 December 2024, at 07:52.