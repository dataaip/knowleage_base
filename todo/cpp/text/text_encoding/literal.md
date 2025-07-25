# std::text_encoding::literal

From cppreference.com
< cpp‎ | text‎ | text encoding
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

std::text_encoding

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| Creation | | | | |
| text_encoding::text_encoding") | | | | |
| ****text_encoding::literal**** | | | | |
| text_encoding::environment | | | | |
| Observers | | | | |
| text_encoding::mib | | | | |
| text_encoding::name | | | | |
| text_encoding::aliases | | | | |
| text_encoding::environment_is | | | | |
| Helpers | | | | |
| text_encoding::**comp-name** | | | | |
| Non-member functions | | | | |
| operator==(std::text_encoding) | | | | |
| Member types | | | | |
| text_encoding::id | | | | |
| text_encoding::aliases_view | | | | |
| Helper classes | | | | |
| hash<std::text_encoding> | | | | |

|  |  |  |
| --- | --- | --- |
| static consteval text_encoding literal() noexcept; |  | (since C++26) |
|  |  |  |

Constructs a new `text_encoding` object representing the ordinary character literal encoding. It is used to determine the character encoding applied to ordinary character or string literals (e.g. "This is literal").

This function is deleted unless the CHAR_BIT is 8.

### Parameters

(none)

### Return value

The object holding the representation of the ordinary literal encoding.

### Notes

This function can be implemented by constructing `text_encoding` with compiler-specific builtin macros such as `__clang_literal_encoding__` from Clang, or `__GNUC_EXECUTION_CHARSET_NAME` from GCC. These macros, which are known at compile-time, expand to a narrow string literal containing the name of the narrow execution character set used (ordinary literal encoding).

The value returned by literal() may depend on compiler options such as `-fexec-charset=encoding-name` in GCC or Clang or `/execution-charset:encoding-name` in MSVC.

### Example

This example demonstrates the assertion that the ordinary literal encoding should be UTF-8.

Run this code

```
#include <text_encoding>
 
static_assert(std::text_encoding::literal() == std::text_encoding::UTF8);
 
int main()
{
    // if the literal encoding is UTF-8, then this unprefixed string literal is
    // encoded as UTF-8
    constexpr char green_heart[] = "\N{GREEN HEART}";
 
    // this prefixed string literal is always encoded as UTF-8 regardless of the
    // literal encoding
    constexpr char8_t green_heart_u8[] = u8"\N{GREEN HEART}";
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/text/text_encoding/literal&oldid=179082>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 20:50.