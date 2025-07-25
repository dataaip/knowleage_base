# std::basic_string<CharT,Traits,Allocator>::basic_string

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | ****basic_string::basic_string**** | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | basic_string::resize_and_overwrite(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| basic_string() : basic_string(Allocator()) {} |  | (since C++11)  (until C++17) |
| basic_string() noexcept(noexcept(Allocator()))      : basic_string(Allocator()) {} |  | (since C++17)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| explicit basic_string( const Allocator& alloc = Allocator() ); |  | (until C++11) |
| explicit basic_string( const Allocator& alloc ); |  | (noexcept since C++17)  (constexpr since C++20) |
|  |  |  |
| --- | --- | --- |
| basic_string( size_type count, CharT ch,                const Allocator& alloc = Allocator() ); | (3) | (constexpr since C++20) |
| template< class InputIt >  basic_string( InputIt first, InputIt last, const Allocator& alloc = Allocator() ); | (4) | (constexpr since C++20) |
| template< container-compatible-range<CharT> R >  constexpr basic_string( std::from_range_t, R&& rg, const Allocator& = Allocator()); | (5) | (since C++23) |
| basic_string( const CharT\* s, size_type count,                const Allocator& alloc = Allocator() ); | (6) | (constexpr since C++20) |
| basic_string( const CharT\* s, const Allocator& alloc = Allocator() ); | (7) | (constexpr since C++20) |
| basic_string( std::nullptr_t ) = delete; | (8) | (since C++23) |
| template< class StringViewLike >  explicit basic_string( const StringViewLike& t, const Allocator& alloc = Allocator() ); | (9) | (since C++17)  (constexpr since C++20) |
| template< class StringViewLike >  basic_string( const StringViewLike& t,                size_type pos, size_type count, const Allocator& alloc = Allocator() ); | (10) | (since C++17) |
| basic_string( const basic_string& other ); | (11) | (constexpr since C++20) |
| basic_string( basic_string&& other ) noexcept; | (12) | (since C++11)  (constexpr since C++20) |
| basic_string( const basic_string& other, const Allocator& alloc ); | (13) | (since C++11)  (constexpr since C++20) |
| basic_string( basic_string&& other, const Allocator& alloc ); | (14) | (since C++11)  (constexpr since C++20) |
| basic_string( const basic_string& other, size_type pos,                const Allocator& alloc = Allocator() ); | (15) | (constexpr since C++20) |
| constexpr basic_string( basic_string&& other, size_type pos,                          const Allocator& alloc = Allocator() ); | (16) | (since C++23) |
| basic_string( const basic_string& other,                size_type pos, size_type count, const Allocator& alloc = Allocator() ); | (17) | (constexpr since C++20) |
| constexpr basic_string( basic_string&& other,                          size_type pos, size_type count, const Allocator& alloc = Allocator() ); | (18) | (since C++23) |
| basic_string( std::initializer_list<CharT> ilist,                const Allocator& alloc = Allocator() ); | (19) | (since C++11)  (constexpr since C++20) |
|  |  |  |

Constructs new string from a variety of data sources and optionally using user supplied allocator alloc.

1) The default constructor since C++11. Constructs an empty string with a default-constructed allocator. If Allocator is not DefaultConstructible, the behavior is undefined.2) The default constructor until C++11. Constructs an empty string with the given allocator alloc.3) Constructs a string with count copies of character ch.

|  |  |
| --- | --- |
| If `CharT` is not CopyInsertable into std::basic_string<CharT>, the behavior is undefined. | (since C++11) |
| This overload participates in overload resolution only if `Allocator` satisfies the requirements of Allocator. | (since C++17) |

4) Constructs a string with the contents of the range ``first`,`last`)`. Each iterator in `[`first`,`last`)` is dereferenced exactly once.

|  |  |
| --- | --- |
| If `InputIt` does not satisfy the requirements of [LegacyInputIterator, overload (3) is called instead with arguments static_cast<size_type>(first), last and alloc. | (until C++11) |
| This overload participates in overload resolution only if `InputIt` satisfies the requirements of LegacyInputIterator.  If `CharT` is not EmplaceConstructible into std::basic_string<CharT> from \*first, the behavior is undefined. | (since C++11) |

5) Constructs a string with the contents of the range rg. Each iterator in rg is dereferenced exactly once. If `CharT` is not EmplaceConstructible into std::basic_string<CharT> from \*ranges::begin(rg), the behavior is undefined.6) Constructs a string with the contents of the range ``s`,`s + count`)`. If `[`s`,`s + count`)` is not a valid range, the behavior is undefined.7) Equivalent to basic_string(s, Traits::length(s), alloc).

