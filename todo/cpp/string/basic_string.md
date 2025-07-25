# std::basic_string

From cppreference.com
< cpp‎ | string
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
| ****basic_string**** | | | | |
| basic_string_view(C++17) | | | | |
| char_traits | | | | |

****std::basic_string****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](basic_string/operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string>` |  |  |
| template<  class CharT,      class Traits = std::char_traits<CharT>,      class Allocator = std::allocator<CharT> > class basic_string; | (1) |  |
| namespace pmr {  template<      class CharT,      class Traits = std::char_traits<CharT>  > using basic_string =      std::basic_string<CharT, Traits, std::pmr::polymorphic_allocator<CharT>>; } | (2) | (since C++17) |
|  |  |  |

The class template `basic_string` stores and manipulates sequences of character-like objects, which are non-array objects of TrivialType and StandardLayoutType. The class is dependent neither on the character type nor on the nature of operations on that type. The definitions of the operations are supplied via the `Traits` template parameter - a specialization of std::char_traits or a compatible traits class.

The elements of a `basic_string` are stored contiguously, that is, for a `basic_string` s, &\*(s.begin() + n) == &\*s.begin() + n for any n in `[`​0​`,`s.size()`)`, and \*(s.begin() + s.size()) has value CharT() (a null terminator)(since C++11); or, equivalently, a pointer to s[0] can be passed to functions that expect a pointer to the first element of an array(until C++11)a null-terminated array(since C++11) of `CharT`.

`std::basic_string` satisfies the requirements of AllocatorAwareContainer (except that customized `construct`/`destroy` are not used for construction/destruction of elements), SequenceContainer and ContiguousContainer(since C++17).

If any of `Traits::char_type` and `Allocator::char_type` is different from `CharT`, the program is ill-formed.

|  |  |
| --- | --- |
| Member functions of `std::basic_string` are constexpr: it is possible to create and use `std::string` objects in the evaluation of a constant expression.  However, `std::string` objects generally cannot be constexpr, because any dynamically allocated storage must be released in the same evaluation of constant expression. | (since C++20) |

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<string>` | |
| Type | Definition |
| `std::string` | std::basic_string<char> |
| `std::wstring` | std::basic_string<wchar_t> |
| `std::u8string` (C++20) | std::basic_string<char8_t> |
| `std::u16string` (C++11) | std::basic_string<char16_t> |
| `std::u32string` (C++11) | std::basic_string<char32_t> |
| `std::pmr::string` (C++17) | std::pmr::basic_string<char> |
| `std::pmr::wstring` (C++17) | std::pmr::basic_string<wchar_t> |
| `std::pmr::u8string` (C++20) | std::pmr::basic_string<char8_t> |
| `std::pmr::u16string` (C++17) | std::pmr::basic_string<char16_t> |
| `std::pmr::u32string` (C++17) | std::pmr::basic_string<char32_t> |

### Template parameters

|  |  |  |
| --- | --- | --- |
| CharT | - | character type |
| Traits | - | traits class specifying the operations on the character type |
| Allocator | - | Allocator type used to allocate internal storage |

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `traits_type` | `Traits` |
| `value_type` | `CharT` |
| `allocator_type` | `Allocator` |
| `size_type` | |  |  | | --- | --- | | `Allocator::size_type` | (until C++11) | | std::allocator_traits<Allocator>::size_type | (since C++11) | |
| `difference_type` | |  |  | | --- | --- | | Allocator::difference_type | (until C++11) | | std::allocator_traits<Allocator>::difference_type | (since C++11) | |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `pointer` | |  |  | | --- | --- | | `Allocator::pointer` | (until C++11) | | std::allocator_traits<Allocator>::pointer | (since C++11) | |
| `const_pointer` | |  |  | | --- | --- | | `Allocator::const_pointer` | (until C++11) | | std::allocator_traits<Allocator>::const_pointer | (since C++11) | |
| `iterator` | |  |  | | --- | --- | | LegacyRandomAccessIterator and LegacyContiguousIterator to `value_type` | (until C++20) | | LegacyRandomAccessIterator, `contiguous_iterator`, and ConstexprIterator to `value_type` | (since C++20) | |
| `const_iterator` | |  |  | | --- | --- | | LegacyRandomAccessIterator and LegacyContiguousIterator to const value_type | (until C++20) | | LegacyRandomAccessIterator, `contiguous_iterator`, and ConstexprIterator to const value_type | (since C++20) | |
| `reverse_iterator` | std::reverse_iterator<iterator> |
| `const_reverse_iterator` | std::reverse_iterator<const_iterator> |

### Data members

|  |  |
| --- | --- |
| constexpr size_type `npos` [static] | the special value size_type(-1), its exact meaning depends on the context |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_string`   (public member function) |
| (destructor) | destroys the string, deallocating internal storage if used   (public member function) |
| operator= | assigns values to the string   (public member function) |
| assign | assign characters to a string   (public member function) |
| assign_range(C++23) | assign a range of characters to a string   (public member function) |
| get_allocator | returns the associated allocator   (public member function) |
| Element access | |
| at | accesses the specified character with bounds checking   (public member function) |
| [operator[]](basic_string/operator_at.html "cpp/string/basic string/operator at") | accesses the specified character   (public member function) |
| front(DR\*) | accesses the first character   (public member function) |
| back(DR\*) | accesses the last character   (public member function) |
| data | returns a pointer to the first character of a string   (public member function) |
| c_str | returns a non-modifiable standard C character array version of the string   (public member function) |
| operator basic_string_view(C++17) | returns a non-modifiable `basic_string_view` into the entire string   (public member function) |
| Iterators | |
| begincbegin(C++11) | returns an iterator to the beginning   (public member function) |
| endcend(C++11) | returns an iterator to the end   (public member function) |
| rbegincrbegin(C++11) | returns a reverse iterator to the beginning   (public member function) |
| rendcrend(C++11) | returns a reverse iterator to the end   (public member function) |
| Capacity | |
| empty | checks whether the string is empty   (public member function) |
| sizelength | returns the number of characters   (public member function) |
| max_size | returns the maximum number of characters   (public member function) |
| reserve | reserves storage   (public member function) |
| capacity | returns the number of characters that can be held in currently allocated storage   (public member function) |
| shrink_to_fit(DR\*) | reduces memory usage by freeing unused memory   (public member function) |
| Modifiers | |
| clear | clears the contents   (public member function) |
| insert | inserts characters   (public member function) |
| insert_range(C++23) | inserts a range of characters   (public member function) |
| erase | removes characters   (public member function) |
| push_back | appends a character to the end   (public member function) |
| pop_back(DR\*) | removes the last character   (public member function) |
| append | appends characters to the end   (public member function) |
| append_range(C++23) | appends a range of characters to the end   (public member function) |
| operator+= | appends characters to the end   (public member function) |
| replace | replaces specified portion of a string   (public member function) |
| replace_with_range(C++23) | replaces specified portion of a string with a range of characters   (public member function) |
| copy | copies characters   (public member function) |
| resize | changes the number of characters stored   (public member function) |
| resize_and_overwrite(C++23) | changes the number of characters stored and possibly overwrites indeterminate contents via user-provided operation   (public member function) |
| swap | swaps the contents   (public member function) |
| Search | |
| find | finds the first occurrence of the given substring   (public member function) |
| rfind | find the last occurrence of a substring   (public member function) |
| find_first_of | find first occurrence of characters   (public member function) |
| find_first_not_of | find first absence of characters   (public member function) |
| find_last_of | find last occurrence of characters   (public member function) |
| find_last_not_of | find last absence of characters   (public member function) |
| Operations | |
| compare | compares two strings   (public member function) |
| starts_with(C++20) | checks if the string starts with the given prefix   (public member function) |
| ends_with(C++20) | checks if the string ends with the given suffix   (public member function) |
| contains(C++23) | checks if the string contains the given substring or character   (public member function) |
| substr | returns a substring   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator+ | concatenates two strings, a string and a char, or a string and string_view   (function template) |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares two strings   (function template) |
| std::swap(std::basic_string) | specializes the std::swap algorithm   (function template) |
| erase(std::basic_string)erase_if(std::basic_string)(C++20) | erases all elements satisfying specific criteria   (function template) |
| Input/output | |
| operator<<operator>> | performs stream input and output on strings   (function template) |
| getline | read data from an I/O stream into a string   (function template) |
| Numeric conversions | |
| stoistolstoll(C++11)(C++11)(C++11) | converts a string to a signed integer   (function) |
| stoulstoull(C++11)(C++11) | converts a string to an unsigned integer   (function) |
| stofstodstold(C++11)(C++11)(C++11) | converts a string to a floating point value   (function) |
| to_string(C++11) | converts an integral or floating-point value to `string`   (function) |
| to_wstring(C++11) | converts an integral or floating-point value to `wstring`   (function) |

### Literals

|  |  |
| --- | --- |
| Defined in inline namespace `std::literals::string_literals` | |
| operator""s(C++14) | converts a character array literal to `basic_string`   (function) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::basic_string>(C++11) | hash support for strings   (class template specialization) |

### Deduction guides (since C++17)

### Iterator invalidation

References, pointers, and iterators referring to the elements of a `basic_string` may be invalidated by any standard library function taking a reference to non-const `basic_string` as an argument, such as std::getline, std::swap, or operator>>, and by calling non-const member functions, except [operator[]](basic_string/operator_at.html "cpp/string/basic string/operator at"), `at`, `data`, `front`, `back`, `begin`, `rbegin`, `end`, and `rend`.

### Notes

Although it is required that customized `construct` or `destroy` is used when constructing or destroying elements of `std::basic_string` until C++23, all implementations only used the default mechanism. The requirement is corrected by P1072R10 to match existing practice.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_string_udls` | `201304L` | (C++14) | User-defined literals for string types |
| `__cpp_lib_starts_ends_with` | `201711L` | (C++20) | `starts_with`, `ends_with` |
| `__cpp_lib_constexpr_string` | `201907L` | (C++20) | Constexpr for `std::basic_string` |
| `__cpp_lib_char8_t` | `201907L` | (C++20) | `std::u8string` |
| `__cpp_lib_erase_if` | `202002L` | (C++20) | `erase`, `erase_if` |
| `__cpp_lib_string_contains` | `202011L` | (C++23) | `contains` |
| `__cpp_lib_string_resize_and_overwrite` | `202110L` | (C++23) | `resize_and_overwrite` |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Member functions for construction, insertion, and replacement that accept container compatible range |

### Example

Run this code

```
#include <iostream>
#include <string>
 
int main()
{
    using namespace std::literals;
 
    // Creating a string from const char*
    std::string str1 = "hello";
 
    // Creating a string using string literal
    auto str2 = "world"s;
 
    // Concatenating strings
    std::string str3 = str1 + " " + str2;
 
    // Print out the result
    std::cout << str3 << '\n';
 
    std::string::size_type pos = str3.find(" ");
    str1 = str3.substr(pos + 1); // the part after the space
    str2 = str3.substr(0, pos);  // the part till the space
 
    std::cout << str1 << ' ' << str2 << '\n';
 
    // Accessing an element using subscript operator[]
    std::cout << str1[0] << '\n';
    str1[0] = 'W';
    std::cout << str1 << '\n';
}

```

Output:

```
hello world
world hello
w
World

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 530 | C++98 | contiguity of the storage for elements of `basic_string` was accidently made not required by LWG259 | required again |
| LWG 2861 | C++98 | `value_type` was `Traits::char_type` | changed to `CharT` |
| LWG 2994 (P1148R0) | C++98 | the behavior is undefined if any of `Traits::char_type`[[1]](basic_string.html#cite_note-1) and `Allocator::char_type` is different from `CharT` | the program is ill-formed in this case |

1. ↑ The `Traits::char_type` case is fixed in P1148R0.

### See also

|  |  |
| --- | --- |
| basic_string_view(C++17) | read-only string view   (class template) |

### External links

|  |
| --- |
| C++ string handling |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string&oldid=177591>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 November 2024, at 18:05.