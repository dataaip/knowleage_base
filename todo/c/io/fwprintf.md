# wprintf, fwprintf, swprintf, wprintf_s, fwprintf_s, swprintf_s, snwprintf_s

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | ****wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s****(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fsetpos | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | tmpfiletmpfile_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | tmpnamtmpnam_s(C11) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<wchar.h>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| int wprintf( const wchar_t\* format, ... ); |  | (since C95)  (until C99) |
| int wprintf( const wchar_t\* restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| int fwprintf( FILE\* stream, const wchar_t\* format, ... ); |  | (since C95)  (until C99) |
| int fwprintf( FILE\* restrict stream,                const wchar_t\* restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| int swprintf( wchar_t\* buffer, size_t bufsz,                const wchar_t\* format, ... ); |  | (since C95)  (until C99) |
| int swprintf( wchar_t\* restrict buffer, size_t bufsz,                const wchar_t\* restrict format, ... ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| int wprintf_s( const wchar_t\* restrict format, ... ); | (4) | (since C11) |
| int fwprintf_s( FILE\* restrict stream,                  const wchar_t\* restrict format, ... ); | (5) | (since C11) |
| int swprintf_s( wchar_t\* restrict buffer, rsize_t bufsz,                  const wchar_t\* restrict format, ... ); | (6) | (since C11) |
| int snwprintf_s( wchar_t\* restrict s, rsize_t n,                   const wchar_t\* restrict format, ... ); | (7) | (since C11) |
|  |  |  |

Loads the data from the given locations, converts them to wide string equivalents and writes the results to a variety of sinks.

1) Writes the results to stdout.2) Writes the results to a file stream stream.3) If bufsz is greater than zero, writes the results to a wide string buffer. At most bufsz - 1 wide characters are written followed by null wide character. If bufsz is zero, nothing is written (and buffer may be a null pointer).4-6) Same as (1-3), except that the following errors are detected at runtime and call the currently installed constraint handler function:

:   - the conversion specifier `%n` is present in format
    - any of the arguments corresponding to `%s` is a null pointer
    - format or buffer is a null pointer
    - bufsz is zero or greater than RSIZE_MAX / sizeof(wchar_t)
    - encoding errors occur in any of string and character conversion specifiers
    - (only for `swprintf_s`) the number of wide characters to be written, including the null, would exceed bufsz.

7) Same as (6), except it will truncate the result to fit within the array pointed to by s.

:   As with all bounds-checked functions, `wprintf_s`, `fwprintf_s`, `swprintf_s`, and `snwprintf_s` are only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <stdio.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | output file stream to write to |
| buffer | - | pointer to a wide character string to write to |
| bufsz | - | up to bufsz - 1 wide characters may be written, plus the null terminator |
| format | - | pointer to a null-terminated wide string specifying how to interpret the data |
| ... | - | arguments specifying data to print. If any argument after default argument promotions is not the type expected by the corresponding conversion specifier, or if there are fewer arguments than required by format, the behavior is undefined. If there are more arguments than required by format, the extraneous arguments are evaluated and ignored. |

The ****format**** string consists of ordinary wide characters (except `%`), which are copied unchanged into the output stream, and conversion specifications. Each conversion specification has the following format:

:   - introductory `%` character.

:   - (optional) one or more flags that modify the behavior of the conversion:

    :   - `-`: the result of the conversion is left-justified within the field (by default it is right-justified).
        - `+`: the sign of signed conversions is always prepended to the result of the conversion (by default the result is preceded by minus only when it is negative).
        - **space**: if the result of a signed conversion does not start with a sign character, or is empty, space is prepended to the result. It is ignored if `+` flag is present.
        - `#`: **alternative form** of the conversion is performed. See the table below for exact effects otherwise the behavior is undefined.
        - `0`: for integer and floating-point number conversions, leading zeros are used to pad the field instead of **space** characters. For integer numbers it is ignored if the precision is explicitly specified. For other conversions using this flag results in undefined behavior. It is ignored if `-` flag is present.

:   - (optional) integer value or `*` that specifies minimum field width. The result is padded with **space** characters (by default), if required, on the left when right-justified, or on the right if left-justified. In the case when `*` is used, the width is specified by an additional argument of type int, which appears before the argument to be converted and the argument supplying precision if one is supplied. If the value of the argument is negative, it results with the `-` flag specified and positive field width (Note: This is the minimum width: The value is never truncated.).

:   - (optional) `.` followed by integer number or `*`, or neither that specifies **precision** of the conversion. In the case when `*` is used, the **precision** is specified by an additional argument of type int, which appears before the argument to be converted, but after the argument supplying minimum field width if one is supplied. If the value of this argument is negative, it is ignored. If neither a number nor `*` is used, the precision is taken as zero. See the table below for exact effects of **precision**.

:   - (optional) **length modifier** that specifies the size of the argument (in combination with the conversion format specifier, it specifies the type of the corresponding argument).

