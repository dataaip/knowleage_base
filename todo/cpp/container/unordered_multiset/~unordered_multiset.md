# std::unordered_multiset<Key,Hash,KeyEqual,Allocator>::~unordered_multiset

From cppreference.com
< cpp‎ | container‎ | unordered multiset
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

`std::unordered_multiset`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multiset::unordered_multiset | | | | | | ****unordered_multiset::~unordered_multiset**** | | | | | | unordered_multiset::operator= | | | | | | unordered_multiset::get_allocator | | | | | | Iterators | | | | | | unordered_multiset::beginunordered_multiset::cbegin | | | | | | unordered_multiset::endunordered_multiset::cend | | | | | | Capacity | | | | | | unordered_multiset::size | | | | | | unordered_multiset::max_size | | | | | | unordered_multiset::empty | | | | | | Modifiers | | | | | | unordered_multiset::clear | | | | | | unordered_multiset::insert | | | | | | unordered_multiset::insert_range(C++23) | | | | | | unordered_multiset::emplace | | | | | | unordered_multiset::emplace_hint | | | | | | unordered_multiset::erase | | | | | | unordered_multiset::swap | | | | | | unordered_multiset::extract(C++17) | | | | | | unordered_multiset::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multiset::count | | | | | | unordered_multiset::find | | | | | | unordered_multiset::contains(C++20) | | | | | | unordered_multiset::equal_range | | | | | | Bucket interface | | | | | | unordered_multiset::begin(size_type)unordered_multiset::cbegin(size_type) | | | | | | unordered_multiset::end(size_type)unordered_multiset::cend(size_type) | | | | | | unordered_multiset::bucket_count | | | | | | unordered_multiset::max_bucket_count | | | | | | unordered_multiset::bucket_size | | | | | | unordered_multiset::bucket | | | | | | Hash policy | | | | | | unordered_multiset::load_factor | | | | | | unordered_multiset::max_load_factor | | | | | | unordered_multiset::rehash | | | | | | unordered_multiset::reserve | | | | | | Observers | | | | | | unordered_multiset::hash_function | | | | | | unordered_multiset::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multiset) | | | | | | erase_if(std::unordered_multiset)(C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| ~unordered_multiset(); |  | (since C++11) |
|  |  |  |

A destructor.
Destructs the `unordered_multiset`. The destructors of the elements are called and the used storage is deallocated. Note, that if the elements are pointers, the pointed-to objects are not destroyed.

### Complexity

Linear in the size of the `unordered_multiset`.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multiset/%7Eunordered_multiset&oldid=135866>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 07:33.