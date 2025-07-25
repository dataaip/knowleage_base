# Static assertion (since C11)

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

 Declarations

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Pointer | | | | |
| Array | | | | |
| enum | | | | |
| struct | | | | |
| union | | | | |
| Bit-field | | | | |
| Atomic types (C11) | | | | |
| const | | | | |
| constexpr(C23) | | | | |
| volatile | | | | |
| restrict(C99) | | | | |
| Alignment specifiers | | | | |
| Storage duration and linkage | | | | |
| External and tentative definitions | | | | |
| typedef | | | | |
| ****Static assertions**** | | | | |
| Attributes (C23) | | | | |

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `_Static_assert` `(` expression `,` message `)` |  | (since C11)(deprecated in C23) |
|  | | | | | | | | | |
| `static_assert` `(` expression `,` message `)` |  | (since C23) |
|  | | | | | | | | | |
| `_Static_assert` `(` expression `)` |  | (since C23)(deprecated in C23) |
|  | | | | | | | | | |
| `static_assert` `(` expression `)` |  | (since C23) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| expression | - | any integer constant expression |
| message | - | any string literal |

|  |  |
| --- | --- |
| This keyword is also available as convenience macro static_assert, available in the header <assert.h>. | (until C23) |
| Both of `static_assert` and `_Static_assert` have the same effects. `_Static_assert` is a deprecated spelling that is kept for compatibility.  An implementation may also define `static_assert` and/or `_Static_assert` as predefined macros, and `static_assert` is no longer provided by <assert.h>. | (since C23) |

### Explanation

The constant expression is evaluated at compile time and compared to zero. If it compares equal to zero, a compile-time error occurs and the compiler must display message as part of the error message (except that characters not in basic character set are not required to be displayed)(until C23)should display message (if provided) as part of the error message(since C23).

Otherwise, if expression does not equal zero, nothing happens; no code is emitted.

### Keywords

_Static_assert, static_assert

### Example

Run this code

```
#include <assert.h> // no longer needed since C23
 
int main(void)
{
    // Test if math works, C23:
    static_assert((2 + 2) % 3 == 1, "Whoa dude, you knew!");
    // Pre-C23 alternative:
    _Static_assert(2 + 2 * 2 == 6, "Lucky guess!?");
 
    // This will produce an error at compile time.
    // static_assert(sizeof(int) < sizeof(char), "Unmet condition!");
 
    constexpr int _42 = 2 * 3 * 2 * 3 + 2 * 3;
    static_assert(_42 == 42); // the message string can be omitted.
 
    // const int _13 = 13;
    // Compile time error - not an integer constant expression:
    // static_assert(_13 == 13);
}

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.7.11 Static assertions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.10 Static assertions (p: 105)

:   - 7.2 Diagnostics <assert.h> (p: 135)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.10 Static assertions (p: 145)

:   - 7.2 Diagnostics <assert.h> (p: 186-187)

### See also

|  |  |
| --- | --- |
| assert | aborts the program if the user-specified condition is not true. May be disabled for release builds   (function macro) |
| C++ documentation for `static_assert` declaration | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/_Static_assert&oldid=180000>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 January 2025, at 07:47.