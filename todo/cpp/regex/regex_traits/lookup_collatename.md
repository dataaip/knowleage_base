# std::regex_traits<CharT>::lookup_collatename

From cppreference.com
< cpp‎ | regex‎ | regex traits
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

std::regex_traits

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| regex_traits::regex_traits | | | | |
| regex_traits::length | | | | |
| regex_traits::translate | | | | |
| regex_traits::translate_nocase | | | | |
| regex_traits::transform | | | | |
| regex_traits::transform_primary | | | | |
| ****regex_traits::lookup_collatename**** | | | | |
| regex_traits::lookup_classname | | | | |
| regex_traits::isctype | | | | |
| regex_traits::value | | | | |
| regex_traits::imbue | | | | |
| regex_traits::getloc | | | | |

|  |  |  |
| --- | --- | --- |
| template< class ForwardIt >  string_type lookup_collatename( ForwardIt first, ForwardIt last ) const; |  |  |
|  |  |  |

If the character sequence `[`first`,`last`)` represents the name of a valid collating element in the currently imbued locale, returns the name of that collating element. Otherwise, returns an empty string.

Collating elements are the symbols found in POSIX regular expressions between `[.` and `.]`. For example, `[.a.]` matches the character `a` in the C locale. `[.tilde.]` matches the character `~` in the C locale as well. `[.ch.]` matches the digraph `ch` in Czech locale, but generates std::regex_error with error code std::regex_constants::error_collate in most other locales.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | a pair of iterators which determines the sequence of characters that represents a collating element name |
| Type requirements | | |
| -`ForwardIt` must meet the requirements of LegacyForwardIterator. | | |

### Return value

The representation of the named collating element as a character string.

### Example

Run this code

```
#include <iostream>
#include <regex>
#include <string>
 
struct noisy_traits : std::regex_traits<char>
{
    template<class Iter>
    string_type lookup_collatename(Iter first, Iter last) const
    {
        string_type result = regex_traits::lookup_collatename(first, last);
        std::cout << "regex_traits<>::lookup_collatename(\""
                  << string_type(first, last)
                  << "\") returns \"" << result << "\"\n";
        return result;
    }
};
 
int main()
{
    std::string str = "z|}a"; // C locale collation order: x,y,z,{,|,},~
    std::basic_regex<char, noisy_traits> re("[x-[.tilde.]]*a", std::regex::basic);
    std::cout << std::boolalpha << std::regex_match(str, re) << '\n';
}

```

Possible output:

```
regex_traits<>::lookup_collatename("tilde") returns "~"
true

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_traits/lookup_collatename&oldid=161051>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 October 2023, at 09:14.