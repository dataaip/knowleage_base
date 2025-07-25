# std::priority_queue<T,Container,Compare>::empty

From cppreference.com
< cpp‎ | container‎ | priority queue
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

`std::priority_queue`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| priority_queue::priority_queue | | | | |
| priority_queue::~priority_queue | | | | |
| priority_queue::operator= | | | | |
| Element access | | | | |
| priority_queue::top | | | | |
| Capacity | | | | |
| ****priority_queue::empty**** | | | | |
| priority_queue::size | | | | |
| Modifiers | | | | |
| priority_queue::push | | | | |
| priority_queue::push_range(C++23) | | | | |
| priority_queue::emplace(C++11) | | | | |
| priority_queue::pop | | | | |
| priority_queue::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::priority_queue)(C++11) | | | | |
| Helper classes | | | | |
| uses_allocator<std::priority_queue>(C++11) | | | | |
| formatter<std::priority_queue>(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| bool empty() const; |  |  |
|  |  |  |

Checks if the underlying container has no elements. Equivalent to: return`c`.empty().

### Parameters

(none)

### Return value

true if the underlying container is empty, false otherwise.

### Complexity

Constant.

### Example

Run this code

```
#include <cassert>
#include <queue>
 
int main()
{
    std::priority_queue<int> queue;
    assert(queue.empty());
 
    queue.push(42);
    assert(!queue.empty());
 
    queue.pop();
    assert(queue.empty());
}

```

### See also

|  |  |
| --- | --- |
| size | returns the number of elements   (public member function) |
| empty(C++17) | checks whether the container is empty   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/priority_queue/empty&oldid=133060>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 August 2021, at 10:52.