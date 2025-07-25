# raise

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | signal | | | | | | ****raise**** | | | | | | sig_atomic_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIG_DFLSIG_IGN | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGABRTSIGFPESIGILL | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGINTSIGSEGVSIGTERM | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<signal.h>` |  |  |
| int raise( int sig ); |  |  |
|  |  |  |

Sends signal sig to the program. The signal handler, specified using signal(), is invoked.

If the user-defined signal handling strategy is not set using signal() yet, it is implementation-defined whether the signal will be ignored or default handler will be invoked.

### Parameters

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| sig | - | the signal to be sent. It can be an implementation-defined value or one of the following values:  |  |  | | --- | --- | | SIGABRTSIGFPESIGILLSIGINTSIGSEGVSIGTERM | defines signal types   (macro constant) | |

### Return value

​0​ upon success, non-zero value on failure.

### Example

Run this code

```
#include <signal.h>
#include <stdio.h>
 
void signal_handler(int signal)
{
    printf("Received signal %d\n", signal);
}
 
int main(void)
{
    // Install a signal handler.
    signal(SIGTERM, signal_handler);
 
    printf("Sending signal %d\n", SIGTERM);
    raise(SIGTERM);
    printf("Exit main()\n");
}

```

Output:

```
Sending signal 15
Received signal 15
Exit main()

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.14.2.1 The raise function (p: 194-195)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.14.2.1 The raise function (p: 267)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.14.2.1 The raise function (p: 248)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.7.2.1 The raise function

### See also

|  |  |
| --- | --- |
| signal | sets a signal handler for particular signal   (function) |
| C++ documentation for raise | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/raise&oldid=140326>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 June 2022, at 06:43.