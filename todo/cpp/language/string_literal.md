# String literal

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
| Character - ****String**** - nullptr (C++11) | | | | |
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

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | ****String literals**** | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `"`s-char-seq ﻿(optional)`"` | (1) |  |
|  | | | | | | | | | |
| `R"`d-char-seq ﻿(optional)`(`r-char-seq ﻿(optional)`)`d-char-seq ﻿(optional)`"` | (2) | (since C++11) |
|  | | | | | | | | | |
| `L"`s-char-seq ﻿(optional)`"` | (3) |  |
|  | | | | | | | | | |
| `LR"`d-char-seq ﻿(optional)`(`r-char-seq ﻿(optional)`)`d-char-seq ﻿(optional)`"` | (4) | (since C++11) |
|  | | | | | | | | | |
| `u8"`s-char-seq ﻿(optional)`"` | (5) | (since C++11) |
|  | | | | | | | | | |
| `u8R"`d-char-seq ﻿(optional)`(`r-char-seq ﻿(optional)`)`d-char-seq ﻿(optional)`"` | (6) | (since C++11) |
|  | | | | | | | | | |
| `u"`s-char-seq ﻿(optional)`"` | (7) | (since C++11) |
|  | | | | | | | | | |
| `uR"`d-char-seq ﻿(optional)`(`r-char-seq ﻿(optional)`)`d-char-seq ﻿(optional)`"` | (8) | (since C++11) |
|  | | | | | | | | | |
| `U"`s-char-seq ﻿(optional)`"` | (9) | (since C++11) |
|  | | | | | | | | | |
| `UR"`d-char-seq ﻿(optional)`(`r-char-seq ﻿(optional)`)`d-char-seq ﻿(optional)`"` | (10) | (since C++11) |
|  | | | | | | | | | |

### Explanation

|  |  |  |
| --- | --- | --- |
| s-char-seq | - | A sequence of one or more s-char ﻿s |
| s-char | - | One of  - a basic-s-char - an escape sequence, as defined in escape sequences - a universal character name, as defined in escape sequences |
| basic-s-char | - | A character from the translation character set, except the double-quote ", backslash \, or new-line character |
| d-char-seq | - | A sequence of one or more d-char ﻿s, at most 16 characters long |
| d-char | - | A character from the basic character set, except parentheses, backslash and spaces |
| r-char-seq | - | A sequence of one or more r-char ﻿s, except that it must not contain the closing sequence `)`d-char-seq`"` |
| r-char | - | A character from the translation character set |

| Syntax | Kind | Type | Encoding |
| --- | --- | --- | --- |
| (1,2) | ordinary string literal | const char[N] | ordinary literal encoding |
| (3,4) | wide string literal | const wchar_t[N] | wide literal encoding |
| (5,6) | UTF-8 string literal | |  |  | | --- | --- | | const char[N] | (until C++20) | | const char8_t[N] | (since C++20) | | UTF-8 |
| (7,8) | UTF-16 string literal | const char16_t[N] | UTF-16 |
| (9,10) | UTF-32 string literal | const char32_t[N] | UTF-32 |

In the types listed in the table above, N is the number of encoded code units, which is determined below.

Ordinary and UTF-8(since C++11) string literals are collectively referred to as narrow string literals.

Evaluating a string literal results in a string literal object with static storage duration. Whether all string literals are stored in nonoverlapping objects and whether successive evaluations of a string literal yield the same or a different object is unspecified.

The effect of attempting to modify a string literal object is undefined.

```
bool b = "bar" == 3 + "foobar"; // can be true or false, unspecified
 
const char* pc = "Hello";
char* p = const_cast<char*>(pc);
p[0] = 'M'; // undefined behavior

```

|  |  |
| --- | --- |
| Raw string literals Raw string literals are string literals with a prefix containing `R` (syntaxes (2,4,6,8,10)). They do not escape any character, which means anything between the delimiters d-char-seq ﻿`(` and `)`d-char-seq becomes part of the string. The terminating d-char-seq is the same sequence of characters as the initial d-char-seq.   ```text // OK: contains one backslash, // equivalent to "\\" R"(\)";   // OK: contains four \n pairs, // equivalent to "\\n\\n\\n\\n" R"(\n\n\n\n)";   // OK: contains one close-parenthesis, two double-quotes and one open-parenthesis, // equivalent to ")\"\"(" R"-()""()-";   // OK: equivalent to "\n)\\\na\"\"\n" R"a( )\ a"" )a";   // OK: equivalent to "x = \"\"\\y\"\"" R"(x = ""\y"")";   // R"<<(-_-)>>"; // Error: begin and end delimiters do not match // R"-()-"-()-"; // Error: )-" appears in the middle and terminates the literal ``` | (since C++11) |

