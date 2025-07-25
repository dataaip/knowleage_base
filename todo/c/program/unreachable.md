# unreachable

From cppreference.com
< c‎ | program
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

 Program support utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Program termination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abort | | | | | | exit | | | | | | quick_exit(C11) | | | | | | _Exit(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atexit | | | | | | at_quick_exit(C11) | | | | | | EXIT_SUCCESSEXIT_FAILURE | | | | | |
| Unreachable control flow | | | | |
| ****unreachable****(C23) | | | | |
| Communicating with the environment | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | getenvgetenv_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | system | | | | | |  | | | | | |
| Memory alignment query | | | | |
| memalignment(C23) | | | | |
| Signals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | signal | | | | | | raise | | | | | | sig_atomic_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIG_DFLSIG_IGN | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGABRTSIGFPESIGILL | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGINTSIGSEGVSIGTERM | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stddef.h>` |  |  |
| #define unreachable() /\* see below \*/ |  | (since C23) |
|  |  |  |

The function-like macro `unreachable` expands to a void expression. Executing unreachable() results in undefined behavior.

An implementation may use this to optimize impossible code branches away (typically, in optimized builds) or to trap them to prevent further execution (typically, in debug builds).

### Possible implementation

|  |
| --- |
| ```text // Uses compiler specific extensions if possible. #ifdef __GNUC__ // GCC, Clang, ICC   #define unreachable() (__builtin_unreachable())   #elifdef _MSC_VER // MSVC   #define unreachable() (__assume(false))   #else // Even if no extension is used, undefined behavior is still raised by // the empty function body and the noreturn attribute.   // The external definition of unreachable_impl must be emitted in a separated TU // due to the rule for inline functions in C.   [[noreturn]] inline void unreachable_impl() {} #define unreachable() (unreachable_impl())   #endif ``` |

### Example

Run this code

```
#include <assert.h>
#include <stddef.h>
#include <stdint.h>
#include <stdlib.h>
 
struct Color { uint8_t r, g, b, a; };
struct ColorSpan { struct Color* data; size_t size; };
 
// Assume that only restricted set of texture caps is supported.
struct ColorSpan allocate_texture(size_t xy)
{
    switch (xy)
    {
    case 128: [[fallthrough]];
    case 256: [[fallthrough]];
    case 512:
    {
        /* ... */
        struct ColorSpan result = {
            .data = malloc(xy * xy * sizeof(struct Color)),
            .size = xy * xy
        };
 
        if (!result.data)
            result.size = 0;
 
        return result;
    }
    default:
        unreachable();
    }
}
 
int main(void)
{
    struct ColorSpan tex = allocate_texture(128); // OK
    assert(tex.size == 128 * 128);
 
    struct ColorSpan badtex = allocate_texture(32);  // Undefined behavior
 
    free(badtex.data);
    free(tex.data);
}

```

Possible output:

```
Segmentation fault

```

### See also

|  |  |
| --- | --- |
| C++ documentation for unreachable | |

### External Links

|  |  |
| --- | --- |
| 1. | GCC docs: `__builtin_unreachable` |
| 2. | Clang docs: `__builtin_unreachable` |
| 3. | MSVC docs: `__assume` |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/unreachable&oldid=178607>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 14:23.