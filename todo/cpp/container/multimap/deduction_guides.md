# deduction guides for `std::multimap`

From cppreference.com
< cpp‎ | container‎ | multimap
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

std::multimap

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multimap::multimap | | | | | | multimap::~multimap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multimap::operator= | | | | | | multimap::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multimap::beginmultimap::cbegin(C++11) | | | | | | multimap::endmultimap::cend(C++11) | | | | | | multimap::rbeginmultimap::crbegin(C++11) | | | | | | multimap::rendmultimap::crend(C++11) | | | | | | Capacity | | | | | | multimap::size | | | | | | multimap::max_size | | | | | | multimap::empty | | | | | | Observers | | | | | | multimap::key_comp | | | | | | multimap::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multimap::clear | | | | | | multimap::insert | | | | | | multimap::erase | | | | | | multimap::swap | | | | | | multimap::merge(C++17) | | | | | | multimap::insert_range(C++23) | | | | | | multimap::emplace(C++11) | | | | | | multimap::emplace_hint(C++11) | | | | | | multimap::extract(C++17) | | | | | | Lookup | | | | | | multimap::count | | | | | | multimap::find | | | | | | multimap::contains(C++20) | | | | | | multimap::equal_range | | | | | | multimap::lower_bound | | | | | | multimap::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::multimap) | | | | | | erase_if(std::multimap)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| ****Deduction guides****(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<map>` |  |  |
| template< class InputIt,  class Comp = std::less<iter_key_t<InputIt>>,            class Alloc = std::allocator<iter_to_alloc_t<InputIt>> >  multimap( InputIt, InputIt, Comp = Comp(), Alloc = Alloc() ) -> multimap<iter_key_t<InputIt>, iter_val_t<InputIt>, Comp, Alloc>; | (1) | (since C++17) |
| template< class Key,  class T,            class Comp = std::less<Key>,            class Alloc = std::allocator<std::pair<const Key, T>> >  multimap( std::initializer_list<std::pair<Key, T>>, Comp = Comp(), Alloc = Alloc() ) -> multimap<Key, T, Comp, Alloc>; | (2) | (since C++17) |
| template< class InputIt, class Alloc >  multimap( InputIt, InputIt, Alloc )      -> multimap<iter_key_t<InputIt>, iter_val_t<InputIt>, std::less<iter_key_t<InputIt>>, Alloc>; | (3) | (since C++17) |
| template< class Key, class T, class Alloc >  multimap( std::initializer_list<std::pair<Key, T>>, Alloc ) -> multimap<Key, T, std::less<Key>, Alloc>; | (4) | (since C++17) |
| template< ranges::input_range R, class Compare = std::less<range_key_t<R>,  class Alloc = std::allocator<range_to_alloc_t<R>> >  multimap( std::from_range_t, R&&, Compare = Compare(), Alloc = Alloc() ) -> multimap<range_key_t<R>, range_mapped_t<R>, Compare, Alloc>; | (5) | (since C++23) |
| template< ranges::input_range R, class Alloc >  multimap( std::from_range_t, R&&, Alloc ) -> multimap<range_key_t<R>, range_mapped_t<R>, std::less<range_key_t<R>>, Alloc>; | (6) | (since C++23) |
| Exposition-only helper type aliases |  |  |
| template< class InputIter >  using iter_val_t = typename std::iterator_traits<InputIter>::value_type; |  | (exposition only\*) |
| template< class InputIter >  using iter_key_t = std::remove_const_t< std::tuple_element_t<0, iter_val_t<InputIter>>>; |  | (exposition only\*) |
| template< class InputIter >  using iter_mapped_t = std::tuple_element_t<1, iter_val_t<InputIter>>; |  | (exposition only\*) |
| template< class InputIter >  using iter_to_alloc_t =      std::pair<std::add_const_t<tuple_element_t<0, iter_val_t<InputIter>>>, std::tuple_element_t<1, iter_val_t<InputIter>>>; |  | (exposition only\*) |
| template< ranges::input_range Range >  using range_key_t = std::remove_const_t<typename ranges::range_value_t<Range>::first_type>; |  | (since C++23)  (exposition only\*) |
| template< ranges::input_range Range >  using range_mapped_t = typename ranges::range_value_t<Range>::second_type; |  | (since C++23)  (exposition only\*) |
| template< ranges::input_range Range >  using range_to_alloc_t =      std::pair<std::add_const_t<typename ranges::range_value_t<Range>::first_type>, typename ranges::range_value_t<Range>::second_type>; |  | (since C++23)  (exposition only\*) |
|  |  |  |

1-4) These deduction guides are provided for `multimap` to allow deduction from an iterator range (overloads (1,3)) and std::initializer_list (overloads (2,4)).5,6) These deduction guides are provided for `multimap` to allow deduction from a std::from_range_t tag and an `input_range`.

These overloads participate in overload resolution only if `InputIt` satisfies LegacyInputIterator, `Alloc` satisfies Allocator, and `Comp` does not satisfy Allocator.

Note: the extent to which the library determines that a type does not satisfy LegacyInputIterator is unspecified, except that as a minimum integral types do not qualify as input iterators. Likewise, the extent to which it determines that a type does not satisfy Allocator is unspecified, except that as a minimum the member type `Alloc::value_type` must exist and the expression std::declval<Alloc&>().allocate(std::size_t{}) must be well-formed when treated as an unevaluated operand.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overload (5,6) |

### Example

Run this code

```
#include <map>
 
int main()
{
    // std::multimap m1 = {{"foo", 1}, {"bar", 2}};
        // Error: braced-init-list has no type; cannot deduce
        // pair<Key, T> from {"foo", 1} or {"bar", 2}
 
    std::multimap m1 = {std::pair{"foo", 2}, {"bar", 3}}; // guide #2
    std::multimap m2(m1.begin(), m1.end()); // guide #1
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3025 | C++17 | initializer-list guides take std::pair<const Key, T> | use std::pair<Key, T> |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multimap/deduction_guides&oldid=135729>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2021, at 07:44.