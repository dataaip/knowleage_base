# deduction guides for `std::flat_set`

From cppreference.com
< cpp‎ | container‎ | flat set
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

std::flat_set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_set::flat_set | | | | | | flat_set::operator= | | | | | | Iterators | | | | | | flat_set::beginflat_set::cbegin | | | | | | flat_set::endflat_set::cend | | | | | | flat_set::rbeginflat_set::crbegin | | | | | | flat_set::rendflat_set::crend | | | | | | Capacity | | | | | | flat_set::size | | | | | | flat_set::max_size | | | | | | flat_set::empty | | | | | | Observers | | | | | | flat_set::key_comp | | | | | | flat_set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_set::clear | | | | | | flat_set::insert | | | | | | flat_set::insert_range | | | | | | flat_set::emplace | | | | | | flat_set::emplace_hint | | | | | | flat_set::erase | | | | | | flat_set::swap | | | | | | flat_set::extract | | | | | | flat_set::replace | | | | | | Lookup | | | | | | flat_set::count | | | | | | flat_set::find | | | | | | flat_set::contains | | | | | | flat_set::equal_range | | | | | | flat_set::lower_bound | | | | | | flat_set::upper_bound | | | | | | | Non-member functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_set) | | | | | | erase_if(std::flat_set) | | | | | | |
| Helper classes | | | | |
| uses_allocator<std::flat_set> | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| ****Deduction guides**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<flat_set>` |  |  |
| template< class KeyContainer,  class Compare = std::less<typename KeyContainer::value_type> >  flat_set( KeyContainer, Compare = Compare() ) -> flat_set<typename KeyContainer::value_type, Compare, KeyContainer>; | (1) | (since C++23) |
| template< class KeyContainer, class Allocator >  flat_set( KeyContainer, Allocator )      -> flat_set<typename KeyContainer::value_type, std::less<typename KeyContainer::value_type>, KeyContainer>; | (2) | (since C++23) |
| template< class KeyContainer, class Compare, class Allocator >  flat_set( KeyContainer, Compare, Allocator ) -> flat_set<typename KeyContainer::value_type, Compare, KeyContainer>; | (3) | (since C++23) |
| template< class KeyContainer,  class Compare = std::less<typename KeyContainer::value_type> >  flat_set( std::sorted_unique_t, KeyContainer, Compare = Compare() ) -> flat_set<typename KeyContainer::value_type, Compare, KeyContainer>; | (4) | (since C++23) |
| template< class KeyContainer, class Allocator >  flat_set( std::sorted_unique_t, KeyContainer, Allocator )      -> flat_set<typename KeyContainer::value_type, std::less<typename KeyContainer::value_type>, KeyContainer>; | (5) | (since C++23) |
| template< class KeyContainer, class Compare, class Allocator >  flat_set( std::sorted_unique_t, KeyContainer, Compare, Allocator ) -> flat_set<typename KeyContainer::value_type, Compare, KeyContainer>; | (6) | (since C++23) |
| template< class InputIter,  class Compare = std::less</\*iter-value-type\*/<InputIter>> >  flat_set( InputIter, InputIter, Compare = Compare() ) -> flat_set</\*iter-value-type\*/<InputIter>, Compare>; | (7) | (since C++23) |
| template< class InputIter,  class Compare = std::less</\*iter-value-type\*/<InputIter>> >  flat_set( std::sorted_unique_t, InputIter, InputIter, Compare = Compare() ) -> flat_set</\*iter-value-type\*/<InputIter>, Compare>; | (8) | (since C++23) |
| template< ranges::input_range R,  class Compare = std::less<ranges::range_value_t<R>>,            class Allocator = std::allocator<ranges::range_value_t<R>> >  flat_set( std::from_range_t, R&&, Compare = Compare(), Allocator = Allocator() )      -> flat_set<ranges::range_value_t<R>, Compare,                  std::vector<ranges::range_value_t<R>, /\*alloc-rebind\*/<Allocator, ranges::range_value_t<R>>>>; | (9) | (since C++23) |
| template< ranges::input_range R, class Allocator >  flat_set( std::from_range_t, R&&, Allocator )      -> flat_set<ranges::range_value_t<R>, std::less<ranges::range_value_t<R>>,                  std::vector<ranges::range_value_t<R>, /\*alloc-rebind\*/<Allocator, ranges::range_value_t<R>>>>; | (10) | (since C++23) |
| template< class Key, class Compare = std::less<Key> >  flat_set( std::initializer_list<Key>, Compare = Compare() ) -> flat_set<Key, Compare>; | (11) | (since C++23) |
| template< class Key, class Compare = std::less<Key> >  flat_set( std::sorted_unique_t,                 std::initializer_list<Key>, Compare = Compare() ) -> flat_set<Key, Compare>; | (12) | (since C++23) |
|  |  |  |

These deduction guides are provided for  to allow deduction from:

1) A container and a comparator.2) A container and an allocator.3) A container, a comparator and an allocator.4) The std::sorted_unique_t tag, a container and a comparator.5) The std::sorted_unique_t tag, a container and an allocator.6) The std::sorted_unique_t tag, a container, a comparator and an allocator.7) An iterator range and a comparator.8) The std::sorted_unique_t tag, an iterator range and a comparator.9) The std::from_range_t tag, an `input_range` range, a comparator and an allocator.10) The std::from_range_t tag, an `input_range` range and an allocator.11) The std::initializer_list and a comparator.12) The std::sorted_unique_t tag, the std::initializer_list and a comparator.

These overloads participate in overload resolution only if `InputIt` satisfies LegacyInputIterator, `Alloc` satisfies Allocator, and `Comp` does not satisfy Allocator.

Note: the extent to which the library determines that a type does not satisfy LegacyInputIterator is unspecified, except that as a minimum integral types do not qualify as input iterators. Likewise, the extent to which it determines that a type does not satisfy Allocator is unspecified, except that as a minimum the member type `Alloc::value_type` must exist and the expression std::declval<Alloc&>().allocate(std::size_t{}) must be well-formed when treated as an unevaluated operand.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_set/deduction_guides&oldid=171808>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 May 2024, at 16:25.