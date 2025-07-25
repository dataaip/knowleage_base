# std::forward_list<T,Allocator>::splice_after

From cppreference.com
< cpp‎ | container‎ | forward list
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

std::forward_list

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_list::forward_list | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | forward_list::clear | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | forward_list::insert_after | | | | | | forward_list::emplace_after | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | forward_list::merge | | | | | | ****forward_list::splice_after**** | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | erase(std::forward_list)erase_if(std::forward_list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void splice_after( const_iterator pos, forward_list& other ); | (1) | (since C++11) |
| void splice_after( const_iterator pos, forward_list&& other ); | (2) | (since C++11) |
| void splice_after( const_iterator pos, forward_list& other,                     const_iterator it ); | (3) | (since C++11) |
| void splice_after( const_iterator pos, forward_list&& other,                     const_iterator it ); | (4) | (since C++11) |
| void splice_after( const_iterator pos, forward_list& other,                     const_iterator first, const_iterator last ); | (5) | (since C++11) |
| void splice_after( const_iterator pos, forward_list&& other,                     const_iterator first, const_iterator last ); | (6) | (since C++11) |
|  |  |  |

Moves elements from another `forward_list` to \*this. The elements are inserted after the element pointed to by pos.

No elements are copied. No iterators or references become invalidated. The iterators to the moved elements now refer into \*this, not into other.

1,2) Moves all elements from other into \*this. The container other becomes empty after the operation.3,4) Moves the element pointed to by the iterator following it from other into \*this. Has no effect if pos == it or if pos == ++it.5,6) Moves the elements in the range `(`first`,`last`)` from other into \*this. The element pointed-to by first is not moved.

The behavior is undefined if

- get_allocator() != other.get_allocator(),
- pos is neither before_begin() nor a dereferenceable iterator in ``begin()`,`end()`)`,
- for overloads (1,2), \*this and other refer to the same object,
- for overloads (3,4), the iterator following it is not a [dereferenceable iterator into other, or
- for overloads (5,6),

:   - `(`first`,`last`)` is not a valid range in other,
    - some iterators in `(`first`,`last`)` are not dereferenceable, or
    - pos is in `(`first`,`last`)`.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | element after which the content will be inserted |
| other | - | another container to move the content from |
| it | - | iterator preceding the iterator to the element to move from other to \*this |
| first, last | - | the range of elements to move from other to \*this |

### Exceptions

Throws nothing.

### Complexity

1,2) Linear in the size of other.3,4) Constant.5,6) Linear in std::distance(first, last).

### Example

Run this code

```
#include <cassert>
#include <forward_list>
 
int main()
{
    using F = std::forward_list<int>;
 
    // Demonstrate the meaning of open range (first, last)
    // in overload (5): the first element of l1 is not moved.
    F l1 = {1, 2, 3, 4, 5};
    F l2 = {10, 11, 12};
 
    l2.splice_after(l2.cbegin(), l1, l1.cbegin(), l1.cend());
    // Not equivalent to l2.splice_after(l2.cbegin(), l1);
    // which is equivalent to
    // l2.splice_after(l2.cbegin(), l1, l1.cbefore_begin(), l1.end());
 
    assert((l1 == F{1}));
    assert((l2 == F{10, 2, 3, 4, 5, 11, 12}));
 
    // Overload (1)
    F x = {1, 2, 3, 4, 5};
    F y = {10, 11, 12};
    x.splice_after(x.cbegin(), y);
    assert((x == F{1, 10, 11, 12, 2, 3, 4, 5}));
    assert((y == F{}));
 
    // Overload (3)
    x = {1, 2, 3, 4, 5};
    y = {10, 11, 12};
    x.splice_after(x.cbegin(), y, y.cbegin());
    assert((x == F{1, 11, 2, 3, 4, 5}));
    assert((y == F{10, 12}));
 
    // Overload (5)
    x = {1, 2, 3, 4, 5};
    y = {10, 11, 12};
    x.splice_after(x.cbegin(), y, y.cbegin(), y.cend());
    assert((x == F{1, 11, 12, 2, 3, 4, 5}));
    assert((y == F{10}));
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2045 | C++11 | O(1) splicing could not be guaranteed if get_allocator() != other.get_allocator() | the behavior is undefined in this case |
| LWG 2222 | C++11 | the element pointed to by it is not moved, but pointers, references and iterators referring to it would refer to an element in \*this after splicing | still refer to the element in other |

### See also

|  |  |
| --- | --- |
| merge | merges two sorted lists   (public member function) |
| removeremove_if | removes elements satisfying specific criteria   (public member function) |
| before_begincbefore_begin | returns an iterator to the element before beginning   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list/splice_after&oldid=177694>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 November 2024, at 00:03.