:   - conversion format specifier.

The following format specifiers are available:

| Conversion Specifier | Explanation | Expected Argument Type | | | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ****Length Modifier********→**** | | `hh` (C99) | `h` | (none) | `l` | `ll` (C99) | `j` (C99) | `z` (C99) | `t` (C99) | `L` |
| `%` | Writes literal `%`. The full conversion specification must be `%%`. | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| `c` | Writes a ****single character****.  The argument is first converted to wchar_t as if by calling btowc. If the ****l**** modifier is used, the wint_t argument is first converted to wchar_t. | N/A | N/A | int | wint_t | N/A | N/A | N/A | N/A | N/A |
| `s` | Writes a ****character string****  The argument must be a pointer to the initial element of a character array containing a multibyte character sequence beginning in the initial shift state, which is converted to wide character array as if by a call to mbrtowc with zero-initialized conversion state. **Precision** specifies the maximum number of wide characters to be written. If **Precision** is not specified, writes every wide characters up to and not including the first null terminator. If the ****l**** specifier is used, the argument must be a pointer to the initial element of an array of wchar_t. | N/A | N/A | char\* | wchar_t\* | N/A | N/A | N/A | N/A | N/A |
| `d` `i` | Converts a ****signed integer**** into decimal representation **[-]dddd**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1.  If both the converted value and the precision are ​0​ the conversion results in no characters. | signed char | short | int | long | long long | intmax_t | signed size_t | ptrdiff_t | N/A |
| `o` | Converts an ****unsigned integer**** into octal representation **oooo**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. In the **alternative implementation** precision is increased if necessary, to write one leading zero. In that case if both the converted value and the precision are ​0​, single ​0​ is written. | unsigned char | unsigned short | unsigned int | unsigned long | unsigned long long | uintmax_t | size_t | unsigned version of ptrdiff_t | N/A |
| `x` `X` | Converts an ****unsigned integer**** into hexadecimal representation **hhhh**.  For the `x` conversion letters `abcdef` are used.  For the `X` conversion letters `ABCDEF` are used.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. In the **alternative implementation** `0x` or `0X` is prefixed to results if the converted value is nonzero. | N/A |
| `u` | Converts an ****unsigned integer**** into decimal representation **dddd**.  **Precision** specifies the minimum number of digits to appear. The default precision is 1. If both the converted value and the precision are ​0​ the conversion results in no characters. | N/A |
| `f` `F` | Converts ****floating-point number**** to the decimal notation in the style **[-]ddd.ddd**.  **Precision** specifies the exact number of digits to appear after the decimal point character. The default precision is 6. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | double | double(C99) | N/A | N/A | N/A | N/A | long double |
| `e` `E` | Converts ****floating-point number**** to the decimal exponent notation.  For the `e` conversion style **[-]d.ddd** ﻿`e`**±dd** is used.  For the `E` conversion style **[-]d.ddd** ﻿`E`**±dd** is used.  The exponent contains at least two digits, more digits are used only if necessary. If the value is ​0​, the exponent is also ​0​. **Precision** specifies the exact number of digits to appear after the decimal point character. The default precision is 6. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `a` `A` (C99) | Converts ****floating-point number**** to the hexadecimal exponent notation.  For the `a` conversion style **[-]** ﻿`0x`**h.hhh** ﻿`p`**±d** is used.  For the `A` conversion style **[-]** ﻿`0X`**h.hhh** ﻿`P`**±d** is used.  The first hexadecimal digit is not `0` if the argument is a normalized floating-point value. If the value is ​0​, the exponent is also ​0​. **Precision** specifies the exact number of digits to appear after the hexadecimal point character. The default precision is sufficient for exact representation of the value. In the **alternative implementation** decimal point character is written even if no digits follow it. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `g` `G` | Converts ****floating-point number**** to decimal or decimal exponent notation depending on the value and the **precision**.  For the `g` conversion style conversion with style `e` or `f` will be performed.  For the `G` conversion style conversion with style `E` or `F` will be performed.  Let `P` equal the precision if nonzero, 6 if the precision is not specified, or 1 if the precision is ​0​. Then, if a conversion with style `E` would have an exponent of `X`:   - if **P > X ≥ −4**, the conversion is with style `f` or `F` and precision **P − 1 − X**. - otherwise, the conversion is with style `e` or `E` and precision **P − 1**.   Unless **alternative representation** is requested the trailing zeros are removed, also the decimal point character is removed if no fractional part is left. For infinity and not-a-number conversion style see notes. | N/A | N/A | N/A | N/A | N/A | N/A |
| `n` | Returns the ****number of characters written**** so far by this call to the function.  The result is **written** to the value pointed to by the argument. The specification may not contain any **flag**, **field width**, or **precision**. | signed char\* | short\* | int\* | long\* | long long\* | intmax_t\* | signed size_t\* | ptrdiff_t\* | N/A |
| `p` | Writes an implementation defined character sequence defining a ****pointer****. | N/A | N/A | void\* | N/A | N/A | N/A | N/A | N/A | N/A |

