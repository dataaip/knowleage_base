# memalignment

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
| unreachable(C23) | | | | |
| Communicating with the environment | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | getenvgetenv_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | system | | | | | |  | | | | | |
| Memory alignment query | | | | |
| ****memalignment****(C23) | | | | |
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
| Defined in header `<stdlib.h>` |  |  |
| size_t memalignment( const void \*p ); |  | (since C23) |
|  |  |  |

Returns the maximum alignment satisfied by the provided address. The return value can be greater than any alignment value supported by the implementation. If `p` is a null pointer value, ​0​ is returned to indicate that the pointer cannot be used to access an object of any type.

If the return value compares is greater than or equal to alignof(T), the alignment requirement for the type `T` is satisfied by the pointer.

A freestanding implementation needs to provide `memalignment`.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | pointer to query alignment |

### Return value

The alignment value of `p`, or ​0​ if `p` is a null pointer value.

### Notes

On common platforms where

- null pointers are cast to integer ​0​,
- pointer values are directly cast to the numeric values of virtual addresses, and
- size_t is same as uintptr_t,

this function can be implemented as return (size_t)p & -(size_t)p;.

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
 
int main()
{
    alignas(128) int i = 0;
    printf("%zu\n%zu\n", memalignment(nullptr), memalignment(&i));
}

```

Possible output:

```
0
128

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.9.1 The memalignment function (p: 374)

### See also

|  |  |
| --- | --- |
| aligned_alloc(C11) | allocates aligned memory   (function) |
| free_aligned_sized(C23) | deallocates previously allocated sized and aligned memory   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/memalignment&oldid=176982>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 October 2024, at 03:00.