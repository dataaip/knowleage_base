# wcstof, wcstod, wcstold

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Character classification | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswalnum(C95) | | | | | | iswalpha(C95) | | | | | | iswlower(C95) | | | | | | iswupper(C95) | | | | | | iswdigit(C95) | | | | | | iswxdigit(C95) | | | | | | iswblank(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswctype(C95) | | | | | | iswcntrl(C95) | | | | | | iswgraph(C95) | | | | | | iswspace(C95) | | | | | | iswprint(C95) | | | | | | iswpunct(C95) | | | | | | wctype(C95) | | | | | | | Character manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | towlower(C95) | | | | | | towupper(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wctrans(C95) | | | | | | towctrans(C95) | | | | | | | Conversions to numeric formats | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstolwcstoll(C95)(C99) | | | | | | ****wcstofwcstodwcstold****(C99)(C95)(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstoulwcstoull(C95)(C99) | | | | | | wcstoimaxwcstoumax(C99)(C99) | | | | | |  | | | | | | | String manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscpywcscpy_s(C95)(C11) | | | | | | wcsncpywcsncpy_s(C95)(C11) | | | | | | wcsxfrm(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscatwcscat_s(C95)(C11) | | | | | | wcsncatwcsncat_s(C95)(C11) | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | String examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcslenwcsnlen_s(C95)(C11) | | | | | | wcsstr(C95) | | | | | | wcscmp(C95) | | | | | | wcsncmp(C95) | | | | | | wcscoll(C95) | | | | | | wcschr(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcsrchr(C95) | | | | | | wcspbrk(C95) | | | | | | wcsspn(C95) | | | | | | wcscspn(C95) | | | | | | wcstokwcstok_s(C95)(C11) | | | | | |  | | | | | | | Array manipulation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemcpywmemcpy_s(C95)(C11) | | | | | | wmemmovewmemmove_s(C95)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemcmp(C95) | | | | | | wmemchr(C95) | | | | | | wmemset(C95) | | | | | |  | | | | | | | Types | | | | | | wchar_t wint_t(C95) | | | | | | wctrans_t wctype_t(C95)(C95) | | | | | | Macros | | | | | | WCHAR_MIN WCHAR_MAX(C95)(C95) | | | | | | WEOF(C95) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<wchar.h>` |  |  |
| float       wcstof( const wchar_t\* restrict str, wchar_t\*\* restrict str_end ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| double      wcstod( const wchar_t\* str, wchar_t\*\* str_end ); |  | (since C95)  (until C99) |
| double      wcstod( const wchar_t\* restrict str, wchar_t\*\* restrict str_end ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| long double wcstold( const wchar_t\* restrict str, wchar_t\*\* restrict str_end ); |  | (since C99) |
|  |  |  |

Interprets a floating-point value in a wide string pointed to by str.

Function discards any whitespace characters (as determined by iswspace) until first non-whitespace character is found. Then it takes as many characters as possible to form a valid floating-point representation and converts them to a floating-point value. The valid floating-point value can be one of the following:

- decimal floating-point expression. It consists of the following parts:

:   - (optional) plus or minus sign
    - nonempty sequence of decimal digits optionally containing decimal-point character (as determined by the current C locale) (defines significand)
    - (optional) `e` or `E` followed with optional minus or plus sign and nonempty sequence of decimal digits (defines exponent to base 10)

|  |  |
| --- | --- |
| - hexadecimal floating-point expression. It consists of the following parts:   - (optional) plus or minus sign - `0x` or `0X` - nonempty sequence of hexadecimal digits optionally containing a decimal-point character (as determined by the current C locale) (defines significand) - (optional) `p` or `P` followed with optional minus or plus sign and nonempty sequence of decimal digits (defines exponent to base 2)   - infinity expression. It consists of the following parts:   - (optional) plus or minus sign - `INF` or `INFINITY` ignoring case   - not-a-number expression. It consists of the following parts:   - (optional) plus or minus sign - `NAN` or `NAN(`**char_sequence**`)` ignoring case of the `NAN` part. **char_sequence** can only contain digits, Latin letters, and underscores. The result is a quiet NaN floating-point value. | (since C99) |

- any other expression that may be accepted by the currently installed C locale

The functions sets the pointer pointed to by str_end to point to the wide character past the last character interpreted. If str_end is a null pointer, it is ignored.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated wide string to be interpreted |
| str_end | - | pointer to a pointer to a wide character. |

### Return value

Floating-point value corresponding to the contents of str on success. If the converted value falls out of range of corresponding return type, range error occurs and HUGE_VAL, HUGE_VALF or HUGE_VALL is returned. If no conversion can be performed, ​0​ is returned.

### Example

Run this code

```
#include <errno.h>
#include <stdio.h>
#include <wchar.h>
 
int main(void)
{
    const wchar_t* p = L"111.11 -2.22 0X1.BC70A3D70A3D7P+6  1.18973e+4932zzz";
    printf("Parsing L\"%ls\":\n", p);
    wchar_t* end;
    for (double f = wcstod(p, &end); p != end; f = wcstod(p, &end))
    {
        printf("'%.*ls' -> ", (int)(end-p), p);
        p = end;
        if (errno == ERANGE){
            printf("range error, got ");
            errno = 0;
        }
        printf("%f\n", f);
    }
}

```

Output:

```
Parsing L"111.11 -2.22 0X1.BC70A3D70A3D7P+6  1.18973e+4932zzz":
'111.11' -> 111.110000
' -2.22' -> -2.220000
' 0X1.BC70A3D70A3D7P+6' -> 111.110000
'  1.18973e+4932' -> range error, got inf

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.29.4.1.1 The wcstod, wcstof, and wcstold functions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.29.4.1.1 The wcstod, wcstof, and wcstold functions (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.29.4.1.1 The wcstod, wcstof, and wcstold functions (p: 426-428)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.24.4.1.1 The wcstod, wcstof, and wcstold functions (p: 372-374)

### See also

|  |  |
| --- | --- |
| strtofstrtodstrtold(C99)(C99) | converts a byte string to a floating-point value   (function) |
| C++ documentation for wcstof, wcstod, wcstold | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/wide/wcstof&oldid=172070>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 May 2024, at 21:07.