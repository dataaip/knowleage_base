# atomic_is_lock_free

From cppreference.com
< c‎ | atomic
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

 Concurrency support library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Threads | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_create | | | | | | thrd_equal | | | | | | thrd_current | | | | | | thrd_sleep | | | | | | thrd_yield | | | | | | thrd_exit | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_detach | | | | | | thrd_join | | | | | | thrd_successthrd_timedoutthrd_busythrd_nomemthrd_error | | | | | | | Atomic operations | | | | | | atomic_init | | | | | | ATOMIC_VAR_INIT(until C23) | | | | | | ATOMIC_\*\*\*_LOCK_FREE | | | | | | ****atomic_is_lock_free**** | | | | | | atomic_store | | | | | | atomic_load | | | | | | atomic_exchange | | | | | | atomic_compare_exchange | | | | | | atomic_fetch_add | | | | | | atomic_fetch_sub | | | | | | atomic_fetch_or | | | | | | atomic_fetch_xor | | | | | | atomic_fetch_and | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Atomic flags | | | | | | atomic_flag | | | | | | ATOMIC_FLAG_INIT | | | | | | atomic_flag_test_and_set | | | | | | atomic_flag_clear | | | | | | Memory ordering | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memory_order | | | | | | kill_dependency | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atomic_thread_fence | | | | | | atomic_signal_fence | | | | | | | Mutual exclusion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_init | | | | | | mtx_lock | | | | | | mtx_timedlock | | | | | | mtx_trylock | | | | | | call_once | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_unlock | | | | | | mtx_destroy | | | | | | mtx_plainmtx_recursivemtx_timed | | | | | | | Condition variables | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cnd_init | | | | | | cnd_signal | | | | | | cnd_broadcast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cnd_wait | | | | | | cnd_timedwait | | | | | | cnd_destroy | | | | | | | Thread-local storage | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thread_local | | | | | | TSS_DTOR_ITERATIONS | | | | | | tss_create | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tss_get | | | | | | tss_set | | | | | | tss_delete | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdatomic.h>` |  |  |
| _Bool atomic_is_lock_free( const volatile A\* obj ); |  | (since C11) |
|  |  |  |

Determines if the atomic operations on all objects of the type `A` (the type of the object pointed to by `obj`) are lock-free. In any given program execution, the result of calling `atomic_is_lock_free` is the same for all pointers of the same type.

This is a generic function defined for all atomic object types `A`. The argument is pointer to a volatile atomic type to accept addresses of both non-volatile and volatile (e.g. memory-mapped I/O) atomic objects, and volatile semantic is preserved when applying this operation to volatile atomic objects.

It is unspecified whether the name of a generic function is a macro or an identifier declared with external linkage. If a macro definition is suppressed in order to access an actual function (e.g. parenthesized like (atomic_is_lock_free)(...)), or a program defines an external identifier with the name of a generic function, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| obj | - | pointer to the atomic object to inspect |

### Return value

true if the operations on all objects of the type `A` are lock-free, false otherwise.

### Example

Run this code

```
#include <stdio.h>
#include <stdatomic.h>
 
_Atomic struct A { int a[100]; } a;
_Atomic struct B { int x, y; } b;
int main(void)
{
    printf("_Atomic struct A is lock free? %s\n", 
            atomic_is_lock_free(&a) ? "true" : "false");
    printf("_Atomic struct B is lock free? %s\n", 
            atomic_is_lock_free(&b) ? "true" : "false");
}

```

Possible output:

```
_Atomic struct A is lock free? false
_Atomic struct B is lock free? true

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| DR 465 | C11 | this function was per-object | this functions is per-type |

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.17.5.1 The atomic_is_lock_free generic function (p: 205)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.17.5.1 The atomic_is_lock_free generic function (p: 280)

### See also

|  |  |
| --- | --- |
| ATOMIC_BOOL_LOCK_FREEATOMIC_CHAR_LOCK_FREEATOMIC_CHAR16_T_LOCK_FREEATOMIC_CHAR32_T_LOCK_FREEATOMIC_WCHAR_T_LOCK_FREEATOMIC_SHORT_LOCK_FREEATOMIC_INT_LOCK_FREEATOMIC_LONG_LOCK_FREEATOMIC_LLONG_LOCK_FREEATOMIC_POINTER_LOCK_FREE(C11) | indicates that the given atomic type is lock-free   (macro constant) |
| C++ documentation for atomic_is_lock_free | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/atomic/atomic_is_lock_free&oldid=138687>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 March 2022, at 22:41.