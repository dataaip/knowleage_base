# std::unordered_multimap

From cppreference.com
< cpp‎ | container
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
| ****unordered_multimap****(C++11) | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multimap::unordered_multimap | | | | | | unordered_multimap::~unordered_multimap | | | | | | unordered_multimap::operator= | | | | | | unordered_multimap::get_allocator | | | | | | Iterators | | | | | | unordered_multimap::beginunordered_multimap::cbegin | | | | | | unordered_multimap::endunordered_multimap::cend | | | | | | Capacity | | | | | | unordered_multimap::size | | | | | | unordered_multimap::max_size | | | | | | unordered_multimap::empty | | | | | | Modifiers | | | | | | unordered_multimap::clear | | | | | | unordered_multimap::insert | | | | | | unordered_multimap::insert_range(C++23) | | | | | | unordered_multimap::emplace | | | | | | unordered_multimap::emplace_hint | | | | | | unordered_multimap::erase | | | | | | unordered_multimap::swap | | | | | | unordered_multimap::extract(C++17) | | | | | | unordered_multimap::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multimap::count | | | | | | unordered_multimap::find | | | | | | unordered_multimap::contains(C++20) | | | | | | unordered_multimap::equal_range | | | | | | Bucket interface | | | | | | unordered_multimap::begin(size_type)unordered_multimap::cbegin(size_type) | | | | | | unordered_multimap::end(size_type)unordered_multimap::cend(size_type) | | | | | | unordered_multimap::bucket_count | | | | | | unordered_multimap::max_bucket_count | | | | | | unordered_multimap::bucket_size | | | | | | unordered_multimap::bucket | | | | | | Hash policy | | | | | | unordered_multimap::load_factor | | | | | | unordered_multimap::max_load_factor | | | | | | unordered_multimap::rehash | | | | | | unordered_multimap::reserve | | | | | | Observers | | | | | | unordered_multimap::hash_function | | | | | | unordered_multimap::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multimap) | | | | | | erase_if(std::unordered_multimap)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<unordered_map>` |  |  |
| template<  class Key,      class T,      class Hash = std::hash<Key>,      class KeyEqual = std::equal_to<Key>,      class Allocator = std::allocator<std::pair<const Key, T>> > class unordered_multimap; | (1) | (since C++11) |
| namespace pmr {  template<          class Key,          class T,          class Hash = std::hash<Key>,          class Pred = std::equal_to<Key>      > using unordered_multimap =            std::unordered_multimap<Key, T, Hash, Pred,                std::pmr::polymorphic_allocator<std::pair<const Key, T>>>; } | (2) | (since C++17) |
|  |  |  |

`std::unordered_multimap` is an unordered associative container that supports equivalent keys (an unordered_multimap may contain multiple copies of each key value) and that associates values of another type with the keys. The unordered_multimap class supports forward iterators. Search, insertion, and removal have average constant-time complexity.

Internally, the elements are not sorted in any particular order, but organized into buckets. Which bucket an element is placed into depends entirely on the hash of its key. This allows fast access to individual elements, since once the hash is computed, it refers to the exact bucket the element is placed into.

The iteration order of this container is not required to be stable (so, for example, std::equal cannot be used to compare two `std::unordered_multimap`s), except that every group of elements whose keys compare **equivalent** (compare equal with key_eq() as the comparator) forms a contiguous subrange in the iteration order, also accessible with equal_range().

`std::unordered_multimap` meets the requirements of Container, AllocatorAwareContainer, UnorderedAssociativeContainer.

### Template parameters

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Add descriptions of the template parameters. |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `key_type` | `Key` |
| `mapped_type` | `T` |
| `value_type` | std::pair<const Key, T> |
| `size_type` | Unsigned integer type (usually std::size_t) |
| `difference_type` | Signed integer type (usually std::ptrdiff_t) |
| `hasher` | `Hash` |
| `key_equal` | `KeyEqual` |
| `allocator_type` | `Allocator` |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `pointer` | std::allocator_traits<Allocator>::pointer |
| `const_pointer` | std::allocator_traits<Allocator>::const_pointer |
| `iterator` | LegacyForwardIterator to `value_type` |
| `const_iterator` | LegacyForwardIterator to const value_type |
| `local_iterator` | An iterator type whose category, value, difference, pointer and reference types are the same as `iterator`. This iterator can be used to iterate through a single bucket but not across buckets |
| `const_local_iterator` | An iterator type whose category, value, difference, pointer and reference types are the same as `const_iterator`. This iterator can be used to iterate through a single bucket but not across buckets |
| `node_type` (since C++17) | a specialization of node handle representing a container node |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `unordered_multimap`   (public member function) |
| (destructor) | destructs the `unordered_multimap`   (public member function) |
| operator= | assigns values to the container   (public member function) |
| get_allocator | returns the associated allocator   (public member function) |
| Iterators | |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend | returns an iterator to the end   (public member function) |
| Capacity | |
| empty | checks whether the container is empty   (public member function) |
| size | returns the number of elements   (public member function) |
| max_size | returns the maximum possible number of elements   (public member function) |
| Modifiers | |
| clear | clears the contents   (public member function) |
| insert | inserts elements or nodes(since C++17)   (public member function) |
| insert_range(C++23) | inserts a range of elements   (public member function) |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| erase | erases elements   (public member function) |
| swap | swaps the contents   (public member function) |
| extract(C++17) | extracts nodes from the container   (public member function) |
| merge(C++17) | splices nodes from another container   (public member function) |
| Lookup | |
| count | returns the number of elements matching specific key   (public member function) |
| find | finds element with specific key   (public member function) |
| contains(C++20) | checks if the container contains element with specific key   (public member function) |
| equal_range | returns range of elements matching a specific key   (public member function) |
| Bucket interface | |
| begin(size_type)cbegin(size_type) | returns an iterator to the beginning of the specified bucket   (public member function) |
| end(size_type)cend(size_type) | returns an iterator to the end of the specified bucket   (public member function) |
| bucket_count | returns the number of buckets   (public member function) |
| max_bucket_count | returns the maximum number of buckets   (public member function) |
| bucket_size | returns the number of elements in specific bucket   (public member function) |
| bucket | returns the bucket for specific key   (public member function) |
| Hash policy | |
| load_factor | returns average number of elements per bucket   (public member function) |
| max_load_factor | manages maximum average number of elements per bucket   (public member function) |
| rehash | reserves at least the specified number of buckets and regenerates the hash table   (public member function) |
| reserve | reserves space for at least the specified number of elements and regenerates the hash table   (public member function) |
| Observers | |
| hash_function | returns function used to hash the keys   (public member function) |
| key_eq | returns the function used to compare keys for equality   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the values in the unordered_multimap   (function template) |
| std::swap(std::unordered_multimap)(C++11) | specializes the std::swap algorithm   (function template) |
| erase_if(std::unordered_multimap)(C++20) | erases all elements satisfying specific criteria   (function template) |

|  |  |
| --- | --- |
| Deduction guides | (since C++17) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges construction and insertion for containers |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2050 | C++11 | the definitions of `reference`, `const_reference`, `pointer` and `const_pointer` were based on `allocator_type` | based on `value_type` and std::allocator_traits |

### See also

|  |  |
| --- | --- |
| unordered_map(C++11) | collection of key-value pairs, hashed by keys, keys are unique   (class template) |
| multimap | collection of key-value pairs, sorted by keys   (class template) |
| flat_multimap(C++23) | adapts two containers to provide a collection of key-value pairs, sorted by keys   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multimap&oldid=177452>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 15:46.