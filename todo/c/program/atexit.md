# atexit

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abort | | | | | | exit | | | | | | quick_exit(C11) | | | | | | _Exit(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****atexit**** | | | | | | at_quick_exit(C11) | | | | | | EXIT_SUCCESSEXIT_FAILURE | | | | | |
| Unreachable control flow | | | | |
| unreachable(C23) | | | | |
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
| Defined in header `<stdlib.h>` |  |  |
| int atexit( void (\*func)(void) ); |  |  |
|  |  |  |

Registers the function pointed to by `func` to be called on normal program termination (via exit() or returning from `main()`). The functions will be called in reverse order they were registered, i.e. the function registered last will be executed first.

The same function may be registered more than once.

The implementation is guaranteed to support the registration of at least 32 functions. The exact limit is implementation-defined.

### Parameters

|  |  |  |
| --- | --- | --- |
| func | - | pointer to a function to be called on normal program termination |

### Return value

​0​ if the registration succeeds, nonzero value otherwise.

### Example

Run this code

```
#include <stdlib.h>
#include <stdio.h>
 
void f1(void)
{
    puts("f1");
}
 
void f2(void)
{
    puts("f2");
}
 
int main(void)
{
    if ( ! atexit(f1) && ! atexit(f2) && ! atexit(f2) )
        return EXIT_SUCCESS ;
 
    // atexit registration failed
    return EXIT_FAILURE ;
 
}   // <- if registration was successful calls f2, f2, f1

```

Output:

```
f2
f2
f1

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22.4.2 The atexit function (p: 255)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.4.2 The atexit function (p: 350)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.4.2 The atexit function (p: 315)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 7.10.4.2 The atexit function (p: 156)

### See also

|  |  |
| --- | --- |
| at_quick_exit(C11) | registers a function to be called on quick_exit invocation   (function) |
| C++ documentation for atexit | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/atexit&oldid=172244>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 June 2024, at 07:34.