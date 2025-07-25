# std::flat_multiset

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
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| ****flat_multiset****(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

****std::flat_multiset****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_multiset::flat_multiset | | | | | | flat_multiset::operator= | | | | | | Iterators | | | | | | flat_multiset::beginflat_multiset::cbegin | | | | | | flat_multiset::endflat_multiset::cend | | | | | | flat_multiset::rbeginflat_multiset::crbegin | | | | | | flat_multiset::rendflat_multiset::crend | | | | | | Capacity | | | | | | flat_multiset::size | | | | | | flat_multiset::max_size | | | | | | flat_multiset::empty | | | | | | Observers | | | | | | flat_multiset::key_comp | | | | | | flat_multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_multiset::clear | | | | | | flat_multiset::insert | | | | | | flat_multiset::insert_range | | | | | | flat_multiset::emplace | | | | | | flat_multiset::emplace_hint | | | | | | flat_multiset::erase | | | | | | flat_multiset::swap | | | | | | flat_multiset::extract | | | | | | flat_multiset::replace | | | | | | Lookup | | | | | | flat_multiset::count | | | | | | flat_multiset::find | | | | | | flat_multiset::contains | | | | | | flat_multiset::equal_range | | | | | | flat_multiset::lower_bound | | | | | | flat_multiset::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_multiset) | | | | | | erase_if(std::flat_multiset) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_multiset> | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<flat_set>` |  |  |
| template<  class Key,      class Compare = std::less<Key>,      class KeyContainer = std::vector<Key> > class flat_multiset; |  | (since C++23) |
|  |  |  |

The flat multiset is a container adaptor that gives the functionality of an associative container that stores a sorted set of objects of type `Key`. Unlike std::flat_set, multiple keys with equivalent values are allowed. Sorting is done using the key comparison function `Compare`.

The class template `flat_multiset` acts as a wrapper to the underlying sorted container passed as object of type `KeyContainer`.

Everywhere the standard library uses the Compare requirements, uniqueness is determined by using the equivalence relation. Informally, two objects a and b are considered equivalent if neither compares less than the other: !comp(a, b) && !comp(b, a).

`std::flat_multiset` meets the requirements of Container, ReversibleContainer, optional container requirements, and all requirements of AssociativeContainer (including logarithmic search complexity), except that:

- requirements related to nodes are not applicable,
- iterator invalidation requirements differ,
- the complexity of insertion and erasure operations is linear.

A flat multiset supports most AssociativeContainer's operations that use equal keys.

### Iterator invalidation

|  |  |
| --- | --- |
|  | This section is incomplete |

### Template parameters

|  |  |  |
| --- | --- | --- |
| Key | - | The type of the stored elements. The program is ill-formed if `Key` is not the same type as `KeyContainer::value_type`. |
| Compare | - | A Compare type providing a strict weak ordering. |
| KeyContainer | - | The type of the underlying SequenceContainer to store the elements. The iterators of such container should satisfy LegacyRandomAccessIterator or model `random_access_iterator`. The standard containers std::vector and std::deque satisfy these requirements. |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `container_type` | `Key``Container` |
| `key_type` | `Key` |
| `value_type` | `Key` |
| `key_compare` | `Compare` |
| `value_compare` | `Compare` |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `size_type` | typename KeyContainer::size_type |
| `difference_type` | typename KeyContainer::difference_type |
| `iterator` | implementation-defined LegacyRandomAccessIterator and `random_access_iterator` to `value_type` |
| `const_iterator` | implementation-defined LegacyRandomAccessIterator and `random_access_iterator` to const value_type |
| `reverse_iterator` | std::reverse_iterator<iterator> |
| `const_reverse_iterator` | std::reverse_iterator<const_iterator> |

### Member objects

|  |  |
| --- | --- |
| Member | Description |
| `container_type` `c` (private) | the adapted container (exposition-only member object\*) |
| `key_compare` `compare` (private) | the comparison function object (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `flat_multiset`   (public member function) |
| (destructor)(implicitly declared) | destroys every element of the container adaptor   (public member function) |
| operator= | assigns values to the container adaptor   (public member function) |
| Iterators | |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend | returns an iterator to the end   (public member function) |
| rbegincrbegin | returns a reverse iterator to the beginning   (public member function) |
| rendcrend | returns a reverse iterator to the end   (public member function) |
| Capacity | |
| empty | checks whether the container adaptor is empty   (public member function) |
| size | returns the number of elements   (public member function) |
| max_size | returns the maximum possible number of elements   (public member function) |
| Modifiers | |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| insert | inserts elements   (public member function) |
| insert_range | inserts a range of elements   (public member function) |
| extract | extracts the underlying container   (public member function) |
| replace | replaces the underlying container   (public member function) |
| erase | erases elements   (public member function) |
| swap | swaps the contents   (public member function) |
| clear | clears the contents   (public member function) |
| Lookup | |
| find | finds element with specific key   (public member function) |
| count | returns the number of elements matching specific key   (public member function) |
| contains | checks if the container contains element with specific key   (public member function) |
| lower_bound | returns an iterator to the first element **not less** than the given key   (public member function) |
| upper_bound | returns an iterator to the first element **greater** than the given key   (public member function) |
| equal_range | returns range of elements matching a specific key   (public member function) |
| Observers | |
| key_comp | returns the function that compares keys   (public member function) |
| value_comp | returns the function that compares keys in objects of type `value_type`   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<=>(C++23) | lexicographically compares the values of two `flat_multiset`s   (function template) |
| std::swap(std::flat_multiset)(C++23) | specializes the std::swap algorithm   (function template) |
| erase_if(std::flat_multiset)(C++23) | erases all elements satisfying specific criteria   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::uses_allocator<std::flat_multiset>(C++23) | specializes the std::uses_allocator type trait   (class template specialization) |

### Tags

|  |  |
| --- | --- |
| sorted_equivalentsorted_equivalent_t(C++23) | indicates that elements of a range are sorted (uniqueness is not required) (tag) |

### Deduction guides

### Notes

The member types `iterator` and `const_iterator` may be aliases to the same type. This means defining a pair of function overloads using the two types as parameter types may violate the One Definition Rule. Since `iterator` is convertible to `const_iterator`, a single function with a `const_iterator` as parameter type will work instead.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_flat_set` | `202207L` | (C++23) | std::flat_set and `std::flat_multiset` |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| flat_set(C++23) | adapts a container to provide a collection of unique keys, sorted by keys   (class template) |
| multiset | collection of keys, sorted by keys   (class template) |
| unordered_multiset(C++11) | collection of keys, hashed by keys   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_multiset&oldid=177442>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 14:53.