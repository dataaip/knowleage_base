# sig_atomic_t

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
| memalignment(C23) | | | | |
| Signals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | signal | | | | | | raise | | | | | | ****sig_atomic_t**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIG_DFLSIG_IGN | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGABRTSIGFPESIGILL | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGINTSIGSEGVSIGTERM | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<signal.h>` |  |  |
| typedef /\* unspecified \*/ sig_atomic_t; |  |  |
|  |  |  |

An integer type which can be accessed as an atomic entity even in the presence of asynchronous interrupts made by signals.

### Example

Run this code

```
#include <signal.h>
#include <stdio.h>
 
volatile sig_atomic_t gSignalStatus = 0;
 
void signal_handler(int status)
{
    gSignalStatus = status;
}
 
int main(void)
{
    /* Install a signal handler. */
    signal(SIGINT, signal_handler);
 
    printf("SignalValue:    %d\n", gSignalStatus);
    printf("Sending signal: %d\n", SIGINT);
    raise(SIGINT);
    printf("SignalValue:    %d\n", gSignalStatus);
}

```

Possible output:

```
SignalValue:    0
Sending signal: 2
SignalValue:    2

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.14/2 Signal handling <signal.h> (p: 194-195)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.14/2 Signal handling <signal.h> (p: 265)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.14/2 Signal handling <signal.h> (p: 246)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.7 SIGNAL HANDLING <signal.h>

### See also

|  |  |
| --- | --- |
| signal | sets a signal handler for particular signal   (function) |
| C++ documentation for sig_atomic_t | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/sig_atomic_t&oldid=140328>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 June 2022, at 07:00.