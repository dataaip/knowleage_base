# strstr

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atoiatolatoll(C99) | | | | | | atof | | | | | | strtolstrtoll(C99) | | | | | | strtoulstrtoull(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoimaxstrtoumax(C99)(C99) | | | | | | strtofstrtodstrtold(C99)(C99) | | | | | | strfromfstrfromdstrfroml(C23)(C23)(C23) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpystrcpy_s(C11) | | | | | | strncpystrncpy_s(C11) | | | | | | strcatstrcat_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strncatstrncat_s(C11) | | | | | | strxfrm | | | | | | strdup(C23) | | | | | | strndup(C23) | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlenstrnlen_s(C11) | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | ****strstr**** | | | | | | strtokstrtok_s(C11) | | | | | |  | | | | | |
| Memory manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memsetmemset_explicitmemset_s(C23)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpymemcpy_s(C11) | | | | | | memmovememmove_s(C11) | | | | | | memccpy(C23) | | | | | |
| Miscellaneous | | | | |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
| char\* strstr( const char\* str, const char\* substr ); | (1) |  |
| /\*QChar\*/\* strstr( /\*QChar\*/\* str, const char\* substr ); | (2) | (since C23) |
|  |  |  |

1) Finds the first occurrence of the null-terminated byte string pointed to by substr in the null-terminated byte string pointed to by str. The terminating null characters are not compared.2) Type-generic function equivalent to (1). Let `T` be an unqualified character object type.

:   - If `str` is of type const T\*, the return type is const char\*.
    - Otherwise, if `str` is of type T\*, the return type is char\*.
    - Otherwise, the behavior is undefined.

If a macro definition of each of these generic functions is suppressed to access an actual function (e.g. if (strstr) or a function pointer is used), the actual function declaration (1) becomes visible.

The behavior is undefined if either str or substr is not a pointer to a null-terminated byte string.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to examine |
| substr | - | pointer to the null-terminated byte string to search for |

### Return value

Pointer to the first character of the found substring in str, or a null pointer if such substring is not found. If substr points to an empty string, str is returned.

### Example

Run this code

```
#include <stdio.h>
#include <string.h>
 
void find_str(char const* str, char const* substr)
{
    char const* pos = strstr(str, substr);
    if (pos)
        printf(
            "Found the string [%s] in [%s] at position %td\n",
            substr, str, pos - str
        );
    else
        printf(
            "The string [%s] was not found in [%s]\n",
            substr, str
        );
}
 
int main(void)
{
    char const* str = "one two three";
    find_str(str, "two");
    find_str(str, "");
    find_str(str, "nine");
    find_str(str, "n");
 
    return 0;
}

```

Output:

```
Found the string [two] in [one two three] at position 4
Found the string [] in [one two three] at position 0
The string [nine] was not found in [one two three]
Found the string [n] in [one two three] at position 1

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.5.7 The strstr function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.24.5.7 The strstr function (p: 269)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.24.5.7 The strstr function (p: 369)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.21.5.7 The strstr function (p: 332)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.11.5.7 The strstr function

### See also

|  |  |
| --- | --- |
| strchr | finds the first occurrence of a character   (function) |
| strrchr | finds the last occurrence of a character   (function) |
| C++ documentation for strstr | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/strstr&oldid=176824>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 October 2024, at 04:06.