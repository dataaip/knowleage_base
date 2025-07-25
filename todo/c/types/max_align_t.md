# max_align_t

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
| nullptr_t(C23) | | | | |
| NULL | | | | |
| ****max_align_t****(C11) | | | | |
| offsetof | | | | |
| Numeric limits | | | | |
| Fixed width integer types (C99) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stddef.h>` |  |  |
| typedef /\*implementation-defined\*/ max_align_t; |  | (since C11) |
|  |  |  |

`max_align_t` is a type whose alignment requirement is at least as strict (as large) as that of every scalar type.

### Notes

Pointers returned by allocation functions such as malloc are suitably aligned for any object, which means they are aligned at least as strictly as `max_align_t`.

### Example

Run this code

```
#include <inttypes.h>
#include <stdalign.h>
#include <stddef.h>
#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    size_t a = alignof(max_align_t);
    printf("Alignment of max_align_t is %zu (%#zx)\n", a, a);
 
    void *p = malloc(123);
    printf("The address obtained from malloc(123) is %#" PRIxPTR"\n",
            (uintptr_t)p);
    free(p);
}

```

Possible output:

```
Alignment of max_align_t is 16 (0x10)
The address obtained from malloc(123) is 0x1fa67010

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.19 Common definitions <stddef.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.19 Common definitions <stddef.h> (p: 211)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.19 Common definitions <stddef.h> (p: 288)

### See also

|  |  |
| --- | --- |
| C++ documentation for max_align_t | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/types/max_align_t&oldid=171582>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 May 2024, at 13:31.