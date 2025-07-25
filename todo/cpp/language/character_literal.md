# Character literal

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
| ****Character**** - String - nullptr (C++11) | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | ****Character literals**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `'`c-char ﻿`'` | (1) |  |
|  | | | | | | | | | |
| `u8'`c-char ﻿`'` | (2) | (since C++17) |
|  | | | | | | | | | |
| `u'`c-char ﻿`'` | (3) | (since C++11) |
|  | | | | | | | | | |
| `U'`c-char ﻿`'` | (4) | (since C++11) |
|  | | | | | | | | | |
| `L'`c-char ﻿`'` | (5) |  |
|  | | | | | | | | | |
| `'`c-char-sequence ﻿`'` | (6) |  |
|  | | | | | | | | | |
| `L'`c-char-sequence ﻿`'` | (7) | (until C++23) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| c-char | - | either  - a basic-c-char, - an escape sequence, as defined in escape sequences - a universal character name, as defined in escape sequences |
| basic-c-char | - | A character from the basic source character set(until C++23)translation character set(since C++23), except the single-quote ', backslash \, or new-line character |
| c-char-sequence | - | two or more c-chars |

### Explanation

1) Ordinary character literal, e.g. 'a' or '\n' or '\13'. Such literal has type char and the value equal to the representation of c-char in the execution character set(until C++23)the corresponding code point from ordinary literal encoding(since C++23).2) UTF-8 character literal, e.g. u8'a'. Such literal has type char(until C++20)char8_t(since C++20) and the value equal to ISO/IEC 10646 code point value of c-char, provided that the code point value is representable with a single UTF-8 code unit (that is, c-char is in the range 0x0-0x7F, inclusive).3) UTF-16 character literal, e.g. u'猫', but not u'🍌' (u'\U0001f34c'). Such literal has type char16_t and the value equal to ISO/IEC 10646 code point value of c-char, provided that the code point value is representable with a single UTF-16 code unit (that is, c-char is in the range 0x0-0xFFFF, inclusive).4) UTF-32 character literal, e.g. U'猫' or U'🍌'. Such literal has type char32_t and the value equal to ISO/IEC 10646 code point value of c-char.5) Wide character literal, e.g. L'β' or L'猫'. Such literal has type wchar_t and the value equal to the value of c-char in the execution wide character set(until C++23)the corresponding code point from wide literal encoding(since C++23).6) Ordinary multicharacter literal(until C++23)Multicharacter literal(since C++23), e.g. 'AB', is conditionally-supported, has type int and implementation-defined value.7) Wide multicharacter literal, e.g. L'AB', is conditionally-supported, has type wchar_t and implementation-defined value.

#### Non-encodable characters

1-5) Given that c-char is not a numeric escape sequence (see below), if c-char is not representable in the literal’s associated character encoding or cannot be encoded as a single code unit in that encoding (e.g. a non-BMP value on Windows where wchar_t is 16-bit), the program is ill-formed.6) If any c-char in c-char-sequence cannot be encoded as a single code unit in ordinary literal encoding, the program is ill-formed.

|  |  |
| --- | --- |
| 7) If any c-char in c-char-sequence cannot be encoded as a single code unit in wide literal encoding, the program is ill-formed. | (until C++23) |

#### Numeric escape sequences

Numeric (octal and hexadecimal) escape sequences can be used for specifying the value of the character.

|  |  |
| --- | --- |
| If the character literal contains only one numeric escape sequence, and the value specified by the escape sequence is representable by the unsigned version of its type, the character literal has the same value as the specified value (possibly after conversion to the character type).  A UTF-**N** character literal can have any value representable by its type. If the value does not correspond to a valid Unicode code point, or if the its corresponding code point is not representable as single code unit in UTF-**N**, it can still be specified by a numeric escape sequence with the value. E.g. u8'\xff' is well-formed and equal to char8_t(0xFF). | (since C++23) |

|  |  |
| --- | --- |
| If the value specified by a numeric escape sequence used in an ordinary or wide character literal is not representable by char or wchar_t respectively, the value of the character literal is implementation-defined. | (until C++23) |
| If the value specified by a numeric escape sequence used in an ordinary or wide character literal with one c-char is representable by the unsigned version of the underlying type of char or wchar_t respectively, the value of the literal is the integer value of that unsigned integer type and the specified value converted to the type of the literal. Otherwise, the program is ill-formed. | (since C++23) |

|  |  |
| --- | --- |
| If the value specified by a numeric escape sequence used in a UTF-**N** character literal is not representable by the corresponding `charN_t`, the value of the character literal is implementation-defined(until C++17)the program is ill-formed(since C++17). | (since C++11) |

### Notes

Multicharacter literals were inherited by C from the B programming language. Although not specified by the C or C++ standard, most compilers (MSVC is a notable exception) implement multicharacter literals as specified in B: the values of each char in the literal initialize successive bytes of the resulting integer, in big-endian zero-padded right-adjusted order, e.g. the value of '\1' is 0x00000001 and the value of '\1\2\3\4' is 0x01020304.

