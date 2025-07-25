# btowc

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | ****btowc****(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<wchar.h>` |  |  |
| wint_t btowc( int c ); |  | (since C95) |
|  |  |  |

Widens a single-byte character `c` (reinterpreted as unsigned char) to its wide character equivalent.

Most multibyte character encodings use single-byte codes to represent the characters from the ASCII character set. This function may be used to convert such characters to wchar_t.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | single-byte character to widen |

### Return value

WEOF if `c` is EOF

wide character representation of `c` if (unsigned char)c is a valid single-byte character in the initial shift state, WEOF otherwise.

### Example

Run this code

```
#include <stdio.h>
#include <wchar.h>
#include <locale.h>
#include <assert.h>
 
void try_widen(unsigned char c)
{
    wint_t w = btowc(c);
    if(w != WEOF)
        printf("The single-byte character %#x widens to %#x\n", c, w);
    else
        printf("The single-byte character %#x failed to widen\n", c);
}
 
int main(void)
{
    char *loc = setlocale(LC_ALL, "lt_LT.iso88594");
    assert(loc);
    printf("In Lithuanian ISO-8859-4 locale:\n");
    try_widen('A');
    try_widen('\xdf'); // German letter ß (U+00df) in ISO-8859-4
    try_widen('\xf9'); // Lithuanian letter ų (U+0173) in ISO-8859-4
 
    setlocale(LC_ALL, "lt_LT.utf8");
    printf("In Lithuanian UTF-8 locale:\n");
    try_widen('A');
    try_widen('\xdf');
    try_widen('\xf9');
}

```

Possible output:

```
In Lithuanian ISO-8859-4 locale:
The single-byte character 0x41 widens to 0x41
The single-byte character 0xdf widens to 0xdf
The single-byte character 0xf9 widens to 0x173
In Lithuanian UTF-8 locale:
The single-byte character 0x41 widens to 0x41
The single-byte character 0xdf failed to widen
The single-byte character 0xf9 failed to widen

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.29.6.1.1 The btowc function (p: 441)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.24.6.1.1 The btowc function (p: 387)

### See also

|  |  |
| --- | --- |
| wctob(C95) | narrows a wide character to a single-byte narrow character, if possible   (function) |
| C++ documentation for btowc | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/btowc&oldid=76790>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 March 2015, at 07:58.