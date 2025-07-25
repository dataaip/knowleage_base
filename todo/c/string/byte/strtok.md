# strtok, strtok_s

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlenstrnlen_s(C11) | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | ****strtokstrtok_s****(C11) | | | | | |  | | | | | |
| Memory manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memsetmemset_explicitmemset_s(C23)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpymemcpy_s(C11) | | | | | | memmovememmove_s(C11) | | | | | | memccpy(C23) | | | | | |
| Miscellaneous | | | | |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| char\* strtok( char\* str, const char\* delim ); |  | (until C99) |
| char\* strtok( char\* restrict str, const char\* restrict delim ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| char\* strtok_s( char\* restrict str, rsize_t\* restrict strmax,                  const char\* restrict delim, char\*\* restrict ptr ); | (2) | (since C11) |
|  |  |  |

1) Finds the next token in a null-terminated byte string pointed to by str. The separator characters are identified by null-terminated byte string pointed to by delim. This function is designed to be called multiple times to obtain successive tokens from the same string.

:   - If str is not a null pointer, the call is treated as the first call to `strtok` for this particular string. The function searches for the first character which is **not** contained in delim.

    :   - If no such character was found, there are no tokens in str at all, and the function returns a null pointer.
        - If such character was found, it is the **beginning of the token**. The function then searches from that point on for the first character that **is** contained in delim.

        :   - If no such character was found, str has only one token, and future calls to `strtok` will return a null pointer
            - If such character was found, it is **replaced** by the null character '\0' and the pointer to the following character is stored in a static location for subsequent invocations.

        - The function then returns the pointer to the beginning of the token

    - If str is a null pointer, the call is treated as a subsequent call to `strtok`: the function continues from where it left in previous invocation. The behavior is the same as if the previously stored pointer is passed as str.

 The behavior is undefined if either str or delim is not a pointer to a null-terminated byte string.2) Same as (1), except that on every step, writes the number of characters left to see in str into \*strmax and writes the tokenizer's internal state to \*ptr. Repeat calls (with null str) must pass strmax and ptr with the values stored by the previous call. Also, the following errors are detected at runtime and call the currently installed constraint handler function, without storing anything in the object pointed to by ptr

:   - strmax, delim, or ptr is a null pointer
    - on a non-initial call (with null str), `*ptr` is a null pointer
    - on the first call, \*strmax is zero or greater than RSIZE_MAX
    - search for the end of a token reaches the end of the source string (as measured by the initial value of \*strmax) without encountering the null terminator

 The behavior is undefined if both str points to a character array which lacks the null character and strmax points to a value which is greater than the size of that character array.

:   As with all bounds-checked functions, `strtok_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <string.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to tokenize |
| delim | - | pointer to the null-terminated byte string identifying delimiters |
| strmax | - | pointer to an object which initially holds the size of str: strtok_s stores the number of characters that remain to be examined |
| ptr | - | pointer to an object of type char\*, which is used by strtok_s to store its internal state |

### Return value

Returns pointer to the beginning of the next token or a null pointer if there are no more tokens.

### Note

This function is destructive: it writes the '\0' characters in the elements of the string str. In particular, a string literal cannot be used as the first argument of `strtok`.

Each call to `strtok` modifies a static variable: is not thread safe.

Unlike most other tokenizers, the delimiters in `strtok` can be different for each subsequent token, and can even depend on the contents of the previous tokens.

The `strtok_s` function differs from the POSIX `strtok_r` function by guarding against storing outside of the string being tokenized, and by checking runtime constraints. The Microsoft CRT `strtok_s` signature matches this POSIX `strtok_r` definition, not the C11 `strtok_s`.

### Example

Run this code

```
#define __STDC_WANT_LIB_EXT1__ 1
#include <stdio.h>
#include <string.h>
 
int main(void)
{
    char input[] = "A bird came down the walk";
    printf("Parsing the input string '%s'\n", input);
    char* token = strtok(input, " ");
    while (token)
    {
        puts(token);
        token = strtok(NULL, " ");
    }
 
    printf("Contents of the input string now: '");
    for (size_t n = 0; n < sizeof input; ++n)
        input[n] ? putchar(input[n]) : fputs("\\0", stdout);
    puts("'");
 
#ifdef __STDC_LIB_EXT1__
    char str[] = "A bird came down the walk";
    rsize_t strmax = sizeof str;
    const char* delim = " ";
    char* next_token;
    printf("Parsing the input string '%s'\n", str);
    token = strtok_s(str, &strmax, delim, &next_token);
    while (token)
    {
        puts(token);
        token = strtok_s(NULL, &strmax, delim, &next_token);
    }
 
    printf("Contents of the input string now: '");
    for (size_t n = 0; n < sizeof str; ++n)
        str[n] ? putchar(str[n]) : fputs("\\0", stdout);
    puts("'");
#endif
}

```

Possible output:

```
Parsing the input string 'A bird came down the walk'
A
bird
came
down
the
walk
Contents of the input string now: 'A\0bird\0came\0down\0the\0walk\0'
Parsing the input string 'A bird came down the walk'
A
bird
came
down
the
walk
Contents of the input string now: 'A\0bird\0came\0down\0the\0walk\0'

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.5.8 The strtok function (p: TBD)

:   - K.3.7.3.1 The strtok_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.24.5.8 The strtok function (p: TBD)

:   - K.3.7.3.1 The strtok_s function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.24.5.8 The strtok function (p: 369-370)

:   - K.3.7.3.1 The strtok_s function (p: 620-621)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.21.5.8 The strtok function (p: 332-333)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.11.5.8 The strtok function

### See also

|  |  |
| --- | --- |
| strpbrk | finds the first location of any character in one string, in another string   (function) |
| strcspn | returns the length of the maximum initial segment that consists   of only the characters not found in another byte string   (function) |
| strspn | returns the length of the maximum initial segment that consists   of only the characters found in another byte string   (function) |
| wcstokwcstok_s(C95)(C11) | finds the next token in a wide string   (function) |
| C++ documentation for strtok | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/strtok&oldid=180163>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2025, at 22:30.