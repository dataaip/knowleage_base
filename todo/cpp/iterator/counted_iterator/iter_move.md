# iter_move(std::counted_iterator)

From cppreference.com
< cpp‎ | iterator‎ | counted iterator
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

std::counted_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| counted_iterator::counted_iterator | | | | |
| counted_iterator::operator= | | | | |
| counted_iterator::base | | | | |
| counted_iterator::count | | | | |
| counted_iterator::operator\*counted_iterator::operator-> | | | | |
| [counted_iterator::operator[]](operator_at.html "cpp/iterator/counted iterator/operator at") | | | | |
| counted_iterator::operator++counted_iterator::operator++(int)counted_iterator::operator+counted_iterator::operator+=counted_iterator::operator--counted_iterator::operator--(int)counted_iterator::operator-counted_iterator::operator-= | | | | |
| Non-member functions | | | | |
| operator==operator<=>(C++20)(C++20) | | | | |
| operator==(default_sentinel_t)(C++20) | | | | |
| operator+(C++20) | | | | |
| operator-(C++20) | | | | |
| operator-(default_sentinel_t)(C++20) | | | | |
| ****iter_move****(C++20) | | | | |
| iter_swap(C++20) | | | | |
| Helper classes | | | | |
| iterator_traits<std::counted_iterator>(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| friend constexpr decltype(auto) iter_move( const std::counted_iterator& i )  noexcept(noexcept(ranges::iter_move(i.base())))         requires std::input_iterator<I>; |  | (since C++20) |
|  |  |  |

Casts the result of dereferencing the underlying iterator to its associated rvalue reference type.

The function body is equivalent to return ranges::iter_move(i.base());.

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when std::counted_iterator<I> is an associated class of the arguments.

If i.count() is equal to ​0​, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| i | - | a source iterator adaptor |

### Return value

An rvalue reference or a prvalue temporary.

### Complexity

Constant.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <iterator>
#include <string>
#include <vector>
 
void print(auto const& rem, auto const& v)
{
    std::cout << rem << '[' << size(v) << "] {";
    for (char comma[]{0, ' ', 0}; auto const& s : v)
        std::cout << comma << std::quoted(s), *comma = ',';
    std::cout << "}\n";
}
 
int main()
{
    std::vector<std::string> p{"Alpha", "Bravo", "Charlie"}, q;
    print("p", p);
    print("q", q);
 
    using RI = std::counted_iterator<std::vector<std::string>::iterator>;
 
    for (RI iter{p.begin(), 2}; iter != std::default_sentinel; ++iter)
        q.emplace_back(/* ADL */ iter_move(iter));
 
    print("p", p);
    print("q", q);
}

```

Possible output:

```
p[3] {"Alpha", "Bravo", "Charlie"}
q[0] {}
p[3] {"", "", "Charlie"}
q[2] {"Alpha", "Bravo"}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3953 | C++20 | the return type was std::iter_rvalue_reference_t<I> | changed to decltype(auto) |

### See also

|  |  |
| --- | --- |
| iter_move(C++20) | casts the result of dereferencing an object to its associated rvalue reference type (customization point object) |
| iter_swap(C++20) | swaps the objects pointed to by two underlying iterators   (function template) |
| move(C++11) | converts the argument to an xvalue   (function template) |
| move_if_noexcept(C++11) | converts the argument to an xvalue if the move constructor does not throw   (function template) |
| forward(C++11) | forwards a function argument and use the type template argument to preserve its value category   (function template) |
| ranges::move(C++20) | moves a range of elements to a new location (algorithm function object) |
| ranges::move_backward(C++20) | moves a range of elements to a new location in backwards order (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/counted_iterator/iter_move&oldid=169860>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 February 2024, at 18:15.