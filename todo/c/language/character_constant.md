# Character constant

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
| ****character constant**** | | | | |
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

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `'`c-char `'` | (1) |  |
|  | | | | | | | | | |
| `u8'`c-char `'` | (2) | (since C23) |
|  | | | | | | | | | |
| `u'`c-char `'` | (3) | (since C11) |
|  | | | | | | | | | |
| `U'`c-char `'` | (4) | (since C11) |
|  | | | | | | | | | |
| `L'`c-char `'` | (5) |  |
|  | | | | | | | | | |
| `'`c-char-sequence `'` | (6) |  |
|  | | | | | | | | | |
| `L'`c-char-sequence `'` | (7) |  |
|  | | | | | | | | | |
| `u'`c-char-sequence `'` | (8) | (since C11)(removed in C23) |
|  | | | | | | | | | |
| `U'`c-char-sequence `'` | (9) | (since C11)(removed in C23) |
|  | | | | | | | | | |

where

- c-char is either

:   - a character from the basic source character set minus single-quote (`'`), backslash (`\`), or the newline character.
    - escape sequence: one of special character escapes \' \" \? \\ \a \b \f \n \r \t \v, hex escapes \x... or octal escapes \... as defined in escape sequences.

|  |  |
| --- | --- |
| - universal character name, \u... or \U... as defined in escape sequences. | (since C99) |

- c-char-sequence is a sequence of two or more c-chars.

1) single-byte integer character constant, e.g. 'a' or '\n' or '\13'. Such constant has type int and a value equal to the representation of c-char in the execution character set as a value of type char mapped to int. If c-char is not representable as a single byte in the execution character set, the value is implementation-defined.2) UTF-8 character constant, e.g. u8'a'. Such constant has type char8_t and the value equal to ISO 10646 code point value of c-char, provided that the code point value is representable with a single UTF-8 code unit (that is, c-char is in the range 0x0-0x7F, inclusive). If c-char is not representable with a single UTF-8 code unit, the program is ill-formed.

|  |  |
| --- | --- |
| 3) 16-bit wide character constant, e.g. u'貓', but not u'🍌' (u'\U0001f34c'). Such constant has type char16_t and a value equal to the value of c-char in the 16-bit encoding produced by mbrtoc16 (normally UTF-16). If c-char is not representable or maps to more than one 16-bit character, the value is implementation-defined.4) 32-bit wide character constant, e.g. U'貓' or U'🍌'. Such constant has type char32_t and a value equal to the value of c-char in in the 32-bit encoding produced by mbrtoc32 (normally UTF-32). If c-char is not representable or maps to more than one 32-bit character, the value is implementation-defined. | (until C23) |
| 3) UTF-16 character constant, e.g. u'貓', but not u'🍌' (u'\U0001f34c'). Such constant has type char16_t and the value equal to ISO 10646 code point value of c-char, provided that the code point value is representable with a single UTF-16 code unit (that is, c-char is in the range 0x0-0xD7FF or 0xE000-0xFFFF, inclusive). If c-char is not representable with a single UTF-16 code unit, the program is ill-formed.4) UTF-32 character constant, e.g. U'貓' or U'🍌'. Such constant has type char32_t and the value equal to ISO 10646 code point value of c-char, provided that the code point value is representable with a single UTF-32 code unit (that is, c-char is in the range 0x0-0xD7FF or 0xE000-0x10FFFF, inclusive). If c-char is not representable with a single UTF-32 code unit, the program is ill-formed. | (since C23) |

5) wide character constant, e.g. L'β' or L'貓. Such constant has type wchar_t and a value equal to the value of c-char in the execution wide character set (that is, the value that would be produced by mbtowc). If c-char is not representable or maps to more than one wide character (e.g. a non-BMP value on Windows where wchar_t is 16-bit), the value is implementation-defined .6) multicharacter constant, e.g. 'AB', has type int and implementation-defined value.7) wide multicharacter constant, e.g. L'AB', has type wchar_t and implementation-defined value.8) 16-bit multicharacter constant, e.g. u'CD', has type char16_t and implementation-defined value.9) 32-bit multicharacter constant, e.g. U'XY', has type char32_t and implementation-defined value.

### Notes

Multicharacter constants were inherited by C from the B programming language. Although not specified by the C standard, most compilers (MSVC is a notable exception) implement multicharacter constants as specified in B: the values of each char in the constant initialize successive bytes of the resulting integer, in big-endian zero-padded right-adjusted order, e.g. the value of '\1' is 0x00000001 and the value of '\1\2\3\4' is 0x01020304.

In C++, encodable ordinary character literals have type char, rather than int.

Unlike integer constants, a character constant may have a negative value if char is signed: on such implementations '\xFF' is an int with the value -1.

When used in a controlling expression of #if or #elif, character constants may be interpreted in terms of the source character set, the execution character set, or some other implementation-defined character set.

16/32-bit multicharacter constants are not widely supported and removed in C23. Some common implementations (e.g. clang) do not accept them at all.

### Example

Run this code

```
#include <stddef.h>
#include <stdio.h>
#include <uchar.h>
 
int main (void)
{
    printf("constant value     \n");
    printf("-------- ----------\n");
 
    // integer character constants,
    int c1='a'; printf("'a':\t %#010x\n", c1);
    int c2='🍌'; printf("'🍌':\t %#010x\n\n", c2); // implementation-defined
 
    // multicharacter constant
    int c3='ab'; printf("'ab':\t %#010x\n\n", c3); // implementation-defined
 
    // 16-bit wide character constants
    char16_t uc1 = u'a'; printf("'a':\t %#010x\n", (int)uc1);
    char16_t uc2 = u'¢'; printf("'¢':\t %#010x\n", (int)uc2);
    char16_t uc3 = u'猫'; printf("'猫':\t %#010x\n", (int)uc3);
    // implementation-defined (🍌 maps to two 16-bit characters)
    char16_t uc4 = u'🍌'; printf("'🍌':\t %#010x\n\n", (int)uc4);
 
    // 32-bit wide character constants
    char32_t Uc1 = U'a'; printf("'a':\t %#010x\n", (int)Uc1);
    char32_t Uc2 = U'¢'; printf("'¢':\t %#010x\n", (int)Uc2);
    char32_t Uc3 = U'猫'; printf("'猫':\t %#010x\n", (int)Uc3);
    char32_t Uc4 = U'🍌'; printf("'🍌':\t %#010x\n\n", (int)Uc4);
 
    // wide character constants
    wchar_t wc1 = L'a'; printf("'a':\t %#010x\n", (int)wc1);
    wchar_t wc2 = L'¢'; printf("'¢':\t %#010x\n", (int)wc2);
    wchar_t wc3 = L'猫'; printf("'猫':\t %#010x\n", (int)wc3);
    wchar_t wc4 = L'🍌'; printf("'🍌':\t %#010x\n\n", (int)wc4);
}

```

Possible output:

```
constant value     
-------- ----------
'a':	 0x00000061
'🍌':	 0xf09f8d8c
 
'ab':	 0x00006162
 
'a':	 0x00000061
'¢':	 0x000000a2
'猫':	 0x0000732b
'🍌':	 0x0000df4c
 
'a':	 0x00000061
'¢':	 0x000000a2
'猫':	 0x0000732b
'🍌':	 0x0001f34c
 
'a':	 0x00000061
'¢':	 0x000000a2
'猫':	 0x0000732b
'🍌':	 0x0001f34c

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.4.4.4 Character constants (p: 48-50)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.4.4.4 Character constants (p: 67-70)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.4.4.4 Character constants (p: 59-61)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.1.3.4 Character constants

### See also

|  |  |
| --- | --- |
| C++ documentation for Character literal | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/character_constant&oldid=146412>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 January 2023, at 07:48.