# toupper

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | isalnum | | | | | | isalpha | | | | | | islower | | | | | | isupper | | | | | | isdigit | | | | | | isxdigit | | | | | | isblank(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iscntrl | | | | | | isgraph | | | | | | isspace | | | | | | isprint | | | | | | ispunct | | | | | | tolower | | | | | | ****toupper**** | | | | | |
| Conversions to and from numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atoiatolatoll(C99) | | | | | | atof | | | | | | strtolstrtoll(C99) | | | | | | strtoulstrtoull(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoimaxstrtoumax(C99)(C99) | | | | | | strtofstrtodstrtold(C99)(C99) | | | | | | strfromfstrfromdstrfroml(C23)(C23)(C23) | | | | | |
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
| Defined in header `<ctype.h>` |  |  |
| int toupper( int ch ); |  |  |
|  |  |  |

Converts the given character to uppercase according to the character conversion rules defined by the currently installed C locale.

In the default "C" locale, the following lowercase letters `abcdefghijklmnopqrstuvwxyz` are replaced with respective uppercase letters `ABCDEFGHIJKLMNOPQRSTUVWXYZ`.

### Parameters

|  |  |  |
| --- | --- | --- |
| ch | - | character to be converted. If the value of ch is not representable as unsigned char and does not equal EOF, the behavior is undefined. |

### Return value

Uppercase version of ch or unmodified ch if no uppercase version is listed in the current C locale.

### Example

Run this code

```
#include <ctype.h>
#include <limits.h>
#include <locale.h>
#include <stdio.h>
 
int main(void)
{
    // in the default locale:
    for (unsigned char l = 0, u; l != UCHAR_MAX; ++l)
        if ((u = toupper(l)) != l)
            printf("%c%c ", l, u);
    printf("\n\n");
 
    unsigned char c = '\xb8'; // the character ž in ISO-8859-15
                              // but ¸ (cedilla) in ISO-8859-1
    setlocale(LC_ALL, "en_US.iso88591");
    printf("in iso8859-1, toupper('0x%x') gives 0x%x\n", c, toupper(c));
    setlocale(LC_ALL, "en_US.iso885915");
    printf("in iso8859-15, toupper('0x%x') gives 0x%x\n", c, toupper(c));
}

```

Possible output:

```
aA bB cC dD eE fF gG hH iI jJ kK lL mM nN oO pP qQ rR sS tT uU vV wW xX yY zZ
 
in iso8859-1, toupper('0xb8') gives 0xb8
in iso8859-15, toupper('0xb8') gives 0xb4

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.4.2.2 The toupper function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.4.2.2 The toupper function (p: 147-148)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.4.2.2 The toupper function (p: 204)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.4.2.2 The toupper function (p: 185)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.3.2.2 The toupper function

### See also

|  |  |
| --- | --- |
| tolower | converts a character to lowercase   (function) |
| towupper(C95) | converts a wide character to uppercase   (function) |
| C++ documentation for toupper | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/toupper&oldid=172959>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 June 2024, at 17:32.