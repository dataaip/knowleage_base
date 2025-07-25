# Predefined Boolean constants (since C23)

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
| ****true/false****(C23) | | | | |
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
| `true` | (1) | (since C23) |
|  | | | | | | | | | |
| `false` | (2) | (since C23) |
|  | | | | | | | | | |

### Explanation

Keywords true and false represent predefined constants. They are non-lvalues of type `bool`.

### Notes

See integral conversions for implicit conversions from bool to other types and boolean conversions for the implicit conversions from other types to bool.

Until C23, true and false were implemented as macros provided in <stdbool.h>. An implementation may also define bool, true, and false as predefined macros in C23 for compatibility.

### Example

Run this code

```
#include <assert.h>
 
int main()
{
    assert(true == 1 && 0 == false);
}

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.4.4.6 Predefined constants (p: 66)

### See also

|  |  |
| --- | --- |
| C++ documentation for Boolean literals | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/bool_constant&oldid=176320>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 September 2024, at 14:37.