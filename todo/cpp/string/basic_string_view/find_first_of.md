# std::basic_string_view<CharT,Traits>::find_first_of

From cppreference.com
< cpp‎ | string‎ | basic string view
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

Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_string | | | | |
| basic_string_view(C++17) | | | | |
| char_traits | | | | |

std::basic_string_view

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string_view::basic_string_view | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Operations | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | basic_string_view::compare | | | | | | basic_string_view::starts_with(C++20) | | | | | | basic_string_view::ends_with(C++20) | | | | | | basic_string_view::contains(C++23) | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | ****basic_string_view::find_first_of**** | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](operator_at.html "cpp/string/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | operator<< | | | | | | operator""sv | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u8string_view>hash<std::u16string_view>hash<std::u32string_view>(C++20) | | | | | | Deduction guides (C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr size_type      find_first_of( basic_string_view v, size_type pos = 0 ) const noexcept; | (1) | (since C++17) |
| constexpr size_type      find_first_of( CharT ch, size_type pos = 0 ) const noexcept; | (2) | (since C++17) |
| constexpr size_type      find_first_of( const CharT\* s, size_type pos, size_type count ) const; | (3) | (since C++17) |
| constexpr size_type      find_first_of( const CharT\* s, size_type pos = 0 ) const; | (4) | (since C++17) |
|  |  |  |

Finds the first character equal to any of the characters in the given character sequence.

1) Finds the first occurrence of any of the characters of v in this view, starting at position pos.2) Equivalent to find_first_of(basic_string_view(std::addressof(ch), 1), pos).3) Equivalent to find_first_of(basic_string_view(s, count), pos).4) Equivalent to find_first_of(basic_string_view(s), pos).

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | view to search for |
| pos | - | position at which to start the search |
| count | - | length of the string of characters to search for |
| s | - | pointer to a string of characters to search for |
| ch | - | character to search for |

### Return value

Position of the first occurrence of any character of the substring, or npos if no such character is found.

### Complexity

O(size() \* v.size()) at worst.

### Example

Run this code

```
#include <string_view>
 
using namespace std::literals;
constexpr auto N = std::string_view::npos;
 
constexpr bool is_white_space(const char c)
{
    return " \t\n\f\r\v"sv.find_first_of(c) != N;
};
 
static_assert(
    1 == "alignas"sv.find_first_of("klmn"sv) &&
      //   └─────────────────────────┘
    N == "alignof"sv.find_first_of("wxyz"sv) &&
      //
    3 == "concept"sv.find_first_of("bcde"sv, /* pos= */ 1) &&
      //     └───────────────────────┘
    N == "consteval"sv.find_first_of("oxyz"sv, /* pos= */ 2) &&
      //
    6 == "constexpr"sv.find_first_of('x') &&
      //        └─────────────────────┘
    N == "constinit"sv.find_first_of('x') &&
      //
    6 == "const_cast"sv.find_first_of('c', /* pos= */ 4) &&
      //        └──────────────────────┘
    N == "continue"sv.find_first_of('c', /* pos= */ 42) &&
      //
    5 == "co_await"sv.find_first_of("cba", /* pos= */ 4) &&
      //       └───────────────────────┘
    7 == "decltype"sv.find_first_of("def", /* pos= */ 2, /* count= */ 2) &&
      //         └────────────────────┘
    N == "decltype"sv.find_first_of("def", /* pos= */ 2, /* count= */ 1) &&
      //
    is_white_space(' ') && is_white_space('\r') && !is_white_space('\a')
);
 
int main() {}

```

### See also

|  |  |
| --- | --- |
| find | find characters in the view   (public member function) |
| rfind | find the last occurrence of a substring   (public member function) |
| find_last_of | find last occurrence of characters   (public member function) |
| find_first_not_of | find first absence of characters   (public member function) |
| find_last_not_of | find last absence of characters   (public member function) |
| find_first_of | find first occurrence of characters   (public member function of `std::basic_string<CharT,Traits,Allocator>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string_view/find_first_of&oldid=171369>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 April 2024, at 15:18.