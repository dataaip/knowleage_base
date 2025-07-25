# strtof, strtod, strtold

From cppreference.com
< c‎ | string‎ | byte
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

 Null-terminated byte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | isalnum | | | | | | isalpha | | | | | | islower | | | | | | isupper | | | | | | isdigit | | | | | | isxdigit | | | | | | isblank(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iscntrl | | | | | | isgraph | | | | | | isspace | | | | | | isprint | | | | | | ispunct | | | | | | tolower | | | | | | toupper | | | | | |
| Conversions to and from numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atoiatolatoll(C99) | | | | | | atof | | | | | | strtolstrtoll(C99) | | | | | | strtoulstrtoull(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoimaxstrtoumax(C99)(C99) | | | | | | ****strtofstrtodstrtold****(C99)(C99) | | | | | | strfromfstrfromdstrfroml(C23)(C23)(C23) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpystrcpy_s(C11) | | | | | | strncpystrncpy_s(C11) | | | | | | strcatstrcat_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strncatstrncat_s(C11) | | | | | | strxfrm | | | | | | strdup(C23) | | | | | | strndup(C23) | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlenstrnlen_s(C11) | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtokstrtok_s(C11) | | | | | |  | | | | | |
| Memory manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memsetmemset_explicitmemset_s(C23)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpymemcpy_s(C11) | | | | | | memmovememmove_s(C11) | | | | | | memccpy(C23) | | | | | |
| Miscellaneous | | | | |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
| float       strtof ( const char\* restrict str, char\*\* restrict str_end ); | (1) | (since C99) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| double      strtod ( const char\*          str, char\*\*          str_end ); |  | (until C99) |
| double      strtod ( const char\* restrict str, char\*\* restrict str_end ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| long double strtold( const char\* restrict str, char\*\* restrict str_end ); | (3) | (since C99) |
|  |  |  |

Interprets a floating-point value in a byte string pointed to by str.

Function discards any whitespace characters (as determined by isspace) until first non-whitespace character is found. Then it takes as many characters as possible to form a valid floating-point representation and converts them to a floating-point value. The valid floating-point value can be one of the following:

- decimal floating-point expression. It consists of the following parts:

:   - (optional) plus or minus sign
    - nonempty sequence of decimal digits optionally containing decimal-point character (as determined by the current C locale) (defines significand)
    - (optional) `e` or `E` followed with optional minus or plus sign and nonempty sequence of decimal digits (defines exponent to base 10)

|  |  |
| --- | --- |
| - hexadecimal floating-point expression. It consists of the following parts:   - (optional) plus or minus sign - `0x` or `0X` - nonempty sequence of hexadecimal digits optionally containing a decimal-point character (as determined by the current C locale) (defines significand) - (optional) `p` or `P` followed with optional minus or plus sign and nonempty sequence of decimal digits (defines exponent to base 2)   - infinity expression. It consists of the following parts:   - (optional) plus or minus sign - `INF` or `INFINITY` ignoring case   - not-a-number expression. It consists of the following parts:   - (optional) plus or minus sign - `NAN` or `NAN(`**char_sequence**`)` ignoring case of the `NAN` part. **char_sequence** can only contain digits, Latin letters, and underscores. The result is a quiet NaN floating-point value. | (since C99) |

- any other expression that may be accepted by the currently installed C locale

The functions sets the pointer pointed to by str_end to point to the character past the last character interpreted. If str_end is a null pointer, it is ignored.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to be interpreted |
| str_end | - | pointer to a pointer to character |

### Return value

Floating-point value corresponding to the contents of str on success. If the converted value falls out of range of corresponding return type, range error occurs (errno is set to ERANGE) and HUGE_VAL, HUGE_VALF or HUGE_VALL is returned. If no conversion can be performed, ​0​ is returned.

### Example

Run this code

```
#include <errno.h>
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    // parsing with error handling
    const char* p = "111.11 -2.22 Nan nan(2) inF 0X1.BC70A3D70A3D7P+6  1.18973e+4932zzz";
    printf("Parsing '%s':\n", p);
    char* end = NULL;
    for (double f = strtod(p, &end); p != end; f = strtod(p, &end))
    {
        printf("'%.*s' -> ", (int)(end - p), p);
        p = end;
        if (errno == ERANGE)
        {
            printf("range error, got ");
            errno = 0;
        }
        printf("%f\n", f);
    }
 
    // parsing without error handling
    printf("\"  -0.0000000123junk\"  -->  %g\n", strtod("  -0.0000000123junk", NULL));
    printf("\"junk\"                 -->  %g\n", strtod("junk", NULL));
}

```

Possible output:

```
Parsing '111.11 -2.22 Nan nan(2) inF 0X1.BC70A3D70A3D7P+6  1.18973e+4932zzz':
'111.11' -> 111.110000
' -2.22' -> -2.220000
' Nan' -> nan
' nan(2)' -> nan
' inF' -> inf
' 0X1.BC70A3D70A3D7P+6' -> 111.110000
'  1.18973e+4932' -> range error, got inf
"  -0.0000000123junk"  -->  -1.23e-08
"junk"                 -->  0

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.22.1.3 The strtod, strtof, and strtold functions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22.1.3 The strtod, strtof, and strtold functions (p: 249-251)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.1.3 The strtod, strtof, and strtold functions (p: 342-344)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.1.3 The strtod, strtof, and strtold functions (p: 308-310)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10.1.4 The strtod function

### See also

|  |  |
| --- | --- |
| atof | converts a byte string to a floating-point value   (function) |
| wcstofwcstodwcstold(C99)(C95)(C99) | converts a wide string to a floating-point value   (function) |
| C++ documentation for strtof, strtod, strtold | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/strtof&oldid=178833>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 December 2024, at 03:13.