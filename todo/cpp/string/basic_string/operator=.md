# std::basic_string<CharT,Traits,Allocator>::operator=

From cppreference.com
< cpp‎ | string‎ | basic string
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

std::basic_string

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | ****basic_string::operator=**** | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| basic_string& operator=( const basic_string& str ); | (1) | (constexpr since C++20) |
| basic_string& operator=( basic_string&& str )      noexcept(/\* see below \*/); | (2) | (since C++11)  (constexpr since C++20) |
| basic_string& operator=( const CharT\* s ); | (3) | (constexpr since C++20) |
| basic_string& operator=( CharT ch ); | (4) | (constexpr since C++20) |
| basic_string& operator=( std::initializer_list<CharT> ilist ); | (5) | (since C++11)  (constexpr since C++20) |
| template<class StringViewLike>  basic_string& operator=( const StringViewLike& t ); | (6) | (since C++17)  (constexpr since C++20) |
| basic_string& operator=( std::nullptr_t ) = delete; | (7) | (since C++23) |
|  |  |  |

Replaces the contents of the string.

1) Replaces the contents with a copy of str. If \*this and str are the same object, this function has no effect.2) Replaces the contents with those of str using SequenceContainer's move assignment semantics. Unlike other sequence container move assignments, references, pointers, and iterators to elements of str may be invalidated.3) Replaces the contents with those of null-terminated character string pointed to by s as if by assign(s, Traits::length(s)).4) Replaces the contents with character ch as if by assign(std::addressof(ch), 1).5) Replaces the contents with those of the initializer list ilist as if by assign(ilist.begin(), ilist.size()).6) Implicitly converts t to a string view sv as if by std::basic_string_view<CharT, Traits> sv = t;, then replaces the contents with those of the sv as if by assign(sv). This overload participates in overload resolution only if std::is_convertible_v<const StringViewLike&,  
                      std::basic_string_view<CharT, Traits>> is true and std::is_convertible_v<const StringViewLike&, const CharT\*> is false.7) `std::basic_string` cannot be assigned from nullptr.

### Parameters

|  |  |  |
| --- | --- | --- |
| ch | - | value to initialize characters of the string with |
| str | - | string to be used as source to initialize the string with |
| s | - | pointer to a null-terminated character string to use as source to initialize the string with |
| ilist | - | std::initializer_list to initialize the string with |
| t | - | object convertible to std::basic_string_view to initialize the string with |

### Return value

\*this

### Complexity

1) Linear in size of str.2) Linear in the size of \*this (formally, each `CharT` has to be destroyed). If allocators do not compare equal and do not propagate, then also linear in the size of str (copy must be made).3) Linear in size of s.4) Constant.5) Linear in size of ilist.6) Linear in size of t.

### Exceptions

2)noexcept specification:noexcept(std::allocator_traits<Allocator>::  

propagate_on_container_move_assignment::value ||

std::allocator_traits<Allocator>::is_always_equal::value)

If the operation would cause `size()` to exceed `max_size()`, throws std::length_error.

If an exception is thrown for any reason, this function has no effect (strong exception safety guarantee).

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <string>
 
int main()
{
    std::string str1;
    std::string str2{"alpha"};
 
    // (1) operator=(const basic_string&);
    str1 = str2;
    std::cout << std::quoted(str1) << ' '   // "alpha"
              << std::quoted(str2) << '\n'; // "alpha"
 
    // (2) operator=(basic_string&&);
    str1 = std::move(str2);
    std::cout << std::quoted(str1) << ' '   // "alpha"
              << std::quoted(str2) << '\n'; // "" or "alpha" (unspecified)
 
    // (3) operator=(const CharT*);
    str1 = "beta";
    std::cout << std::quoted(str1) << '\n'; // "beta"
 
    // (4) operator=(CharT);
    str1 = '!'; 
    std::cout << std::quoted(str1) << '\n'; // "!"
 
    // (5) operator=(std::initializer_list<CharT>);
    str1 = {'g', 'a', 'm', 'm', 'a'};
    std::cout << std::quoted(str1) << '\n'; // "gamma"
 
    // (6) operator=(const T&);
    str1 = 35U; // equivalent to str1 = static_cast<char>(35U);
    std::cout << std::quoted(str1) << '\n'; // "#" (ASCII = 35)
}

```

Possible output:

```
"alpha" "alpha"
"alpha" ""
"beta"
"!"
"gamma"
"#"

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 847 | C++98 | there was no exception safety guarantee | added strong exception safety guarantee |
| LWG 2063 | C++11 | the move assignment operator did not follow SequenceContainer's semantic requirement | follows |
| LWG 2946 | C++17 | overload (6) caused ambiguity in some cases | avoided by making it a template |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_string`   (public member function) |
| assign | assign characters to a string   (public member function) |
| operator= | assigns a view   (public member function of `std::basic_string_view<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/operator%3D&oldid=172092>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 May 2024, at 00:04.