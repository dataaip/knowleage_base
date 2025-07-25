# deduction guides for `std::flat_map`

From cppreference.com
< cpp‎ | container‎ | flat map
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

std::flat_map

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_map::flat_map | | | | | | flat_map::operator= | | | | | | Element access | | | | | | flat_map::at | | | | | | [flat_map::operator[]](operator_at.html "cpp/container/flat map/operator at") | | | | | | Iterators | | | | | | flat_map::beginflat_map::cbegin | | | | | | flat_map::endflat_map::cend | | | | | | flat_map::rbeginflat_map::crbegin | | | | | | flat_map::rendflat_map::crend | | | | | | Lookup | | | | | | flat_map::count | | | | | | flat_map::find | | | | | | flat_map::contains | | | | | | flat_map::equal_range | | | | | | flat_map::lower_bound | | | | | | flat_map::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | flat_map::size | | | | | | flat_map::max_size | | | | | | flat_map::empty | | | | | | Modifiers | | | | | | flat_map::clear | | | | | | flat_map::erase | | | | | | flat_map::swap | | | | | | flat_map::emplace | | | | | | flat_map::extract | | | | | | flat_map::replace | | | | | | flat_map::insert | | | | | | flat_map::insert_range | | | | | | flat_map::insert_or_assign | | | | | | flat_map::emplace_hint | | | | | | flat_map::try_emplace | | | | | | Observers | | | | | | flat_map::key_comp | | | | | | flat_map::keys | | | | | | flat_map::value_comp | | | | | | flat_map::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_map) | | | | | | erase_if(std::flat_map) | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_map> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| ****Deduction guides**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<flat_map>` |  |  |
| template< class KeyContainer, class MappedContainer,  class Compare = std::less<typename KeyContainer::value_type> >  flat_map( KeyContainer, MappedContainer, Compare = Compare() )      -> flat_map<typename KeyContainer::value_type,                  typename MappedContainer::value_type,                 Compare, KeyContainer, MappedContainer>; | (1) | (since C++23) |
| template< class KeyContainer, class MappedContainer, class Allocator >  flat_map( KeyContainer, MappedContainer, Allocator )      -> flat_map<typename KeyContainer::value_type,                  typename MappedContainer::value_type,                  std::less<typename KeyContainer::value_type>,                 KeyContainer, MappedContainer>; | (2) | (since C++23) |
| template< class KeyContainer, class MappedContainer,  class Compare, class Allocator >  flat_map( KeyContainer, MappedContainer, Compare, Allocator )      -> flat_map<typename KeyContainer::value_type,                  typename MappedContainer::value_type,                 Compare, KeyContainer, MappedContainer>; | (3) | (since C++23) |
| template< class KeyContainer, class MappedContainer,  class Compare = std::less<typename KeyContainer::value_type> >  flat_map( std::sorted_unique_t, KeyContainer, MappedContainer,            Compare = Compare() )      -> flat_map<typename KeyContainer::value_type,                  typename MappedContainer::value_type,                 Compare, KeyContainer, MappedContainer>; | (4) | (since C++23) |
| template< class KeyContainer, class MappedContainer, class Allocator >  flat_map( std::sorted_unique_t, KeyContainer, MappedContainer,            Allocator )      -> flat_map<typename KeyContainer::value_type,                  typename MappedContainer::value_type,                  std::less<typename KeyContainer::value_type>,                 KeyContainer, MappedContainer>; | (5) | (since C++23) |
| template< class KeyContainer, class MappedContainer,  class Compare, class Allocator>  flat_map( std::sorted_unique_t, KeyContainer, MappedContainer,            Compare, Allocator )      -> flat_map<typename KeyContainer::value_type,                  typename MappedContainer::value_type,                 Compare, KeyContainer, MappedContainer>; | (6) | (since C++23) |
| template< class InputIter,  class Compare = std::less</\*iter-key-type\*/<InputIter>> >  flat_map( InputIter, InputIter, Compare = Compare() )      -> flat_map</\*iter-key-type\*/<InputIter>, /\*iter-mapped-type\*/<InputIter>, Compare>; | (7) | (since C++23) |
| template< class InputIter,  class Compare = std::less</\*iter-key-type\*/<InputIter>> >  flat_map( std::sorted_unique_t, InputIter, InputIter,            Compare = Compare() )      -> flat_map</\*iter-key-type\*/<InputIter>, /\*iter-mapped-type\*/<InputIter>, Compare>; | (8) | (since C++23) |
| template< ranges::input_range R,  class Compare = std::less</\*range-key-type\*/<R>>,            class Allocator = allocator<byte> >  flat_map( std::from_range_t, R&&, Compare = Compare(),            Allocator = Allocator() )      -> flat_map</\*range-key-type\*/<R>, /\*range-mapped-type\*/<R>, Compare,                  std::vector</\*range-key-type\*/<R>,                              /\*alloc-rebind\*/<Allocator,                                               /\*range-key-type\*/<R>>>,                  std::vector</\*range-mapped-type\*/<R>,                              /\*alloc-rebind\*/<Allocator, /\*range-mapped-type\*/<R>>>>; | (9) | (since C++23) |
| template< ranges::input_range R, class Allocator >  flat_map( std::from_range_t, R&&, Allocator )      -> flat_map</\*range-key-type\*/<R>, /\*range-mapped-type\*/<R>,                  std::less</\*range-key-type\*/<R>>,                  std::vector</\*range-key-type\*/<R>,                              /\*alloc-rebind\*/<Allocator,                                               /\*range-key-type\*/<R>>>,                  std::vector</\*range-mapped-type\*/<R>,                              /\*alloc-rebind\*/<Allocator, /\*range-mapped-type\*/<R>>>>; | (10) | (since C++23) |
| template< class Key, class T, class Compare = std::less<Key> >  flat_map( std::initializer_list<pair<Key, T>>, Compare = Compare() ) -> flat_map<Key, T, Compare>; | (11) | (since C++23) |
| template< class Key, class T, class Compare = std::less<Key> >  flat_map( std::sorted_unique_t, std::initializer_list<pair<Key, T>>,            Compare = Compare() ) -> flat_map<Key, T, Compare>; | (12) | (since C++23) |
|  |  |  |

These deduction guides are provided for  to allow deduction from:

1) A key-container, a mapped-container and a comparator.2) A key-container, a mapped-container and an allocator.3) A key-container, a mapped-container, a comparator and an allocator.4) The std::sorted_unique_t tag, a key-container, a mapped-container and a comparator.5) The std::sorted_unique_t tag, a key-container, a mapped-container and an allocator.6) The std::sorted_unique_t tag, a key-container, a mapped-container, a comparator and an allocator.7) An iterator range and a comparator.8) The std::sorted_unique_t tag, an iterator range and a comparator.9) The std::from_range_t tag, an `input_range` range, a comparator and an allocator.10) The std::from_range_t tag, an `input_range` range and an allocator.11) The std::initializer_list and a comparator.12) The std::sorted_unique_t tag, the std::initializer_list and a comparator.

These overloads participate in overload resolution only if `InputIt` satisfies LegacyInputIterator, `Alloc` satisfies Allocator, and `Comp` does not satisfy Allocator.

Note: the extent to which the library determines that a type does not satisfy LegacyInputIterator is unspecified, except that as a minimum integral types do not qualify as input iterators. Likewise, the extent to which it determines that a type does not satisfy Allocator is unspecified, except that as a minimum the member type `Alloc::value_type` must exist and the expression std::declval<Alloc&>().allocate(std::size_t{}) must be well-formed when treated as an unevaluated operand.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_map/deduction_guides&oldid=171813>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 May 2024, at 18:08.