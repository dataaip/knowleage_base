# std::experimental::to_array

From cppreference.com
< cpp‎ | experimental
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::propagate_const | | | | |
| experimental::not_fn | | | | |
| experimental::observer_ptr | | | | |
| experimental::make_array | | | | |
| ****experimental::to_array**** | | | | |
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/array>` |  |  |
| template< class T, std::size_t N >  constexpr std::array<std::remove_cv_t<T>, N> to_array(T (&a)[N]); |  | (library fundamentals TS v2) |
|  |  |  |

Creates a std::array from the built-in array a. The elements of the std::array are copy-initialized from the corresponding element of a.

### Parameters

|  |  |  |
| --- | --- | --- |
| a | - | the built-in array to be used to initialize the std::array |

### Return value

An std::array object whose elements are copy-initialized from the corresponding element of a.

### Possible implementation

|  |
| --- |
| ```text namespace detail {     template<class T, std::size_t N, std::size_t... I>     constexpr std::array<std::remove_cv_t<T>, N>         to_array_impl(T (&a)[N], std::index_sequence<I...>)     {         return { {a[I]...} };     } }   template<class T, std::size_t N> constexpr std::array<std::remove_cv_t<T>, N> to_array(T (&a)[N]) {     return detail::to_array_impl(a, std::make_index_sequence<N>{}); } ``` |

### Example

Run this code

```
#include <cassert>
#include <cstdlib>
#include <experimental/array>
#include <unistd.h>
 
// mkstemp(3) that works
template<std::size_t N>
int tempfd(char const (&tmpl)[N])
{
    auto s = std::experimental::to_array(tmpl);
    int fd = mkstemp(s.data());
    if (fd != -1)
        unlink(s.data());
 
    return fd;
}
 
int main()
{
    int fd = tempfd("/tmp/test.XXXXXX");
    int rt = close(fd);
    assert(rt == 0);
}

```

### See also

|  |  |
| --- | --- |
| make_array(library fundamentals TS v2) | creates a std::array object whose size and optionally element type are deduced from the arguments   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/to_array&oldid=156340>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 August 2023, at 05:02.