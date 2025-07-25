# std::span<T,Extent>::rend, std::span<T,Extent>::crend

From cppreference.com
< cpp‎ | container‎ | span
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

std::span

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| span::span | | | | |
| span::operator= | | | | |
| Element access | | | | |
| span::front | | | | |
| span::back | | | | |
| span::at(C++26) | | | | |
| [span::operator[]](operator_at.html "cpp/container/span/operator at") | | | | |
| span::data | | | | |
| Iterators | | | | |
| span::beginspan::cbegin(C++23) | | | | |
| span::endspan::cend(C++23) | | | | |
| span::rbeginspan::crbegin(C++23) | | | | |
| ****span::rendspan::crend****(C++23) | | | | |
| Observers | | | | |
| span::empty | | | | |
| span::size | | | | |
| span::size_bytes | | | | |
| Subviews | | | | |
| span::first | | | | |
| span::last | | | | |
| span::subspan | | | | |
| Non-member functions | | | | |
| as_bytesas_writable_bytes | | | | |
| Non-member constant | | | | |
| dynamic_extent | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr reverse_iterator rend() const noexcept; | (1) | (since C++20) |
| constexpr const_reverse_iterator crend() const noexcept; | (2) | (since C++23) |
|  |  |  |

Returns a reverse iterator to the element following the last element of the reversed `span`. It corresponds to the element preceding the first element of the non-reversed `span`. This element acts as a placeholder, attempting to access it results in undefined behavior.

!range-rbegin-rend.svg

### Parameters

(none)

### Return value

Reverse iterator to the element following the last element.

### Complexity

Constant.

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <span>
#include <string_view>
 
void ascending(const std::span<const std::string_view> data,
               const std::string_view term)
{
    std::for_each(data.begin(), data.end(),
        [](const std::string_view x) { std::cout << x << ' '; });
    std::cout << term;
}
 
void descending(const std::span<const std::string_view> data,
                const std::string_view term)
{
    std::for_each(data.rbegin(), data.rend(),
        [](const std::string_view x) { std::cout << x << ' '; });
    std::cout << term;
}
 
int main()
{
    constexpr std::string_view bars[]{"▁","▂","▃","▄","▅","▆","▇","█"};
    ascending(bars, " ");
    descending(bars, "\n");
}

```

Output:

```
▁ ▂ ▃ ▄ ▅ ▆ ▇ █  █ ▇ ▆ ▅ ▄ ▃ ▂ ▁

```

### See also

|  |  |
| --- | --- |
| rbegincrbegin(C++23) | returns a reverse iterator to the beginning   (public member function) |
| rendcrend(C++14) | returns a reverse end iterator for a container or array   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/span/rend&oldid=135420>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2021, at 12:10.