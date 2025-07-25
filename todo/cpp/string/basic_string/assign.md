# std::basic_string<CharT,Traits,Allocator>::assign

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | ****basic_string::assign**** | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| basic_string& assign( const basic_string& str ); | (1) | (constexpr since C++20) |
| basic_string& assign( basic_string&& str ) noexcept(/\* see below \*/); | (2) | (since C++11)  (constexpr since C++20) |
| basic_string& assign( size_type count, CharT ch ); | (3) | (constexpr since C++20) |
| basic_string& assign( const CharT\* s, size_type count ); | (4) | (constexpr since C++20) |
| basic_string& assign( const CharT\* s ); | (5) | (constexpr since C++20) |
| template< class SV >  basic_string& assign( const SV& t ); | (6) | (since C++17)  (constexpr since C++20) |
| template< class SV >  basic_string& assign( const SV& t,                       size_type pos, size_type count = npos); | (7) | (since C++17)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (8) |  |
| basic_string& assign( const basic_string& str,                        size_type pos, size_type count ); |  | (until C++14) |
| basic_string& assign( const basic_string& str,                        size_type pos, size_type count = npos); |  | (since C++14)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt >  basic_string& assign( InputIt first, InputIt last ); | (9) | (constexpr since C++20) |
| basic_string& assign( std::initializer_list<CharT> ilist ); | (10) | (since C++11)  (constexpr since C++20) |
|  |  |  |

Replaces the contents of the string.

1) Equivalent to return \*this = str;.2) Equivalent to return \*this = std::move(str);.3) Replaces the contents with count copies of character ch. Equivalent to clear(); resize(n, c); return \*this;.4) Replaces the contents with copies of the characters in the range ``s`,`s + count`)`. If `[`s`,`s + count`)` is not a [valid range, the behavior is undefined.5) Equivalent to return assign(s, Traits::length(s));.6,7) Replaces the contents with characters in a string view sv constructed from t.

- If only t is provided, replaces the contents with all characters in sv.
- If pos is also provided:
  - If count is `npos`, replaces the contents with all characters in sv starting from pos.
  - Otherwise, replaces the contents with the std::min(count, sv.size() - pos) characters in sv starting from pos.
 These overloads participate in overload resolution only if all following conditions are satisfied:

- std::is_convertible_v<const SV&, std::basic_string_view<CharT, Traits>> is true.
- std::is_convertible_v<const SV&, const CharT\*> is false.
6) Equivalent to std::basic_string_view<CharT, Traits> sv = t;  
return assign(sv.data(), sv.size());.7) Equivalent to std::basic_string_view<CharT, Traits> sv = t;  
return assign(sv.substr(pos, count));.8) Replaces the contents with characters in str.

- If count is `npos`, replaces the contents with all characters in str starting from pos.
- Otherwise, replaces the contents with the std::min(count, str.size() - pos) characters in str starting from pos.

|  |  |
| --- | --- |
| Equivalent to return assign(std::basic_string_view<CharT, Traits>                   (str).substr(pos, count));. | (since C++20) |

9) Equivalent to return assign(basic_string(first, last, get_allocator()));.

|  |  |
| --- | --- |
| This overload participates in overload resolution only if `InputIt` satisfies the requirements of LegacyInputIterator. | (since C++11) |

10) Equivalent to return assign(ilist.begin(), ilist.size());.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | string to be used as source to initialize the characters with |
| count | - | size of the resulting string |
| ch | - | value to initialize characters of the string with |
| s | - | pointer to a character string to use as source to initialize the string with |
| t | - | object (convertible to std::basic_string_view) to initialize the characters of the string with |
| pos | - | index of the first character to take |
| first, last | - | range to copy the characters from |
| ilist | - | std::initializer_list to initialize the characters of the string with |

### Return value

\*this

### Exceptions

2)noexcept specification:noexcept(std::allocator_traits<Allocator>::  

propagate_on_container_move_assignment::value ||

std::allocator_traits<Allocator>::is_always_equal::value)

If the operation would cause `size()` to exceed `max_size()`, throws std::length_error.

7) If pos > sv.size() is true, throws std::out_of_range.8) If pos > str.size() is true, throws std::out_of_range.

If an exception is thrown for any reason, this function has no effect (strong exception safety guarantee).

### Example

Run this code

```
#include <iostream>
#include <iterator>
#include <string>
 
int main()
{
    std::string s;
    // assign(size_type count, CharT ch)
    s.assign(4, '=');
    std::cout << s << '\n'; // "===="
 
    std::string const c("Exemplary");
    // assign(const basic_string& str)
    s.assign(c);
    std::cout << c << " == " << s << '\n'; // "Exemplary == Exemplary"
 
    // assign(const basic_string& str, size_type pos, size_type count)
    s.assign(c, 0, c.length() - 1);
    std::cout << s << '\n'; // "Exemplar";
 
    // assign(basic_string&& str)
    s.assign(std::string("C++ by ") + "example");
    std::cout << s << '\n'; // "C++ by example"
 
    // assign(const CharT* s, size_type count)
    s.assign("C-style string", 7);
    std::cout << s << '\n'; // "C-style"
 
    // assign(const CharT* s)
    s.assign("C-style\0string");
    std::cout << s << '\n'; // "C-style"
 
    char mutable_c_str[] = "C-style string";
    // assign(InputIt first, InputIt last)
    s.assign(std::begin(mutable_c_str), std::end(mutable_c_str) - 1);
    std::cout << s << '\n'; // "C-style string"
 
    // assign(std::initializer_list<CharT> ilist)
    s.assign({'C', '-', 's', 't', 'y', 'l', 'e'});
    std::cout << s << '\n'; // "C-style"
}

```

Output:

```
====
Exemplary == Exemplary
Exemplar
C++ by example
C-style
C-style
C-style string
C-style

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 847 | C++98 | there was no exception safety guarantee | added strong exception safety guarantee |
| LWG 2063 | C++11 | non-normative note stated that overload (2) can be implemented by swapping | corrected to require move assignment |
| LWG 2250 | C++98 | the behavior of overload (8) was undefined if pos > str.size() is true | always throws an exception in this case |
| LWG 2579 | C++98 | overload (1) and the copy assignment operator had different effects | they have the same effect |
| LWG 2946 | C++17 | overload (6) caused ambiguity in some cases | avoided by making it a template |

### See also

|  |  |
| --- | --- |
| assign_range(C++23) | assign a range of characters to a string   (public member function) |
| (constructor) | constructs a `basic_string`   (public member function) |
| operator= | assigns values to the string   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/assign&oldid=178467>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 December 2024, at 23:14.