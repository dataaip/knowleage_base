# memory_order

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Threads | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_create | | | | | | thrd_equal | | | | | | thrd_current | | | | | | thrd_sleep | | | | | | thrd_yield | | | | | | thrd_exit | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thrd_detach | | | | | | thrd_join | | | | | | thrd_successthrd_timedoutthrd_busythrd_nomemthrd_error | | | | | | | Atomic operations | | | | | | atomic_init | | | | | | ATOMIC_VAR_INIT(until C23) | | | | | | ATOMIC_\*\*\*_LOCK_FREE | | | | | | atomic_is_lock_free | | | | | | atomic_store | | | | | | atomic_load | | | | | | atomic_exchange | | | | | | atomic_compare_exchange | | | | | | atomic_fetch_add | | | | | | atomic_fetch_sub | | | | | | atomic_fetch_or | | | | | | atomic_fetch_xor | | | | | | atomic_fetch_and | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Atomic flags | | | | | | atomic_flag | | | | | | ATOMIC_FLAG_INIT | | | | | | atomic_flag_test_and_set | | | | | | atomic_flag_clear | | | | | | Memory ordering | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****memory_order**** | | | | | | kill_dependency | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | atomic_thread_fence | | | | | | atomic_signal_fence | | | | | | | Mutual exclusion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_init | | | | | | mtx_lock | | | | | | mtx_timedlock | | | | | | mtx_trylock | | | | | | call_once | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mtx_unlock | | | | | | mtx_destroy | | | | | | mtx_plainmtx_recursivemtx_timed | | | | | | | Condition variables | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cnd_init | | | | | | cnd_signal | | | | | | cnd_broadcast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cnd_wait | | | | | | cnd_timedwait | | | | | | cnd_destroy | | | | | | | Thread-local storage | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | thread_local | | | | | | TSS_DTOR_ITERATIONS | | | | | | tss_create | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tss_get | | | | | | tss_set | | | | | | tss_delete | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdatomic.h>` |  |  |
| enum memory_order  {      memory_order_relaxed,      memory_order_consume,      memory_order_acquire,      memory_order_release,      memory_order_acq_rel,      memory_order_seq_cst }; |  | (since C11) |
|  |  |  |

`memory_order` specifies how memory accesses, including regular, non-atomic memory accesses, are to be ordered around an atomic operation. Absent any constraints on a multi-core system, when multiple threads simultaneously read and write to several variables, one thread can observe the values change in an order different from the order another thread wrote them. Indeed, the apparent order of changes can even differ among multiple reader threads. Some similar effects can occur even on uniprocessor systems due to compiler transformations allowed by the memory model.

The default behavior of all atomic operations in the language and the library provides for **sequentially consistent ordering** (see discussion below). That default can hurt performance, but the library's atomic operations can be given an additional `memory_order` argument to specify the exact constraints, beyond atomicity, that the compiler and processor must enforce for that operation.

### Constants

|  |  |
| --- | --- |
| Defined in header `<stdatomic.h>` | |
| Value | Explanation |
| `memory_order_relaxed` | Relaxed operation: there are no synchronization or ordering constraints imposed on other reads or writes, only this operation's atomicity is guaranteed (see Relaxed ordering below). |
| `memory_order_consume` | A load operation with this memory order performs a **consume operation** on the affected memory location: no reads or writes in the current thread dependent on the value currently loaded can be reordered before this load. Writes to data-dependent variables in other threads that release the same atomic variable are visible in the current thread. On most platforms, this affects compiler optimizations only (see Release-Consume ordering below). |
| `memory_order_acquire` | A load operation with this memory order performs the **acquire operation** on the affected memory location: no reads or writes in the current thread can be reordered before this load. All writes in other threads that release the same atomic variable are visible in the current thread (see Release-Acquire ordering below). |
| `memory_order_release` | A store operation with this memory order performs the **release operation**: no reads or writes in the current thread can be reordered after this store. All writes in the current thread are visible in other threads that acquire the same atomic variable (see Release-Acquire ordering below) and writes that carry a dependency into the atomic variable become visible in other threads that consume the same atomic (see Release-Consume ordering below). |
| `memory_order_acq_rel` | A read-modify-write operation with this memory order is both an **acquire operation** and a **release operation**. No memory reads or writes in the current thread can be reordered before the load, nor after the store. All writes in other threads that release the same atomic variable are visible before the modification and the modification is visible in other threads that acquire the same atomic variable. |
| `memory_order_seq_cst` | A load operation with this memory order performs an **acquire operation**, a store performs a **release operation**, and read-modify-write performs both an **acquire operation** and a **release operation**, plus a single total order exists in which all threads observe all modifications in the same order (see Sequentially-consistent ordering below). |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: happens-before and other concepts, as in C++, but keep modification orders and the four consistencies in c/language/atomic |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: when doing above, don't forget that although happens-before wasn't acyclic in C11 as published, this was updated to match C++11 via DR 401 |

#### Relaxed ordering

Atomic operations tagged memory_order_relaxed are not synchronization operations; they do not impose an order among concurrent memory accesses. They only guarantee atomicity and modification order consistency.

For example, with x and y initially zero,

// Thread 1:  
r1 = atomic_load_explicit(y, memory_order_relaxed); // A  
atomic_store_explicit(x, r1, memory_order_relaxed); // B  
// Thread 2:  
r2 = atomic_load_explicit(x, memory_order_relaxed); // C  
atomic_store_explicit(y, 42, memory_order_relaxed); // D
is allowed to produce r1 == r2 == 42 because, although A is **sequenced-before** B within thread 1 and C is **sequenced before** D within thread 2, nothing prevents D from appearing before A in the modification order of y, and B from appearing before C in the modification order of x. The side-effect of D on y could be visible to the load A in thread 1 while the side effect of B on x could be visible to the load C in thread 2. In particular, this may occur if D is completed before C in thread 2, either due to compiler reordering or at runtime.

Typical use for relaxed memory ordering is incrementing counters, such as the reference counters , since this only requires atomicity, but not ordering or synchronization .

#### Release-Consume ordering

If an atomic store in thread A is tagged memory_order_release, an atomic load in thread B from the same variable is tagged memory_order_consume, and the load in thread B reads a value written by the store in thread A, then the store in thread A is **dependency-ordered before** the load in thread B.

All memory writes (non-atomic and relaxed atomic) that **happened-before** the atomic store from the point of view of thread A, become **visible side-effects** within those operations in thread B into which the load operation **carries dependency**, that is, once the atomic load is completed, those operators and functions in thread B that use the value obtained from the load are guaranteed to see what thread A wrote to memory.

The synchronization is established only between the threads **releasing** and **consuming** the same atomic variable. Other threads can see different order of memory accesses than either or both of the synchronized threads.

On all mainstream CPUs other than DEC Alpha, dependency ordering is automatic, no additional CPU instructions are issued for this synchronization mode, only certain compiler optimizations are affected (e.g. the compiler is prohibited from performing speculative loads on the objects that are involved in the dependency chain).

Typical use cases for this ordering involve read access to rarely written concurrent data structures (routing tables, configuration, security policies, firewall rules, etc) and publisher-subscriber situations with pointer-mediated publication, that is, when the producer publishes a pointer through which the consumer can access information: there is no need to make everything else the producer wrote to memory visible to the consumer (which may be an expensive operation on weakly-ordered architectures). An example of such scenario is `rcu_dereference`.

Note that currently (2/2015) no known production compilers track dependency chains: consume operations are lifted to acquire operations.

#### Release sequence

If some atomic is store-released and several other threads perform read-modify-write operations on that atomic, a "release sequence" is formed: all threads that perform the read-modify-writes to the same atomic synchronize with the first thread and each other even if they have no `memory_order_release` semantics. This makes single producer - multiple consumers situations possible without imposing unnecessary synchronization between individual consumer threads.

#### Release-Acquire ordering

If an atomic store in thread A is tagged memory_order_release, an atomic load in thread B from the same variable is tagged memory_order_acquire, and the load in thread B reads a value written by the store in thread A, then the store in thread A **synchronizes-with** the load in thread B.

All memory writes (including non-atomic and relaxed atomic) that **happened-before** the atomic store from the point of view of thread A, become **visible side-effects** in thread B. That is, once the atomic load is completed, thread B is guaranteed to see everything thread A wrote to memory. This promise only holds if B actually returns the value that A stored, or a value from later in the release sequence.

The synchronization is established only between the threads **releasing** and **acquiring** the same atomic variable. Other threads can see different order of memory accesses than either or both of the synchronized threads.

On strongly-ordered systems — x86, SPARC TSO, IBM mainframe, etc. — release-acquire ordering is automatic for the majority of operations. No additional CPU instructions are issued for this synchronization mode; only certain compiler optimizations are affected (e.g., the compiler is prohibited from moving non-atomic stores past the atomic store-release or performing non-atomic loads earlier than the atomic load-acquire). On weakly-ordered systems (ARM, Itanium, PowerPC), special CPU load or memory fence instructions are used.

Mutual exclusion locks, such as mutexes or atomic spinlocks, are an example of release-acquire synchronization: when the lock is released by thread A and acquired by thread B, everything that took place in the critical section (before the release) in the context of thread A has to be visible to thread B (after the acquire) which is executing the same critical section.

#### Sequentially-consistent ordering

Atomic operations tagged memory_order_seq_cst not only order memory the same way as release/acquire ordering (everything that **happened-before** a store in one thread becomes a **visible side effect** in the thread that did a load), but also establish a **single total modification order** of all atomic operations that are so tagged.

Formally,

each `memory_order_seq_cst` operation B that loads from atomic variable M, observes one of the following:

- the result of the last operation A that modified M, which appears before B in the single total order,
- OR, if there was such an A, B may observe the result of some modification on M that is not `memory_order_seq_cst` and does not **happen-before** A,
- OR, if there wasn't such an A, B may observe the result of some unrelated modification of M that is not `memory_order_seq_cst`.

If there was a `memory_order_seq_cst` atomic_thread_fence operation X **sequenced-before** B, then B observes one of the following:

- the last `memory_order_seq_cst` modification of M that appears before X in the single total order,
- some unrelated modification of M that appears later in M's modification order.

For a pair of atomic operations on M called A and B, where A writes and B reads M's value, if there are two `memory_order_seq_cst` atomic_thread_fences X and Y, and if A is **sequenced-before** X, Y is **sequenced-before** B, and X appears before Y in the Single Total Order, then B observes either:

- the effect of A,
- some unrelated modification of M that appears after A in M's modification order.

For a pair of atomic modifications of M called A and B, B occurs after A in M's modification order if

- there is a `memory_order_seq_cst` atomic_thread_fence X such that A is **sequenced-before** X and X appears before B in the Single Total Order,
- or, there is a `memory_order_seq_cst` atomic_thread_fence Y such that Y is **sequenced-before** B and A appears before Y in the Single Total Order,
- or, there are `memory_order_seq_cst` atomic_thread_fences X and Y such that A is **sequenced-before** X, Y is **sequenced-before** B, and X appears before Y in the Single Total Order.

Note that this means that:

1) as soon as atomic operations that are not tagged `memory_order_seq_cst` enter the picture, the sequential consistency is lost,2) the sequentially-consistent fences are only establishing total ordering for the fences themselves, not for the atomic operations in the general case (**sequenced-before** is not a cross-thread relationship, unlike **happens-before**).

Sequential ordering may be necessary for multiple producer-multiple consumer situations where all consumers must observe the actions of all producers occurring in the same order.

Total sequential ordering requires a full memory fence CPU instruction on all multi-core systems. This may become a performance bottleneck since it forces the affected memory accesses to propagate to every core.

### Relationship with volatile

Within a thread of execution, accesses (reads and writes) through volatile lvalues cannot be reordered past observable side-effects (including other volatile accesses) that are separated by a sequence point within the same thread, but this order is not guaranteed to be observed by another thread, since volatile access does not establish inter-thread synchronization.

In addition, volatile accesses are not atomic (concurrent read and write is a data race) and do not order memory (non-volatile memory accesses may be freely reordered around the volatile access).

One notable exception is Visual Studio, where, with default settings, every volatile write has release semantics and every volatile read has acquire semantics (Microsoft Docs), and thus volatiles may be used for inter-thread synchronization. Standard volatile semantics are not applicable to multi-threaded programming, although they are sufficient for e.g. communication with a signal handler that runs in the same thread when applied to sig_atomic_t variables.

### Examples

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.17.1/4 memory_order (p: TBD)

:   - 7.17.3 Order and consistency (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.17.1/4 memory_order (p: 200)

:   - 7.17.3 Order and consistency (p: 201-203)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.17.1/4 memory_order (p: 273)

:   - 7.17.3 Order and consistency (p: 275-277)

### See also

|  |  |
| --- | --- |
| C++ documentation for memory order | |

### External links

|  |  |
| --- | --- |
| 1. | MOESI protocol |
| 2. | x86-TSO: A Rigorous and Usable Programmer’s Model for x86 Multiprocessors P. Sewell et. al., 2010 |
| 3. | A Tutorial Introduction to the ARM and POWER Relaxed Memory Models P. Sewell et al, 2012 |
| 4. | MESIF: A Two-Hop Cache Coherency Protocol for Point-to-Point Interconnects J.R. Goodman, H.H.J. Hum, 2009 |
| 5. | Memory Models Russ Cox, 2021 |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Let's find good refs on QPI, MOESI, and maybe Dragon. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/atomic/memory_order&oldid=175729>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2024, at 12:53.