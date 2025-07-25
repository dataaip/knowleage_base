# C attribute: deprecated (since C23)

From cppreference.com
< c‎ | language‎ | attributes
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
| Static assertions | | | | |
| Attributes (C23) | | | | |

 Attributes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****deprecated****(C23) | | | | |
| fallthrough(C23) | | | | |
| nodiscard(C23) | | | | |
| maybe_unused(C23) | | | | |
| noreturn_Noreturn(C23)(C23)(deprecated) | | | | |
| unsequenced(C23) | | | | |
| reproducible(C23) | | | | |

Indicates that the name or entity declared with this attribute is deprecated, that is, the use is allowed, but discouraged for some reason.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `[[` `deprecated` `]]` `[[` `__deprecated__` `]]` | (1) |  |
|  | | | | | | | | | |
| `[[` `deprecated` `(` string-literal `)` `]]` `[[` `__deprecated__` `(` string-literal `)` `]]` | (2) |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| string-literal | - | text that could be used to explain the rationale for deprecation and/or to suggest a replacing entity |

### Explanation

Indicates that the use of the name or entity declared with this attribute is allowed, but discouraged for some reason. Compilers typically issue warnings on such uses. The string-literal, if specified, is usually included in the warnings.

This attribute is allowed in declarations of the following names or entities:

- struct/union: struct [[deprecated]] S;,
- typedef-name: [[deprecated]] typedef S\* PS;,
- objects: [[deprecated]] int x;,
- struct/union member: union U { [[deprecated]] int n; };,
- function: [[deprecated]] void f(void);,
- enumeration: enum [[deprecated]] E {};,
- enumerator: enum { A [[deprecated]], B [[deprecated]] = 42 };.

A name declared non-deprecated may be redeclared deprecated. A name declared deprecated cannot be un-deprecated by redeclaring it without this attribute.

### Example

Run this code

```
#include <stdio.h>
 
[[deprecated]]
void TriassicPeriod(void)
{
    puts("Triassic Period: [251.9 - 208.5] million years ago.");
}
 
[[deprecated("Use NeogenePeriod() instead.")]]
void JurassicPeriod(void)
{
    puts("Jurassic Period: [201.3 - 152.1] million years ago.");
}
 
[[deprecated("Use calcSomethingDifferently(int).")]]
int calcSomething(int x)
{
    return x * 2;
}
 
int main(void)
{
    TriassicPeriod();
    JurassicPeriod();
}

```

Possible output:

```
Triassic Period: [251.9 - 208.5] million years ago.
Jurassic Period: [201.3 - 152.1] million years ago.
 
prog.c:23:5: warning: 'TriassicPeriod' is deprecated [-Wdeprecated-declarations]
    TriassicPeriod();
    ^
prog.c:3:3: note: 'TriassicPeriod' has been explicitly marked deprecated here
[[deprecated]]
  ^
prog.c:24:5: warning: 'JurassicPeriod' is deprecated: Use NeogenePeriod() instead. [-Wdeprecated-declarations]
    JurassicPeriod();
    ^
prog.c:9:3: note: 'JurassicPeriod' has been explicitly marked deprecated here
[[deprecated("Use NeogenePeriod() instead.")]]
  ^
2 warnings generated.

```

### See also

|  |  |
| --- | --- |
| C++ documentation for deprecated | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/attributes/deprecated&oldid=155182>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 July 2023, at 05:28.