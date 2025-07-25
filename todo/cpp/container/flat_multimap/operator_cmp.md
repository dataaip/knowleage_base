# operator==,<=>(std::flat_multimap)

From cppreference.com
< cpp‎ | container‎ | flat multimap
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

std::flat_multimap

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_multimap::flat_multimap | | | | | | flat_multimap::operator= | | | | | | Modifiers | | | | | | flat_multimap::clear | | | | | | flat_multimap::erase | | | | | | flat_multimap::swap | | | | | | flat_multimap::extract | | | | | | flat_multimap::replace | | | | | | flat_multimap::insert | | | | | | flat_multimap::insert_range | | | | | | flat_multimap::emplace | | | | | | flat_multimap::emplace_hint | | | | | | Lookup | | | | | | flat_multimap::count | | | | | | flat_multimap::find | | | | | | flat_multimap::contains | | | | | | flat_multimap::equal_range | | | | | | flat_multimap::lower_bound | | | | | | flat_multimap::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | flat_multimap::beginflat_multimap::cbegin | | | | | | flat_multimap::endflat_multimap::cend | | | | | | flat_multimap::rbeginflat_multimap::crbegin | | | | | | flat_multimap::rendflat_multimap::crend | | | | | | Capacity | | | | | | flat_multimap::size | | | | | | flat_multimap::max_size | | | | | | flat_multimap::empty | | | | | | Observers | | | | | | flat_multimap::key_comp | | | | | | flat_multimap::keys | | | | | | flat_multimap::value_comp | | | | | | flat_multimap::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_multimap) | | | | | | erase_if(std::flat_multimap) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator==operator<=>**** | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_multimap> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| friend bool operator==( const std::flat_multimap& lhs,                          const std::flat_multimap& rhs ); | (1) | (since C++23) |
| friend synth-three-way-result<value_type>      operator<=>( const std::flat_multimap& lhs, const std::flat_multimap& rhs ); | (2) | (since C++23) |
|  |  |  |

Compares the contents of the underlying containers of two container adaptors. The comparison is done by applying the corresponding operator to the underlying containers.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: For "flat" containers only: copy parts of Template:cpp/container/operator_cmp |

### Parameters

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| lhs, rhs | - | container adaptors whose contents to compare  |  |  | | --- | --- | |  | This section is incomplete Reason: Add named requirements to "flat" container inner types | |

### Return value

1) true if the corresponding comparison yields true, false otherwise.2) Result of three-way comparison on underlying containers.

### Complexity

1) Constant if lhs and rhs are of different size, otherwise linear in the size of the `flat_multimap`.2)
Linear in the size of the container.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_multimap/operator_cmp&oldid=169572>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2024, at 16:54.