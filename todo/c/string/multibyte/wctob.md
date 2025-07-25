# wctob

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | ****wctob****(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<wchar.h>` |  |  |
| int wctob( wint_t c ); |  | (since C95) |
|  |  |  |

Narrows a wide character `c` if its multibyte character equivalent in the initial shift state is a single byte.

This is typically possible for the characters from the ASCII character set, since most multibyte encodings (such as UTF-8) use single bytes to encode those characters.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | wide character to narrow |

### Return value

EOF if `c` does not represent a multibyte character with length 1 in initial shift state.

otherwise, the single-byte representation of `c` as unsigned char converted to int

### Example

Run this code

```
#include <locale.h>
#include <wchar.h>
#include <stdio.h>
#include <assert.h>
 
void try_narrowing(wchar_t c)
{
    int cn = wctob(c);
    if(cn != EOF)
        printf("%#x narrowed to %#x\n", c, cn);
    else
        printf("%#x could not be narrowed\n", c);
}
 
int main(void)
{
    char* utf_locale_present = setlocale(LC_ALL, "th_TH.utf8");
    assert(utf_locale_present);
    puts("In Thai UTF-8 locale:");
    try_narrowing(L'a');
    try_narrowing(L'๛');
 
    char* tis_locale_present = setlocale(LC_ALL, "th_TH.tis620");
    assert(tis_locale_present);
    puts("In Thai TIS-620 locale:");
    try_narrowing(L'a');
    try_narrowing(L'๛');
}

```

Possible output:

```
In Thai UTF-8 locale:
0x61 narrowed to 0x61
0xe5b could not be narrowed
In Thai TIS-620 locale:
0x61 narrowed to 0x61
0xe5b narrowed to 0xfb

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.29.6.1.2 The wctob function (p: 441)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.24.6.1.2 The wctob function (p: 387)

### See also

|  |  |
| --- | --- |
| btowc(C95) | widens a single-byte narrow character to wide character, if possible   (function) |
| C++ documentation for wctob | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/wctob&oldid=76791>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 March 2015, at 08:05.