### Initialization

String literal objects are initialized with the sequence of code unit values corresponding to the string literal’s sequence of s-char ﻿s and r-char ﻿s(since C++11), plus a terminating null character (U+0000), in order as follows:

1) For each contiguous sequence of basic-s-char ﻿s, r-char ﻿s,(since C++11) simple escape sequences and universal character names, the sequence of character it denotes is encoded to a code unit sequence using the string literal’s associated character encoding. If a character lacks representation in the associated character encoding, then the program is ill-formed. If the associated character encoding is stateful, the first such sequence is encoded beginning with the initial encoding state and each subsequent sequence is encoded beginning with the final
encoding state of the prior sequence.2) For each numeric escape sequence, given v as the integer value represented by the octal or hexadecimal number comprising the sequence of digits in the escape sequence, and `T` as the string literal’s array element type (see the table above):

- If v does not exceed the range of representable values of `T`, then the escape sequence contributes a single code unit with value v.
- Otherwise, if the string literal is of syntax (1) or (3), and(since C++11) v does not exceed the range of representable values of the corresponding unsigned type for the underlying type of `T`, then the escape sequence contributes a single code unit with a unique value of type `T`, that is congruent to v mod 2S  
  , where S is the width of `T`.
- Otherwise, the program is ill-formed.
 If the associated character encoding is stateful, all such sequences have no effect on encoding state.3) Each conditional escape sequence contributes an implementation-defined code unit sequence. If the associated character encoding is stateful, it is implementation-defined what effect these sequences have on encoding state.

### Concatenation

Adjacent string literals are concatenated at translation phase 6 (after preprocessing):

- If the two string literals are of the same kind, the concatenated string literal is also of that kind.

