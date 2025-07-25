# std::basic_string_view<CharT,Traits>::basic_string_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | ****basic_string_view::basic_string_view**** | | | | | | basic_string_view::operator= | | | | | | Iterators | | | | | | basic_string_view::beginbasic_string_view::cbegin | | | | | | basic_string_view::endbasic_string_view::cend | | | | | | basic_string_view::rbeginbasic_string_view::crbegin | | | | | | basic_string_view::rendbasic_string_view::crend | | | | | | Capacity | | | | | | basic_string_view::sizebasic_string_view::length | | | | | | basic_string_view::max_size | | | | | | basic_string_view::empty | | | | | | Operations | | | | | | basic_string_view::copy | | | | | | basic_string_view::substr | | | | | | basic_string_view::compare | | | | | | basic_string_view::starts_with(C++20) | | | | | | basic_string_view::ends_with(C++20) | | | | | | basic_string_view::contains(C++23) | | | | | | basic_string_view::find | | | | | | basic_string_view::rfind | | | | | | basic_string_view::find_first_of | | | | | | basic_string_view::find_last_of | | | | | | basic_string_view::find_first_not_of | | | | | | basic_string_view::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | basic_string_view::at | | | | | | [basic_string_view::operator[]](operator_at.html "cpp/string/basic string view/operator at") | | | | | | basic_string_view::front | | | | | | basic_string_view::back | | | | | | basic_string_view::data | | | | | | Modifiers | | | | | | basic_string_view::remove_prefix | | | | | | basic_string_view::remove_suffix | | | | | | basic_string_view::swap | | | | | | Constants | | | | | | basic_string_view::npos | | | | | | Non-member functions | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | operator<< | | | | | | operator""sv | | | | | | Helper classes | | | | | | hash<std::string_view>hash<std::wstring_view>hash<std::u8string_view>hash<std::u16string_view>hash<std::u32string_view>(C++20) | | | | | | Deduction guides (C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr basic_string_view() noexcept; | (1) | (since C++17) |
| constexpr basic_string_view( const basic_string_view& other ) noexcept = default; | (2) | (since C++17) |
| constexpr basic_string_view( const CharT\* s, size_type count ); | (3) | (since C++17) |
| constexpr basic_string_view( const CharT\* s ); | (4) | (since C++17) |
| template< class It, class End >  constexpr basic_string_view( It first, End last ); | (5) | (since C++20) |
| template< class R >  constexpr explicit basic_string_view( R&& r ); | (6) | (since C++23) |
| constexpr basic_string_view( std::nullptr_t ) = delete; | (7) | (since C++23) |
|  |  |  |

1) Default constructor. Constructs an empty `std::basic_string_view`. After construction, data() is equal to nullptr, and size() is equal to ​0​.2) Copy constructor. Constructs a view of the same content as other. After construction, data() is equal to other.data(), and size() is equal to other.size().3) Constructs a view of the first count characters of the character array starting with the element pointed by s. s can contain null characters. The behavior is undefined if ``s`,`s + count`)` is not a valid range (even though the constructor may not access any of the elements of this range). After construction, [data() is equal to s, and size() is equal to count.4) Constructs a view of the null-terminated character string pointed to by s, not including the terminating null character. The length of the view is determined as if by Traits::length(s). The behavior is undefined if ``s`,`s + Traits::length(s)`)` is not a valid range. After construction, [data() is equal to s, and size() is equal to Traits::length(s).5) Constructs a `std::basic_string_view` over the range ``first`,`last`)`. The behavior is undefined if `[`first`,`last`)` is not a valid range, if `It` does not actually model [`contiguous_iterator`, or if `End` does not actually model `sized_sentinel_for` for `It`. After construction, data() is equal to std::to_address(first), and size() is equal to last - first.

This overload participates in overload resolution only if all following conditions are satisfied:

:   - `It` satisfies `contiguous_iterator`,
    - `End` satisfies `sized_sentinel_for` for `It`,
    - std::iter_value_t<It> and `CharT` are the same type, and
    - `End` is not convertible to std::size_t.

6) Constructs a `std::basic_string_view` over the range r. After construction, data() is equal to ranges::data(r), and size() is equal to ranges::size(r).

This overload participates in overload resolution only if all following conditions are satisfied:

:   - std::remove_cvref_t<R> is not the same type as `std::basic_string_view`,
    - `R` models `contiguous_range` and `sized_range`,
    - ranges::range_value_t<R> and `CharT` are the same type,
    - `R` is not convertible to const CharT\*, and
    - Let d be an lvalue of type std::remove_cvref_t<R>, d.operator ::std::basic_string_view<CharT, Traits>() is not a valid expression.

7) `std::basic_string_view` cannot be constructed from nullptr.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another view to initialize the view with |
| s | - | pointer to a character array or a C string to initialize the view with |
| count | - | number of characters to include in the view |
| first | - | iterator to the first character of the sequence |
| last | - | iterator past the last character of the sequence or another sentinel |
| r | - | a contiguous range that contains the sequence |

### Complexity

1-3,5,6) Constant.4) Linear in length of s.

### Example

Run this code

```
#include <array>
#include <iomanip>
#include <iostream>
#include <string>
#include <string_view>
 
int main()
{
    std::string cppstr = "Foo";
    std::string_view cppstr_v(cppstr); // overload (2), after
                                       // std::string::operator string_view
    std::cout << "1) cppstr_v: " << std::quoted(cppstr_v) << '\n';
 
    char array[3] = {'B', 'a', 'r'};
    std::string_view array_v(array, std::size(array)); // overload (3)
    std::cout << "2) array_v: " << std::quoted(array_v) << '\n';
 
    const char* one_0_two = "One\0Two";
 
    std::string_view one_two_v{one_0_two, 7}; // overload (3)
    std::cout << "3) one_two_v: \"";
    for (char c : one_two_v)
        std::cout << (c != '\0' ? c : '?');
    std::cout << "\", one_two_v.size(): " << one_two_v.size() << '\n';
 
    std::string_view one_v{one_0_two}; // overload (4)
    std::cout << "4) one_v: " << std::quoted(one_v) << ", one_v.size(): " 
              << one_v.size() << '\n';
 
    constexpr std::wstring_view wcstr_v = L"xyzzy"; // overload (4)
    std::cout << "5) wcstr_v.size(): " << wcstr_v.size() << '\n';
 
    std::array ar = {'P', 'u', 'b'};
    std::string_view ar_v(ar.begin(), ar.end()); // overload (5), C++20
    std::cout << "6) ar_v: " << std::quoted(ar_v) << '\n';
 
//  std::string_view ar_v2{ar}; // overload (6), OK in C++23
//  std::cout << "ar_v2: " << std::quoted(ar_v2) << '\n'; // ar_v2: "Pub"
 
    [[maybe_unused]] auto zero = [] { /* ... */ return nullptr; };
//  std::string_view s{zero()}; // overload (7), won't compile since C++23
}

```

Output:

```
1) cppstr_v: "Foo"
2) array_v: "Bar"
3) one_two_v: "One?Two", one_two_v.size(): 7
4) one_v: "One", one_v.size(): 3
5) wcstr_v.size(): 5
6) ar_v: "Pub"

```

### See also

|  |  |
| --- | --- |
| operator= | assigns a view   (public member function) |
| (constructor) | constructs a `basic_string`   (public member function of `std::basic_string<CharT,Traits,Allocator>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string_view/basic_string_view&oldid=178189>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 December 2024, at 21:54.