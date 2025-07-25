# Phases of translation

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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Character sets | | | | |
| ****Translation phases**** | | | | |
| Punctuation | | | | |
| Identifier | | | | |
| Scope | | | | |
| Lifetime | | | | |
| Lookup and name spaces | | | | |
| Type | | | | |
| Arithmetic types | | | | |
| Objects and alignment | | | | |
| The main() function | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model and data races | | | | |

The C source file is processed by the compiler **as if** the following phases take place, in this exact order. Actual implementation may combine these actions or process them differently as long as the behavior is the same.

### Phase 1

1) The individual bytes of the source code file (which is generally a text file in some multibyte encoding such as UTF-8) are mapped, in implementation defined manner, to the characters of the **source character set**. In particular, OS-dependent end-of-line indicators are replaced by newline characters.

:   The **source character set** is a multibyte character set which includes the **basic source character set** as a single-byte subset, consisting of the following 96 characters:

a) 5 whitespace characters (space, horizontal tab, vertical tab, form feed, new-line)b) 10 digit characters from '0' to '9'c) 52 letters from 'a' to 'z' and from 'A' to 'Z'd) 29 punctuation characters: _ { } [ ] # ( ) < > % : ; . ? \* + - / ^ & | ~ ! = , \ " '2) Trigraph sequences are replaced by corresponding single-character representations.(until C23)

### Phase 2

1) Whenever backslash appears at the end of a line (immediately followed by the newline character), both backslash and newline are deleted, combining two physical source lines into one logical source line. This is a single-pass operation: a line ending in two backslashes followed by an empty line does not combine three lines into one.Run this code

```
#include <stdio.h>
 
#define PUTS p\
u\
t\
s
/* Line splicing is in phase 2 while macros
 * are tokenized in phase 3 and expanded in phase 4,
 * so the above is equivalent to #define PUTS puts
 */
 
int main(void)
{
 /* Use line splicing to call puts */ PUT\
S\
("Output ends here\\
0Not printed" /* After line splicing, the remaining backslash
               * escapes the 0, ending the string early.
               */
);
}

```

2) If a non-empty source file does not end with a newline character after this step (whether it had no newline originally, or it ended with a backslash), the behavior is undefined.

### Phase 3

1) The source file is decomposed into comment, sequences of whitespace characters (space, horizontal tab, new-line, vertical tab, and form-feed), and **preprocessing tokens**, which are the followinga) header names: <stdio.h> or "myfile.h"b) identifiersc) preprocessing numbers, which cover integer constants and floating constants, but also cover some invalid tokens such as 1..E+3.foo or 0JBKd) character constants and string literalse) operators and punctuators, such as +, <<=, <%, or ##.f) individual non-whitespace characters that do not fit in any other category2) Each comment is replaced by one space character3) Newlines are kept, and it's implementation-defined whether non-newline whitespace sequences may be collapsed into single space characters.

If the input has been parsed into preprocessing tokens up to a given character, the next preprocessing token is generally taken to be the longest sequence of characters that could constitute a preprocessing token, even if that would cause subsequent analysis to fail. This is commonly known as **maximal munch**.

```
int foo = 1;
// int bar = 0xE+foo; // error: invalid preprocessing number 0xE+foo
int bar = 0xE/*Comment expands to a space*/+foo; // OK: 0xE + foo
int baz = 0xE + foo; // OK: 0xE + foo
int pub = bar+++baz; // OK: bar++ + baz
int ham = bar++-++baz; // OK: bar++ - ++baz
// int qux = bar+++++baz; // error: bar++ ++ +baz, not bar++ + ++baz
int qux = bar+++/*Saving comment*/++baz; // OK: bar++ + ++baz

```

The sole exception to the maximal munch rule is:

- Header name preprocessing tokens are only formed within a #include or #embed(since C23) directive, in __has_include and __has_embed expressions(since C23) and in implementation-defined locations within a #pragma directive.

```
#define MACRO_1 1
#define MACRO_2 2
#define MACRO_3 3
#define MACRO_EXPR (MACRO_1 <MACRO_2> MACRO_3) // OK: <MACRO_2> is not a header-name

```

### Phase 4

1) Preprocessor is executed.2) Each file introduced with the #include directive goes through phases 1 through 4, recursively.3) At the end of this phase, all preprocessor directives are removed from the source.

### Phase 5

1) All characters and escape sequences in character constants and string literals are converted from **source character set** to **execution character set** (which may be a multibyte character set such as UTF-8, as long as all 96 characters from the **basic source character set** listed in phase 1 have single-byte representations). If the character specified by an escape sequence isn't a member of the execution character set, the result is implementation-defined, but is guaranteed to not be a null (wide) character.

Note: the conversion performed at this stage can be controlled by command line options in some implementations: gcc and clang use -finput-charset to specify the encoding of the source character set, -fexec-charset and -fwide-exec-charset to specify the encodings of the execution character set in the string literals and character constants that don't have an encoding prefix(since C11).

### Phase 6

Adjacent string literals are concatenated.

### Phase 7

Compilation takes place: the tokens are syntactically and semantically analyzed and translated as a translation unit.

### Phase 8

Linking takes place: Translation units and library components needed to satisfy external references are collected into a program image which contains information needed for execution in its execution environment (the OS).

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 5.1.1.2 Translation phases (p: TBD)

:   - 5.2.1 Character sets (p: TBD)

:   - 6.4 Lexical elements (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 5.1.1.2 Translation phases (p: 9-10)

:   - 5.2.1 Character sets (p: 17)

:   - 6.4 Lexical elements (p: 41-54)

- C11 standard (ISO/IEC 9899:2011):

:   - 5.1.1.2 Translation phases (p: 10-11)

:   - 5.2.1 Character sets (p: 22-24)

:   - 6.4 Lexical elements (p: 57-75)

- C99 standard (ISO/IEC 9899:1999):

:   - 5.1.1.2 Translation phases (p: 9-10)

:   - 5.2.1 Character sets (p: 17-19)

:   - 6.4 Lexical elements (p: 49-66)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 2.1.1.2 Translation phases

:   - 2.2.1 Character sets

:   - 3.1 Lexical elements

### See also

|  |  |
| --- | --- |
| C++ documentation for Phases of translation | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/translation_phases&oldid=160564>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 October 2023, at 16:26.