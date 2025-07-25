# std::istreambuf_iterator

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator | | | | | | make_reverse_iterator(C++14) | | | | | | move_iterator(C++11) | | | | | | make_move_iterator(C++11) | | | | | | default_sentinel_tdefault_sentinel(C++20)(C++20) | | | | | | unreachable_sentinel_tunreachable_sentinel(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | front_insert_iterator | | | | | | back_insert_iterator | | | | | | inserter | | | | | | insert_iterator | | | | | | front_inserter | | | | | | back_inserter | | | | | | move_sentinel(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator(C++20) | | | | | | counted_iterator(C++20) | | | | | | basic_const_iterator(C++23) | | | | | | const_iterator(C++23) | | | | | | const_sentinel(C++23) | | | | | | make_const_iterator(C++23) | | | | | | make_const_sentinel(C++23) | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****istreambuf_iterator**** | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

****std::istreambuf_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| istreambuf_iterator::istreambuf_iterator | | | | |
| istreambuf_iterator::operator\* | | | | |
| istreambuf_iterator::operator++istreambuf_iterator::operator++(int) | | | | |
| istreambuf_iterator::equal | | | | |
| Non-member functions | | | | |
| operator==operator!=(until C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iterator>` |  |  |
|  |  |  |
| --- | --- | --- |
| template< class CharT, class Traits = std::char_traits<CharT> >  class istreambuf_iterator      : public std::iterator<std::input_iterator_tag,                             CharT, typename Traits::off_type, /\* unspecified \*/, CharT> |  | (until C++17) |
| template< class CharT, class Traits = std::char_traits<CharT> >  class istreambuf_iterator; |  | (since C++17) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

`std::istreambuf_iterator` is a single-pass input iterator that reads successive characters from the std::basic_streambuf object for which it was constructed.

The default-constructed `std::istreambuf_iterator` is known as the **end-of-stream** iterator. When a `std::istreambuf_iterator` reaches the end of the underlying stream, it becomes equal to the end-of-stream iterator. Dereferencing or incrementing it further invokes undefined behavior.

|  |  |
| --- | --- |
| `std::istreambuf_iterator` has a trivial copy constructor, a constexpr default constructor, and a trivial destructor. | (since C++11) |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `iterator_category` | std::input_iterator_tag |
| `value_type` | CharT |
| `difference_type` | typename Traits::off_type |
| `pointer` | /\* unspecified \*/ |
| `reference` | CharT |
| `char_type` | `CharT` |
| `traits_type` | `Traits` |
| `int_type` | typename Traits::int_type |
| `streambuf_type` | std::basic_streambuf<CharT, Traits> |
| `istream_type` | std::basic_istream<CharT, Traits> |
| `/* proxy */` | Implementation-defined class type. A `proxy` object holds a `char_type` character and a `streambuf_type*` pointer. Dereferencing a `proxy` object with `operator*` yields the stored character. (exposition-only member type\*) |

|  |  |
| --- | --- |
| Member types `iterator_category`, `value_type`, `difference_type`, `pointer` and `reference` are required to be obtained by inheriting from std::iterator<std::input_iterator_tag, CharT, typename Traits::off_type, /\* unspecified \*/, CharT>. | (until C++17) |

The member type `pointer` is usually `CharT*` (see below).

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `istreambuf_iterator`   (public member function) |
| (destructor)(implicitly declared) | destructs an `istreambuf_iterator`   (public member function) |
| operator\* | obtains a copy of the current character   (public member function) |
| operator++operator++(int) | advances the iterator   (public member function) |
| equal | tests if both `istreambuf_iterator`s are end-of-stream or if both are valid   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=(removed in C++20) | compares two `istreambuf_iterator`s   (function template) |

### Notes

The resolution of LWG issue 659 introduced operator->. It is expected that given an `std::istreambuf_iterator` i, the expressions (\*i).m and i->m have the same effect.

However, the resolution does not provide a formal specification of its behavior. Thus it is implemented differently, including returning nullptr, returning the address of a temporary, or does even provide the member at all. Its intended behavior can hardly be achieved, and it is removed by the resolution of LWG issue 2790.

The resolution of LWG issue 659 also made the member type `pointer` unspecified in order to allow `operator->` to return a proxy. This is to allow `operator->` to compile when `CharT` is not a class type.

### Example

Run this code

```
#include <iostream>
#include <iterator>
#include <sstream>
#include <string>
 
int main()
{
    // typical use case: an input stream represented as a pair of iterators
    std::istringstream in{"Hello, world"};
    std::istreambuf_iterator<char> it{in}, end;
    std::string ss{it, end};
    std::cout << "ss has " << ss.size() << " bytes; "
                 "it holds \"" << ss << "\"\n";
 
    // demonstration of the single-pass nature
    std::istringstream s{"abc"};
    std::istreambuf_iterator<char> i1{s}, i2{s};
    std::cout << "i1 returns '" << *i1 << "'\n"
                 "i2 returns '" << *i2 << "'\n";
 
    ++i1;
    std::cout << "after incrementing i1, but not i2:\n"
                 "i1 returns '" << *i1 << "'\n"
                 "i2 returns '" << *i2 << "'\n";
 
    ++i2;
    std::cout << "after incrementing i2, but not i1:\n"
                 "i1 returns '" << *i1 << "'\n"
                 "i2 returns '" << *i2 << "'\n";
}

```

Output:

```
ss has 12 bytes; it holds "Hello, world"
i1 returns 'a'
i2 returns 'a'
after incrementing i1, but not i2:
i1 returns 'b'
i2 returns 'b'
after incrementing i2, but not i1:
i1 returns 'c'
i2 returns 'c'

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 659 | C++98 | 1. `std::istreambuf_iterator` did not have operator-> 2. the member type `pointer` was specified as `CharT*` | 1. added 2. made unspecified |
| LWG 2790 | C++98 | the operator-> added by LWG issue 659 was not useful | removed |

### See also

|  |  |
| --- | --- |
| ostreambuf_iterator | output iterator that writes to std::basic_streambuf   (class template) |
| istream_iterator | input iterator that reads from std::basic_istream   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/istreambuf_iterator&oldid=179750>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 January 2025, at 17:14.