In C, character constants such as 'a' or '\n' have type int, rather than char.

### Example

Run this code

```
#include <cstdint>
#include <iomanip>
#include <iostream>
#include <string_view>
 
template<typename CharT>
void dump(std::string_view s, const CharT c)
{
    const uint8_t* data{reinterpret_cast<const uint8_t*>(&c)};
 
    std::cout << s << " \t" << std::hex
              << std::uppercase << std::setfill('0');
 
    for (auto i{0U}; i != sizeof(CharT); ++i)
        std::cout << std::setw(2) << static_cast<unsigned>(data[i]) << ' ';
 
    std::cout << '\n';
}
 
void print(std::string_view str = "") { std::cout << str << '\n'; }
 
int main()
{
    print("Ordinary character literals:");
    char c1 = 'a'; dump("'a'", c1);
    char c2 = '\x2a'; dump("'*'", c2);
 
    print("\n" "Ordinary multi-character literals:");
    int mc1 = 'ab'; dump("'ab'", mc1);       // implementation-defined
    int mc2 = 'abc'; dump("'abc'", mc2);     // implementation-defined
 
    print("\n" "UTF-8 character literals:");
    char8_t C1 = u8'a'; dump("u8'a'", C1);
//  char8_t C2 = u8'¢'; dump("u8'¢'", C2);   // error: ¢ maps to two UTF-8 code units
//  char8_t C3 = u8'猫'; dump("u8'猫'", C3); // error: 猫 maps to three UTF-8 code units
//  char8_t C4 = u8'🍌'; dump("u8'🍌'", C4); // error: 🍌 maps to four UTF-8 code units
 
    print("\n" "UTF-16 character literals:");
    char16_t uc1 = u'a'; dump("u'a'", uc1);
    char16_t uc2 = u'¢'; dump("u'¢'", uc2);
    char16_t uc3 = u'猫'; dump("u'猫'", uc3);
//  char16_t uc4 = u'🍌'; dump("u'🍌'", uc4); // error: 🍌 maps to two UTF-16 code units
 
    print("\n" "UTF-32 character literals:");
    char32_t Uc1 = U'a'; dump("U'a'", Uc1);
    char32_t Uc2 = U'¢'; dump("U'¢'", Uc2);
    char32_t Uc3 = U'猫'; dump("U'猫'", Uc3);
    char32_t Uc4 = U'🍌'; dump("U'🍌'", Uc4);
 
    print("\n" "Wide character literals:");
    wchar_t wc1 = L'a'; dump("L'a'", wc1);
    wchar_t wc2 = L'¢'; dump("L'¢'", wc2);
    wchar_t wc3 = L'猫'; dump("L'猫'", wc3);
    wchar_t wc4 = L'🍌'; dump("L'🍌'", wc4);  // unsupported on Windows since C++23
}

```

Possible output:

```
Ordinary character literals:
'a' 	61 
'*' 	2A 
 
Ordinary multi-character literals:
'ab' 	62 61 00 00 
'abc' 	63 62 61 00 
 
UTF-8 character literals:
u8'a' 	61 
 
UTF-16 character literals:
u'a' 	61 00 
u'¢' 	A2 00 
u'猫' 	2B 73 
 
UTF-32 character literals:
U'a' 	61 00 00 00 
U'¢' 	A2 00 00 00 
U'猫' 	2B 73 00 00 
U'🍌' 	4C F3 01 00 
 
Wide character literals:
L'a' 	61 00 00 00 
L'¢' 	A2 00 00 00 
L'猫' 	2B 73 00 00 
L'🍌' 	4C F3 01 00

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 912 | C++98 | non-encodable ordinary character literal was unspecified | specified as conditionally-supported |
| CWG 1024 | C++98 | multicharacter literal was required to be supported | made conditionally-supported |
| CWG 1656 | C++98 | the meaning of numeric escape sequence in a character literal was unclear | specified |
| P1854R4 | C++98 | non-encodable character literals were conditionally-supported | the program is ill-formed |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 5.13.3 Character literals [lex.ccon]

- C++20 standard (ISO/IEC 14882:2020):

:   - 5.13.3 Character literals [lex.ccon]

- C++17 standard (ISO/IEC 14882:2017):

:   - 5.13.3 Character literals [lex.ccon]

- C++14 standard (ISO/IEC 14882:2014):

:   - 2.14.3 Character literals [lex.ccon]

- C++11 standard (ISO/IEC 14882:2011):

:   - 2.14.3 Character literals [lex.ccon]

- C++03 standard (ISO/IEC 14882:2003):

:   - 2.13.2 Character literals [lex.ccon]

- C++98 standard (ISO/IEC 14882:1998):

:   - 2.13.2 Character literals [lex.ccon]

### See also

|  |  |
| --- | --- |
| user-defined literals(C++11) | literals with user-defined suffix |
| C documentation for Character constant | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/character_literal&oldid=157264>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 August 2023, at 23:23.