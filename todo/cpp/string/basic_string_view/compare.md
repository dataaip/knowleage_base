# std::basic_string_view<CharT,Traits>::compare

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string_view::basic_string_view | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Operations | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | ****basic_string_view::compare**** | | | | | | basic_string_view::starts_with(C++20) | | | | | | basic_string_view::ends_with(C++20) | | | | | | basic_string_view::contains(C++23) | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | basic_string_view::find_first_of | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](operator_at.html "cpp/string/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | operator<< | | | | | | operator""sv | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u8string_view>hash<std::u16string_view>hash<std::u32string_view>(C++20) | | | | | | Deduction guides (C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr int compare( basic_string_view v ) const noexcept; | (1) | (since C++17) |
| constexpr int compare( size_type pos1, size_type count1,                         basic_string_view v ) const; | (2) | (since C++17) |
| constexpr int compare( size_type pos1, size_type count1, basic_string_view v,                         size_type pos2, size_type count2 ) const; | (3) | (since C++17) |
| constexpr int compare( const CharT\* s ) const; | (4) | (since C++17) |
| constexpr int compare( size_type pos1, size_type count1,                         const CharT\* s ) const; | (5) | (since C++17) |
| constexpr int compare( size_type pos1, size_type count1,                         const CharT\* s, size_type count2 ) const; | (6) | (since C++17) |
|  |  |  |

Compares two character sequences.

1) The length `rlen` of the sequences to compare is the smaller of size() and v.size(). The function compares the two views by calling traits::compare(data(), v.data(), rlen), and returns a value according to the following table:

| Condition | | Result | Return value |
| --- | --- | --- | --- |
| `Traits::compare(data(), v.data(), rlen) < 0` | | `this` is **less** than `v` | < 0 |
| `Traits::compare(data(), v.data(), rlen) == 0` | `size() < v.size()` | `this` is **less** than `v` | < 0 |
| `size() == v.size()` | `this` is **equal** to `v` | ​0​ |
| `size() > v.size()` | `this` is **greater** than `v` | > 0 |
| `Traits::compare(data(), v.data(), rlen) > 0` | | `this` is **greater** than `v` | > 0 |

2) Equivalent to substr(pos1, count1).compare(v).3) Equivalent to substr(pos1, count1).compare(v.substr(pos2, count2)).4) Equivalent to compare(basic_string_view(s)).5) Equivalent to substr(pos1, count1).compare(basic_string_view(s)).6) Equivalent to substr(pos1, count1).compare(basic_string_view(s, count2)).

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | view to compare |
| s | - | pointer to the character string to compare to |
| count1 | - | number of characters of this view to compare |
| pos1 | - | position of the first character in this view to compare |
| count2 | - | number of characters of the given view to compare |
| pos2 | - | position of the first character of the given view to compare |

### Return value

Negative value if this view is less than the other character sequence, zero if the both character sequences are equal, positive value if this view is greater than the other character sequence.

### Complexity

1) Linear in the number of characters compared.

### Example

Run this code

```
#include <string_view>
 
int main()
{
    using std::operator""sv;
    static_assert("abc"sv.compare("abcd"sv) < 0);
    static_assert("abcd"sv.compare("abc"sv) > 0);
    static_assert("abc"sv.compare("abc"sv) == 0);
    static_assert(""sv.compare(""sv) == 0);
}

```

### See also

|  |  |
| --- | --- |
| compare | compares two strings   (public member function of `std::basic_string<CharT,Traits,Allocator>`) |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(C++17)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares two string views   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string_view/compare&oldid=152756>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 June 2023, at 07:49.