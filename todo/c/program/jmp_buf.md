# jmp_buf

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | signal | | | | | | raise | | | | | | sig_atomic_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIG_DFLSIG_IGN | | | | | | SIG_ERR | | | | | |
| Signal types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGABRTSIGFPESIGILL | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | SIGINTSIGSEGVSIGTERM | | | | | |
| Non-local jumps | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | longjmp | | | | | |
| Types | | | | |
| ****jmp_buf**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<setjmp.h>` |  |  |
| typedef /\* unspecified \*/ jmp_buf; |  |  |
|  |  |  |

The `jmp_buf` type is an array type suitable for storing information to restore a calling environment. The stored information is sufficient to restore execution at the correct block of the program and invocation of that block. The state of floating-point status flags, or open files, or any other data is not stored in an object of type `jmp_buf`.

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.13/2 Nonlocal jumps <setjmp.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.13/2 Nonlocal jumps <setjmp.h> (p: 191)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.13/2 Nonlocal jumps <setjmp.h> (p: 262)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.13/2 Nonlocal jumps <setjmp.h> (p: 243)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.6 NON-LOCAL JUMPS <setjmp.h>

### See also

|  |  |
| --- | --- |
| setjmp | saves the context   (function macro) |
| longjmp | jumps to specified location   (function) |
| C++ documentation for jmp_buf | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/jmp_buf&oldid=180111>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 February 2025, at 18:44.