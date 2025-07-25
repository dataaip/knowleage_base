# Phases of translation

From cppreference.com
< cpp‎ | language
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Punctuation | | | | |
| Names and identifiers | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| Scope | | | | |
| Object lifetime | | | | |
| Storage duration and linkage | | | | |
| Definitions and ODR | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| ****Phases of translation**** | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

C++ source files are processed by the compiler to produce C++ programs.

### Translation process

The text of a C++ program is kept in units called **source files**.

C++ source files undergo **translation** to become a **translation unit**, consisting of the following steps:

1. Maps each source file to a character sequence.
2. Converts each character sequence to a preprocessing token sequence, separated by whitespace.
3. Converts each preprocessing token to a token, forming a token sequence.
4. Converts each token sequence to a translation unit.

A C++ program can be formed from translated translation units. Translation units can be separately translated and then later linked to produce an executable program.

The process above can be organized into 9 translation phases.

### Preprocessing tokens

A **preprocessing token** is the minimal lexical element of the language in translation phases 3 through 6.

The categories of preprocessing token are:

- header names (such as <iostream> or "myfile.h")

|  |  |
| --- | --- |
| - placeholder tokens produced by preprocessing import and module directives (i.e. import XXX; and module XXX;) | (since C++20) |

- identifiers
- preprocessing numbers (see below)
- character literals, including user-defined character literals(since C++11)
- string literals, including user-defined string literals(since C++11)
- operators and punctuators, including alternative tokens
- individual non-whitespace characters that do not fit in any other category

