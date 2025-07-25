# std::begin, std::cbegin

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****begincbegin****(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<array>` |  |  |
| Defined in header `<deque>` |  |  |
| Defined in header `<flat_map>` |  |  |
| Defined in header `<flat_set>` |  |  |
| Defined in header `<forward_list>` |  |  |
| Defined in header `<inplace_vector>` |  |  |
| Defined in header `<iterator>` |  |  |
| Defined in header `<list>` |  |  |
| Defined in header `<map>` |  |  |
| Defined in header `<regex>` |  |  |
| Defined in header `<set>` |  |  |
| Defined in header `<span>` |  |  |
| Defined in header `<string>` |  |  |
| Defined in header `<string_view>` |  |  |
| Defined in header `<unordered_map>` |  |  |
| Defined in header `<unordered_set>` |  |  |
| Defined in header `<vector>` |  |  |
| template< class C >   auto begin( C& c ) -> decltype(c.begin()); | (1) | (since C++11)  (constexpr since C++17) |
| template< class C >   auto begin( const C& c ) -> decltype(c.begin()); | (2) | (since C++11)  (constexpr since C++17) |
| template< class T, std::size_t N >   T\* begin( T (&array)[N] ); | (3) | (since C++11)  (noexcept since C++14)  (constexpr since C++14) |
| template< class C >   constexpr auto cbegin( const C& c ) noexcept(/\* see below \*/) -> decltype(std::begin(c)); | (4) | (since C++14) |
|  |  |  |

Returns an iterator to the beginning of the given range.

1,2) Returns c.begin(), which is typically an iterator to the beginning of the sequence represented by c.1) If `C` is a standard Container, returns a `C::iterator` object.2) If `C` is a standard Container, returns a `C::const_iterator` object.3) Returns a pointer to the beginning of array.4) Returns std::begin(c), with c always treated as const-qualified. If `C` is a standard Container, returns a `C::const_iterator` object.

!range-begin-end.svg

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | a container or view with a `begin` member function |
| array | - | an array of arbitrary type |

### Return value

1,2) c.begin()3) array4) c.begin()

### Exceptions

4)noexcept specification:noexcept(noexcept(std::begin(c)))

### Overloads

Custom overloads of `begin` may be provided for classes and enumerations that do not expose a suitable `begin()` member function, yet can be iterated. The following overloads are already provided by the standard library:

|  |  |
| --- | --- |
| std::begin(std::initializer_list)(C++11) | overloads ****std::begin****   (function template) |
| std::begin(std::valarray)(C++11) | overloads ****std::begin****   (function template) |
| begin(std::filesystem::directory_iterator)end(std::filesystem::directory_iterator)(C++17) | range-based for loop support   (function) |
| begin(std::filesystem::recursive_directory_iterator)end(std::filesystem::recursive_directory_iterator) | range-based for loop support   (function) |

Similar to the use of `swap` (described in Swappable), typical use of the `begin` function in generic context is an equivalent of using std::begin; begin(arg);, which allows both the ADL-selected overloads for user-defined types and the standard library function templates to appear in the same overload set.

```
template<typename Container, typename Function>
void for_each(Container&& cont, Function f)
{
    using std::begin;
    auto it = begin(cont);
    using std::end;
    auto end_it = end(cont);
    while (it != end_it)
    {
        f(*it);
        ++it;
    }
}

```

|  |  |
| --- | --- |
| Overloads of `begin` found by argument-dependent lookup can be used to customize the behavior of std::ranges::begin, std::ranges::cbegin, and other customization pointer objects depending on std::ranges::begin. | (since C++20) |

### Notes

The non-array overloads exactly reflect the behavior of `C::begin`. Their effects may be surprising if the member function does not have a reasonable implementation.

`std::cbegin` is introduced for unification of member and non-member range accesses. See also LWG issue 2128.

If `C` is a shallow-const view, `std::cbegin` may return a mutable iterator. Such behavior is unexpected for some users. See also P2276 and P2278.

### Example

Run this code

```
#include <iostream>
#include <iterator>
#include <vector>
 
int main() 
{
    std::vector<int> v = {3, 1, 4};
    auto vi = std::begin(v);
    std::cout << std::showpos << *vi << '\n'; 
 
    int a[] = {-5, 10, 15};
    auto ai = std::begin(a);
    std::cout << *ai << '\n';
}

```

Output:

```
+3
-5

```

### See also

|  |  |
| --- | --- |
| endcend(C++11)(C++14) | returns an iterator to the end of a container or array   (function template) |
| ranges::begin(C++20) | returns an iterator to the beginning of a range (customization point object) |
| ranges::cbegin(C++20) | returns an iterator to the beginning of a read-only range (customization point object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/begin&oldid=177482>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 21:52.