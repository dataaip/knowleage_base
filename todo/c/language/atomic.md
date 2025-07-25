# Atomic types

From cppreference.com
< c‎ | language
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

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 Declarations

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Pointer | | | | |
| Array | | | | |
| enum | | | | |
| struct | | | | |
| union | | | | |
| Bit-field | | | | |
| ****Atomic types**** (C11) | | | | |
| const | | | | |
| constexpr(C23) | | | | |
| volatile | | | | |
| restrict(C99) | | | | |
| Alignment specifiers | | | | |
| Storage duration and linkage | | | | |
| External and tentative definitions | | | | |
| typedef | | | | |
| Static assertions | | | | |
| Attributes (C23) | | | | |

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `_Atomic` `(` type-name `)` | (1) | (since C11) |
|  | | | | | | | | | |
| `_Atomic` type-name | (2) | (since C11) |
|  | | | | | | | | | |

1) Use as a type specifier; this designates a new atomic type2) Use as a type qualifier; this designates the atomic version of type-name. In this role, it may be mixed with `const`, `volatile`, and `restrict`, although unlike other qualifiers, the atomic version of type-name may have a different size, alignment, and object representation.

|  |  |  |
| --- | --- | --- |
| type-name | - | any type other than array or function. For (1), type-name also cannot be atomic or cvr-qualified |

The header <stdatomic.h> defines many convenience type aliases, from atomic_bool to atomic_uintmax_t, which simplify the use of this keyword with built-in and library types.

```
_Atomic const int* p1;  // p is a pointer to an atomic const int
const atomic_int* p2;   // same
const _Atomic(int)* p3; // same

```

If the macro constant __STDC_NO_ATOMICS__ is defined by the compiler, the keyword _Atomic is not provided.

### Explanation

Objects of atomic types are the only objects that are free from data races; that is, they may be modified by two threads concurrently or modified by one and read by another.

Each atomic object has its own associated **modification order**, which is a total order of modifications made to that object. If, from some thread's point of view, modification `A` of some atomic `M` happens-before modification `B` of the same atomic `M`, then in the modification order of `M`, `A` occurs before `B`.

Note that although each atomic object has its own modification order, there is no single total order; different threads may observe modifications to different atomic objects in different orders.

There are four coherence kinds that are guaranteed for all atomic operations:

- ****write-write coherence****: If an operation `A` that modifies an atomic object `M` **happens-before** an operation `B` that modifies `M`, then `A` appears earlier than `B` in the modification order of `M`.
- ****read-read coherence****: If a value computation `A` of an atomic object `M` happens before a value computation `B` of `M`, and `A` takes its value from a side effect `X` on `M`, then the value computed by `B` is either the value stored by `X` or is the value stored by a side effect `Y` on `M`, where `Y` appears later than `X` in the modification order of `M`.
- ****read-write coherence****: If a value computation `A` of an atomic object `M` **happens-before** an operation `B` on `M`, then `A` takes its value from a side effect `X` on `M`, where `X` appears before `B` in the modification order of `M`.
- ****write-read coherence****: If a side effect `X` on an atomic object `M` **happens-before** a value computation `B` of `M`, then the evaluation `B` takes its value from `X` or from a side effect `Y` that appears after `X` in the modification order of `M`.

Some atomic operations are also synchronization operations; they may have additional release semantics, acquire semantics, or sequentially-consistent semantics. See memory_order.

Built-in increment and decrement operators and compound assignment are read-modify-write atomic operations with total sequentially consistent ordering (as if using memory_order_seq_cst). If less strict synchronization semantics are desired, the standard library functions may be used instead.

Atomic properties are only meaningful for lvalue expressions. Lvalue-to-rvalue conversion (which models a memory read from an atomic location to a CPU register) strips atomicity along with other qualifiers.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: more, review interaction with memory_order and atomic library pages |

### Notes

Accessing a member of an atomic struct/union is undefined behavior.

The library type sig_atomic_t does not provide inter-thread synchronization or memory ordering, only atomicity.

The `volatile` types do not provide inter-thread synchronization, memory ordering, or atomicity.

Implementations are recommended to ensure that the representation of _Atomic(T) in C is same as that of std::atomic<T> in C++ for every possible type `T`. The mechanisms used to ensure atomicity and memory ordering should be compatible.

### Keywords

_Atomic

### Example

Run this code

```
#include <stdatomic.h>
#include <stdio.h>
#include <threads.h>
 
atomic_int acnt;
int cnt;
 
int f(void* thr_data)
{
    for (int n = 0; n < 1000; ++n)
    {
        ++cnt;
        ++acnt;
        // for this example, relaxed memory order is sufficient, e.g.
        // atomic_fetch_add_explicit(&acnt, 1, memory_order_relaxed);
    }
    return 0;
}
 
int main(void)
{
    thrd_t thr[10];
    for (int n = 0; n < 10; ++n)
        thrd_create(&thr[n], f, NULL);
    for (int n = 0; n < 10; ++n)
        thrd_join(thr[n], NULL);
 
    printf("The atomic counter is %u\n", acnt);
    printf("The non-atomic counter is %u\n", cnt);
}

```

Possible output:

```
The atomic counter is 10000
The non-atomic counter is 8644

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.7.2.4 Atomic type specifiers (p: TBD)

:   - 7.17 Atomics <stdatomic.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.2.4 Atomic type specifiers (p: 87)

:   - 7.17 Atomics <stdatomic.h> (p: 200-209)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.2.4 Atomic type specifiers (p: 121)

:   - 7.17 Atomics <stdatomic.h> (p: 273-286)

### See also

|  |  |
| --- | --- |
| ****Concurrency support library**** | |
| C++ documentation for atomic | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/atomic&oldid=180288>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 February 2025, at 20:20.