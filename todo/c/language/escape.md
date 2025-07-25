# Escape sequences

From cppreference.com
< c‎ | language
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

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| value category | | | | |
| evaluation order and sequence points | | | | |
| constant expressions | | | | |
| implicit conversions | | | | |
| generic selection (C11) | | | | |
| constants and literals | | | | |
| integer constant | | | | |
| floating constant | | | | |
| character constant | | | | |
| true/false(C23) | | | | |
| nullptr(C23) | | | | |
| string literal | | | | |
| compound literal (C99) | | | | |
| operators | | | | |
| operator precedence | | | | |
| member access and indirection | | | | |
| logical operators | | | | |
| comparison operators | | | | |
| arithmetic operators | | | | |
| assignment operators | | | | |
| increment and decrement | | | | |
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

Escape sequences are used to represent certain special characters within string literals and character constants.

The following escape sequences are available. ISO C requires a diagnostic if the backslash is followed by any character not listed here:

| Escape  sequence | Description | Representation |
| --- | --- | --- |
| Simple escape sequences | | |
| `\'` | single quote | byte `0x27` in ASCII encoding |
| `\"` | double quote | byte `0x22` in ASCII encoding |
| `\?` | question mark | byte `0x3f` in ASCII encoding |
| `\\` | backslash | byte `0x5c` in ASCII encoding |
| `\a` | audible bell | byte `0x07` in ASCII encoding |
| `\b` | backspace | byte `0x08` in ASCII encoding |
| `\f` | form feed - new page | byte `0x0c` in ASCII encoding |
| `\n` | line feed - new line | byte `0x0a` in ASCII encoding |
| `\r` | carriage return | byte `0x0d` in ASCII encoding |
| `\t` | horizontal tab | byte `0x09` in ASCII encoding |
| `\v` | vertical tab | byte `0x0b` in ASCII encoding |
| Numeric escape sequences | | |
| `\nnn` | arbitrary octal value | code unit `nnn` |
| `\xn...` | arbitrary hexadecimal value | code unit `n...` (arbitrary number of hexadecimal digits) |
| Universal character names | | |
| `\unnnn` (since C99) | Unicode value in allowed range; may result in several code units | code point `U+nnnn` |
| `\Unnnnnnnn` (since C99) | Unicode value in allowed range; may result in several code units | code point `U+nnnnnnnn` |

|  |  |
| --- | --- |
| Range of universal character names If a universal character name corresponds to a code point that is not `0x24` ('$'), `0x40` ('@'), nor `0x60` ('`') and less than `0xA0`, or a surrogate code point (the range `0xD800-0xDFFF`, inclusive), or greater than `0x10FFFF`, i.e. not a Unicode code point(since C23), the program is ill-formed. In other words, members of basic source character set and control characters (in ranges `0x0-0x1F` and `0x7F-0x9F`) cannot be expressed in universal character names. | (since C99) |

### Notes

\0 is the most commonly used octal escape sequence, because it represents the terminating null character in null-terminated strings.

The new-line character \n has special meaning when used in text mode I/O: it is converted to the OS-specific newline byte or byte sequence.

Octal escape sequences have a length limit of three octal digits but terminate at the first character that is not a valid octal digit if encountered sooner.

Hexadecimal escape sequences have no length limit and terminate at the first character that is not a valid hexadecimal digit. If the value represented by a single hexadecimal escape sequence does not fit the range of values represented by the character type used in this string literal or character constant (char, char8_t(since C23), char16_t, char32_t(since C11), or wchar_t), the result is unspecified.

|  |  |
| --- | --- |
| A universal character name in a narrow string literal or a 16-bit string literal(since C11) may map to more than one code unit, e.g. \U0001f34c is 4 char code units in UTF-8 (\xF0\x9F\x8D\x8C) and 2 char16_t code units in UTF-16 (\xD83C\xDF4C)(since C11). | (since C99) |

|  |  |
| --- | --- |
| A universal character name corresponding to a code pointer greater than `0x10FFFF` (which is undefined in ISO/ISC 10646) can be used in character constants and string literals. Such usage is not allowed in C++20. | (since C99) (until C23) |

|  |  |
| --- | --- |
| The question mark escape sequence \? is used to prevent trigraphs from being interpreted inside string literals: a string such as "??/" is compiled as "\", but if the second question mark is escaped, as in "?\?/", it becomes "??/" | (until C23) |

### Example

Run this code

```
#include <stdio.h>
 
int main(void)
{
    printf("This\nis\na\ntest\n\nShe said, \"How are you?\"\n");
}

```

Output:

```
This
is
a
test
 
She said, "How are you?"

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 5.2.2 Character display semantics (p: 18-19)

:   - 6.4.3 Universal Character names (p: 44)

:   - 6.4.4.4 Character constants (p: 48-50)

- C11 standard (ISO/IEC 9899:2011):

:   - 5.2.2 Character display semantics (p: 24-25)

:   - 6.4.3 Universal Character names (p: 61)

:   - 6.4.4.4 Character constants (p: 67-70)

- C99 standard (ISO/IEC 9899:1999):

:   - 5.2.2 Character display semantics (p: 19-20)

:   - 6.4.3 Universal Character names (p: 53)

:   - 6.4.4.4 Character constants (p: 59-61)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 2.2.2 Character display semantics

:   - 3.1.3.4 Character constants

### See also

- ASCII chart

|  |  |
| --- | --- |
| C++ documentation for Escape sequences | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/escape&oldid=158256>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 September 2023, at 10:25.