:   The program is ill-formed if the character matching this category is

    - apostrophe (', U+0027),
    - quotation mark (", U+0022), or
    - a character not in the basic character set.

#### Preprocessing numbers

The set of preprocessing tokens of preprocessing number is a superset of the union of the sets of tokens of integer literals and floating-point literals:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `.`(optional) digit pp-continue-seq ﻿(optional) |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| digit | - | one of digits 0-9 |
| pp-continue-seq | - | a sequence of pp-continue ﻿s |

Each pp-continue is one of the following:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| identifier-continue | (1) |  |
|  | | | | | | | | | |
| exp-char sign-char | (2) |  |
|  | | | | | | | | | |
| `.` | (3) |  |
|  | | | | | | | | | |
| `’` digit | (4) | (since C++14) |
|  | | | | | | | | | |
| `’` nondigit | (5) | (since C++14) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| identifier-continue | - | any non-first character of a valid identifier |
| exp-char | - | one of `P`, `p`,(since C++11) `E` and `e` |
| sign-char | - | one of `+` and `-` |
| digit | - | one of digits 0-9 |
| nondigit | - | one of Latin letters A/a-Z/z and underscore |

A preprocessing number does not have a type or a value; it acquires both after a successful conversion an integer/floating-point literal token.

#### Whitespace

**Whitespace** consists of comments, whitespace characters, or both.

The following characters are whitespace characters:

- character tabulation (U+0009)
- line feed / new-line character (U+000A)
- line tabulation (U+000B)
- form feed (U+000C)
- space (U+0020)

Whitespace is usually used to separate preprocessing tokens, with the following exceptions:

- It is not a separator in header name, character literal and string literal.
- Preprocessing tokens separated by whitespace containing new-line characters cannot form preprocessing directives.

```
#include "my header"        // OK, using a header name containing whitespace
 
#include/*hello*/<iostream> // OK, using a comment as whitespace
 
#include
<iostream> // Error: #include cannot span across multiple lines
 
"str ing"  // OK, a single preprocessing token (string literal)
' '        // OK, a single preprocessing token (character literal)

```

#### Maximal munch

If the input has been parsed into preprocessing tokens up to a given character, the next preprocessing token is generally taken to be the longest sequence of characters that could constitute a preprocessing token, even if that would cause subsequent analysis to fail. This is commonly known as **maximal munch**.

```
int foo = 1;
int bar = 0xE+foo;   // Error: invalid preprocessing number 0xE+foo
int baz = 0xE + foo; // OK

```

In other words, the maximal munch rule is in favor of multi-character operators and punctuators:

```
int foo = 1;
int bar = 2;
 
int num1 = foo+++++bar; // Error: treated as “foo++ ++ +baz”, not “foo++ + ++baz”
int num2 = -----foo;    // Error: treated as “-- -- -foo”, not “- -- --foo”

```

The maximal munch rule has the following exceptions:

- Header name preprocessing tokens are only formed in the following cases:

:   - after the include preprocessing token in an #include directive

|  |  |
| --- | --- |
| - in a __has_include expression | (since C++17) |
| - after the import preprocessing token in an import directive | (since C++20) |

```
std::vector<int> x; // OK, “int” is not a header name

```

- If the next three characters are <:: and the subsequent character is neither : nor >, the < is treated as a preprocessing token by itself instead of the first character of the alternative token <:.

```
struct Foo { static const int v = 1; };
std::vector<::Foo> x;  // OK, <: not taken as the alternative token for [
extern int y<::>;      // OK, same as “extern int y[];”
int z<:::Foo::value:>; // OK, same as “int z[::Foo::value];”

```

|  |  |
| --- | --- |
| - If the next two characters are >> and one of the > character can complete a template identifier, the character is treated as a preprocessing token alone instead of being part of the preprocessing token >>.  ```text template<int i> class X { /* ... */ }; template<class T> class Y { /* ... */ };   Y<X<1>> x3;      // OK, declares a variable “x3” of type “Y<X<1> >” Y<X<6>>1>> x4;   // Syntax error Y<X<(6>>1)>> x5; // OK ```  - If the next character begins a sequence of characters that could be the prefix and initial double quote of a raw string literal, the next preprocessing token is a raw string literal. The literal consists of the shortest sequence of characters that matches the raw-string pattern.  ```text #define R "x" const char* s = R"y";         // ill-formed raw string literal, not "x" "y" const char* s2 = R"(a)" "b)"; // a raw string literal followed by a normal string literal ``` | (since C++11) |

### Tokens

A **token** is the minimal lexical element of the language in translation phase 7.

The categories of token are:

- identifiers
- keywords
- literals
- operators and punctuators (except preprocessing operators)

### Translation phases

Translation is performed as if in the order from phase 1 to phase 9. Implementations behave as if these separate phases occur, although in practice different phases can be folded together.

#### Phase 1: Mapping source characters

|  |  |  |  |
| --- | --- | --- | --- |
| 1) The individual bytes of the source code file are mapped (in implementation-defined manner) to the characters of the basic source character set. In particular, OS-dependent end-of-line indicators are replaced by newline characters.2) The set of source file characters accepted is implementation-defined(since C++11). Any source file character that cannot be mapped to a character in the basic source character set is replaced by its universal character name (escaped with `\u` or `\U`) or by some implementation-defined form that is handled equivalently.  |  |  | | --- | --- | | 3) Trigraph sequences are replaced by corresponding single-character representations. | (until C++17) | | (until C++23) |
| Input files that are a sequence of UTF-8 code units (UTF-8 files) are guaranteed to be supported. The set of other supported kinds of input files is implementation-defined. If the set is non-empty, the kind of an input file is determined in an implementation-defined manner that includes a means of designating input files as UTF-8 files, independent of their content (recognizing the byte order mark is not sufficient).   - If an input file is determined to be a UTF-8 file, then it shall be a well-formed UTF-8 code unit sequence and it is decoded to produce a sequence of Unicode scalar values. A sequence of translation character set elements is then formed by mapping each Unicode scalar value to the corresponding translation character set element. In the resulting sequence, each pair of characters in the input sequence consisting of carriage return (U+000D) followed by line feed (U+000A), as well as each carriage return (U+000D) not immediately followed by a line feed (U+000A), is replaced by a single new-line character. - For any other kind of input file supported by the implementation, characters are mapped (in implementation-defined manner) to a sequence of translation character set elements. In particular, OS-dependent end-of-line indicators are replaced by new-line characters. | (since C++23) |

#### Phase 2: Splicing lines

1) If the first translation character is byte order mark (U+FEFF), it is deleted. (since C++23)Whenever backslash (\) appears at the end of a line (immediately followed by zero or more whitespace characters other than new-line followed by(since C++23) the newline character), these characters are deleted, combining two physical source lines into one logical source line. This is a single-pass operation; a line ending in two backslashes followed by an empty line does not combine three lines into one.2) If a non-empty source file does not end with a newline character after this step (end-of-line backslashes are no longer splices at this point), a terminating newline character is added.

#### Phase 3: Lexing

1) The source file is decomposed into preprocessing tokens and whitespace:

```
// The following #include directive can de decomposed into 5 preprocessing tokens:
 
//     punctuators (#, < and >)
//          │
// ┌────────┼────────┐
// │        │        │
   #include <iostream>
//     │        │
//     │        └── header name (iostream)
//     │
//     └─────────── identifier (include)

```

 If a source file ends in a partial preprocessing token or in a partial comment, the program is ill-formed:

```
// Error: partial string literal
"abc

```

```
// Error: partial comment
/* comment

```

