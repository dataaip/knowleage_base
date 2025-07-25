# std::queue<T,Container>::operator=

From cppreference.com
< cpp‎ | container‎ | queue
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

`std::queue`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| queue::queue | | | | |
| queue::~queue | | | | |
| ****queue::operator=**** | | | | |
| Element access | | | | |
| queue::front | | | | |
| queue::back | | | | |
| Capacity | | | | |
| queue::empty | | | | |
| queue::size | | | | |
| Modifiers | | | | |
| queue::push | | | | |
| queue::push_range(C++23) | | | | |
| queue::emplace(C++11) | | | | |
| queue::pop | | | | |
| queue::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::queue)(C++11) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(C++20) | | | | |
| Helper classes | | | | |
| uses_allocator<std::queue>(C++11) | | | | |
| formatter<std::queue>(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| queue& operator=( const queue& other ); | (1) | (implicitly declared) |
| queue& operator=( queue&& other ); | (2) | (since C++11)  (implicitly declared) |
|  |  |  |

Replaces the contents of the container adaptor with the contents of given argument.

1) Copy assignment operator. Replaces the contents with a copy of the contents of other. Effectively calls c = other.c;.2) Move assignment operator. Replaces the contents with those of other using move semantics. Effectively calls c = std::move(other.c);.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another container adaptor to be used as source |

### Return value

\*this

### Complexity

1,2) Equivalent to that of operator= of the underlying
container.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs the `queue`   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/queue/operator%3D&oldid=135383>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2021, at 07:12.