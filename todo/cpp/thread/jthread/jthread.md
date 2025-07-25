# std::jthread::jthread

From cppreference.com
< cpp‎ | thread‎ | jthread
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

Concurrency support library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Threads | | | | | | thread(C++11) | | | | | | jthread(C++20) | | | | | | hardware_destructive_interference_sizehardware_constructive_interference_size(C++17)(C++17) | | | | | | `this_thread` namespace | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | get_id(C++11) | | | | | | yield(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sleep_for(C++11) | | | | | | sleep_until(C++11) | | | | | | | Cooperative cancellation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stop_token(C++20) | | | | | | inplace_stop_token")(C++26) | | | | | | never_stop_token(C++26) | | | | | | stop_source(C++20) | | | | | | inplace_stop_source")(C++26) | | | | | | stop_callback(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_stop_callback")(C++26) | | | | | | stop_callback_for_t(C++26) | | | | | | stoppable_token(C++26) | | | | | | unstoppable_token(C++26) | | | | | | **stoppable-source**")(C++26) | | | | | | **stoppable-callback-for**")(C++26) | | | | | | | Mutual exclusion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mutex(C++11) | | | | | | recursive_mutex(C++11) | | | | | | shared_mutex(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | timed_mutex(C++11) | | | | | | recursive_timed_mutex(C++11) | | | | | | shared_timed_mutex(C++14) | | | | | | | Generic lock management | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lock(C++11) | | | | | | lock_guard(C++11) | | | | | | scoped_lock(C++17) | | | | | | unique_lock(C++11) | | | | | | shared_lock(C++14) | | | | | | once_flag(C++11) | | | | | | call_once(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | try_lock(C++11) | | | | | | defer_locktry_to_lockadopt_lockdefer_lock_ttry_to_lock_tadopt_lock_t(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | | | | | | | Condition variables | | | | | | condition_variable(C++11) | | | | | | condition_variable_any(C++11) | | | | | | notify_all_at_thread_exit(C++11) | | | | | | cv_status(C++11) | | | | | | Semaphores | | | | | | counting_semaphorebinary_semaphore(C++20)(C++20) | | | | | | Latches and Barriers | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | latch(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | barrier(C++20) | | | | | | | Futures | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | promise(C++11) | | | | | | future(C++11) | | | | | | shared_future(C++11) | | | | | | packaged_task(C++11) | | | | | | async(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | launch(C++11) | | | | | | future_status(C++11) | | | | | | future_error(C++11) | | | | | | future_category(C++11) | | | | | | future_errc(C++11) | | | | | | | Safe Reclamation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rcu_obj_base")(C++26) | | | | | | rcu_domain")(C++26) | | | | | | rcu_default_domain")(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rcu_synchronize")(C++26) | | | | | | rcu_barrier")(C++26) | | | | | | rcu_retire")(C++26) | | | | | | | Hazard Pointers | | | | | | hazard_pointer_obj_base")(C++26) | | | | | | hazard_pointer")(C++26) | | | | | | make_hazard_pointer")(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Atomic types | | | | | | atomic(C++11) | | | | | | atomic_ref(C++20) | | | | | | atomic_flag(C++11) | | | | | | Initialization of atomic types | | | | | | atomic_init(C++11)(deprecated in C++20) | | | | | | ATOMIC_VAR_INIT(C++11)(deprecated in C++20) | | | | | | ATOMIC_FLAG_INIT(C++11) | | | | | | Memory ordering | | | | | | memory_order(C++11) | | | | | | kill_dependency(C++11) | | | | | | atomic_thread_fence(C++11) | | | | | | atomic_signal_fence(C++11) | | | | | | Free functions for atomic operations | | | | | | atomic_storeatomic_store_explicit(C++11)(C++11) | | | | | | atomic_loadatomic_load_explicit(C++11)(C++11) | | | | | | atomic_exchangeatomic_exchange_explicit(C++11)(C++11) | | | | | | atomic_compare_exchange_weakatomic_compare_exchange_weak_explicitatomic_compare_exchange_strongatomic_compare_exchange_strong_explicit(C++11)(C++11)(C++11)(C++11) | | | | | | atomic_fetch_addatomic_fetch_add_explicit(C++11)(C++11) | | | | | | atomic_fetch_subatomic_fetch_sub_explicit(C++11)(C++11) | | | | | | atomic_fetch_andatomic_fetch_and_explicit(C++11)(C++11) | | | | | | atomic_fetch_oratomic_fetch_or_explicit(C++11)(C++11) | | | | | | atomic_fetch_xoratomic_fetch_xor_explicit(C++11)(C++11) | | | | | | atomic_fetch_maxatomic_fetch_max_explicit(C++26)(C++26) | | | | | | atomic_fetch_minatomic_fetch_min_explicit(C++26)(C++26) | | | | | | atomic_is_lock_free(C++11) | | | | | | atomic_waitatomic_wait_explicit(C++20)(C++20) | | | | | | atomic_notify_one(C++20) | | | | | | atomic_notify_all(C++20) | | | | | | Free functions for atomic flags | | | | | | atomic_flag_test_and_setatomic_flag_test_and_set_explicit(C++11)(C++11) | | | | | | atomic_flag_clearatomic_flag_clear_explicit(C++11)(C++11) | | | | | | atomic_flag_testatomic_flag_test_explicit(C++20)(C++20) | | | | | | atomic_flag_waitatomic_flag_wait_explicit(C++20)(C++20) | | | | | | atomic_flag_notify_one(C++20) | | | | | | atomic_flag_notify_all(C++20) | | | | | |

std::jthread

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****jthread::jthread**** | | | | |
| jthread::~jthread | | | | |
| jthread::operator= | | | | |
| Observers | | | | |
| jthread::joinable | | | | |
| jthread::get_id | | | | |
| jthread::native_handle | | | | |
| jthread::hardware_concurrency | | | | |
| Operations | | | | |
| jthread::join | | | | |
| jthread::detach | | | | |
| jthread::swap | | | | |
| Stop token handling | | | | |
| jthread::get_stop_source | | | | |
| jthread::get_stop_token | | | | |
| jthread::request_stop | | | | |
| Non-member functions | | | | |
| swap(std::jthread) | | | | |

|  |  |  |
| --- | --- | --- |
| jthread() noexcept; | (1) | (since C++20) |
| jthread( jthread&& other ) noexcept; | (2) | (since C++20) |
| template< class F, class... Args >   explicit jthread( F&& f, Args&&... args ); | (3) | (since C++20) |
| jthread( const jthread& ) = delete; | (4) | (since C++20) |
|  |  |  |

Constructs new `std::jthread` object.

1) Creates new `std::jthread` object which does not represent a thread.2) Move constructor. Constructs the `std::jthread` object to represent the thread of execution that was represented by other. After this call other no longer represents a thread of execution.3) Creates new `std::jthread` object and associates it with a thread of execution.

