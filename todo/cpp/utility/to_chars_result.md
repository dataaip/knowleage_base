# std::to_chars_result

From cppreference.com
< cpp‎ | utility
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

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | ****to_chars_result****(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<charconv>` |  |  |
| struct to_chars_result; |  | (since C++17) |
|  |  |  |

`std::to_chars_result` is the return type of std::to_chars. It has no base classes, and only has the following members.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| ptr | a pointer of type char\*   (public member object) |
| ec | an error code of type std::errc   (public member object) |

### Member and friend functions

## operator==(std::to_chars_result)

|  |  |  |
| --- | --- | --- |
| friend bool operator==( const to_chars_result&,                          const to_chars_result& ) = default; |  | (since C++20) |
|  |  |  |

Compares the two arguments using default comparisons (which uses operator== to compare `ptr` and `ec` respectively).

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when std::to_chars_result is an associated class of the arguments.

The `!=` operator is synthesized from `operator==`.

## operator bool

|  |  |  |
| --- | --- | --- |
| constexpr explicit operator bool() const noexcept; |  | (since C++26) |
|  |  |  |

Checks whether the conversion is successful. Returns ec == std::errc{}.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_to_chars` | `201611L` | (C++17) | Elementary string conversions (std::to_chars, std::from_chars) |
| `202306L` | (C++26) | Testing for success or failure of <charconv> functions |

### Example

Run this code

```
#include <array>
#include <charconv>
#include <iostream>
#include <string_view>
#include <system_error>
 
void show_to_chars(auto... format_args)
{
    std::array<char, 10> str;
 
#if __cpp_lib_to_chars >= 202306L and __cpp_structured_bindings >= 202406L
    // use C++26 structured bindings declaration as condition (P0963)
    // and C++26 to_chars_result::operator bool() for error checking (P2497)
    if (auto [ptr, ec] =
            std::to_chars(str.data(), str.data() + str.size(), format_args...))
        std::cout << std::string_view(str.data(), ptr) << '\n';
    else
        std::cout << std::make_error_code(ec).message() << '\n';
#elif __cpp_lib_to_chars >= 202306L
    // use C++26 to_chars_result::operator bool() for error checking (P2497)
    if (auto result =
            std::to_chars(str.data(), str.data() + str.size(), format_args...))
        std::cout << std::string_view(str.data(), result.ptr) << '\n';
    else
        std::cout << std::make_error_code(result.ec).message() << '\n';
#else
    // fallback to C++17 if-with-initializer and structured bindings
    if (auto [ptr, ec] =
            std::to_chars(str.data(), str.data() + str.size(), format_args...);
        ec == std::errc())
        std::cout << std::string_view(str.data(), ptr - str.data()) << '\n';
    else
        std::cout << std::make_error_code(ec).message() << '\n';
#endif
}
 
int main()
{
    show_to_chars(42);
    show_to_chars(+3.14159F);
    show_to_chars(-3.14159, std::chars_format::fixed);
    show_to_chars(-3.14159, std::chars_format::scientific, 3);
    show_to_chars(3.1415926535, std::chars_format::fixed, 10);
}

```

Possible output:

```
42
3.14159
-3.14159
-3.142e+00
Value too large for defined data type

```

### See also

|  |  |
| --- | --- |
| to_chars(C++17) | converts an integer or floating-point value to a character sequence   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/to_chars_result&oldid=179103>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 21:56.