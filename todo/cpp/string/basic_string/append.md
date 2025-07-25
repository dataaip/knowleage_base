# std::basic_string<CharT,Traits,Allocator>::append

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | ****basic_string::append**** | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| basic_string& append( size_type count, CharT ch ); | (1) | (constexpr since C++20) |
| basic_string& append( const CharT\* s, size_type count ); | (2) | (constexpr since C++20) |
| basic_string& append( const CharT\* s ); | (3) | (constexpr since C++20) |
| template< class SV >  basic_string& append( const SV& t ); | (4) | (since C++17)  (constexpr since C++20) |
| template< class SV >  basic_string& append( const SV& t, size_type pos,                       size_type count = npos ); | (5) | (since C++17)  (constexpr since C++20) |
| basic_string& append( const basic_string& str ); | (6) | (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (7) |  |
| basic_string& append( const basic_string& str,                        size_type pos, size_type count ); |  | (until C++14) |
| basic_string& append( const basic_string& str,                        size_type pos, size_type count = npos ); |  | (since C++14)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt >  basic_string& append( InputIt first, InputIt last ); | (8) | (constexpr since C++20) |
| basic_string& append( std::initializer_list<CharT> ilist ); | (9) | (since C++11)  (constexpr since C++20) |
|  |  |  |

Appends additional characters to the string.

1) Appends count copies of character ch.2) Appends characters in the range ``s`,`s + count`)`. If `[`s`,`s + count`)` is not a [valid range, the behavior is undefined.3) Equivalent to return append(s, Traits::length(s));.4,5) Appends characters in a string view sv constructed from t.

- If only t is provided, all characters in sv are appended.
- If pos is also provided:
  - If count is `npos`, all characters in sv starting from pos are appended.
  - Otherwise, the std::min(count, sv.size() - pos) characters in sv starting from pos are appended.
 These overloads participate in overload resolution only if all following conditions are satisfied:

- std::is_convertible_v<const SV&, std::basic_string_view<CharT, Traits>> is true.
- std::is_convertible_v<const SV&, const CharT\*> is false.
4) Equivalent to std::basic_string_view<CharT, Traits> sv = t;  
return append(sv.data(), sv.size());.5) Equivalent to std::basic_string_view<CharT, Traits> sv = t;  
return append(sv.substr(pos, count));.6,7) Appends characters in another string str.

- If only str is provided, all characters in it are appended.
- If pos is also provided:
  - If count is `npos`, all characters in str starting from pos are appended.
  - Otherwise, the std::min(count, str.size() - pos) characters in str starting from pos are appended.
6) Equivalent to return append(str.data(), str.size());.

|  |  |
| --- | --- |
| 7) Equivalent to return append(std::basic_string_view<CharT, Traits>                   (str).substr(pos, count));. | (since C++20) |

8) Equivalent to return append(basic_string(first, last, get_allocator()));.

|  |  |
| --- | --- |
| This overload has the same effect as overload (1) if `InputIt` is an integral type. | (until C++11) |
| This overload participates in overload resolution only if `InputIt` satisfies the requirements of LegacyInputIterator. | (since C++11) |

9) Equivalent to return append(ilist.begin(), ilist.size());.

### Parameters

|  |  |  |
| --- | --- | --- |
| count | - | number of characters to append |
| ch | - | character value to append |
| s | - | pointer to the character string to append |
| t | - | object convertible to std::basic_string_view with the characters to append |
| pos | - | the index of the first character to append |
| str | - | string to append |
| first, last | - | range of characters to append |
| ilist | - | initializer list with the characters to append |

### Return value

\*this

### Complexity

There are no standard complexity guarantees, typical implementations behave similar to std::vector::insert().

### Exceptions

If the operation would cause `size()` to exceed `max_size()`, throws std::length_error.

5) If pos > sv.size() is true, throws std::out_of_range.7) If pos > str.size() is true, throws std::out_of_range.

If an exception is thrown for any reason, this function has no effect (strong exception safety guarantee).

### Example

Run this code

```
#include <cassert>
#include <string>
 
int main()
{
    std::string str = "std::string";
    const char* cptr = "C-string";
    const char carr[] = "range";
 
    std::string result;
 
    // 1) Append a char 3 times.
    // Note: This is the only overload accepting “CharT”s.
    result.append(3, '*');
    assert(result == "***");
 
    // 2) Append a fixed-length C-string
    result.append(cptr, 5);
    assert(result == "***C-str");
 
    // 3) Append a null-terminated C-string
    // Note: Because “append” returns *this, we can chain calls together.
    result.append(1, ' ').append(cptr);
    assert(result == "***C-str C-string");
 
    // 6) Append a whole string
    result.append(1, ' ').append(str);
    assert(result == "***C-str C-string std::string");
 
    // 7) Append part of a string
    result.append(str, 3, 2);
    assert(result == "***C-str C-string std::string::");
 
    // 8) Append range
    result.append(&carr[2], &carr[3]);
    assert(result == "***C-str C-string std::string::n");
 
    // 9) Append initializer list
    result.append({'p', 'o', 's'});
    assert(result == "***C-str C-string std::string::npos");
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 847 | C++98 | there was no exception safety guarantee | added strong exception safety guarantee |
| LWG 2250 | C++98 | the behavior of overload (7) was undefined if pos > str.size() is true | always throws an exception in this case |
| LWG 2788 | C++98 | overload (8) used a default constructed allocator to construct the temporary string | obtains the allocator from get_allocator() |
| LWG 2946 | C++17 | overload (4) causes ambiguity in some cases | avoided by making it a template |

### See also

|  |  |
| --- | --- |
| append_range(C++23) | appends a range of characters to the end   (public member function) |
| operator+= | appends characters to the end   (public member function) |
| strcat | concatenates two strings   (function) |
| strncat | concatenates a certain amount of characters of two strings   (function) |
| wcscat | appends a copy of one wide string to another   (function) |
| wcsncat | appends a certain amount of wide characters from one wide string to another   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/append&oldid=178401>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 December 2024, at 07:09.