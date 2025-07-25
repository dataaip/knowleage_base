# abort

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****abort**** | | | | | | exit | | | | | | quick_exit(C11) | | | | | | _Exit(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atexit | | | | | | at_quick_exit(C11) | | | | | | EXIT_SUCCESSEXIT_FAILURE | | | | | |
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
|  |  |  |
| --- | --- | --- |
| void abort(void); |  | (until C11) |
| _Noreturn void abort(void); |  | (since C11)  (until C23) |
| [[noreturn]] void abort(void); |  | (since C23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Causes abnormal program termination unless SIGABRT is being caught by a signal handler passed to signal and the handler does not return.

Functions passed to atexit() are not called. Whether open resources such as files are closed is implementation defined. An implementation defined status is returned to the host environment that indicates unsuccessful execution.

### Parameters

(none)

### Return value

(none)

### Notes

POSIX specifies that the `abort()` function overrides blocking or ignoring the `SIGABRT` signal.

Some compiler intrinsics, e.g. `__builtin_trap` (gcc, clang, and icc) or `__fastfail`/`__debugbreak` (msvc), can be used to terminate the program as fast as possible.

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    FILE *fp = fopen("data.txt","r");
    if (fp == NULL)
    {
        fprintf(stderr, "error opening file data.txt in function main()\n");
        abort();
    }
 
    /* Normal processing continues here. */
    fclose(fp);
    printf("Normal Return\n");
    return 0;
}

```

Output:

```
error opening file data.txt in function main()

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22.4.1 The abort function (p: 255)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.4.1 The abort function (p: 350)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.4.1 The abort function (p: 315)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10.4.1 The abort function

### See also

|  |  |
| --- | --- |
| exit | causes normal program termination with cleaning up   (function) |
| atexit | registers a function to be called on exit() invocation   (function) |
| quick_exit(C11) | causes normal program termination without completely cleaning up   (function) |
| C++ documentation for abort | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/abort&oldid=167782>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 December 2023, at 01:49.