|  |  |
| --- | --- |
| - If an ordinary string literal is adjacent to a wide string literal, the behavior is undefined. | (until C++11) |
| - If an ordinary string literal is adjacent to a non-ordinary string literal, the concatenated string literal is of the kind of the latter. - If a UTF-8 string literal is adjacent to a wide string literal, the program is ill-formed.  |  |  | | --- | --- | | - Any other combination is conditionally supported with implementation-defined semantics.[[1]](string_literal.html#cite_note-1) | (until C++23) | | - Any other combination is ill-formed. | (since C++23) | | (since C++11) |

```
"Hello, " " world!" // at phase 6, the 2 string literals form "Hello, world!"
 
L"Δx = %" PRId16    // at phase 4, PRId16 expands to "d"
                    // at phase 6, L"Δx = %" and "d" form L"Δx = %d"

```

1. ↑ No known implementation supports such concatenation.

### Unevaluated strings

The following contexts expect a string literal, but do not evaluate it:

- language linkage specification

|  |  |
| --- | --- |
| - `static_assert` - literal operator name | (since C++11) |
| - `[[deprecated]]` | (since C++14) |
| - `[[nodiscard]]` | (since C++20) |
| - deleted function body | (since C++26) |

|  |  |
| --- | --- |
| It is unspecified whether non-ordinary string literals are allowed in these contexts, except that a literal operator name must use an ordinary string literal(since C++11). | (until C++26) |
| Only ordinary string literals are allowed in these contexts.  Each universal character name and each simple escape sequence in an unevaluated string is replaced by the member of the translation character set it denotes. An unevaluated string that contains a numeric escape sequence or a conditional escape sequence is ill-formed. | (since C++26) |

### Notes

String literals can be used to initialize character arrays. If an array is initialized like char str[] = "foo";, str will contain a copy of the string "foo".

|  |  |
| --- | --- |
| String literals are convertible and assignable to non-const char\* or wchar_t\* in order to be compatible with C, where string literals are of types char[N] and wchar_t[N]. Such implicit conversion is deprecated. | (until C++11) |
| String literals are not convertible or assignable to non-const `CharT*`. An explicit cast (e.g. `const_cast`) must be used if such conversion is wanted. | (since C++11) |

A string literal is not necessarily a null-terminated character sequence: if a string literal has embedded null characters, it represents an array which contains more than one string.

```
const char* p = "abc\0def"; // std::strlen(p) == 3, but the array has size 8

```

If a valid hexadecimal digit follows a hexadecimal escape sequence in a string literal, it would fail to compile as an invalid escape sequence. String concatenation can be used as a workaround:

```
//const char* p = "\xfff"; // error: hexadecimal escape sequence out of range
const char* p = "\xff""f"; // OK: the literal is const char[3] holding {'\xff','f','\0'}

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_char8_t` | `202207L` | (C++23) (DR20) | char8_t compatibility and portability fix (allow initialization of (unsigned) char arrays from UTF-8 string literals) |
| `__cpp_raw_strings` | `200710L` | (C++11) | Raw string literals |
| `__cpp_unicode_literals` | `200710L` | (C++11) | Unicode string literals |

### Example

Run this code

```
#include <iostream>
 
// array1 and array2 contains the same values:
char array1[] = "Foo" "bar";
char array2[] = {'F', 'o', 'o', 'b', 'a', 'r', '\0'};
 
const char* s1 = R"foo(
Hello
  World
)foo";
// same as
const char* s2 = "\nHello\n  World\n";
// same as
const char* s3 = "\n"
                 "Hello\n"
                 "  World\n";
 
const wchar_t* s4 = L"ABC" L"DEF"; // OK, same as
const wchar_t* s5 = L"ABCDEF";
const char32_t* s6 = U"GHI" "JKL"; // OK, same as
const char32_t* s7 = U"GHIJKL";
const char16_t* s9 = "MN" u"OP" "QR"; // OK, same as
const char16_t* sA = u"MNOPQR";
 
// const auto* sB = u"Mixed" U"Types";
        // before C++23 may or may not be supported by
        // the implementation; ill-formed since C++23
 
const wchar_t* sC = LR"--(STUV)--"; // OK, raw string literal
 
int main()
{
    std::cout << array1 << ' ' << array2 << '\n'
              << s1 << s2 << s3 << std::endl;
    std::wcout << s4 << ' ' << s5 << ' ' << sC
               << std::endl;
}

```

Output:

```
Foobar Foobar
 
Hello
  World
 
Hello
  World
 
Hello
  World
 
ABCDEF ABCDEF STUV

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 411 (P2029R4) | C++98 | escape sequences in string literals were not allowed to map to multiple code units | allowed |
| CWG 1656 (P2029R4) | C++98 | the characters denoted by numeric escape sequences in string literals were unclear | made clear |
| CWG 1759 | C++11 | a UTF-8 string literal might have code units that are not representable in char | char can represent all UTF-8 code units |
| CWG 1823 | C++98 | whether string literals are distinct was implementation-defined | distinctness is unspecified, and same string literal can yield different object |
| CWG 2333 (P2029R4) | C++11 | it was unclear whether numeric escape sequences were allowed in UTF-8/16/32 string literals | made clear |
| CWG 2870 | C++11 | the concatenation result of two ordinary string literals was unclear | made clear |
| P1854R4 | C++98 | ordinary and wide string literals with non-encodable characters were conditionally-supported | programs with such literals are ill-formed |
| P2029R4 | C++98 | 1. it was unclear whether string literals     could contain non-encodable characters 2. it was unclear whether string literals could     contain numeric escape sequences such     that the code units they represent are not     representable in the literals' array element type | 1. made conditionally-supported for     ordinary and wide string literals[[1]](string_literal.html#cite_note-2) 2. ill-formed if the code units are     neither representable in the     unsigned integer type corresponding     to the underlying type |

1. ↑ P1854R4 was accepted as a DR later, overriding this resolution.

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 5.13.5 String literals [lex.string]

- C++20 standard (ISO/IEC 14882:2020):

:   - 5.13.5 String literals [lex.string]

- C++17 standard (ISO/IEC 14882:2017):

:   - 5.13.5 String literals [lex.string]

- C++14 standard (ISO/IEC 14882:2014):

:   - 2.14.5 String literals [lex.string]

- C++11 standard (ISO/IEC 14882:2011):

:   - 2.14.5 String literals [lex.string]

- C++03 standard (ISO/IEC 14882:2003):

:   - 2.13.4 String literals [lex.string]

- C++98 standard (ISO/IEC 14882:1998):

:   - 2.13.4 String literals [lex.string]

### See also

|  |  |
| --- | --- |
| user-defined literals(C++11) | literals with user-defined suffix |
| C documentation for String literals | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/string_literal&oldid=179505>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 January 2025, at 13:10.