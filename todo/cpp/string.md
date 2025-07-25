# Strings library

From cppreference.com
< cpp
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
| ****Strings library**** | | | | |
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

****Strings library****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_string | | | | |
| basic_string_view(C++17) | | | | |
| char_traits | | | | |

### Characters

In the C++ standard library, a **character** is an object which, when treated sequentially, can represent text.

The term means not only objects of character types, but also any value that can be represented by a type that provides the definitions specified in the strings library and following libraries:

- localization library
- input/output library

|  |  |
| --- | --- |
| - regular expressions library | (since C++11) |

In the strings library and regular expressions library(since C++11), a character can be of only **char-like types**, i.e. those non-array types that satisfy the requirements of
PODType(until C++20)TrivialType and StandardLayoutType(since C++20)(until C++26)TriviallyCopyable and StandardLayoutType(since C++26).

|  |  |
| --- | --- |
| For any char-like type `T`, std::is_trivially_default_constructible_v<T> is true. | (since C++26) |

Therefore, characters are also referred as **char-like objects** in the strings library and regular expressions library(since C++11).

Some standard library components accept **character container types**. They, too, are types used to represent individual characters. Such types are used for one of the template arguments of std::char_traits and the class templates which use std::char_traits.

### Library components

The C++ strings library includes the following components:

#### Character traits

Many character-related class templates (such as std::basic_string) need a set of related types and functions to complete the definition of their semantics. These types and functions are provided as a set of member typedef names and functions in the template parameter `Traits` used by each such template. The classes which are able to complete those semantics are CharTraits.

The string library provides the class template std::char_traits that defines types and functions for std::basic_string and std::basic_string_view(since C++17).

The following specializations are defined, all of them satisfy the CharTraits requirements:

|  |  |  |
| --- | --- | --- |
| Defined in header `<string>` |  |  |
| template<> class char_traits<char>; |  |  |
| template<> class char_traits<wchar_t>; |  |  |
| template<> class char_traits<char8_t>; |  | (since C++20) |
| template<> class char_traits<char16_t>; |  | (since C++11) |
| template<> class char_traits<char32_t>; |  | (since C++11) |
|  |  |  |

When a user-defined character container type for std::basic_string and std::basic_string_view(since C++17) is used, it is also necessary to provide a corresponding character trait class (which can be a specialization of std::char_traits).

#### String classes (std::string etc.)

The class template std::basic_string generalizes how sequences of characters are manipulated and stored. String creation, manipulation, and destruction are all handled by a convenient set of class methods and related functions.

Several specializations of std::basic_string are provided for commonly-used types:

|  |  |
| --- | --- |
| Defined in header `<string>` | |
| Type | Definition |
| `std::string` | std::basic_string<char> |
| `std::wstring` | std::basic_string<wchar_t> |
| `std::u8string` (since C++20) | std::basic_string<char8_t> |
| `std::u16string` (since C++11) | std::basic_string<char16_t> |
| `std::u32string` (since C++11) | std::basic_string<char32_t> |

#### String view classes (std::string_view etc.) (since C++17)

The class template std::basic_string_view provides a lightweight object that offers read-only access to a string or a part of a string using an interface similar to the interface of std::basic_string.

Several specializations of std::basic_string_view are provided for commonly-used types:

|  |  |
| --- | --- |
| Defined in header `<string_view>` | |
| Type | Definition |
| `std::string_view` | std::basic_string_view<char> |
| `std::wstring_view` | std::basic_string_view<wchar_t> |
| `std::u8string_view` (since C++20) | std::basic_string_view<char8_t> |
| `std::u16string_view` | std::basic_string_view<char16_t> |
| `std::u32string_view` | std::basic_string_view<char32_t> |

### Relevant libraries

The text processing library provides support for localizations, string conversions (e.g. std::toupper), character classification functions (e.g. std::isspace), and text encoding recognition (std::text_encoding).

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 1170 | C++98 | char-like types could be array types | prohibited |

### See also

|  |  |
| --- | --- |
| C documentation for Strings library | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string&oldid=179902>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 11:14.