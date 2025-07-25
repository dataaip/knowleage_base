# std::atomic<T>::operator++,++(int),--,--(int)

From cppreference.com
< cpp‎ | atomic‎ | atomic
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

std::atomic

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| atomic::atomic | | | | |
| atomic::operator= | | | | |
| atomic::is_lock_free | | | | |
| atomic::store | | | | |
| atomic::load | | | | |
| atomic::operator T | | | | |
| atomic::exchange | | | | |
| atomic::compare_exchange_strongatomic::compare_exchange_weak | | | | |
| atomic::wait(C++20) | | | | |
| atomic::notify_one(C++20) | | | | |
| atomic::notify_all(C++20) | | | | |
| Constants | | | | |
| atomic::is_always_lock_free(C++17) | | | | |
| Specialized member functions | | | | |
| Specialized for integral, floating-point (C++20) and pointer types | | | | |
| atomic::fetch_add | | | | |
| atomic::fetch_sub | | | | |
| atomic::operator+=atomic::operator-= | | | | |
| Specialized for integral and pointer types only | | | | |
| atomic::fetch_max(C++26) | | | | |
| atomic::fetch_min(C++26) | | | | |
| ****atomic::operator++atomic::operator++(int)atomic::operator--atomic::operator--(int)**** | | | | |
| Specialized for integral types only | | | | |
| atomic::fetch_and | | | | |
| atomic::fetch_or | | | | |
| atomic::fetch_xor | | | | |
| atomic::operator&=atomic::operator|=atomic::operator^= | | | | |

|  |  |  |
| --- | --- | --- |
| member only of `atomic<Integral` ﻿`>` specializations |  |  |
| T operator++() noexcept; | (1) | (since C++11) |
| T operator++() volatile noexcept; | (2) | (since C++11) |
| T operator++( int ) noexcept; | (3) | (since C++11) |
| T operator++( int ) volatile noexcept; | (4) | (since C++11) |
| T operator--() noexcept; | (5) | (since C++11) |
| T operator--() volatile noexcept; | (6) | (since C++11) |
| T operator--( int ) noexcept; | (7) | (since C++11) |
| T operator--( int ) volatile noexcept; | (8) | (since C++11) |
| member only of `atomic<T*>` partial specialization |  |  |
| T\* operator++() noexcept; | (9) | (since C++11) |
| T\* operator++() volatile noexcept; | (10) | (since C++11) |
| T\* operator++( int ) noexcept; | (11) | (since C++11) |
| T\* operator++( int ) volatile noexcept; | (12) | (since C++11) |
| T\* operator--() noexcept; | (13) | (since C++11) |
| T\* operator--() volatile noexcept; | (14) | (since C++11) |
| T\* operator--( int ) noexcept; | (15) | (since C++11) |
| T\* operator--( int ) volatile noexcept; | (16) | (since C++11) |
|  |  |  |

Atomically increments or decrements the current value. The operation is read-modify-write operation.

- operator++() performs atomic pre-increment. Equivalent to return fetch_add(1) + 1;.
- operator++(int) performs atomic post-increment. Equivalent to return fetch_add(1);.
- operator--() performs atomic pre-decrement. Equivalent to return fetch_sub(1) - 1;.
- operator--(int) performs atomic post-decrement. Equivalent to return fetch_sub(1);.

1-8) For signed integral types, arithmetic is defined to use two’s complement representation. There are no undefined results.9-16) The result may be an undefined address, but the operations otherwise have no undefined behavior. If `T` is not a complete object type, the program is ill-formed.

|  |  |
| --- | --- |
| It is deprecated if std::atomic<T>::is_always_lock_free is false and any volatile overload participates in overload resolution. | (since C++20) |

### Return value

operator++() and operator--() return the value of the atomic variable after the modification. Formally, the result of incrementing/decrementing the value immediately preceding the effects of this function in the modification order of \*this.

operator++(int) and operator--(int) return the value of the atomic variable before the modification. Formally, the value immediately preceding the effects of this function in the modification order of \*this.

### Notes

Unlike most pre-increment and pre-decrement operators, the pre-increment and pre-decrement operators for atomic types do not return a reference to the modified object. They return a copy of the stored value instead.

### Example

Run this code

```
#include <atomic>
#include <chrono>
#include <iomanip>
#include <iostream>
#include <mutex>
#include <random>
#include <string>
#include <thread>
 
std::atomic<int> atomic_count{0};
 
std::mutex cout_mutex;
int completed_writes{0};
 
constexpr int global_max_count{72};
constexpr int writes_per_line{8};
constexpr int max_delay{100};
 
template<int Max>
int random_value()
{
    static std::uniform_int_distribution<int> distr{1, Max};
    static std::random_device engine;
    static std::mt19937 noise{engine()};
    static std::mutex rand_mutex;
    std::lock_guard lock{rand_mutex};
    return distr(noise);
}
 
int main()
{
    auto work = [](const std::string id)
    {
        for (int count{}; (count = ++atomic_count) <= global_max_count;)
        {
            std::this_thread::sleep_for(
                std::chrono::milliseconds(random_value<max_delay>()));
 
            // print thread `id` and `count` value
            {
                std::lock_guard lock{cout_mutex};
 
                const bool new_line = ++completed_writes % writes_per_line == 0;
 
                std::cout << id << std::setw(3) << count << "  "
                          << (new_line ? "\n" : "") << std::flush;
            }
        }
    };
 
    std::jthread j1(work, "░"), j2(work, "▒"), j3(work, "▓"), j4(work, "█");
}

```

Possible output:

```
▒  2  ░  1  ▒  5  ▒  7  █  4  ░  6  ▓  3  ▒  8  
▓ 11  █  9  ▓ 13  ░ 10  █ 14  ▒ 12  ░ 16  ░ 19  
▓ 15  ▒ 18  ▓ 21  ▒ 22  █ 17  █ 25  ▒ 24  █ 26  
░ 20  ░ 29  ▒ 27  ▓ 23  ▒ 31  ▒ 33  ▓ 32  █ 28  
░ 30  ░ 37  ▒ 34  ▓ 35  █ 36  █ 41  ▓ 40  ▒ 39  
░ 38  ▓ 43  █ 42  ▓ 46  ▓ 48  █ 47  █ 50  ░ 45  
▒ 44  ▒ 53  ▒ 54  ▓ 49  ▒ 55  █ 51  ▒ 57  █ 58  
░ 52  ▓ 56  ░ 61  ▒ 59  █ 60  ▓ 62  ▒ 64  ░ 63  
░ 68  ▓ 66  █ 65  █ 71  ▒ 67  ▓ 70  ░ 69  █ 72

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P0558R1 | C++11 | arithmetic permitted on pointers to (possibly cv-qualified) void or function | made ill-formed |

### See also

|  |  |
| --- | --- |
| fetch_add | atomically adds the argument to the value stored in the atomic object and obtains the value held previously   (public member function) |
| fetch_sub | atomically subtracts the argument from the value stored in the atomic object and obtains the value held previously   (public member function) |
| operator+=operator-= | adds to or subtracts from the atomic value   (public member function) |
| operator&=operator|=operator^= | performs bitwise AND, OR, XOR with the atomic value   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/atomic/atomic/operator_arith&oldid=171387>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 April 2024, at 19:17.