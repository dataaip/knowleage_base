# Enumerations

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
| ****enum**** | | | | |
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

An **enumerated type** is a distinct type whose value is a value of its **underlying type** (see below), which includes the values of explicitly named constants (**enumeration constants**).

### Syntax

Enumerated type is declared using the following **enumeration specifier** as the type-specifier in the declaration grammar:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `enum` attr-spec-seq ﻿(optional) identifier ﻿(optional) `{` enumerator-list `}` | (1) |  |
|  | | | | | | | | | |
| `enum` attr-spec-seq ﻿(optional) identifier ﻿(optional) `:` type `{` enumerator-list `}` | (2) | (since C23) |
|  | | | | | | | | | |

1) Declares an enumeration without a fixed underlying type.2) Declares an enumeration of fixed underlying type type.

where enumerator-list is a comma-separated list(with trailing comma permitted)(since C99) of enumerator, each of which has the form:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| enumeration-constant attr-spec-seq ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| enumeration-constant attr-spec-seq ﻿(optional) `=` constant-expression | (2) |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| identifier, enumeration-constant | - | identifiers that are introduced by this declaration |
| constant-expression | - | integer constant expression whose value is representable as a value of type int(until C23). If the enumeration has a fixed underlying type, representable as a value of type(since C23) |
| attr-spec-seq | - | (C23)optional list of attributes,  - applied to the whole enumeration if appears after `enum`, - applied to the enumerator if appears after enumeration-constant |

As with struct or union, a declaration that introduced an enumerated type and one or more enumeration constants may also declare one or more objects of that type or type derived from it.

```
enum color { RED, GREEN, BLUE } c = RED, *cp = &c;
// introduces the type enum color
// the integer constants RED, GREEN, BLUE
// the object c of type enum color
// the object cp of type pointer to enum color

```

### Explanation

Each enumeration-constant that appears in the body of an enumeration specifier becomes an integer constant with type int(until C23) in the enclosing scope and can be used whenever integer constants are required (e.g. as a case label or as a non-VLA array size).

|  |  |
| --- | --- |
| During the processing of each enumeration constant in the enumerator list, the type of the enumeration constant shall be:   - the previously declared type, if it is a redeclaration of the same enumeration constant; or, - the enumerated type, for an enumeration with fixed underlying type; or, - int, if there are no previous enumeration constants in the enumerator list and no explicit = with a defining integer constant expression; or, - int, if given explicitly with = and the value of the integer constant expression is representable by an int; or, - the type of the integer constant expression, if given explicitly with = and if the value of the integer constant expression is not representable by int; or, - the type of the value from last enumeration constant with 1 added to it. If such an integer constant expression would overflow or wraparound the value of the previous enumeration constant from the addition of 1, the type takes on either:   - a suitably sized signed integer type (excluding the bit-precise signed integer types) capable of representing the value of the previous enumeration constant plus 1; or,   - a suitably sized unsigned integer type (excluding the bit-precise unsigned integer types) capable of representing the value of the previous enumeration constant plus 1.   A signed integer type is chosen if the previous enumeration constant being added is of signed integer type. An unsigned integer type is chosen if the previous enumeration constant is of unsigned integer type. If there is no suitably sized integer type described previous which can represent the new value, then the enumeration has no type which is capable of representing all of its values. | (since C23) |

```
enum color { RED, GREEN, BLUE } r = RED;
switch(r)
{
case RED:
    puts("red");
    break;
case GREEN:
    puts("green");
    break;
case BLUE:
    puts("blue");
    break;
}

```

If enumeration-constant is followed by = constant-expression, its value is the value of that constant expression. If enumeration-constant is not followed by = constant-expression, its value is the value one greater than the value of the previous enumerator in the same enumeration. The value of the first enumerator (if it does not use = constant-expression) is zero.

```
enum Foo { A, B, C = 10, D, E = 1, F, G = F + C };
// A=0, B=1, C=10, D=11, E=1, F=2, G=12

```

