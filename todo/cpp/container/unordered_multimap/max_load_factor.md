# std::unordered_multimap<Key,T,Hash,KeyEqual,Allocator>::max_load_factor

From cppreference.com
< cpp‎ | container‎ | unordered multimap
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

`std::unordered_multimap`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multimap::unordered_multimap | | | | | | unordered_multimap::~unordered_multimap | | | | | | unordered_multimap::operator= | | | | | | unordered_multimap::get_allocator | | | | | | Iterators | | | | | | unordered_multimap::beginunordered_multimap::cbegin | | | | | | unordered_multimap::endunordered_multimap::cend | | | | | | Capacity | | | | | | unordered_multimap::size | | | | | | unordered_multimap::max_size | | | | | | unordered_multimap::empty | | | | | | Modifiers | | | | | | unordered_multimap::clear | | | | | | unordered_multimap::insert | | | | | | unordered_multimap::insert_range(C++23) | | | | | | unordered_multimap::emplace | | | | | | unordered_multimap::emplace_hint | | | | | | unordered_multimap::erase | | | | | | unordered_multimap::swap | | | | | | unordered_multimap::extract(C++17) | | | | | | unordered_multimap::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multimap::count | | | | | | unordered_multimap::find | | | | | | unordered_multimap::contains(C++20) | | | | | | unordered_multimap::equal_range | | | | | | Bucket interface | | | | | | unordered_multimap::begin(size_type)unordered_multimap::cbegin(size_type) | | | | | | unordered_multimap::end(size_type)unordered_multimap::cend(size_type) | | | | | | unordered_multimap::bucket_count | | | | | | unordered_multimap::max_bucket_count | | | | | | unordered_multimap::bucket_size | | | | | | unordered_multimap::bucket | | | | | | Hash policy | | | | | | unordered_multimap::load_factor | | | | | | ****unordered_multimap::max_load_factor**** | | | | | | unordered_multimap::rehash | | | | | | unordered_multimap::reserve | | | | | | Observers | | | | | | unordered_multimap::hash_function | | | | | | unordered_multimap::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multimap) | | | | | | erase_if(std::unordered_multimap)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| float max_load_factor() const; | (1) | (since C++11) |
| void max_load_factor( float ml ); | (2) | (since C++11) |
|  |  |  |

Manages the maximum load factor (number of elements per bucket). The container automatically increases the number of buckets if the load factor exceeds this threshold.

1) Returns current maximum load factor.2) Sets the maximum load factor to ml.

### Parameters

|  |  |  |
| --- | --- | --- |
| ml | - | new maximum load factor setting |

### Return value

1) Current maximum load factor.2) (none)

### Complexity

Constant.

### See also

|  |  |
| --- | --- |
| load_factor | returns average number of elements per bucket   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multimap/max_load_factor&oldid=136080>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 December 2021, at 10:57.