|  |  |
| --- | --- |
| This overload participates in overload resolution only if `Allocator` satisfies the requirements of [Allocator. | (since C++17) |

8) `std::basic_string` cannot be constructed from nullptr.9) Implicitly converts t to a string view sv as if by std::basic_string_view<CharT, Traits> sv = t;, then constructs a string as if by basic_string(sv.data(), sv.size(), alloc). This overload participates in overload resolution only if std::is_convertible_v<const StringViewLike&,  
                      std::basic_string_view<CharT, Traits>> is true and std::is_convertible_v<const StringViewLike&, const CharT\*> is false.10) Implicitly converts t to a string view sv as if by std::basic_string_view<CharT, Traits> sv = t;, then constructs a string as if by basic_string(sv.substr(pos, n), alloc). This overload participates in overload resolution only if std::is_convertible_v<const StringViewLike&,  
                      std::basic_string_view<CharT, Traits>> is true.11-18) Constructs a string with (part of) the contents of other. If the type of other is `basic_string&&`, when the construction finishes, other is in a valid but unspecified state.11) The copy constructor.

|  |  |
| --- | --- |
| The allocator is obtained as if by calling std::allocator_traits<Allocator>::     select_on_container_copy_construction         (other.get_allocator()). | (since C++11) |

12) The move constructor. The allocator is obtained by move construction from other.get_allocator().13) Same as the copy constructor, except that alloc is used as the allocator. If `CharT` is not CopyInsertable into std::basic_string<CharT>, the behavior is undefined.14) Same as the move constructor, except that alloc is used as the allocator. If `CharT` is not MoveInsertable into std::basic_string<CharT>, the behavior is undefined.15,16) Constructs a string with the contents of the range ``other.data() + pos`,`other.data() + other.size()`)`.17,18) Constructs a string with the contents of the range `[`other.data() + pos`,`other.data() + (pos + [std::min(count, other.size() - pos))`)`.19) Equivalent to basic_string(ilist.begin(), ilist.end()).

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use for all memory allocations of this string |
| count | - | size of the resulting string |
| ch | - | value to initialize the string with |
| pos | - | position of the first character to include |
| first, last | - | range to copy the characters from |
| s | - | pointer to an array of characters to use as source to initialize the string with |
| other | - | another string to use as source to initialize the string with |
| ilist | - | std::initializer_list to initialize the string with |
| t | - | object (convertible to std::basic_string_view) to initialize the string with |
| rg | - | a container compatible range |

### Complexity

1,2) Constant.3-7) Linear in the size of the string.9-11) Linear in the size of the string.12) Constant.13) Linear in the size of the string.14) Linear in the size of the string if alloc != other.get_allocator() is true, otherwise constant.15-19) Linear in the size of the string.

### Exceptions

10) std::out_of_range if pos is out of range.14) Throws nothing if alloc == str.get_allocator() is true.15-18) std::out_of_range if pos > other.size() is true.

Throws std::length_error if the length of the constructed string would exceed max_size() (for example, if count > max_size() for (3)). Calls to `Allocator::allocate` may throw.

If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).

### Notes

Initialization with a string literal that contains embedded '\0' characters uses the overload (7), which stops at the first null character. This can be avoided by specifying a different constructor or by using `operator""s`:

```
std::string s1 = "ab\0\0cd";   // s1 contains "ab"
std::string s2{"ab\0\0cd", 6}; // s2 contains "ab\0\0cd"
std::string s3 = "ab\0\0cd"s;  // s3 contains "ab\0\0cd"

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Tagged constructor (5) to construct from container compatible range |

### Example

Run this code

```
#include <cassert>
#include <cctype>
#include <iomanip>
#include <iostream>
#include <iterator>
#include <string>
 
