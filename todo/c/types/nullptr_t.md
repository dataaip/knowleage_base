# nullptr_t

From cppreference.com
< c‎ | types
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

 Type support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| size_t | | | | |
| ptrdiff_t | | | | |
| ****nullptr_t****(C23) | | | | |
| NULL | | | | |
| max_align_t(C11) | | | | |
| offsetof | | | | |
| Numeric limits | | | | |
| Fixed width integer types (C99) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stddef.h>` |  |  |
| typedef typeof(nullptr) nullptr_t; |  | (since C23) |
|  |  |  |

`nullptr_t` is the type of the predefined null pointer constant, nullptr. It is a distinct type that is not itself a pointer type. It can be implicitly converted to any pointer type or bool, and the result is the null pointer value of that type or false respectively. No type other than `nullptr_t` itself can be converted or explicitly cast to `nullptr_t`.

sizeof(nullptr_t) and alignof(nullptr_t) are equal to sizeof(void\*) and alignof(void\*) respectively.

`nullptr_t` has only one valid value, i.e., nullptr. The object representation of nullptr is same as that of (void\*)0. If an lvalue conversion produces a `nullptr_t` value with a different object representation, the behavior is undefined.

### Example

Demonstrate that `nullptr_t` is a distinct type.

Run this code

```
#include <stddef.h>
#include <stdio.h>
 
#define DETECT_NULL_POINTER_CONSTANT(e) \
    _Generic(e,                         \
        void* : puts("void*"),          \
        nullptr_t : puts("nullptr_t"),  \
        default : puts("other")         \
    )
 
int main()
{
    DETECT_NULL_POINTER_CONSTANT(((void*)0));
    DETECT_NULL_POINTER_CONSTANT(0);
    DETECT_NULL_POINTER_CONSTANT(nullptr);
}

```

Output:

```
void*
other
nullptr_t

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.21.2 The nullptr_t type (p: 315-316)

### See also

|  |  |
| --- | --- |
| NULL | implementation-defined null pointer constant   (macro constant) |
| C++ documentation for nullptr_t | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/types/nullptr_t&oldid=172487>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 June 2024, at 23:04.