The floating-point conversion functions convert infinity to `inf` or `infinity`. Which one is used is implementation defined.

Not-a-number is converted to `nan` or `nan(char_sequence)`. Which one is used is implementation defined.

The conversions `F`, `E`, `G`, `A` output `INF`, `INFINITY`, `NAN` instead.

The conversion specifier used to print char, unsigned char, signed char, short, and unsigned short expects promoted types of default argument promotions, but before printing its value will be converted to char, unsigned char, signed char, short, and unsigned short. It is safe to pass values of these types because of the promotion that takes place when a variadic function is called.

The correct conversion specifications for the fixed-width character types (int8_t, etc) are defined in the header <inttypes.h> (although PRIdMAX, PRIuMAX, etc is synonymous with `%jd`, `%ju`, etc).

The memory-writing conversion specifier `%n` is a common target of security exploits where format strings depend on user input and is not supported by the bounds-checked `printf_s` family of functions.

There is a sequence point after the action of each conversion specifier; this permits storing multiple `%n` results in the same variable or, as an edge case, printing a string modified by an earlier `%n` within the same call.

If a conversion specification is invalid, the behavior is undefined.

### Return value

1,2) Number of wide characters written if successful or negative value if an error occurred.3) Number of wide characters written (not counting the terminating null wide character) if successful or negative value if an encoding error occurred or if the number of characters to be generated was equal or greater than bufsz (including when bufsz is zero).4,5) Number of wide characters written if successful or negative value if an error occurred.6) Number of wide characters (not counting the terminating null) that were written to buffer. Returns a negative value on encoding errors and on overflow. Returns zero on all other errors.7) Number of wide characters (not counting the terminating null) that would have been written to buffer had bufsz been sufficiently large, or a negative value if an error occurs. (meaning, write was successful and complete only if the return is nonnegative and less than bufsz)

### Notes

While narrow strings provide snprintf, which makes it possible to determine the required output buffer size, there is no equivalent for wide strings (until `snwprintf_s`)(since C11), and in order to determine the buffer size, the program may need to call `swprintf`, check the result value, and reallocate a larger buffer, trying again until successful.

`snwprintf_s`, unlike `swprintf_s`, will truncate the result to fit within the array pointed to by buffer, even though truncation is treated as an error by most bounds-checked functions.

### Example

Run this code

```
#include <locale.h>
#include <wchar.h>
 
int main(void)
{
    char narrow_str[] = "z\u00df\u6c34\U0001f34c";
                  // or "zß水🍌"
                  // or "\x7a\xc3\x9f\xe6\xb0\xb4\xf0\x9f\x8d\x8c";
    wchar_t warr[29]; // the expected string is 28 characters plus 1 null terminator
    setlocale(LC_ALL, "en_US.utf8");
    swprintf(warr, sizeof warr / sizeof* warr,
             L"Converted from UTF-8: '%s'", narrow_str);
    wprintf(L"%ls\n", warr);
}

```

Output:

```
Converted from UTF-8: 'zß水🍌'

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.29.2.1 The fwprintf function (p: TBD)

:   - 7.29.2.3 The swprintf function (p: TBD)

:   - 7.29.2.11 The wprintf function (p: TBD)

:   - K.3.9.1.1 The fwprintf_s function (p: TBD)

:   - K.3.9.1.4 The swprintf_s function (p: TBD)

:   - K.3.9.1.13 The wprintf_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.29.2.1 The fwprintf function (p: TBD)

:   - 7.29.2.3 The swprintf function (p: TBD)

:   - 7.29.2.11 The wprintf function (p: TBD)

:   - K.3.9.1.1 The fwprintf_s function (p: TBD)

:   - K.3.9.1.4 The swprintf_s function (p: TBD)

:   - K.3.9.1.13 The wprintf_s function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.29.2.1 The fwprintf function (p: 403-410)

:   - 7.29.2.3 The swprintf function (p: 416)

:   - 7.29.2.11 The wprintf function (p: 421)

:   - K.3.9.1.1 The fwprintf_s function (p: 628)

:   - K.3.9.1.4 The swprintf_s function (p: 630-631)

:   - K.3.9.1.13 The wprintf_s function (p: 637-638)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.24.2.1 The fwprintf function (p: 349-356)

:   - 7.24.2.3 The swprintf function (p: 362)

:   - 7.24.2.11 The wprintf function (p: 366)

### See also

|  |  |
| --- | --- |
| printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | prints formatted output to stdout, a file stream or a buffer   (function) |
| vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | prints formatted wide character output to stdout, a file stream  or a buffer using variable argument list   (function) |
| fputws(C95) | writes a wide string to a file stream   (function) |
| C++ documentation for wprintf, fwprintf, swprintf | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io/fwprintf&oldid=172124>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 May 2024, at 06:11.