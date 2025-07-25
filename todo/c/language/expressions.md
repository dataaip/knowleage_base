# Expressions

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
| ****Expressions**** | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 ****Expressions****

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

An expression is a sequence of **operators** and their **operands**, that specifies a computation.

Expression evaluation may produce a result (e.g., evaluation of 2 + 2 produces the result 4), may generate side-effects (e.g. evaluation of printf("%d", 4) sends the character '4' to the standard output stream), and may designate objects or functions.

#### General

- value categories (lvalue, non-lvalue object, function designator) classify expressions by their values
- order of evaluation of arguments and subexpressions specifies the order in which intermediate results are obtained

### Operators

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | increment decrement | arithmetic | logical | comparison | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b | a[b]  \*a  &a  a->b  a.b | a(...)  a, b  (type) a  a ? b : c  sizeof   _Alignof (since C11) (until C23)   alignof (since C23) |

- operator precedence defines the order in which operators are bound to their arguments
- alternative representations are alternative spellings for some operators

#### Conversions

- Implicit conversions take place when types of operands do not match the expectations of operators
- Casts may be used to explicitly convert values from one type to another.

#### Other

- constant expressions can be evaluated at compile time and used in compile-time context (non-VLA(since C99)array sizes, static initializers, etc)

|  |  |
| --- | --- |
| - generic selections can execute different expressions depending on the types of the arguments | (since C11) |

|  |  |
| --- | --- |
| - Floating-point arithmetic may raise exceptions and report errors as specified in math_errhandling - The standard #pragmas `FENV_ACCESS`, `FP_CONTRACT`, and `CX_LIMITED_RANGE` as well as the floating-point evaluation precision and rounding direction control the way floating-point arithmetic are executed. | (since C99) |

### Primary expressions

The operands of any operator may be other expressions or they may be **primary expressions** (e.g. in 1 + 2 \* 3, the operands of operator+ are the subexpression 2 \* 3 and the primary expression 1).

Primary expressions are any of the following:

1) Constants and literals (e.g. 2 or "Hello, world")2) Suitably declared identifiers (e.g. n or printf)

|  |  |
| --- | --- |
| 3) Generic selections | (since C11) |

Any expression in parentheses is also classified as a primary expression: this guarantees that the parentheses have higher precedence than any operator.

#### Constants and literals

Constant values of certain types may be embedded in the source code of a C program using specialized expressions known as literals (for lvalue expressions) and constants (for non-lvalue expressions)

- integer constants are decimal, octal, or hexadecimal numbers of integer type.
- character constants are individual characters of type int suitable for conversion to a character type or of type char8_t,(since C23) char16_t, char32_t, or(since C11) wchar_t
- floating constants are values of type float, double, or long double

|  |  |
| --- | --- |
| - predefined constants true/false are values of type bool - predefined constant `nullptr` is a value of type nullptr_t | (since C23) |

- string literals are sequences of characters of type char[], char8_t[](since C23), char16_t[], char32_t[],(since C11) or wchar_t[] that represent null-terminated strings

|  |  |
| --- | --- |
| - compound literals are values of struct, union, or array type directly embedded in program code | (since C99) |

### Unevaluated expressions

The operands of the sizeof operator are expressions that are not evaluated (unless they are VLAs)(since C99). Thus, size_t n = sizeof(printf("%d", 4)); does not perform console output.

|  |  |
| --- | --- |
| The operands of the `_Alignof`(until C23)`alignof`(since C23) operator, the controlling expression of a generic selection, and size expressions of VLAs that are operands of `_Alignof`(until C23)alignof(since C23) are also expressions that are not evaluated. | (since C11) |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.5 Expressions (p: TBD)

:   - 6.6 Constant expressions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.5 Expressions (p: 55-75)

:   - 6.6 Constant expressions (p: 76-77)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5 Expressions (p: 76-105)

:   - 6.6 Constant expressions (p: 106-107)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5 Expressions (p: 67-94)

:   - 6.6 Constant expressions (p: 95-96)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3 EXPRESSIONS

:   - 3.4 CONSTANT EXPRESSIONS

### See also

|  |  |
| --- | --- |
| C++ documentation for Expressions | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/expressions&oldid=178465>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 December 2024, at 22:22.