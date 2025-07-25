# std::coroutine_handle, std::noop_coroutine_handle

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
| coroutine_traits(C++20) | | | | |
| Coroutine handle | | | | |
| ****coroutine_handle****(C++20) | | | | |
| No-op coroutines | | | | |
| noop_coroutine_promise(C++20) | | | | |
| noop_coroutine(C++20) | | | | |
| Trivial awaitables | | | | |
| suspend_never(C++20) | | | | |
| suspend_always(C++20) | | | | |
| Range generators | | | | |
| generator(C++23) | | | | |

****std::coroutine_handle****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| coroutine_handle::coroutine_handle | | | | |
| coroutine_handle::operator= | | | | |
| coroutine_handle::from_promise | | | | |
| Conversion | | | | |
| coroutine_handle::operator coroutine_handle<> | | | | |
| Observers | | | | |
| coroutine_handle::done | | | | |
| coroutine_handle::operator bool | | | | |
| Control | | | | |
| coroutine_handle::operator()coroutine_handle::resume | | | | |
| coroutine_handle::destroy | | | | |
| Promise access | | | | |
| coroutine_handle::promise | | | | |
| Export/import | | | | |
| coroutine_handle::address | | | | |
| coroutine_handle::from_address | | | | |
| Non-member functions | | | | |
| operator==operator<=> | | | | |
| Helper classes | | | | |
| hash<std::coroutine_handle> | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<coroutine>` |  |  |
| template< class Promise = void >  struct coroutine_handle; | (1) | (since C++20) |
| template<>  struct coroutine_handle<void>; | (2) | (since C++20) |
| template<>  struct coroutine_handle<std::noop_coroutine_promise>; | (3) | (since C++20) |
| using noop_coroutine_handle =      std::coroutine_handle<std::noop_coroutine_promise>; | (4) | (since C++20) |
|  |  |  |

The class template `coroutine_handle` can be used to refer to a suspended or executing coroutine. Every specialization of `coroutine_handle` is a LiteralType.

1) Primary template, can be created from the promise object of type `Promise`.2) Specialization std::coroutine_handle<void> erases the promise type. It is convertible from other specializations.3) Specialization std::coroutine_handle<std::noop_coroutine_promise> refers to no-op coroutines. It cannot be created from a promise object.

On typical implementations, every specialization of `std::coroutine_handle` is TriviallyCopyable.

If the program adds specializations for `std::coroutine_handle`, the behavior is undefined.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `ptr` (private) | A pointer void\* to the coroutine state. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `coroutine_handle` object   (public member function) |
| operator= | assigns the `coroutine_handle` object   (public member function) |
| Conversion | |
| operator coroutine_handle<> | obtains a type-erased `coroutine_handle`   (public member function) |
| Observers | |
| done | checks if the coroutine has completed   (public member function) |
| operator bool | checks if the handle represents a coroutine   (public member function) |
| Control | |
| operator()resume | resumes execution of the coroutine   (public member function) |
| destroy | destroys a coroutine   (public member function) |
| Promise Access | |
| promise | access the promise of a coroutine   (public member function) |
| from_promise[static] | creates a `coroutine_handle` from the promise object of a coroutine   (public static member function) |
| Export/Import | |
| address | exports the underlying address, i.e. the pointer backing the coroutine   (public member function) |
| from_address[static] | imports a coroutine from a pointer   (public static member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<=>(C++20) | compares two `coroutine_handle` objects   (function) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::coroutine_handle>(C++20) | hash support for ****std::coroutine_handle****   (class template specialization) |

### Notes

A `coroutine_handle` may be dangling, in which case the `coroutine_handle` must be used carefully in order to avoid undefined behavior.

### Example

Run this code

```
#include <coroutine>
#include <iostream>
#include <optional>
 
template<std::movable T>
class Generator
{
public:
    struct promise_type
    {
        Generator<T> get_return_object()
        {
            return Generator{Handle::from_promise(*this)};
        }
        static std::suspend_always initial_suspend() noexcept
        {
            return {};
        }
        static std::suspend_always final_suspend() noexcept
        {
            return {};
        }
        std::suspend_always yield_value(T value) noexcept
        {
            current_value = std::move(value);
            return {};
        }
        // Disallow co_await in generator coroutines.
        void await_transform() = delete;
        [[noreturn]]
        static void unhandled_exception() { throw; }
 
        std::optional<T> current_value;
    };
 
    using Handle = std::coroutine_handle<promise_type>;
 
    explicit Generator(const Handle coroutine) :
        m_coroutine{coroutine}
    {}
 
    Generator() = default;
    ~Generator()
    {
        if (m_coroutine)
            m_coroutine.destroy();
    }
 
    Generator(const Generator&) = delete;
    Generator& operator=(const Generator&) = delete;
 
    Generator(Generator&& other) noexcept :
        m_coroutine{other.m_coroutine}
    {
        other.m_coroutine = {};
    }
    Generator& operator=(Generator&& other) noexcept
    {
        if (this != &other)
        {
            if (m_coroutine)
                m_coroutine.destroy();
            m_coroutine = other.m_coroutine;
            other.m_coroutine = {};
        }
        return *this;
    }
 
    // Range-based for loop support.
    class Iter
    {
    public:
        void operator++()
        {
            m_coroutine.resume();
        }
        const T& operator*() const
        {
            return *m_coroutine.promise().current_value;
        }
        bool operator==(std::default_sentinel_t) const
        {
            return !m_coroutine || m_coroutine.done();
        }
 
        explicit Iter(const Handle coroutine) :
            m_coroutine{coroutine}
        {}
 
    private:
        Handle m_coroutine;
    };
 
    Iter begin()
    {
        if (m_coroutine)
            m_coroutine.resume();
        return Iter{m_coroutine};
    }
 
    std::default_sentinel_t end() { return {}; }
 
private:
    Handle m_coroutine;
};
 
template<std::integral T>
Generator<T> range(T first, const T last)
{
    while (first < last)
        co_yield first++;
}
 
int main()
{
    for (const char i : range(65, 91))
        std::cout << i << ' ';
    std::cout << '\n';
}

```

Output:

```
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3460 | C++20 | the public base class of `coroutine_handle` could leave it in an undesired state | inheritance removed |

### See also

|  |  |
| --- | --- |
| generator(C++23) | A `view` that represents synchronous coroutine generator   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/coroutine/coroutine_handle&oldid=156820>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 August 2023, at 06:27.