The identifier itself, if used, becomes the name of the enumerated type in the tags name space and requires the use of the keyword enum (unless typedef'd into the ordinary name space).

```
enum color { RED, GREEN, BLUE };
enum color r = RED; // OK
// color x = GREEN; // Error: color is not in ordinary name space
typedef enum color color_t;
color_t x = GREEN; // OK

```

Each enumerated type without a fixed underlying type(since C23) is compatible with one of: char, a signed integer type, or an unsigned integer type (excluding bool and the bit-precise integer types)(since C23). It is implementation-defined which type is compatible with any given enumerated type, but whatever it is, it must be capable of representing all enumerator values of that enumeration. For all enumerations with a fixed underlying type, the enumerated type is compatible with the underlying type of the enumeration.(since C23)

|  |  |
| --- | --- |
| The enumeration member type for an enumerated type without fixed underlying type upon completion is:   - int if all the values of the enumeration are representable as an int; or, - the enumerated type. | (since C23) |
| All enumerations have an underlying type. The underlying type can be explicitly specified using an enum-type-specifier and is its fixed underlying type. If it is not explicitly specified, the underlying type is the enumeration’s compatible type, which is either a signed or unsigned integer type, or char. | (since C23) |

Enumerated types are integer types, and as such can be used anywhere other integer types can, including in implicit conversions and arithmetic operators.

```
enum { ONE = 1, TWO } e;
long n = ONE; // promotion
double d = ONE; // conversion
e = 1.2; // conversion, e is now ONE
e = e + 1; // e is now TWO

```

### Notes

Unlike struct or union, there are no forward-declared enums in C:

```
enum Color; // Error: no forward-declarations for enums in C
enum Color { RED, GREEN, BLUE };

```

Enumerations permit the declaration of named constants in a more convenient and structured
fashion than does #define; they are visible in the debugger, obey scope rules, and participate in the type system.

```
#define TEN 10
struct S { int x : TEN; }; // OK

```

or

```
enum { TEN = 10 };
struct S { int x : TEN; }; // also OK

```

Since C23 constexpr can be used for the same purpose:

```
constexpr int TEN = 10;
struct S { int x : TEN; }; // also OK

```

Moreover, as a struct or union does not establish its scope in C, an enumeration type and its enumeration constants may be introduced in the member specification of the former, and their scope is the same as of the former, afterwards.

```
struct Element
{
    int z;
    enum State { SOLID, LIQUID, GAS, PLASMA } state;
} oxygen = { 8, GAS };
 
// type enum State and its enumeration constants stay visible here, e.g.
void foo(void)
{
    enum State e = LIQUID; // OK
    printf("%d %d %d ", e, oxygen.state, PLASMA); // prints 1 2 3
}

```

### Example

Run this code

```
#include <stdio.h>
 
int main(void)
{
    enum TV { FOX = 11, CNN = 25, ESPN = 15, HBO = 22, MAX = 30, NBC = 32 };
 
    printf("List of cable stations:\n");
    printf(" FOX: \t%2d\n", FOX);
    printf(" HBO: \t%2d\n", HBO);
    printf(" MAX: \t%2d\n", MAX);
}

```

Output:

```
List of cable stations:
 FOX:   11
 HBO:   22
 MAX:   30

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.2.5/21 Types (p: 39)

:   - 6.7.2.2 Enumeration specifiers (p: 107-112)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.2.5/16 Types (p: 32)

:   - 6.7.2.2 Enumeration specifiers (p: 84-85)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.2.5/16 Types (p: 41)

:   - 6.7.2.2 Enumeration specifiers (p: 117-118)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.2.5/16 Types (p: 35)

:   - 6.7.2.2 Enumeration specifiers (p: 105-106)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.1.2.5 Types

:   - 3.5.2.2 Enumeration specifiers

### Keywords

enum

### See also

|  |  |
| --- | --- |
| C++ documentation for enumeration declaration | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/enum&oldid=171799>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 May 2024, at 07:40.