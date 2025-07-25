# _Alignas (since C11)(deprecated in C23), alignas (since C23)

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
| ****Alignment specifiers**** | | | | |
| Storage duration and linkage | | | | |
| External and tentative definitions | | | | |
| typedef | | | | |
| Static assertions | | | | |
| Attributes (C23) | | | | |

Appears in the declaration syntax as one of the type specifiers to modify the alignment requirement of the object being declared.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `_Alignas` `(` expression `)` | (1) | (since C11) |
|  | | | | | | | | | |
| `alignas` `(` expression `)` | (2) | (since C23) |
|  | | | | | | | | | |
| `_Alignas` `(` type `)` | (3) | (since C11) |
|  | | | | | | | | | |
| `alignas` `(` type `)` | (4) | (since C23) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| expression | - | any integer constant expression whose value is a valid alignment or zero |
| type | - | any type name |

|  |  |
| --- | --- |
| The keyword `_Alignas` is also available as convenience macro alignas, available in the header <stdalign.h>. | (until C23) |

### Explanation

The `_Alignas`(until C23)`alignas`(since C23) specifier can only be used when declaring objects that are not bit-fields, and don't have the register storage class. It cannot be used in function parameter declarations, and cannot be used in a typedef.

When used in a declaration, the declared object will have its alignment requirement set to

1,2) the result of the expression, unless it is zero3,4) the alignment requirement of type, that is, to _Alignof(type)(until C23)alignof(type)(since C23)

except when this would weaken the alignment the type would have had naturally.

If expression evaluates to zero, this specifier has no effect.

When multiple `_Alignas`(until C23)`alignas`(since C23) specifiers appear in the same declaration, the strictest one is used.

`_Alignas`(until C23)`alignas`(since C23) specifier only needs to appear on the definition of an object, but if any declaration uses `_Alignas`(until C23)`alignas`(since C23), it must specify the same alignment as the `_Alignas`(until C23)`alignas`(since C23) on the definition. The behavior is undefined if different translation units specify different alignments for the same object.

### Notes

In C++, the `alignas` specifier may also be applied to the declarations of class/struct/union types and enumerations. This is not supported in C, but the alignment of a struct type can be controlled by using `_Alignas`(until C23)`alignas`(since C23) in a member declaration.

### Keywords

alignas,
_Alignas

### Example

Run this code

```
#include <stdalign.h>
#include <stdio.h>
 
// every object of type struct sse_t will be aligned to 16-byte boundary
// (note: needs support for DR 444)
struct sse_t
{
    alignas(16) float sse_data[4];
};
 
// every object of type struct data will be aligned to 128-byte boundary
struct data
{
    char x;
    alignas(128) char cacheline[128]; // over-aligned array of char,
                                      // not array of over-aligned chars
};
 
int main(void)
{
    printf("sizeof(data) = %zu (1 byte + 127 bytes padding + 128-byte array)\n",
           sizeof(struct data));
 
    printf("alignment of sse_t is %zu\n", alignof(struct sse_t));
 
    alignas(2048) struct data d; // this instance of data is aligned even stricter
    (void)d; // suppresses "maybe unused" warning
}

```

Output:

```
sizeof(data) = 256 (1 byte + 127 bytes padding + 128-byte array)
alignment of sse_t is 16

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| DR 444 | C11 | `_Alignas` was not allowed in struct and union members | allowed |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.7.5 Alignment specifier (p: TBD)

:   - 6.2.8 Alignment of objects (p: TBD)

:   - 7.15 Alignment <stdalign.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.5 Alignment specifier (p: 92)

:   - 6.2.8 Alignment of objects (p: 36-37)

:   - 7.15 Alignment <stdalign.h> (p: 196)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.5 Alignment specifier (p: 127-128)

:   - 6.2.8 Alignment of objects (p: 48-49)

:   - 7.15 Alignment <stdalign.h> (p: 268)

### See also

|  |  |
| --- | --- |
| max_align_t(C11) | a type with alignment requirement as great as any other scalar type   (typedef) |
| _Alignof(until C23)alignof(since C23) | queries alignment requirements of an object (operator) |
| C++ documentation for `alignas` specifier | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/_Alignas&oldid=180144>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2025, at 16:54.