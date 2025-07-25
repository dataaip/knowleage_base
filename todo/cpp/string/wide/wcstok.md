# std::wcstok

From cppreference.com
< cpp‎ | string‎ | wide
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

Null-terminated wide strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character classification | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswalnum | | | | | | iswalpha | | | | | | iswlower | | | | | | iswupper | | | | | | iswdigit | | | | | | iswxdigit | | | | | | wctype | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswblank(C++11) | | | | | | iswctype | | | | | | iswcntrl | | | | | | iswgraph | | | | | | iswspace | | | | | | iswprint | | | | | | iswpunct | | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | towlower | | | | | | towupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | towctrans | | | | | | wctrans | | | | | |
| Conversions to numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstolwcstoll(C++11) | | | | | | wcstofwcstodwcstold(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstoulwcstoull(C++11) | | | | | | wcstoimaxwcstouimax(C++11)(C++11) | | | | | |  | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcslen | | | | | | wcscmp | | | | | | wcscoll | | | | | | wcsncmp | | | | | | wcschr | | | | | | wcsrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcspbrk | | | | | | wcsspn | | | | | | wcscspn | | | | | | wcsstr | | | | | | ****wcstok**** | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscpy | | | | | | wcsncpy | | | | | | wcsxfrm | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscat | | | | | | wcsncat | | | | | |  | | | | | |
| Array manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemcpy | | | | | | wmemmove | | | | | | wmemcmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemchr | | | | | | wmemset | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Types | | | | | | wctrans_t | | | | | | wctype_t | | | | | | wint_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Macros | | | | | | WCHAR_MIN WCHAR_MAX WEOF | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cwchar>` |  |  |
| wchar_t\* wcstok( wchar_t\* str, const wchar_t\* delim, wchar_t \*\* ptr); |  |  |
|  |  |  |

Finds the next token in a null-terminated wide string pointed to by str. The separator characters are identified by null-terminated wide string pointed to by delim.

 This function is designed to be called multiples times to obtain successive tokens from the same string.

:   - If str != nullptr, the call is treated as the first call to `std::wcstok` for this particular wide string. The function searches for the first wide character which is **not** contained in delim.

    :   - If no such wide character was found, there are no tokens in str at all, and the function returns a null pointer.
        - If such wide character was found, it is the **beginning of the token**. The function then searches from that point on for the first wide character that **is** contained in delim.

        :   - If no such wide character was found, str has only one token, and future calls to `std::wcstok` will return a null pointer.
            - If such wide character was found, it is **replaced** by the null wide character L'\0' and the parser state (typically a pointer to the following wide character) is stored in the user-provided location \*ptr.

        - The function then returns the pointer to the beginning of the token.

    - If str == nullptr, the call is treated as a subsequent calls to `std::wcstok`: the function continues from where it left in previous invocation with the same \*ptr. The behavior is the same as if the pointer to the wide character that follows the last detected token is passed as str.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated wide string to tokenize |
| delim | - | pointer to the null-terminated wide string identifying delimiters |
| ptr | - | pointer to an object of type wchar_t\*, which is used by wcstok to store its internal state |

### Return value

Pointer to the beginning of the next token or null pointer if there are no more tokens.

### Note

This function is destructive: it writes the L'\0' characters in the elements of the string str. In particular, a wide string literal cannot be used as the first argument of `std::wcstok`.

Unlike std::strtok, this function does not update static storage: it stores the parser state in the user-provided location.

Unlike most other tokenizers, the delimiters in `std::wcstok` can be different for each subsequent token, and can even depend on the contents of the previous tokens.

### Example

Run this code

```
#include <cwchar>
#include <iostream>
 
int main()
{
    wchar_t input[100] = L"A bird came down the walk";
    wchar_t* buffer;
    wchar_t* token = std::wcstok(input, L" ", &buffer);
    while (token)
    {
        std::wcout << token << '\n';
        token = std::wcstok(nullptr, L" ", &buffer);
    }
}

```

Output:

```
A
bird
came
down
the
walk

```

### See also

|  |  |
| --- | --- |
| strtok | finds the next token in a byte string   (function) |
| C documentation for wcstok | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/wide/wcstok&oldid=153121>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 June 2023, at 10:39.