# operator==,!=(std::unordered_multimap)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multimap::unordered_multimap | | | | | | unordered_multimap::~unordered_multimap | | | | | | unordered_multimap::operator= | | | | | | unordered_multimap::get_allocator | | | | | | Iterators | | | | | | unordered_multimap::beginunordered_multimap::cbegin | | | | | | unordered_multimap::endunordered_multimap::cend | | | | | | Capacity | | | | | | unordered_multimap::size | | | | | | unordered_multimap::max_size | | | | | | unordered_multimap::empty | | | | | | Modifiers | | | | | | unordered_multimap::clear | | | | | | unordered_multimap::insert | | | | | | unordered_multimap::insert_range(C++23) | | | | | | unordered_multimap::emplace | | | | | | unordered_multimap::emplace_hint | | | | | | unordered_multimap::erase | | | | | | unordered_multimap::swap | | | | | | unordered_multimap::extract(C++17) | | | | | | unordered_multimap::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multimap::count | | | | | | unordered_multimap::find | | | | | | unordered_multimap::contains(C++20) | | | | | | unordered_multimap::equal_range | | | | | | Bucket interface | | | | | | unordered_multimap::begin(size_type)unordered_multimap::cbegin(size_type) | | | | | | unordered_multimap::end(size_type)unordered_multimap::cend(size_type) | | | | | | unordered_multimap::bucket_count | | | | | | unordered_multimap::max_bucket_count | | | | | | unordered_multimap::bucket_size | | | | | | unordered_multimap::bucket | | | | | | Hash policy | | | | | | unordered_multimap::load_factor | | | | | | unordered_multimap::max_load_factor | | | | | | unordered_multimap::rehash | | | | | | unordered_multimap::reserve | | | | | | Observers | | | | | | unordered_multimap::hash_function | | | | | | unordered_multimap::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multimap) | | | | | | erase_if(std::unordered_multimap)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator==operator!=****(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< class Key, class T, class Hash, class KeyEqual, class Alloc >  bool operator==( const std::unordered_multimap<Key, T, Hash, KeyEqual, Alloc>& lhs, const std::unordered_multimap<Key, T, Hash, KeyEqual, Alloc>& rhs ); | (1) |  |
| template< class Key, class T, class Hash, class KeyEqual, class Alloc >  bool operator!=( const std::unordered_multimap<Key, T, Hash, KeyEqual, Alloc>& lhs, const std::unordered_multimap<Key, T, Hash, KeyEqual, Alloc>& rhs ); | (2) | (until C++20) |
|  |  |  |

Compares the contents of two unordered containers.

The contents of two unordered containers lhs and rhs are equal if the following conditions hold:

- lhs.size() == rhs.size().
- each group of equivalent elements ``lhs_eq1`,`lhs_eq2`)` obtained from lhs.equal_range(lhs_eq1) has a corresponding group of equivalent elements in the other container `[`rhs_eq1`,`rhs_eq2`)` obtained from rhs.equal_range(rhs_eq1), that has the following properties:

:   - [std::distance(lhs_eq1, lhs_eq2) == std::distance(rhs_eq1, rhs_eq2).
    - std::is_permutation(lhs_eq1, lhs_eq2, rhs_eq1) == true.

The behavior is undefined if `Key` or `T` are not EqualityComparable.

The behavior is also undefined if `hash_function()` and `key_eq()` do(until C++20)`key_eq()` does(since C++20) not have the same behavior on lhs and rhs or if operator== for `Key` is not a refinement of the partition into equivalent-key groups introduced by `key_eq()` (that is, if two elements that compare equal using operator== fall into different partitions).

|  |  |
| --- | --- |
| The `!=` operator is synthesized from `operator==`. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | unordered containers to compare |

### Return value

1) true if the contents of the containers are equal, false otherwise.2) true if the contents of the containers are not equal, false otherwise.

### Complexity

Proportional to **ΣSi2** calls to operator== on `value_type`, calls to the predicate returned by `key_eq`, and calls to the hasher returned by `hash_function` in the average case, where **S** is the size of the **i**th equivalent key group. Proportional to **N2** in the worst case, where **N** is the size of the container. Average case becomes proportional to **N** if the elements within each equivalent key group are arranged in the same order (happens when the containers are copies of each other).

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multimap/operator_cmp&oldid=136084>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 December 2021, at 10:57.