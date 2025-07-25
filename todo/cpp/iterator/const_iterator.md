# std::basic_const_iterator

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator | | | | | | make_reverse_iterator(C++14) | | | | | | move_iterator(C++11) | | | | | | make_move_iterator(C++11) | | | | | | default_sentinel_tdefault_sentinel(C++20)(C++20) | | | | | | unreachable_sentinel_tunreachable_sentinel(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | front_insert_iterator | | | | | | back_insert_iterator | | | | | | inserter | | | | | | insert_iterator | | | | | | front_inserter | | | | | | back_inserter | | | | | | move_sentinel(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator(C++20) | | | | | | counted_iterator(C++20) | | | | | | ****basic_const_iterator****(C++23) | | | | | | ****const_iterator****(C++23) | | | | | | ****const_sentinel****(C++23) | | | | | | ****make_const_iterator****(C++23) | | | | | | ****make_const_sentinel****(C++23) | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

****std::basic_const_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_const_iterator::basic_const_iterator | | | | |
| basic_const_iterator::base | | | | |
| basic_const_iterator::operator\*basic_const_iterator::operator-> | | | | |
| [basic_const_iterator::operator[]](basic_const_iterator/operator_at.html "cpp/iterator/basic const iterator/operator at") | | | | |
| basic_const_iterator::operator++basic_const_iterator::operator+=basic_const_iterator::operator--basic_const_iterator::operator-= | | | | |
| basic_const_iterator::operator==basic_const_iterator::operator<basic_const_iterator::operator<=basic_const_iterator::operator>basic_const_iterator::operator>=basic_const_iterator::operator<=> | | | | |
| basic_const_iterator::operator **constant-iterator** | | | | |
| Non-member functions | | | | |
| operator<operator<=operator>operator>=(C++23)(C++23)(C++23)(C++23) | | | | |
| operator+(C++23) | | | | |
| operator-(C++23) | | | | |
| iter_move(std::basic_const_iterator)(C++23) | | | | |
| Helper classes | | | | |
| common_type<std::basic_const_iterator>(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iterator>` |  |  |
| template< std::input_iterator Iter >  class basic_const_iterator; |  | (since C++23) |
|  |  |  |

`std::basic_const_iterator` is an iterator adaptor which behaves exactly like the underlying iterator (which must be at least an LegacyInputIterator or model `input_iterator`), except that dereferencing converts the value returned by the underlying iterator as immutable. Specializations of `std::basic_const_iterator` are constant iterators, that is, the iterator can never be used as an output iterator because modifying elements is not allowed.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `iterator_category` (conditionally present) | If `Iter` models `forward_iterator`:   - member `iterator_category` is the same type as std::iterator_traits<Iter>::iterator_category.   Otherwise, there is no member `iterator_category`. |
| `iterator_concept` | - std::contiguous_iterator_tag, if `Iter` models `contiguous_iterator`; - std::random_access_iterator_tag, if `Iter` models `random_access_iterator`; - std::bidirectional_iterator_tag, if `Iter` models `bidirectional_iterator`; - std::forward_iterator_tag, if `Iter` models `forward_iterator`; - std::input_iterator_tag otherwise. |
| `value_type` | std::iter_value_t<Iter> |
| `difference_type` | std::iter_difference_t<Iter> |
| `reference` (private) | std::iter_const_reference_t<Iter> (exposition-only member type\*) |

### Member objects

|  |  |
| --- | --- |
| Member name | Definition |
| `current` (private) | the underlying iterator from which `base()` copies or moves (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new iterator adaptor   (public member function) |
| base | accesses the underlying iterator   (public member function) |
| operator\*operator-> | accesses the pointed-to element   (public member function) |
| [operator[]](basic_const_iterator/operator_at.html "cpp/iterator/basic const iterator/operator at") | accesses an element by index   (public member function) |
| operator++operator++(int)operator+=operator--operator--(int)operator-= | advances or decrements the iterator   (public member function) |
| operator **constant-iterator** | converts into any constant iterator to which an underlying iterator can be convertible   (public member function) |
| operator==operator<operator>operator<=operator>=operator<=> | compares the underlying iterators   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator<operator>operator<=operator>=operator<=>(C++23) | compares `basic_const_iterator` with non-`basic_const_iterator`   (function template) |
| operator+operator-(C++23) | advances or decrements the iterator   (function template) |
| operator-(C++23) | computes the distance between two iterator adaptors   (function template) |
| iter_move(C++23) | casts the result of dereferencing the underlying iterator to its associated rvalue reference type   (function) |

### Helper classes

|  |  |
| --- | --- |
| std::common_type<std::basic_const_iterator>(C++23) | determines the common type of an iterator and an adapted `basic_const_iterator` type   (class template specialization) |

### Helper alias templates

|  |  |  |
| --- | --- | --- |
| template< std::input_iterator I >  using const_iterator = /\* see description \*/; |  | (since C++23) |
|  |  |  |

If `I` models `constant-iterator` (an exposition-only concept), then const_iterator<I> denotes a type `I`. Otherwise, basic_const_iterator<I>.

|  |  |  |
| --- | --- | --- |
| template< std::semiregular S >  using const_sentinel = /\* see description \*/; |  | (since C++23) |
|  |  |  |

If `S` models `input_iterator`, then const_sentinel<S> denotes a type const_iterator<S>. Otherwise, `S`.

### Helper function templates

|  |  |  |
| --- | --- | --- |
| template< std::input_iterator T >  constexpr const_iterator<T> make_const_iterator( I it ) { return it; } |  | (since C++23) |
| template< std::semiregular S >  constexpr const_sentinel<S> make_const_sentinel( S s ) { return s; } |  | (since C++23) |
|  |  |  |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_as_const` | `202207L` | (C++23) | `std::basic_const_iterator` |
| `202311L` | (C++23) (DR) | `std::basic_const_iterator` should follow its underlying type's convertibility |

### Example

Run this code

```
#include <cassert>
#include <iterator>
#include <vector>
 
int main()
{
    std::vector v{1, 2, 3};
    std::vector<int>::iterator i = v.begin();
    *i = 4;   // OK, v[0] == 4 now
    i[1] = 4; // OK, the same as *(i + 1) = 4;
 
    auto ci = std::make_const_iterator(i);
    assert(*ci == 4);   // OK, can read the underlying object
    assert(ci[0] == 4); // OK, ditto
    // *ci = 13;        // Error: location is read-only
    // ci[0] = 13;      // Error: ditto
    ci.base()[0] = 42;  // OK, underlying iterator is writable
    assert(*ci == 42);  // OK, underlying location v[0] was modified
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2836R1 | C++23 | `basic_const_iterator` doesn't follow its underlying type's convertibility | conversion operator provided |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/basic_const_iterator&oldid=175482>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 August 2024, at 19:26.