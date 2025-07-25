# std::coroutine_traits

From cppreference.com
< cpp‎ | coroutine
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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

Coroutine support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Coroutine traits | | | | |
| ****coroutine_traits****(C++20) | | | | |
| Coroutine handle | | | | |
| coroutine_handle(C++20) | | | | |
| No-op coroutines | | | | |
| noop_coroutine_promise(C++20) | | | | |
| noop_coroutine(C++20) | | | | |
| Trivial awaitables | | | | |
| suspend_never(C++20) | | | | |
| suspend_always(C++20) | | | | |
| Range generators | | | | |
| generator(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<coroutine>` |  |  |
| template< class R, class... Args >  struct coroutine_traits; |  | (since C++20) |
|  |  |  |

Determines the promise type from the return type and parameter types of a coroutine. The standard library implementation provides a publicly accessible member type `promise_type` same as `R::promise_type` if the qualified-id is valid and denotes a type. Otherwise, it has no such member.

Program-defined specializations of `coroutine_traits` must define a publicly accessible nested type `promise_type`, otherwise the program is ill-formed.

### Template parameters

|  |  |  |
| --- | --- | --- |
| R | - | return type of the coroutine |
| Args | - | parameter types of the coroutine, including the implicit object parameter if the coroutine is a non-static member function |

### Nested types

|  |  |
| --- | --- |
| Name | Definition |
| `promise_type` | `R::promise_type` if it is valid, or provided by program-defined specializations |

### Possible implementation

|  |
| --- |
| ```text namespace detail { template<class, class...> struct coroutine_traits_base {};   template<class R, class... Args> requires requires { typename R::promise_type; } struct coroutine_traits_base <R, Args...> {     using promise_type = R::promise_type; }; }   template<class R, class... Args> struct coroutine_traits : detail::coroutine_traits_base<R, Args...> {}; ``` |

### Notes

If the coroutine is a non-static member function, then the first type in `Args...` is the type of the implicit object parameter, and the rest are parameter types of the function (if any).

If `std::coroutine_traits<R, Args...>::promise_type` does not exist or is not a class type, the corresponding coroutine definition is ill-formed.

Users may define explicit or partial specializations of `coroutine_traits` dependent on program-defined types to avoid modification to return types.

### Example

Run this code

```
#include <chrono>
#include <coroutine>
#include <exception>
#include <future>
#include <iostream>
#include <thread>
#include <type_traits>
 
// A program-defined type on which the coroutine_traits specializations below depend
struct as_coroutine {};
 
// Enable the use of std::future<T> as a coroutine type
// by using a std::promise<T> as the promise type.
template<typename T, typename... Args>
    requires(!std::is_void_v<T> && !std::is_reference_v<T>)
struct std::coroutine_traits<std::future<T>, as_coroutine, Args...>
{
    struct promise_type : std::promise<T>
    {
        std::future<T> get_return_object() noexcept
        {
            return this->get_future();
        }
 
        std::suspend_never initial_suspend() const noexcept { return {}; }
        std::suspend_never final_suspend() const noexcept { return {}; }
 
        void return_value(const T& value)
            noexcept(std::is_nothrow_copy_constructible_v<T>)
        {
            this->set_value(value);
        }
 
        void return_value(T&& value) noexcept(std::is_nothrow_move_constructible_v<T>)
        {
            this->set_value(std::move(value));
        }
 
        void unhandled_exception() noexcept
        {
            this->set_exception(std::current_exception());
        }
    };
};
 
// Same for std::future<void>.
template<typename... Args>
struct std::coroutine_traits<std::future<void>, as_coroutine, Args...>
{
    struct promise_type : std::promise<void>
    {
        std::future<void> get_return_object() noexcept
        {
            return this->get_future();
        }
 
        std::suspend_never initial_suspend() const noexcept { return {}; }
        std::suspend_never final_suspend() const noexcept { return {}; }
 
        void return_void() noexcept
        {
            this->set_value();
        }
 
        void unhandled_exception() noexcept
        {
            this->set_exception(std::current_exception());
        }
    };
};
 
// Allow co_await'ing std::future<T> and std::future<void>
// by naively spawning a new thread for each co_await.
template<typename T>
auto operator co_await(std::future<T> future) noexcept
    requires(!std::is_reference_v<T>)
{
    struct awaiter : std::future<T>
    {
        bool await_ready() const noexcept
        {
            using namespace std::chrono_literals;
            return this->wait_for(0s) != std::future_status::timeout;
        }
 
        void await_suspend(std::coroutine_handle<> cont) const
        {
            std::thread([this, cont]
            {
                this->wait();
                cont();
            }).detach();
        }
 
        T await_resume() { return this->get(); }
    };
 
    return awaiter { std::move(future) };
}
 
// Utilize the infrastructure we have established.
std::future<int> compute(as_coroutine)
{
    int a = co_await std::async([] { return 6; });
    int b = co_await std::async([] { return 7; });
    co_return a * b;
}
 
std::future<void> fail(as_coroutine)
{
    throw std::runtime_error("bleah");
    co_return;
}
 
int main()
{
    std::cout << compute({}).get() << '\n';
 
    try
    {
        fail({}).get();
    }
    catch (const std::runtime_error& e)
    {
        std::cout << "error: " << e.what() << '\n';
    }
}

```

Output:

```
42
error: bleah

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/coroutine/coroutine_traits&oldid=170251>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 March 2024, at 05:17.