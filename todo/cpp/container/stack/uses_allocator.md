# std::uses_allocator<std::stack>

From cppreference.com
< cpp‎ | container‎ | stack
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

`std::stack`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| stack::stack | | | | |
| stack::~stack | | | | |
| stack::operator= | | | | |
| Element access | | | | |
| stack::top | | | | |
| Capacity | | | | |
| stack::empty | | | | |
| stack::size | | | | |
| Modifiers | | | | |
| stack::push | | | | |
| stack::push_range(C++23) | | | | |
| stack::emplace(C++11) | | | | |
| stack::pop | | | | |
| stack::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::stack)(C++11) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(C++20) | | | | |
| Helper classes | | | | |
| ****uses_allocator<std::stack>****(C++11) | | | | |
| formatter<std::stack>(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stack>` |  |  |
| template< class T, class Container, class Alloc >  struct uses_allocator<std::stack<T, Container>, Alloc> : std::uses_allocator<Container, Alloc>::type {}; |  | (since C++11) |
|  |  |  |

Provides a transparent specialization of the std::uses_allocator type trait for std::stack: the container adaptor uses allocator if and only if the underlying container does.

## Inherited from std::integral_constant

### Member constants

|  |  |
| --- | --- |
| value[static] | true   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| operator bool | converts the object to bool, returns value   (public member function) |
| operator()(C++14) | returns value   (public member function) |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `value_type` | bool |
| `type` | std::integral_constant<bool, value> |

### Example

Run this code

```
#include <memory>
#include <stack>
 
static_assert(
    std::uses_allocator<std::stack<int>, void>::value == false &&
    std::uses_allocator<std::stack<int>, std::allocator<int>>::value == true
);
 
int main() {}

```

### See also

|  |  |
| --- | --- |
| uses_allocator(C++11) | checks if the specified type supports uses-allocator construction   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/stack/uses_allocator&oldid=142342>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 August 2022, at 13:17.