The new thread of execution starts executing:

|  |  |
| --- | --- |
| std::invoke(**decay-copy**(std::forward<F>(f)), get_stop_token(), **decay-copy**(std::forward<Args>(args))...) | (until C++23) |
| std::invoke(auto(std::forward<F>(f)), get_stop_token(),             auto(std::forward<Args>(args))...) | (since C++23) |

if the expression above is well-formed, otherwise starts executing:

|  |  |
| --- | --- |
| std::invoke(**decay-copy**(std::forward<F>(f)), **decay-copy**(std::forward<Args>(args))...). | (until C++23) |
| std::invoke(auto(std::forward<F>(f)),             auto(std::forward<Args>(args))...). | (since C++23) |

 The calls of **decay-copy** are evaluated(until C++23)The values produced by auto are materialized(since C++23) in the current thread, so that any exceptions thrown during evaluation and copying/moving of the arguments are thrown in the current thread, without starting the new thread. These overloads participate in overload resolution only if std::remove_cvref_t<F> is not the same type as `std::jthread`. If any of the following is false, the program is ill-formed:

- std::is_constructible_v<std::decay_t<F>, F>
- (std::is_constructible_v<std::decay_t<Args>, Args> && ...)
- std::is_invocable_v<std::decay_t<F>, std::decay_t<Args>...> ||  
  std::is_invocable_v<std::decay_t<F>, std::stop_token, std::decay_t<Args>...>
 The completion of the invocation of the constructor synchronizes with the beginning of the invocation of the copy of f on the new thread of execution.4) The copy constructor is deleted; threads are not copyable. No two `std::jthread` objects may represent the same thread of execution.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `std::jthread` object to construct this `std::jthread` object with |
