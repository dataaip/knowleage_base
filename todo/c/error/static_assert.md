# static_assert

From cppreference.com
< c‎ | error
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

 Error handling

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Error codes | | | | |
| Error codes | | | | |
| errno | | | | |
| Assertions | | | | |
| assert | | | | |
| ****static_assert****(C11)(removed in C23) | | | | |
| Bounds checking | | | | |
| set_constraint_handler_s(C11) | | | | |
| abort_handler_s(C11) | | | | |
| ignore_handler_s(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<assert.h>` |  |  |
| #define static_assert _Static_assert |  | (since C11)  (removed in C23) |
|  |  |  |

This convenience macro expands to the keyword _Static_assert.

### Example

Run this code

```
#include <assert.h>
 
int main(void)
{
    static_assert(2 + 2 == 4, "2+2 isn't 4");   // well-formed
 
    static_assert(sizeof(int) < sizeof(char),   // compile-time error
                  "this program requires that int is less than char");
}

```

### Notes

Since C23, static_assert is itself a keyword, which may also be a predefined macro, so <assert.h> no longer provides it.

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.2/3 Diagnostics <assert.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.2/3 Diagnostics <assert.h> (p: 135)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.2/3 Diagnostics <assert.h> (p: 186)

### See also

|  |  |
| --- | --- |
| C++ documentation for Static Assertion | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/error/static_assert&oldid=180039>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 February 2025, at 21:09.