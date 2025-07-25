# std::literals::string_view_literals::operator""sv

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string_view::basic_string_view | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Operations | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | basic_string_view::compare | | | | | | basic_string_view::starts_with(C++20) | | | | | | basic_string_view::ends_with(C++20) | | | | | | basic_string_view::contains(C++23) | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | basic_string_view::find_first_of | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](operator_at.html "cpp/string/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | operator<< | | | | | | ****operator""sv**** | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u8string_view>hash<std::u16string_view>hash<std::u32string_view>(C++20) | | | | | | Deduction guides (C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string_view>` |  |  |
| constexpr std::string_view      operator ""sv( const char\* str, std::size_t len ) noexcept; | (1) | (since C++17) |
| constexpr std::u8string_view      operator ""sv( const char8_t\* str, std::size_t len ) noexcept; | (2) | (since C++20) |
| constexpr std::u16string_view      operator ""sv( const char16_t\* str, std::size_t len ) noexcept; | (3) | (since C++17) |
| constexpr std::u32string_view      operator ""sv( const char32_t\* str, std::size_t len ) noexcept; | (4) | (since C++17) |
| constexpr std::wstring_view      operator ""sv( const wchar_t\* str, std::size_t len ) noexcept; | (5) | (since C++17) |
|  |  |  |

Forms a string view of a character literal.

1) Returns std::string_view{str, len}.2) Returns std::u8string_view{str, len}.3) Returns std::u16string_view{str, len}.4) Returns std::u32string_view{str, len}.5) Returns std::wstring_view{str, len}.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the beginning of the raw character array literal |
| len | - | length of the raw character array literal |

### Return value

The std::basic_string_view literal.

### Notes

These operators are declared in the namespace `std::literals::string_view_literals`, where both `literals` and `string_view_literals` are inline namespaces. Access to these operators can be gained with any of:

- using namespace std::literals,
- using namespace std::string_view_literals, or
- using namespace std::literals::string_view_literals.

### Example

Run this code

```
#include <iostream>
#include <string_view>
#include <typeinfo>
 
void print_each_character(const std::string_view sw)
{
    for (char c : sw)
        std::cout << (c == '\0' ? '@' : c);
    std::cout << '\n';
}
 
int main()
{
    using namespace std::literals;
 
    std::string_view s1 = "abc\0\0def";
    std::string_view s2 = "abc\0\0def"sv;
 
    std::cout << "s1.size(): " << s1.size() << "; s1: ";
    print_each_character(s1);
    std::cout << "s2.size(): " << s2.size() << "; s2: ";
    print_each_character(s2);
 
    std::cout << "substr(1, 4): " << "abcdef"sv.substr(1, 4) << '\n';
 
    auto value_type_info = []<typename T>(T)
    {
        using V = typename T::value_type;
        std::cout << "sizeof " << typeid(V).name() << ": " << sizeof(V) << '\n';
    };
 
    value_type_info("char A"sv);
    value_type_info(L"wchar_t ∀"sv);
    value_type_info(u8"char8_t ∆"sv);
    value_type_info(u"char16_t ∇"sv);
    value_type_info(U"char32_t ∃"sv);
    value_type_info(LR"(raw ⊞)"sv);
}

```

Possible output:

```
s1.size(): 3; s1: abc
s2.size(): 8; s2: abc@@def
substr(1, 4): bcde
sizeof char: 1
sizeof wchar_t: 4
sizeof char8_t: 1
sizeof char16_t: 2
sizeof char32_t: 4
sizeof wchar_t: 4

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_string_view`   (public member function) |
| operator""s(C++14) | converts a character array literal to `basic_string`   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string_view/operator%22%22sv&oldid=152793>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 June 2023, at 10:34.