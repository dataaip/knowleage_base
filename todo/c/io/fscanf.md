# scanf, fscanf, sscanf, scanf_s, fscanf_s, sscanf_s

From cppreference.com
< c‎ | io
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

 File input/output

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****scanffscanfsscanfscanf_sfscanf_ssscanf_s****(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fsetpos | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | tmpfiletmpfile_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | tmpnamtmpnam_s(C11) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdio.h>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| int scanf( const char          \*format, ... ); |  | (until C99) |
| int scanf( const char \*restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| int fscanf( FILE          \*stream, const char          \*format, ... ); |  | (until C99) |
| int fscanf( FILE \*restrict stream, const char \*restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| int sscanf( const char          \*buffer, const char          \*format, ... ); |  | (until C99) |
| int sscanf( const char \*restrict buffer, const char \*restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| int scanf_s(const char \*restrict format, ...); | (4) | (since C11) |
| int fscanf_s(FILE \*restrict stream, const char \*restrict format, ...); | (5) | (since C11) |
| int sscanf_s(const char \*restrict buffer, const char \*restrict format, ...); | (6) | (since C11) |
|  |  |  |

Reads data from a variety of sources, interprets it according to `format` and stores the results into given locations.

1) reads the data from stdin2) reads the data from file stream `stream`3) reads the data from null-terminated character string `buffer`. Reaching the end of the string is equivalent to reaching the end-of-file condition for `fscanf`4-6) Same as (1-3), except that %c, %s, and % conversion specifiers each expect two arguments (the usual pointer and a value of type rsize_t indicating the size of the receiving array, which may be 1 when reading with a %c into a single char) and except that the following errors are detected at runtime and call the currently installed [constraint handler function:

:   - any of the arguments of pointer type is a null pointer
    - `format`, `stream`, or `buffer` is a null pointer
    - the number of characters that would be written by %c, %s, or %, plus the terminating null character, would exceed the second (`rsize_t`) argument provided for each of those conversion specifiers
    - optionally, any other detectable error, such as unknown conversion specifier
:   As with all bounds-checked functions, `scanf_s`, `fscanf_s`, and `sscanf_s` are only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including [<stdio.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | input file stream to read from |
| buffer | - | pointer to a null-terminated character string to read from |
| format | - | pointer to a null-terminated character string specifying how to read the input |
| ... | - | receiving arguments. |

The ****format**** string consists of

- non-whitespace multibyte characters except %: each such character in the format string consumes exactly one identical character from the input stream, or causes the function to fail if the next character on the stream does not compare equal.
- whitespace characters: any single whitespace character in the format string consumes all available consecutive whitespace characters from the input (determined as if by calling isspace in a loop). Note that there is no difference between "\n", " ", "\t\t", or other whitespace in the format string.
- conversion specifications. Each conversion specification has the following format:

:   - introductory % character.

:   - (optional) assignment-suppressing character \*. If this option is present, the function does not assign the result of the conversion to any receiving argument.

:   - (optional) integer number (greater than zero) that specifies **maximum field width**, that is, the maximum number of characters that the function is allowed to consume when doing the conversion specified by the current conversion specification. Note that %s and %[ may lead to buffer overflow if the width is not provided.

:   - (optional) **length modifier** that specifies the size of the receiving argument, that is, the actual destination type. This affects the conversion accuracy and overflow rules. The default destination type is different for each conversion type (see table below).

:   - conversion format specifier.

The following format specifiers are available:

| Conversion specifier | Explanation | Argument type | | | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ****Length modifier →**** | | `hh` (C99) | `h` | (none) | `l` | `ll` (C99) | `j` (C99) | `z` (C99) | `t` (C99) | `L` |
| `%` | Matches literal `%`. | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| `c` | Matches a ****character**** or a sequence of ****characters****.  If a width specifier is used, matches exactly **width** characters (the argument must be a pointer to an array with sufficient room). Unlike %s and %[, does not append the null character to the array. | N/A | N/A | char\* | wchar_t\* | N/A | N/A | N/A | N/A | N/A |
| `s` | Matches a sequence of non-whitespace characters (a ****string****).  If width specifier is used, matches up to **width** or until the first whitespace character, whichever appears first. Always stores a null character in addition to the characters matched (so the argument array must have room for at least **width+1** characters) |
| `[`set`]` | Matches a non-empty sequence of character from set of characters.  If the first character of the set is `^`, then all characters not in the set are matched. If the set begins with `]` or `^]` then the `]` character is also included into the set. It is implementation-defined whether the character `-` in the non-initial position in the scanset may be indicating a range, as in `[0-9]`. If width specifier is used, matches only up to **width**. Always stores a null character in addition to the characters matched (so the argument array must have room for at least **width+1** characters) |
| `d` | Matches a ****decimal integer****.  The format of the number is the same as expected by strtol with the value 10 for the `base` argument | signed char\* or unsigned char\* | signed short\* or unsigned short\* | signed int\* or unsigned int\* | signed long\* or unsigned long\* | signed long long\* or unsigned long long\* | intmax_t\* or uintmax_t\* | size_t\* | ptrdiff_t\* | N/A |
| `i` | Matches an ****integer****.  The format of the number is the same as expected by strtol with the value ​0​ for the `base` argument (base is determined by the first characters parsed) |
| `u` | Matches an unsigned ****decimal integer****.  The format of the number is the same as expected by strtoul with the value 10 for the `base` argument. |
| `o` | Matches an unsigned ****octal integer****.  The format of the number is the same as expected by strtoul with the value 8 for the `base` argument |
| `x`, `X` | Matches an unsigned ****hexadecimal integer****.  The format of the number is the same as expected by strtoul with the value 16 for the `base` argument |
| `n` | Returns the ****number of characters read so far****.  No input is consumed. Does not increment the assignment count. If the specifier has assignment-suppressing operator defined, the behavior is undefined |
| `a`, `A`(C99) `e`, `E` `f`, `F`(C99) `g`, `G` | Matches a ****floating-point number****.  The format of the number is the same as expected by strtof | N/A | N/A | float\* | double\* | N/A | N/A | N/A | N/A | long double\* |
| `p` | Matches implementation defined character sequence defining a ****pointer****.  `printf` family of functions should produce the same sequence using `%p` format specifier | N/A | N/A | void\*\* | N/A | N/A | N/A | N/A | N/A | N/A |

For every conversion specifier other than n, the longest sequence of input characters which does not exceed any specified ﬁeld width and which either is exactly what the conversion specifier expects or is a prefix of a sequence it would expect, is what's consumed from the stream. The ﬁrst character, if any, after this consumed sequence remains unread. If the consumed sequence has length zero or if the consumed sequence cannot be converted as specified above, the matching failure occurs unless end-of-ﬁle, an encoding error, or a read error prevented input from the stream, in which case it is an input failure.

All conversion specifiers other than , c, and n consume and discard all leading whitespace characters (determined as if by calling [isspace) before attempting to parse the input. These consumed characters do not count towards the specified maximum field width.

The conversion specifiers lc, ls, and l perform multibyte-to-wide character conversion as if by calling [mbrtowc with an mbstate_t object initialized to zero before the first character is converted.

The conversion specifiers s and  always store the null terminator in addition to the matched characters. The size of the destination array must be at least one greater than the specified field width. The use of %s or %[, without specifying the destination array size, is as unsafe as [gets.

The correct conversion specifications for the fixed-width integer types (int8_t, etc) are defined in the header `<inttypes.h>` (although SCNdMAX, SCNuMAX, etc is synonymous with %jd, %ju, etc).

There is a sequence point after the action of each conversion specifier; this permits storing multiple fields in the same "sink" variable.

When parsing an incomplete floating-point value that ends in the exponent with no digits, such as parsing "100er" with the conversion specifier %f, the sequence "100e" (the longest prefix of a possibly valid floating-point number) is consumed, resulting in a matching error (the consumed sequence cannot be converted to a floating-point number), with "r" remaining. Some existing implementations do not follow this rule and roll back to consume only "100", leaving "er", e.g. glibc bug 1765.

A conversion specification must be valid. Otherwise, the behavior is undefined.

If a conversion specification is invalid, the behavior is undefined.

### Return value

1-3) Number of receiving arguments successfully assigned (which may be zero in case a matching failure occurred before the first receiving argument was assigned), or EOF if input failure occurs before the first receiving argument was assigned.4-6) Same as (1-3), except that EOF is also returned if there is a runtime constraint violation.

### Complexity

Not guaranteed. Notably, some implementations of `sscanf` are O(N), where N = strlen(buffer) [[1]](https://sourceware.org/bugzilla/show_bug.cgi?id=17577).

### Notes

Because most conversion specifiers first consume all consecutive whitespace, code such as

```
scanf("%d", &a);
scanf("%d", &b);

```

will read two integers that are entered on different lines (second %d will consume the newline left over by the first) or on the same line, separated by spaces or tabs (second %d will consume the spaces or tabs).

The conversion specifiers that do not consume leading whitespace, such as %c, can be made to do so by using a whitespace character in the format string:

```
scanf("%d", &a);
scanf(" %c", &c); // consume all consecutive whitespace after %d, then read a char

```

### Example

Run this code

```
#define __STDC_WANT_LIB_EXT1__ 1
#include <stdio.h>
#include <stddef.h>
#include <locale.h>
 
int main(void)
{
    int i, j;
    float x, y;
    char str1[10], str2[4];
    wchar_t warr[2];
    setlocale(LC_ALL, "en_US.utf8");
 
    char input[] = "25 54.32E-1 Thompson 56789 0123 56ß水";
    /* parse as follows:
       %d: an integer
       %f: a floating-point value
       %9s: a string of at most 9 non-whitespace characters
       %2d: two-digit integer (digits 5 and 6)
       %f:  a floating-point value (digits 7, 8, 9)
       %*d: an integer which isn't stored anywhere
       ' ': all consecutive whitespace
       %3[0-9]: a string of at most 3 decimal digits (digits 5 and 6)
       %2lc: two wide characters, using multibyte to wide conversion  */
    int ret = sscanf(input, "%d%f%9s%2d%f%*d %3[0-9]%2lc",
                     &i, &x, str1, &j, &y, str2, warr);
 
    printf("Converted %d fields:\n"
           "i = %d\n"
           "x = %f\n"
           "str1 = %s\n"
           "j = %d\n"
           "y = %f\n"
           "str2 = %s\n"
           "warr[0] = U+%x\n"
           "warr[1] = U+%x\n",
           ret, i, x, str1, j, y, str2, warr[0], warr[1]);
 
#ifdef __STDC_LIB_EXT1__
    int n = sscanf_s(input, "%d%f%s", &i, &x, str1, (rsize_t)sizeof str1);
    // writes 25 to i, 5.432 to x, the 9 bytes "Thompson\0" to str1, and 3 to n.
#endif
}

```

Possible output:

```
Converted 7 fields:
i = 25
x = 5.432000
str1 = Thompson
j = 56
y = 789.000000
str2 = 56
warr[0] = U+df
warr[1] = U+6c34

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.21.6.2 The fscanf function (p: 231-236)

:   - 7.21.6.4 The scanf function (p: 236-237)

:   - 7.21.6.7 The sscanf function (p: 238-239)

:   - K.3.5.3.2 The fscanf_s function (p: 430-431)

:   - K.3.5.3.4 The scanf_s function (p: 432)

:   - K.3.5.3.7 The sscanf_s function (p: 433)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.21.6.2 The fscanf function (p: 317-324)

:   - 7.21.6.4 The scanf function (p: 325)

:   - 7.21.6.7 The sscanf function (p: 326)

:   - K.3.5.3.2 The fscanf_s function (p: 592-593)

:   - K.3.5.3.4 The scanf_s function (p: 594)

:   - K.3.5.3.7 The sscanf_s function (p: 596)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.19.6.2 The fscanf function (p: 282-289)

:   - 7.19.6.4 The scanf function (p: 290)

:   - 7.19.6.7 The sscanf function (p: 291)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.9.6.2 The fscanf function

:   - 4.9.6.4 The scanf function

:   - 4.9.6.6 The sscanf function

### See also

|  |  |
| --- | --- |
| vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | reads formatted input from stdin, a file stream or a buffer  using variable argument list   (function) |
| fgets | gets a character string from a file stream   (function) |
| printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | prints formatted output to stdout, a file stream or a buffer   (function) |
| C++ documentation for scanf, fscanf, sscanf | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io/fscanf&oldid=140798>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 July 2022, at 11:00.