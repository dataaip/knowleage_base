# std::list<T,Allocator>::splice

From cppreference.com
< cpp‎ | container‎ | list
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

std::list

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | list::list | | | | | | list::~list | | | | | | list::operator= | | | | | | list::assign | | | | | | list::assign_range(C++23) | | | | | | list::get_allocator | | | | | | Element access | | | | | | list::front | | | | | | list::back | | | | | | Iterators | | | | | | list::beginlist::cbegin(C++11) | | | | | | list::endlist::cend(C++11) | | | | | | list::rbeginlist::crbegin(C++11) | | | | | | list::rendlist::crend(C++11) | | | | | | Capacity | | | | | | list::size | | | | | | list::empty | | | | | | list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | list::clear | | | | | | list::insert | | | | | | list::insert_range(C++23) | | | | | | list::emplace(C++11) | | | | | | list::erase | | | | | | list::push_front | | | | | | list::emplace_front(C++11) | | | | | | list::prepend_range(C++23) | | | | | | list::pop_front | | | | | | list::push_back | | | | | | list::emplace_back(C++11) | | | | | | list::append_range(C++23) | | | | | | list::pop_back | | | | | | list::resize | | | | | | list::swap | | | | | | Operations | | | | | | list::merge | | | | | | ****list::splice**** | | | | | | list::removelist::remove_if | | | | | | list::reverse | | | | | | list::unique | | | | | | list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::list) | | | | | | erase(std::list)erase_if(std::list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void splice( const_iterator pos, list& other ); | (1) |  |
| void splice( const_iterator pos, list&& other ); | (2) | (since C++11) |
| void splice( const_iterator pos, list& other, const_iterator it ); | (3) |  |
| void splice( const_iterator pos, list&& other, const_iterator it ); | (4) | (since C++11) |
| void splice( const_iterator pos, list& other,                const_iterator first, const_iterator last); | (5) |  |
| void splice( const_iterator pos, list&& other,                const_iterator first, const_iterator last ); | (6) | (since C++11) |
|  |  |  |

Transfers elements from one list to another.

No elements are copied or moved, only the internal pointers of the list nodes are re-pointed. No iterators or references become invalidated, the iterators to moved elements remain valid, but now refer into \*this, not into other.

1,2) Transfers all elements from other into \*this. The elements are inserted before the element pointed to by pos. The container other becomes empty after the operation.3,4) Transfers the element pointed to by it from other into \*this. The element is inserted before the element pointed to by pos.5,6) Transfers the elements in the range ``first`,`last`)` from other into \*this. The elements are inserted before the element pointed to by pos.

The behavior is undefined if

- get_allocator() != other.get_allocator(),
- for overloads (1,2), \*this and other refer to the same object,
- for overloads (3,4), it is not a [dereferenceable iterator into other, or
- for overloads (5,6),

:   - ``first`,`last`)` is not a [valid range in other, or
    - pos is in ``first`,`last`)`.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | element before which the content will be inserted |
| other | - | another container to transfer the content from |
| it | - | the element to transfer from other to \*this |
| first, last | - | the range of elements to transfer from other to \*this |

### Return value

(none)

### Exceptions

Throws nothing.

### Complexity

1-4) Constant.5,6) Constant if other refers to the same object as \*this, otherwise linear in [std::distance(first, last).

### Example

Run this code

```
#include <iostream>
#include <list>
 
std::ostream& operator<<(std::ostream& ostr, const std::list<int>& list)
{
    for (auto& i : list)
        ostr << ' ' << i;
 
    return ostr;
}
 
int main ()
{
    std::list<int> list1{1, 2, 3, 4, 5};
    std::list<int> list2{10, 20, 30, 40, 50};
 
    auto it = list1.begin();
    std::advance(it, 2);
 
    list1.splice(it, list2);
 
    std::cout << "list1:" << list1 << '\n';
    std::cout << "list2:" << list2 << '\n';
 
    list2.splice(list2.begin(), list1, it, list1.end());
 
    std::cout << "list1:" << list1 << '\n';
    std::cout << "list2:" << list2 << '\n';
}

```

Output:

```
list1: 1 2 10 20 30 40 50 3 4 5
list2:
list1: 1 2 10 20 30 40 50
list2: 3 4 5

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 250 | C++98 | references and iterators to the moved element(s) were all invalidated | they refer or point to the same element(s) in \*this |
| N2525 | C++98 | O(1) splicing could not be guaranteed if get_allocator() != other.get_allocator() | the behavior is undefined in this case |

### See also

|  |  |
| --- | --- |
| merge | merges two sorted lists   (public member function) |
| removeremove_if | removes elements satisfying specific criteria   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/list/splice&oldid=156717>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 August 2023, at 01:26.