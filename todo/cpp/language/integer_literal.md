# Integer literal

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
| Boolean - ****Integer**** - Floating-point | | | | |
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

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****Integer literals**** | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Allows values of integer type to be used in expressions directly.

### Syntax

An integer literal has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| decimal-literal integer-suffix ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| octal-literal integer-suffix ﻿(optional) | (2) |  |
|  | | | | | | | | | |
| hex-literal integer-suffix ﻿(optional) | (3) |  |
|  | | | | | | | | | |
| binary-literal integer-suffix ﻿(optional) | (4) | (since C++14) |
|  | | | | | | | | | |

where

- decimal-literal is a non-zero decimal digit (`1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`), followed by zero or more decimal digits (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`)
- octal-literal is the digit zero (`0`) followed by zero or more octal digits (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`)
- hex-literal is the character sequence `0x` or the character sequence `0X` followed by one or more hexadecimal digits (`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `a`, `A`, `b`, `B`, `c`, `C`, `d`, `D`, `e`, `E`, `f`, `F`)
- binary-literal is the character sequence `0b` or the character sequence `0B` followed by one or more binary digits (`0`, `1`)
- integer-suffix, if provided, may contain one or both of the following (if both are provided, they may appear in any order:

:   - unsigned-suffix (the character `u` or the character `U`)
    - one of

    :   - long-suffix (the character `l` or the character `L`)

|  |  |
| --- | --- |
| - long-long-suffix (the character sequence `ll` or the character sequence `LL`) | (since C++11) |

|  |  |
| --- | --- |
| - size-suffix (the character `z` or the character `Z`) | (since C++23) |

|  |  |
| --- | --- |
| Optional single quotes (') may be inserted between the digits as a separator; they are ignored when determining the value of the literal. | (since C++14) |

An integer literal (as any literal) is a primary expression.

### Explanation

1) Decimal integer literal (base 10).2) Octal integer literal (base 8).3) Hexadecimal integer literal (base 16, the letters 'a' through 'f' represent values (decimal) 10 through 15).4) Binary integer literal (base 2).

The first digit of an integer literal is the most significant.

Example. The following variables are initialized to the same value:

```
int d = 42;
int o = 052;
int x = 0x2a;
int X = 0X2A;
int b = 0b101010; // C++14

```

Example. The following variables are also initialized to the same value:

```
unsigned long long l1 = 18446744073709550592ull;       // C++11
unsigned long long l2 = 18'446'744'073'709'550'592llu; // C++14
unsigned long long l3 = 1844'6744'0737'0955'0592uLL;   // C++14
unsigned long long l4 = 184467'440737'0'95505'92LLU;   // C++14

```

### The type of the literal

The type of the integer literal is the first type in which the value can fit, from the list of types which depends on which numeric base and which integer-suffix was used:

| Suffix | Decimal bases | Binary, octal, or hexadecimal bases |
| --- | --- | --- |
| (no suffix) | - int - long int - long long int (since C++11) | - int - unsigned int - long int - unsigned long int - long long int (since C++11) - unsigned long long int (since C++11) |
| `u` or `U` | - unsigned int - unsigned long int - unsigned long long int (since C++11) | - unsigned int - unsigned long int - unsigned long long int (since C++11) |
| `l` or `L` | - long int - unsigned long int (until C++11) - long long int (since C++11) | - long int - unsigned long int - long long int (since C++11) - unsigned long long int (since C++11) |
| both `l`/`L` and `u`/`U` | - unsigned long int - unsigned long long int (since C++11) | - unsigned long int - unsigned long long int (since C++11) |
| `ll` or `LL` | - long long int (since C++11) | - long long int (since C++11) - unsigned long long int (since C++11) |
| both `ll`/`LL` and `u`/`U` | - unsigned long long int (since C++11) | - unsigned long long int (since C++11) |
| `z` or `Z` | - the signed version of std::size_t (since C++23) | - the signed version of std::size_t (since C++23) - std::size_t (since C++23) |
| both `z`/`Z` and `u`/`U` | - std::size_t (since C++23) | - std::size_t (since C++23) |

If the value of the integer literal that does not have size-suffix(since C++23) is too big to fit in any of the types allowed by suffix/base combination and the compiler supports an extended integer type (such as __int128) which can represent the value of the literal, the literal may be given that extended integer type — otherwise the program is ill-formed.

### Notes

Letters in the integer literals are case-insensitive: `0xDeAdBeEfU` and `0XdeadBEEFu` represent the same number (one exception is the long-long-suffix, which is either `ll` or `LL`, never `lL` or `Ll`)(since C++11).

There are no negative integer literals. Expressions such as -1 apply the unary minus operator to the value represented by the literal, which may involve implicit type conversions.

In C prior to C99 (but not in C++), unsuffixed decimal values that do not fit in long int are allowed to have the type unsigned long int.

|  |  |
| --- | --- |
| When used in a controlling expression of #if or #elif, all signed integer constants act as if they have type std::intmax_t and all unsigned integer constants act as if they have type std::uintmax_t. | (since C++11) |

Due to maximal munch, hexadecimal integer literals ending in `e` and `E`, when followed by the operators `+` or `-`, must be separated from the operator with whitespace or parentheses in the source:

```
auto x = 0xE+2.0;   // error
auto y = 0xa+2.0;   // OK
auto z = 0xE +2.0;  // OK
auto q = (0xE)+2.0; // OK

```

Otherwise, a single invalid preprocessing number token is formed, which causes further analysis to fail.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_binary_literals` | `201304L` | (C++14) | Binary literals |
| `__cpp_size_t_suffix` | `202011L` | (C++23) | Literal suffixes for std::size_t and its signed version |

### Example

Run this code

```
#include <cstddef>
#include <iostream>
#include <type_traits>
 
int main()
{
    std::cout << 123 << '\n'
              << 0123 << '\n'
              << 0x123 << '\n'
              << 0b10 << '\n'
              << 12345678901234567890ull << '\n'
              << 12345678901234567890u << '\n'; // the type is unsigned long long
                                                // even without a long long suffix
 
//  std::cout << -9223372036854775808 << '\n'; // error: the value
               // 9223372036854775808 cannot fit in signed long long, which is the
               // biggest type allowed for unsuffixed decimal integer literal
    std::cout << -9223372036854775808u << '\n'; // unary minus applied to unsigned
               // value subtracts it from 2^64, this gives 9223372036854775808
    std::cout << -9223372036854775807 - 1 << '\n'; // correct way to calculate
                                                   // the value -9223372036854775808
 
#if __cpp_size_t_suffix >= 202011L // C++23
    static_assert(std::is_same_v<decltype(0UZ), std::size_t>);
    static_assert(std::is_same_v<decltype(0Z), std::make_signed_t<std::size_t>>);
#endif
}

```

Output:

```
123
83
291
2
12345678901234567890
12345678901234567890
9223372036854775808
-9223372036854775808

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2698 | C++23 | an integer literal with size-suffix could have an extended integer type | ill-formed if too large |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 5.13.2 Integer literals [lex.icon]

- C++20 standard (ISO/IEC 14882:2020):

:   - 5.13.2 Integer literals [lex.icon]

- C++17 standard (ISO/IEC 14882:2017):

:   - 5.13.2 Integer literals [lex.icon]

- C++14 standard (ISO/IEC 14882:2014):

:   - 2.14.2 Integer literals [lex.icon]

- C++11 standard (ISO/IEC 14882:2011):

:   - 2.14.2 Integer literals [lex.icon]

- C++98 standard (ISO/IEC 14882:1998):

:   - 2.13.1 Integer literals [lex.icon]

### See also

|  |  |
| --- | --- |
| user-defined literals(C++11) | literals with user-defined suffix |
| C documentation for integer constant | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/integer_literal&oldid=170034>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 March 2024, at 10:45.