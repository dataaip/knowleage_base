# wcsncmp

From cppreference.com
< c‎ | string‎ | wide
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

 Null-terminated wide strings

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Character classification | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswalnum(C95) | | | | | | iswalpha(C95) | | | | | | iswlower(C95) | | | | | | iswupper(C95) | | | | | | iswdigit(C95) | | | | | | iswxdigit(C95) | | | | | | iswblank(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswctype(C95) | | | | | | iswcntrl(C95) | | | | | | iswgraph(C95) | | | | | | iswspace(C95) | | | | | | iswprint(C95) | | | | | | iswpunct(C95) | | | | | | wctype(C95) | | | | | | | Character manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | towlower(C95) | | | | | | towupper(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wctrans(C95) | | | | | | towctrans(C95) | | | | | | | Conversions to numeric formats | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstolwcstoll(C95)(C99) | | | | | | wcstofwcstodwcstold(C99)(C95)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstoulwcstoull(C95)(C99) | | | | | | wcstoimaxwcstoumax(C99)(C99) | | | | | |  | | | | | | | String manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscpywcscpy_s(C95)(C11) | | | | | | wcsncpywcsncpy_s(C95)(C11) | | | | | | wcsxfrm(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscatwcscat_s(C95)(C11) | | | | | | wcsncatwcsncat_s(C95)(C11) | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | String examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcslenwcsnlen_s(C95)(C11) | | | | | | wcsstr(C95) | | | | | | wcscmp(C95) | | | | | | ****wcsncmp****(C95) | | | | | | wcscoll(C95) | | | | | | wcschr(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcsrchr(C95) | | | | | | wcspbrk(C95) | | | | | | wcsspn(C95) | | | | | | wcscspn(C95) | | | | | | wcstokwcstok_s(C95)(C11) | | | | | |  | | | | | | | Array manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemcpywmemcpy_s(C95)(C11) | | | | | | wmemmovewmemmove_s(C95)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemcmp(C95) | | | | | | wmemchr(C95) | | | | | | wmemset(C95) | | | | | |  | | | | | | | Types | | | | | | wchar_t wint_t(C95) | | | | | | wctrans_t wctype_t(C95)(C95) | | | | | | Macros | | | | | | WCHAR_MIN WCHAR_MAX(C95)(C95) | | | | | | WEOF(C95) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<wchar.h>` |  |  |
| int wcsncmp( const wchar_t\* lhs, const wchar_t\* rhs, size_t count ); |  | (since C95) |
|  |  |  |

Compares at most `count` wide characters of two null-terminated wide strings. The comparison is done lexicographically.

The sign of the result is the sign of the difference between the values of the first pair of wide characters that differ in the strings being compared.

The behavior is undefined if `lhs` or `rhs` are not pointers to null-terminated strings.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | pointers to the null-terminated wide strings to compare |
| count | - | maximum number of characters to compare |

### Return value

Negative value if `lhs` appears before `rhs` in lexicographical order.

Zero if `lhs` and `rhs` compare equal.

Positive value if `lhs` appears after `rhs` in lexicographical order.

### Notes

This function is not locale-sensitive, unlike wcscoll and wcsxfrm.

### Example

Run this code

```
#include <stdio.h>
#include <wchar.h>
#include <locale.h>
 
void demo(const wchar_t *lhs, const wchar_t *rhs, int sz)
{
    int rc = wcsncmp(lhs, rhs, sz);
    if(rc == 0)
        printf("First %d characters of [%ls] equal [%ls]\n", sz, lhs, rhs);
    else if(rc < 0)
        printf("First %d characters of [%ls] precede [%ls]\n", sz, lhs, rhs);
    else if(rc > 0)
        printf("First %d characters of [%ls] follow [%ls]\n", sz, lhs, rhs);
}
 
int main(void)
{
    const wchar_t *str1 = L"안녕하세요";
    const wchar_t *str2 = L"안녕히 가십시오";
 
    setlocale(LC_ALL, "en_US.utf8");
    demo(str1, str2, 5);
    demo(str2, str1, 8);
    demo(str1, str2, 2);
}

```

Output:

```
First 5 characters of [안녕하세요] precede [안녕히 가십시오]
First 8 characters of [안녕히 가십시오] follow [안녕하세요]
First 2 characters of [안녕하세요] equal [안녕히 가십시오]

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.29.4.4.3 The wcsncmp function (p: 434)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.24.4.4.3 The wcsncmp function (p: 380)

### See also

|  |  |
| --- | --- |
| wcscmp(C95) | compares two wide strings   (function) |
| wmemcmp(C95) | compares a certain amount of wide characters from two arrays   (function) |
| wcscoll(C95) | compares two wide strings in accordance to the current locale   (function) |
| C++ documentation for wcsncmp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/wide/wcsncmp&oldid=87511>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 August 2016, at 10:26.