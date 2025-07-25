# std::flat_multiset<Key,Compare,KeyContainer>::upper_bound

From cppreference.com
< cpp‎ | container‎ | flat multiset
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

std::flat_multiset

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_multiset::flat_multiset | | | | | | flat_multiset::operator= | | | | | | Iterators | | | | | | flat_multiset::beginflat_multiset::cbegin | | | | | | flat_multiset::endflat_multiset::cend | | | | | | flat_multiset::rbeginflat_multiset::crbegin | | | | | | flat_multiset::rendflat_multiset::crend | | | | | | Capacity | | | | | | flat_multiset::size | | | | | | flat_multiset::max_size | | | | | | flat_multiset::empty | | | | | | Observers | | | | | | flat_multiset::key_comp | | | | | | flat_multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_multiset::clear | | | | | | flat_multiset::insert | | | | | | flat_multiset::insert_range | | | | | | flat_multiset::emplace | | | | | | flat_multiset::emplace_hint | | | | | | flat_multiset::erase | | | | | | flat_multiset::swap | | | | | | flat_multiset::extract | | | | | | flat_multiset::replace | | | | | | Lookup | | | | | | flat_multiset::count | | | | | | flat_multiset::find | | | | | | flat_multiset::contains | | | | | | flat_multiset::equal_range | | | | | | flat_multiset::lower_bound | | | | | | ****flat_multiset::upper_bound**** | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_multiset) | | | | | | erase_if(std::flat_multiset) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_multiset> | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| iterator upper_bound( const Key& key ); | (1) | (since C++23) |
| const_iterator upper_bound( const Key& key ) const; | (2) | (since C++23) |
| template< class K >  iterator upper_bound( const K& x ); | (3) | (since C++23) |
| template< class K >  const_iterator upper_bound( const K& x ) const; | (4) | (since C++23) |
|  |  |  |

1,2) Returns an iterator pointing to the first element that is **greater** than key.3,4) Returns an iterator pointing to the first element that compares **greater** to the value x. This overload participates in overload resolution only if the qualified-id Compare::is_transparent is valid and denotes a type. It allows calling this function without constructing an instance of `Key`.

### Parameters

|  |  |  |
| --- | --- | --- |
| key | - | key value to compare the elements to |
| x | - | alternative value that can be compared to `Key` |

### Return value

Iterator pointing to the first element that is **greater** than key. If no such element is found, past-the-end (see end()) iterator is returned.

### Complexity

Logarithmic in the size of the container.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| equal_range | returns range of elements matching a specific key   (public member function) |
| lower_bound | returns an iterator to the first element **not less** than the given key   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_multiset/upper_bound&oldid=169454>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 January 2024, at 06:53.