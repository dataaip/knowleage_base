# std::reverse_iterator

From cppreference.com
< cpp‎ | iterator
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

Iterator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_readable(C++20) | | | | | | indirectly_writable(C++20) | | | | | | weakly_incrementable(C++20) | | | | | | incrementable(C++20) | | | | | | **is-integer-like** **is-signed-integer-like**(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sentinel_for(C++20) | | | | | | sized_sentinel_for(C++20) | | | | | | input_iterator(C++20) | | | | | | output_iterator(C++20) | | | | | | input_or_output_iterator(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_iterator(C++20) | | | | | | bidirectional_iterator(C++20) | | | | | | random_access_iterator(C++20) | | | | | | contiguous_iterator(C++20) | | | | | |  | | | | | |  | | | | | |
| Iterator primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | indirectly_readable_traits(C++20) | | | | | |  | | | | | |  | | | | | |
| Algorithm concepts and utilities | | | | |
| Indirect callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_unary_invocableindirectly_regular_unary_invocable(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_unary_predicate(C++20) | | | | | | indirect_binary_predicate(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_equivalence_relation(C++20) | | | | | | indirect_strict_weak_order(C++20) | | | | | |
| Common algorithm requirements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_movable(C++20) | | | | | | indirectly_movable_storable(C++20) | | | | | | indirectly_copyable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_copyable_storable(C++20) | | | | | | indirectly_swappable(C++20) | | | | | | indirectly_comparable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | permutable(C++20) | | | | | | mergeable(C++20) | | | | | | sortable(C++20) | | | | | |
| Utilities | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_result_t(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected_value_t(C++26) | | | | | |
| Iterator adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****reverse_iterator**** | | | | | | make_reverse_iterator(C++14) | | | | | | move_iterator(C++11) | | | | | | make_move_iterator(C++11) | | | | | | default_sentinel_tdefault_sentinel(C++20)(C++20) | | | | | | unreachable_sentinel_tunreachable_sentinel(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | front_insert_iterator | | | | | | back_insert_iterator | | | | | | inserter | | | | | | insert_iterator | | | | | | front_inserter | | | | | | back_inserter | | | | | | move_sentinel(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator(C++20) | | | | | | counted_iterator(C++20) | | | | | | basic_const_iterator(C++23) | | | | | | const_iterator(C++23) | | | | | | const_sentinel(C++23) | | | | | | make_const_iterator(C++23) | | | | | | make_const_sentinel(C++23) | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

****std::reverse_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| reverse_iterator::reverse_iterator | | | | |
| reverse_iterator::operator= | | | | |
| reverse_iterator::base | | | | |
| reverse_iterator::operator\*reverse_iterator::operator-> | | | | |
| [reverse_iterator::operator[]](reverse_iterator/operator_at.html "cpp/iterator/reverse iterator/operator at") | | | | |
| reverse_iterator::operator++reverse_iterator::operator+reverse_iterator::operator+=reverse_iterator::operator--reverse_iterator::operator-reverse_iterator::operator-= | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | | | | |
| operator+ | | | | |
| operator- | | | | |
| iter_move(C++20) | | | | |
| iter_swap(C++20) | | | | |
| make_reverse_iterator(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iterator>` |  |  |
| template< class Iter >  class reverse_iterator; |  |  |
|  |  |  |

`std::reverse_iterator` is an iterator adaptor that reverses the direction of a given iterator, which must be at least a LegacyBidirectionalIterator or model `bidirectional_iterator`(since C++20). In other words, when provided with a bidirectional iterator, `std::reverse_iterator` produces a new iterator that moves from the end to the beginning of the sequence defined by the underlying bidirectional iterator.

For a reverse iterator r constructed from an iterator i, the relationship &\*r == &\*(i - 1) is always true (as long as r is dereferenceable); thus a reverse iterator constructed from a one-past-the-end iterator dereferences to the last element in a sequence.

This is the iterator returned by member functions `rbegin()` and `rend()` of the standard library containers.

!range-rbegin-rend.svg

### Nested types

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  | | --- | --- | | Type | Definition | | `iterator_type` | `Iter` | | `iterator_category` | std::iterator_traits<Iter>::iterator_category[[1]](reverse_iterator.html#cite_note-iterator-1) | | `value_type` | std::iterator_traits<Iter>::value_type[[1]](reverse_iterator.html#cite_note-iterator-1) | | `difference_type` | std::iterator_traits<Iter>::difference_type | | `pointer` | std::iterator_traits<Iter>::pointer | | `reference` | std::iterator_traits<Iter>::reference | | (until C++20) |
| |  |  | | --- | --- | | Type | Definition | | `iterator_type` | `Iter` | | `iterator_concept` | - std::random_access_iterator_tag if `Iter` models std::random_access_iterator - std::bidirectional_iterator_tag otherwise | | `iterator_category` | - std::random_access_iterator_tag if std::iterator_traits<Iter>::iterator_category models std::derived_from<std::random_access_iterator_tag> - std::iterator_traits<Iter>::iterator_category otherwise | | `value_type` | std::iter_value_t<Iter> | | `difference_type` | std::iter_difference_t<Iter> | | `pointer` | std::iterator_traits<Iter>::pointer | | `reference` | std::iter_reference_t<Iter> | | (since C++20) |

1. ↑ 1.0 1.1 The definition is provided by the base std::iterator specialization until C++17.

### Data members

|  |  |
| --- | --- |
| Member | Description |
| `Iter` `current` | the underlying iterator (protected member object) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new iterator adaptor   (public member function) |
| operator= | assigns another iterator adaptor   (public member function) |
| base | accesses the underlying iterator   (public member function) |
| operator\*operator-> | accesses the pointed-to element   (public member function) |
| [operator[]](reverse_iterator/operator_at.html "cpp/iterator/reverse iterator/operator at") | accesses an element by index   (public member function) |
| operator++operator++(int)operator+=operator+operator--operator--(int)operator-=operator- | advances or decrements the iterator   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | compares the underlying iterators   (function template) |
| operator+ | advances the iterator   (function template) |
| operator- | computes the distance between two iterator adaptors   (function template) |
| iter_move(C++20) | casts the result of dereferencing the adjusted underlying iterator to its associated rvalue reference type   (function) |
| iter_swap(C++20) | swaps the objects pointed to by two adjusted underlying iterators   (function template) |
| make_reverse_iterator(C++14) | creates a ****std::reverse_iterator**** of type inferred from the argument   (function template) |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class Iterator1, class Iterator2 >      requires (!std::sized_sentinel_for<Iterator1, Iterator2>)  inline constexpr bool disable_sized_sentinel_for <std::reverse_iterator<Iterator1>, std::reverse_iterator<Iterator2>> = true; |  | (since C++20) |
|  |  |  |

This partial specialization of `std::disable_sized_sentinel_for` prevents specializations of `reverse_iterator` from satisfying `sized_sentinel_for` if their underlying iterators do not satisfy the concept.

### Possible implementation

Below is a partial implementation focusing on the way the inner iterator is stored, calling std::prev only when the content is fetched via operator\*.

|  |
| --- |
| ```text template<class It> class reverse_iterator { protected:     It current = It(); public:     reverse_iterator() = default;     constexpr explicit reverse_iterator(It itr) : current(itr) {}     template<class U>         requires (!std::is_same_v<U, It> && std::convertible_to<const U&, It>)     constexpr explicit reverse_iterator(const U& other) : current(other.base()) {}       constexpr decltype(auto) operator*() const     {         return *std::prev(current); // <== returns the content of prev     }       constexpr reverse_iterator& operator++() { --current; return *this; }     constexpr reverse_iterator operator++(int) { auto tmp = *this; ++(*this); return tmp; }       constexpr reverse_iterator& operator--() { ++current; return *this; }     constexpr reverse_iterator operator--(int) { auto tmp = *this; --(*this); return tmp; }       constexpr It base() const { return current; }       // Other member functions, friend functions, and member typedefs are not shown here. }; ``` |

### Notes

`std::reverse_iterator` does not work with iterators whose dereference returns a reference to a member of \*this (so-called “stashing iterators”). An example of a stashing iterator is MSVC STL's std::filesystem::path::iterator.

### Example

Run this code

```
#include <cstddef>
#include <iostream>
#include <iterator>
 
template<typename T, std::size_t SIZE>
class Stack
{
    T arr[SIZE];
    std::size_t pos = 0;
public:
    T pop()
    {
        return arr[--pos];
    }
 
    Stack& push(const T& t)
    {
        arr[pos++] = t;
        return *this;
    }
 
    // we wish that looping on Stack would be in LIFO order
    // thus we use std::reverse_iterator as an adaptor to existing iterators
    // (which are in this case the simple pointers: arr, arr + pos)
    auto begin() { return std::reverse_iterator(arr + pos); }
    auto end() { return std::reverse_iterator(arr); }
};
 
int main()
{
    Stack<int, 8> s;
    s.push(5).push(15).push(25).push(35);
    for (int val : s)
        std::cout << val << ' ';
    std::cout << '\n';
}

```

Output:

```
35 25 15 5

```

### See also

|  |  |
| --- | --- |
| [make_reverse_iterator(C++14) | creates a ****std::reverse_iterator**** of type inferred from the argument   (function template) |
| iterator(deprecated in C++17) | base class to ease the definition of required types for simple iterators   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/reverse_iterator&oldid=177444>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 15:00.