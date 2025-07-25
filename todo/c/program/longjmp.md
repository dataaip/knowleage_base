# longjmp

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setjmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****longjmp**** | | | | | |
| Types | | | | |
| jmp_buf | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<setjmp.h>` |  |  |
|  |  |  |
| --- | --- | --- |
| void longjmp( jmp_buf env, int status ); |  | (until C11) |
| _Noreturn void longjmp( jmp_buf env, int status ); |  | (since C11)  (until C23) |
| [[noreturn]] void longjmp( jmp_buf env, int status ); |  | (since C23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Loads the execution context `env` saved by a previous call to setjmp. This function does not return. Control is transferred to the call site of the macro setjmp that set up `env`. That setjmp then returns the value, passed as the `status`.

If the function that called setjmp has exited (whether by return or by a different `longjmp` higher up the stack), the behavior is undefined. In other words, only long jumps up the call stack are allowed.

|  |  |
| --- | --- |
| Jumping across threads (if the function that called `setjmp` was executed by another thread) is also undefined behavior. | (since C11) |

|  |  |
| --- | --- |
| If when setjmp was called, a VLA or another variably-modified type variable was in scope and control left that scope, `longjmp` to that `setjmp` invokes undefined behavior even if control remained within the function.  On the way up the stack, `longjmp` does not deallocate any VLAs, memory leaks may occur if their lifetimes are terminated in this way:   ```text void g(int n) {     int a[n]; // a may remain allocated     h(n); // does not return } void h(int n) {     int b[n]; // b may remain allocated     longjmp(buf, 2); // might cause a memory leak for h's b and g's a } ``` | (since C99) |

### Parameters

|  |  |  |
| --- | --- | --- |
| env | - | variable referring to the execution state of the program saved by setjmp |
| status | - | the value to return from setjmp. If it is equal to ​0​, 1 is used instead |

### Return value

(none)

### Notes

`longjmp` is intended for handling unexpected error conditions where the function cannot return meaningfully. This is similar to exception handling in other programming languages.

### Example

Run this code

```
#include <stdio.h>
#include <setjmp.h>
#include <stdnoreturn.h>
 
jmp_buf my_jump_buffer;
 
noreturn void foo(int status) 
{
    printf("foo(%d) called\n", status);
    longjmp(my_jump_buffer, status + 1); // will return status+1 out of setjmp
}
 
int main(void)
{
    volatile int count = 0; // modified local vars in setjmp scope must be volatile
    if (setjmp(my_jump_buffer) != 5) // compare against constant in an if
        foo(++count);
}

```

Output:

```
foo(1) called
foo(2) called
foo(3) called
foo(4) called

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.13.2.1 The longjmp macro (p: 191-192)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.13.2.1 The longjmp macro (p: 263-264)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.13.2.1 The longjmp macro (p: 244-245)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.6.2.1 The longjmp function

### See also

|  |  |
| --- | --- |
| setjmp | saves the context   (function macro) |
| C++ documentation for longjmp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/program/longjmp&oldid=154421>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 June 2023, at 04:46.