int main()
{
    std::cout << "1)  string(); ";
    std::string s1;
    assert(s1.empty() && (s1.length() == 0) && (s1.size() == 0));
    std::cout << "s1.capacity(): " << s1.capacity() << '\n'; // unspecified
 
    std::cout << "3)  string(size_type count, CharT ch): ";
    std::string s2(4, '=');
    std::cout << std::quoted(s2) << '\n'; // "===="
 
    std::cout << "4)  string(InputIt first, InputIt last): ";
    char mutable_c_str[] = "another C-style string";
    std::string s4(std::begin(mutable_c_str) + 8, std::end(mutable_c_str) - 1);
    std::cout << std::quoted(s4) << '\n'; // "C-style string"
 
    std::cout << "6)  string(CharT const* s, size_type count): ";
    std::string s6("C-style string", 7);
    std::cout << std::quoted(s6) << '\n'; // "C-style", i.e. 0, 7)
 
    std::cout << "7)  string(CharT const* s): ";
    std::string s7("C-style\0string");
    std::cout << std::quoted(s7) << '\n'; // "C-style"
 
    std::cout << "11) string(string&): ";
    std::string const other11("Exemplar");
    std::string s11(other11);
    std::cout << std::quoted(s11) << '\n'; // "Exemplar"
 
    std::cout << "12) string(string&&): ";
    std::string s12(std::string("C++ by ") + std::string("example"));
    std::cout << std::quoted(s12) << '\n'; // "C++ by example"
 
    std::cout << "15) string(const string& other, size_type pos): ";
    std::string const other15("Mutatis Mutandis");
    std::string s15(other15, 8);
    std::cout << std::quoted(s15) << '\n'; // "Mutandis", i.e. [8, 16)
 
    std::cout << "17) string(const string& other, size_type pos, size_type count): ";
    std::string const other17("Exemplary");
    std::string s17(other17, 0, other17.length() - 1);
    std::cout << std::quoted(s17) << '\n'; // "Exemplar"
 
    std::cout << "19) string(std::initializer_list<CharT>): ";
    std::string s19({'C', '-', 's', 't', 'y', 'l', 'e'});
    std::cout << std::quoted(s19) << '\n'; // "C-style"
}

```

Possible output:

```
1)  string(); s1.capacity(): 15
3)  string(size_type count, CharT ch): "===="
4)  string(InputIt first, InputIt last): "C-style string"
6)  string(CharT const* s, size_type count): "C-style"
7)  string(CharT const* s): "C-style"
11) string(string&): "Exemplar"
12) string(string&&): "C++ by example"
15) string(const string& other, size_type pos): "Mutandis"
17) string(const string& other, size_type pos, size_type count): "Exemplar"
19) string(std::initializer_list<CharT>): "C-style"

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| [LWG 301 | C++98 | overload (4) did not use the parameter alloc if `InputIt` is an integral type | use that parameter |
| LWG 438 | C++98 | overload (4) would only call overload (3) if `InputIt` is an integral type | calls overload (3) if `InputIt` is not an LegacyInputIterator |
| LWG 847 | C++98 | there was no exception safety guarantee | added strong exception safety guarantee |
| LWG 2193 | C++11 | the default constructor is explicit | made non-explicit |
| LWG 2235 | C++98 | s could be a null pointer value | the behavior is undefined in this case |
| LWG 2250 | C++98 | the behavior of overload (17) was undefined if pos > other.size() is true | always throws an exception in this case |
| LWG 2583 | C++98 | there was no way to supply an allocator for overload (17) | added overload (15) |
| LWG 2946 | C++17 | overload (9) causes ambiguity in some cases | avoided by making it a template |
| LWG 3076 | C++17 | overloads (3,7) might cause ambiguities in class template argument deduction | constrained |
| LWG 3111 (P1148R0) | C++98 | the resolution of LWG issue 2235 made the behavior of basic_string(nullptr, 0) undefined | the behavior is well- defined in this case[[1]](basic_string.html#cite_note-1) |

1. ↑ ``nullptr`,`nullptr + 0`)` is a valid empty range, because adding zero to a null pointer value is also [well-defined (the result is still a null pointer value).

### See also

|  |  |
| --- | --- |
| assign | assign characters to a string   (public member function) |
| operator= | assigns values to the string   (public member function) |
| to_string(C++11) | converts an integral or floating-point value to `string`   (function) |
| to_wstring(C++11) | converts an integral or floating-point value to `wstring`   (function) |
| (constructor) | constructs a `basic_string_view`   (public member function of `std::basic_string_view<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/basic_string&oldid=178329>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 December 2024, at 00:42.