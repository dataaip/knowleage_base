# std::regex_traits<CharT>::value

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
| regex_traits::lookup_collatename | | | | |
| regex_traits::lookup_classname | | | | |
| regex_traits::isctype | | | | |
| ****regex_traits::value**** | | | | |
| regex_traits::imbue | | | | |
| regex_traits::getloc | | | | |

|  |  |  |
| --- | --- | --- |
| int value( CharT ch, int radix ) const; |  | (since C++11) |
|  |  |  |

Determines the value represented by the digit ch in the numeric base radix, given the currently imbued locale. This function is called by std::regex when processing Quantifiers such as `{1`} or `{2,5`}, Backreferences such as `\1`, and hexadecimal and Unicode character escapes.

### Parameters

|  |  |  |
| --- | --- | --- |
| ch | - | the character that may represent a digit |
| radix | - | either 8, 10, or 16 |

### Return value

The numeric value if ch indeed represents a digit in the currently imbued locale that is valid for the numeric base radix, or -1 on error.

### Example

Run this code

```
#include <iostream>
#include <locale>
#include <map>
#include <regex>
 
// This custom regex traits allows japanese numerals
struct jnum_traits : std::regex_traits<wchar_t>
{   
    static std::map<wchar_t, int> data;
    int value(wchar_t ch, int radix) const
    {
        wchar_t up = std::toupper(ch, getloc());
        return data.count(up) ? data[up] : regex_traits::value(ch, radix);
    }
};
std::map<wchar_t, int> jnum_traits::data = {{L'〇',0}, {L'一',1}, {L'二',2},
                                            {L'三',3}, {L'四',4}, {L'五',5},
                                            {L'六',6}, {L'七',7}, {L'八',8},
                                            {L'九',9}, {L'Ａ',10}, {L'Ｂ',11},
                                            {L'Ｃ',12}, {L'Ｄ',13}, {L'Ｅ',14},
                                            {L'Ｆ',15}};
 
int main()
{   
    std::locale::global(std::locale("ja_JP.utf8"));
    std::wcout.sync_with_stdio(false);
    std::wcout.imbue(std::locale());
 
    std::wstring in = L"風";
 
    if (std::regex_match(in, std::wregex(L"\\u98a8")))
        std::wcout << "\\u98a8 matched " << in << '\n';
 
    if (std::regex_match(in, std::basic_regex<wchar_t, jnum_traits>(L"\\u九八ａ八")))
        std::wcout << L"\\u九八ａ八 with custom traits matched " << in << '\n';
}

```

Output:

```
\u98a8 matched 風
\u九八ａ八 with custom traits matched 風

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_traits/value&oldid=161056>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 October 2023, at 09:25.