# EXIT_SUCCESS, EXIT_FAILURE

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abort | | | | | | exit | | | | | | quick_exit(C11) | | | | | | _Exit(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atexit | | | | | | at_quick_exit(C11) | | | | | | ****EXIT_SUCCESSEXIT_FAILURE**** | | | | | |
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
| #define EXIT_SUCCESS /\*implementation defined\*/ |  |  |
| #define EXIT_FAILURE /\*implementation defined\*/ |  |  |
|  |  |  |

The `EXIT_SUCCESS` and `EXIT_FAILURE` macros expand into integral constant expressions that can be used as arguments to the exit function (and, therefore, as the values to return from the main function), and indicate program execution status.

|  |  |
| --- | --- |
| Constant | Description |
| `EXIT_SUCCESS` | successful execution of a program |
| `EXIT_FAILURE` | unsuccessful execution of a program |

### Notes

Both `EXIT_SUCCESS` and the value zero indicate successful program execution status (see exit), although it is not required that `EXIT_SUCCESS` equals zero.

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    FILE* fp = fopen("data.txt", "r");
    if (fp == NULL)
    {
       fprintf(stderr, "fopen() failed in file %s at line #%d", __FILE__, __LINE__);
       exit(EXIT_FAILURE);
    }
 
    /* Normal processing continues here. */
    fclose(fp);
    printf("Normal Return\n");
 
    return EXIT_SUCCESS;
}

```

Output:

```
fopen() failed in file main.cpp at line #9

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.22/3 General utilities <stdlib.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22/3 General utilities <stdlib.h> (p: 248)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22/3 General utilities <stdlib.h> (p: 340)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20/3 General utilities <stdlib.h> (p: 306)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10 General utilities <stdlib.h>

### See also

|  |  |
| --- | --- |
| C++ documentation for EXIT_SUCCESS, EXIT_FAILURE | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/EXIT_status&oldid=178295>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 December 2024, at 18:19.