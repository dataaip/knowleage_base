# std::forward_list<T,Allocator>::merge

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_list::forward_list | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | forward_list::clear | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | forward_list::insert_after | | | | | | forward_list::emplace_after | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | ****forward_list::merge**** | | | | | | forward_list::splice_after | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | erase(std::forward_list)erase_if(std::forward_list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void merge( forward_list& other ); | (1) | (since C++11) |
| void merge( forward_list&& other ); | (2) | (since C++11) |
| template< class Compare >   void merge( forward_list& other, Compare comp ); | (3) | (since C++11) |
| template< class Compare >   void merge( forward_list&& other, Compare comp ); | (4) | (since C++11) |
|  |  |  |

The function does nothing if other refers to the same object as \*this.

Otherwise, merges other into \*this. Both lists should be sorted. No elements are copied, and the container other becomes empty after the merge. This operation is stable: for equivalent elements in the two lists, the elements from \*this always precede the elements from other, and the order of equivalent elements of \*this and other does not change.

No iterators or references become invalidated. The pointers and references to the elements moved from \*this, as well as the iterators referring to these elements, will refer to the same elements of \*this, instead of other.

1,2) Elements are compared using std::less<T>()(until C++14)std::less<>()(since C++14).3,4) Elements are compared using comp.

If \*this or other is not sorted with respected to the corresponding comparator, or get_allocator() != other.get_allocator(), the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another container to merge |
| comp | - | comparison function object (i.e. an object that satisfies the requirements of Compare) which returns ​true if the first argument is **less** than (i.e. is ordered **before**) the second.   The signature of the comparison function should be equivalent to the following:  bool cmp(const Type1& a, const Type2& b);  While the signature does not need to have const&, the function must not modify the objects passed to it and must be able to accept all values of type (possibly const) `Type1` and `Type2` regardless of value category (thus, `Type1&` is not allowed, nor is `Type1` unless for `Type1` a move is equivalent to a copy(since C++11)).  The types Type1 and Type2 must be such that an object of type forward_list<T, Allocator>::const_iterator can be dereferenced and then implicitly converted to both of them. ​ |
| Type requirements | | |
| -`Compare` must meet the requirements of Compare. | | |

### Return value

(none)

### Exceptions

If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee). Except if the exception comes from a comparison.

### Complexity

If other refers to the same object as \*this, no comparisons are performed.

Otherwise, given \(\scriptsize N\)N as std::distance(begin(), end()) and \(\scriptsize R\)R as std::distance(other.begin(), other.end()):

1,2) At most \(\scriptsize N+R-1\)N+R-1 comparisons using operator<.3,4) At most \(\scriptsize N+R-1\)N+R-1 applications of the comparison function comp.

### Example

Run this code

```
#include <iostream>
#include <forward_list>
 
std::ostream& operator<<(std::ostream& ostr, const std::forward_list<int>& list)
{
    for (const int i : list)
        ostr << ' ' << i;
    return ostr;
}
 
int main()
{
    std::forward_list<int> list1 = {5, 9, 1, 3, 3};
    std::forward_list<int> list2 = {8, 7, 2, 3, 4, 4};
 
    list1.sort();
    list2.sort();
    std::cout << "list1: " << list1 << '\n';
    std::cout << "list2: " << list2 << '\n';
 
    list1.merge(list2);
    std::cout << "merged:" << list1 << '\n';
}

```

Output:

```
list1:  1 3 3 5 9
list2:  2 3 4 4 7 8
merged: 1 2 3 3 3 4 4 5 7 8 9

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2045 | C++11 | O(1) node moving could not be guaranteed if get_allocator() != other.get_allocator() | the behavior is undefined in this case |
| LWG 3088 | C++11 | the effect when \*this and other refer to the same object was not specified operator< could misbehave for pointer elements | specified as no-op implementation-defined strict total order used |

### See also

|  |  |
| --- | --- |
| splice_after | moves elements from another `forward_list`   (public member function) |
| merge | merges two sorted ranges   (function template) |
| inplace_merge | merges two ordered ranges in-place   (function template) |
| ranges::merge(C++20) | merges two sorted ranges (algorithm function object) |
| ranges::inplace_merge(C++20) | merges two ordered ranges in-place (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list/merge&oldid=133661>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2021, at 14:35.