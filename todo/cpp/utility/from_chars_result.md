# std::from_chars_result

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | ****from_chars_result****(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<charconv>` |  |  |
| struct from_chars_result; |  | (since C++17) |
|  |  |  |

`std::from_chars_result` is the return type of std::from_chars. It has no base classes, and only has the following members.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| ptr | a pointer of type const char\*   (public member object) |
| ec | an error code of type std::errc   (public member object) |

### Member and friend functions

## operator==(std::from_chars_result)

|  |  |  |
| --- | --- | --- |
| friend bool operator==( const from_chars_result&,                          const from_chars_result& ) = default; |  | (since C++20) |
|  |  |  |

Compares the two arguments using default comparisons (which uses operator== to compare `ptr` and `ec` respectively).

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when std::from_chars_result is an associated class of the arguments.

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
#include <cassert>
#include <charconv>
#include <iomanip>
#include <iostream>
#include <optional>
#include <string_view>
#include <system_error>
 
int main()
{
    for (std::string_view const str : {"1234", "15 foo", "bar", " 42", "5000000000"})
    {
        std::cout << "String: " << std::quoted(str) << ". ";
        int result{};
        auto [ptr, ec] = std::from_chars(str.data(), str.data() + str.size(), result);
 
        if (ec == std::errc())
            std::cout << "Result: " << result << ", ptr -> " << std::quoted(ptr) << '\n';
        else if (ec == std::errc::invalid_argument)
            std::cout << "This is not a number.\n";
        else if (ec == std::errc::result_out_of_range)
            std::cout << "This number is larger than an int.\n";
    }
 
    // C++23's constexpr from_char demo / C++26's operator bool() demo:
    auto to_int = [](std::string_view s) -> std::optional<int>
    {
        int value{};
#if __cpp_lib_to_chars >= 202306L
        if (std::from_chars(s.data(), s.data() + s.size(), value))
#else
        if (std::from_chars(s.data(), s.data() + s.size(), value).ec == std::errc{})
#endif
            return value;
        else
            return std::nullopt;
    };
 
    assert(to_int("42") == 42);
    assert(to_int("foo") == std::nullopt);
#if __cpp_lib_constexpr_charconv and __cpp_lib_optional >= 202106
    static_assert(to_int("42") == 42);
    static_assert(to_int("foo") == std::nullopt);
#endif
}

```

Output:

```
String: "1234". Result: 1234, ptr -> ""
String: "15 foo". Result: 15, ptr -> " foo"
String: "bar". This is not a number.
String: " 42". This is not a number.
String: "5000000000". This number is larger than an int.

```

### See also

|  |  |
| --- | --- |
| from_chars(C++17) | converts a character sequence to an integer or floating-point value   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/from_chars_result&oldid=179104>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 21:56.