| f | - | Callable object to execute in the new thread |
| args | - | arguments to pass to the new function |

### Postconditions

1) `get_id()` equal to std::jthread::id() (i.e. `joinable()` returns false) and get_stop_source().stop_possible() is false.2) other.get_id() equal to std::jthread::id() and `get_id()` returns the value of other.get_id() prior to the start of construction.3) `get_id()` not equal to std::jthread::id() (i.e. `joinable()` returns true), and get_stop_source().stop_possible() is true.

### Exceptions

3) std::system_error if the thread could not be started. The exception may represent the error condition `std::errc::resource_unavailable_try_again` or another implementation-specific error condition.

### Notes

The arguments to the thread function are moved or copied by value. If a reference argument needs to be passed to the thread function, it has to be wrapped (e.g. with std::ref or std::cref).

Any return value from the function is ignored. If the function throws an exception, std::terminate is called. In order to pass return values or exceptions back to the calling thread, std::promise or std::async may be used.

### Example

Run this code

```
#include <chrono>
#include <iostream>
#include <thread>
#include <utility>
 
using namespace std::literals;
 
void f1(int n)
{
    for (int i = 0; i < 5; ++i)
    {
        std::cout << "Thread 1 executing\n";
        ++n;
        std::this_thread::sleep_for(10ms);
    }
}
 
void f2(int& n)
{
    for (int i = 0; i < 5; ++i)
    {
        std::cout << "Thread 2 executing\n";
        ++n;
        std::this_thread::sleep_for(10ms);
    }
}
 
class foo
{
public:
    void bar()
    {
        for (int i = 0; i < 5; ++i)
        {
            std::cout << "Thread 3 executing\n";
            ++n;
            std::this_thread::sleep_for(10ms);
        }
    }
    int n = 0;
};
 
class baz
{
public:
    void operator()()
    {
        for (int i = 0; i < 5; ++i)
        {
            std::cout << "Thread 4 executing\n";
            ++n;
            std::this_thread::sleep_for(10ms);
        }
    }
    int n = 0;
};
 
int main()
{
    int n = 0;
    foo f;
    baz b;
    std::jthread t0; // t0 is not a thread
    std::jthread t1(f1, n + 1); // pass by value
    std::jthread t2a(f2, std::ref(n)); // pass by reference
    std::jthread t2b(std::move(t2a)); // t2b is now running f2(). t2a is no longer a thread
    std::jthread t3(&foo::bar, &f); // t3 runs foo::bar() on object f
    std::jthread t4(b); // t4 runs baz::operator() on a copy of object b
    t1.join();
    t2b.join();
    t3.join();
    std::cout << "Final value of n is " << n << '\n';
    std::cout << "Final value of f.n (foo::n) is " << f.n << '\n';
    std::cout << "Final value of b.n (baz::n) is " << b.n << '\n';
    // t4 joins on destruction
}

```

Possible output:

```
Thread 2 executing
Thread 1 executing
Thread 4 executing
Thread 3 executing
Thread 3 executing
Thread 4 executing
Thread 2 executing
Thread 1 executing
Thread 3 executing
Thread 1 executing
Thread 4 executing
Thread 2 executing
Thread 3 executing
Thread 1 executing
Thread 4 executing
Thread 2 executing
Thread 3 executing
Thread 1 executing
Thread 4 executing
Thread 2 executing
Final value of n is 5
Final value of f.n (foo::n) is 5
Final value of b.n (baz::n) is 0

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3476 | C++20 | overload (3) directly required (the decayed types of) `F` and the argument types to be move constructible | removed these requirements[[1]](jthread.html#cite_note-1) |

1. ↑ The move-constructibility is already indirectly required by std::is_constructible_v.

### See also

|  |  |
| --- | --- |
| (constructor) | constructs new `thread` object   (public member function of `std::thread`) |
| C documentation for thrd_create | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/thread/jthread/jthread&oldid=172094>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 May 2024, at 06:33.