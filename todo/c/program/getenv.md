# getenv, getenv_s

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****getenvgetenv_s****(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | system | | | | | |  | | | | | |
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
| char \*getenv( const char \*name ); | (1) |  |
| errno_t getenv_s( size_t \*restrict len, char \*restrict value,                    rsize_t valuesz, const char \*restrict name ); | (2) | (since C11) |
|  |  |  |

1) Searches for an environmental variable with name name in the host-specified environment list and returns a pointer to the string that is associated with the matched environment variable. The set of environmental variables and methods of altering it are implementation-defined. This function is not required to be thread-safe. Another call to `getenv`, as well as a call to the POSIX functions `setenv()`, `unsetenv()`, and `putenv()` may invalidate the pointer returned by a previous call or modify the string obtained from a previous call. Modifying the string returned by `getenv` invokes undefined behavior.2) Same as (1), except that the values of the environment variable is written to the user-provided buffer value (unless null) and the number of bytes written is stored in the user-provided location \*len (unless null). If the environment variable is not set in the environment, zero is written to \*len (unless null) and '\0' is written to value[0] (unless null). In addition, the following errors are detected at runtime and call the currently installed constraint handler function:

:   - name is a null pointer
    - valuesz is greater than RSIZE_MAX
    - value is a null pointer and valuesz is not zero
:   As with all bounds-checked functions, `getenv_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <stdlib.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| name | - | null-terminated character string identifying the name of the environmental variable to look for |
| len | - | pointer to a user-provided location where `getenv_s` will store the length of the environment variable |
| value | - | pointer to a user-provided character array where `getenv_s` will store the contents of the environment variable |
| valuesz | - | maximum number of characters that `getenv_s` is allowed to write to `dest` (size of the buffer) |

### Return value

1) character string identifying the value of the environmental variable or null pointer if such variable is not found.2) zero if the environment variable was found, non-zero if it was not found or if a runtime constraint violation occurred. On any error, writes zero to \*len (unless len is a null pointer).

### Notes

On POSIX systems, the environment variables are also accessible through the global variable `environ`, declared as extern char \*\*environ; in <unistd.h>, and through the optional third argument, `envp`, of the main function.

The call to `getenv_s` with a null pointer for value and zero for valuesz is used to determine the size of the buffer required to hold the entire result.

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    const char *name = "PATH";
    const char *env_p = getenv(name);
    if (env_p)
        printf("Your %s is %s\n", name, env_p);
}

```

Possible output:

```
Your PATH is /home/gamer/.local/bin:/usr/local/bin:/usr/bin:/bin:/usr/share/games

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.22.4.6 The getenv function (p: TBD)

:   - K.3.6.2.1 The getenv_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.22.4.6 The getenv function (p: 256-257)

:   - K.3.6.2.1 The getenv_s function (p: 440-441)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.4.6 The getenv function (p: 352-353)

:   - K.3.6.2.1 The getenv_s function (p: 606-607)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.4.5 The getenv function (p: 317)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10.4.4 The getenv function

### See also

|  |  |
| --- | --- |
| C++ documentation for getenv | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/getenv&oldid=160652>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 October 2023, at 14:35.