|  |  |
| --- | --- |
| As characters from the source file are consumed to form the next preprocessing token (i.e., not being consumed as part of a comment or other forms of whitespace), universal character names are recognized and replaced by the designated element of the translation character set, except when matching a character sequence in one of the following preprocessing tokens: - a character literal (c-char-sequence) - a string literal (s-char-sequence and r-char-sequence), excluding delimiters (d-char-sequence) - a header name (h-char-sequence and q-char-sequence) | (since C++23) |

|  |  |
| --- | --- |
| 2) Any transformations performed during phase 1 and(until C++23) phase 2 between the initial and the final double quote of any raw string literal are reverted. | (since C++11) |

3) Whitespace is transformed:

- Each comment is replaced by one space character.
- New-line characters are retained.
- Whether each nonempty sequence of whitespace characters other than new-line is retained or replaced by one space character is unspecified.

#### Phase 4: Preprocessing

1) The preprocessor is executed.2) Each file introduced with the #include directive goes through phases 1 through 4, recursively.3) At the end of this phase, all preprocessor directives are removed from the source.

#### Phase 5: Determining common string literal encodings

|  |  |
| --- | --- |
| 1) All characters in character literals and string literals are converted from the source character set to the encoding (which may be a multibyte character encoding such as UTF-8, as long as the 96 characters of the basic character set have single-byte representations).2) Escape sequences and universal character names in character literals and non-raw string literals are expanded and converted to the literal encoding. If the character specified by a universal character name cannot be encoded as a single code point in the corresponding literal encoding, the result is implementation-defined, but is guaranteed not to be a null (wide) character. | (until C++23) |
| For a sequence of two or more adjacent string literal tokens, a common encoding prefix is determined as described here. Each such string literal token is then considered to have that common encoding prefix. (Character conversion is moved to phase 3) | (since C++23) |

#### Phase 6: Concatenating string literals

Adjacent string literals are concatenated.

#### Phase 7: Compiling

Compilation takes place: each preprocessing token is converted to a token. The tokens are syntactically and semantically analyzed and translated as a translation unit.

#### Phase 8: Instantiating templates

Each translation unit is examined to produce a list of required template instantiations, including the ones requested by explicit instantiations. The definitions of the templates are located, and the required instantiations are performed to produce **instantiation units**.

#### Phase 9: Linking

Translation units, instantiation units, and library components needed to satisfy external references are collected into a program image which contains information needed for execution in its execution environment.

### Notes

Source files, translation units and translated translation units need not necessarily be stored as files, nor need there be any one-to-one correspondence between these entities and any external representation. The description is conceptual only, and does not specify any particular implementation.

|  |  |
| --- | --- |
| The conversion performed at phase 5 can be controlled by command line options in some implementations: gcc and clang use -finput-charset to specify the encoding of the source character set, -fexec-charset and -fwide-exec-charset to specify the ordinary and wide literal encodings respectively, while Visual Studio 2015 Update 2 and later uses /source-charset and /execution-charset to specify the source character set and literal encoding respectively. | (until C++23) |

Some compilers do not implement instantiation units (also known as template repositories or template registries) and simply compile each template instantiation at phase 7, storing the code in the object file where it is implicitly or explicitly requested, and then the linker collapses these compiled instantiations into one at phase 9.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 787 | C++98 | the behavior was undefined if a non-empty source file does not end with a newline character at the end of phase 2 | add a terminating newline character in this case |
| CWG 1104 | C++98 | the alternative token <: caused std::vector<::std::string> to be treated as std::vector:[std::string> | added an additional lexing rule to address this case |
| CWG 1775 | C++11 | forming a universal character name inside a raw string literal in phase 2 resulted in undefined behavior | made well-defined |
| CWG 2747 | C++98 | phase 2 checked the end-of-file splice after splicing, this is unnecessary | removed the check |
| P2621R3 | C++98 | universal character names were not allowed to be formed by line splicing or token concatenation | allowed |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 5.2 Phases of translation [lex.phases]

- C++20 standard (ISO/IEC 14882:2020):

:   - 5.2 Phases of translation [lex.phases]

- C++17 standard (ISO/IEC 14882:2017):

:   - 5.2 Phases of translation [lex.phases]

- C++14 standard (ISO/IEC 14882:2014):

:   - 2.2 Phases of translation [lex.phases]

- C++11 standard (ISO/IEC 14882:2011):

:   - 2.2 Phases of translation [lex.phases]

- C++03 standard (ISO/IEC 14882:2003):

:   - 2.1 Phases of translation [lex.phases]

- C++98 standard (ISO/IEC 14882:1998):

:   - 2.1 Phases of translation [lex.phases]

### See also

|  |  |
| --- | --- |
| C documentation for Phases of translation | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/translation_phases&oldid=179758>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 January 2025, at 07:47.