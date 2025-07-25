# mblen

From cppreference.com
< c‎ | string‎ | multibyte
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Null-terminated byte strings | | | | |
| Null-terminated multibyte strings | | | | |
| Null-terminated wide strings | | | | |

 Null-terminated multibyte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Wide/multibyte conversions | | | | |
| mbsinit(C95) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****mblen**** | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
| int mblen( const char\* s, size_t n ); |  |  |
|  |  |  |

Determines the size, in bytes, of the multibyte character whose first byte is pointed to by `s`.

If `s` is a null pointer, resets the global conversion state and(until C23) determined whether shift sequences are used.

This function is equivalent to the call mbtowc((wchar_t\*)0, s, n), except that conversion state of mbtowc is unaffected.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to the multibyte character |
| n | - | limit on the number of bytes in s that can be examined |

### Return value

If `s` is not a null pointer, returns the number of bytes that are contained in the multibyte character or -1 if the first bytes pointed to by `s` do not form a valid multibyte character or ​0​ if `s` is pointing at the null charcter '\0'.

If `s` is a null pointer, resets its internal conversion state to represent the initial shift state and(until C23) returns ​0​ if the current multibyte encoding is not state-dependent (does not use shift sequences) or a non-zero value if the current multibyte encoding is state-dependent (uses shift sequences).

### Notes

|  |  |
| --- | --- |
| Each call to `mblen` updates the internal global conversion state (a static object of type mbstate_t, only known to this function). If the multibyte encoding uses shift states, care must be taken to avoid backtracking or multiple scans. In any case, multiple threads should not call `mblen` without synchronization: mbrlen may be used instead. | (until C23) |
| `mblen` is not allowed to have an internal state. | (since C23) |

### Example

Run this code

```
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
 
// the number of characters in a multibyte string is the sum of mblen()'s
// note: the simpler approach is mbstowcs(NULL, str, sz)
size_t strlen_mb(const char* ptr)
{
    size_t result = 0;
    const char* end = ptr + strlen(ptr);
    mblen(NULL, 0); // reset the conversion state
    while(ptr < end) {
        int next = mblen(ptr, end - ptr);
        if (next == -1) {
           perror("strlen_mb");
           break;
        }
        ptr += next;
        ++result;
    }
    return result;
}
 
void dump_bytes(const char* str)
{
    for (const char* end = str + strlen(str); str != end; ++str)
        printf("%02X ", (unsigned char)str[0]);
    printf("\n");
}
 
int main(void)
{
    setlocale(LC_ALL, "en_US.utf8");
    const char* str = "z\u00df\u6c34\U0001f34c";
    printf("The string \"%s\" consists of %zu characters, but %zu bytes: ",
            str, strlen_mb(str), strlen(str));
    dump_bytes(str);
}

```

Possible output:

```
The string "zß水🍌" consists of 4 characters, but 10 bytes: 7A C3 9F E6 B0 B4 F0 9F 8D 8C

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22.7.1 The mblen function (p: 260)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.7.1 The mblen function (p: 357)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.7.1 The mblen function (p: 321)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10.7.1 The mblen function

### See also

|  |  |
| --- | --- |
| mbtowc | converts the next multibyte character to wide character   (function) |
| mbrlen(C95) | returns the number of bytes in the next multibyte character, given state   (function) |
| C++ documentation for mblen | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/mblen&oldid=146551>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 January 2023, at 12:49.