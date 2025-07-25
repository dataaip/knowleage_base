# std::list<T,Allocator>::insert

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | list::list | | | | | | list::~list | | | | | | list::operator= | | | | | | list::assign | | | | | | list::assign_range(C++23) | | | | | | list::get_allocator | | | | | | Element access | | | | | | list::front | | | | | | list::back | | | | | | Iterators | | | | | | list::beginlist::cbegin(C++11) | | | | | | list::endlist::cend(C++11) | | | | | | list::rbeginlist::crbegin(C++11) | | | | | | list::rendlist::crend(C++11) | | | | | | Capacity | | | | | | list::size | | | | | | list::empty | | | | | | list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | list::clear | | | | | | ****list::insert**** | | | | | | list::insert_range(C++23) | | | | | | list::emplace(C++11) | | | | | | list::erase | | | | | | list::push_front | | | | | | list::emplace_front(C++11) | | | | | | list::prepend_range(C++23) | | | | | | list::pop_front | | | | | | list::push_back | | | | | | list::emplace_back(C++11) | | | | | | list::append_range(C++23) | | | | | | list::pop_back | | | | | | list::resize | | | | | | list::swap | | | | | | Operations | | | | | | list::merge | | | | | | list::splice | | | | | | list::removelist::remove_if | | | | | | list::reverse | | | | | | list::unique | | | | | | list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::list) | | | | | | erase(std::list)erase_if(std::list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| iterator insert( const_iterator pos, const T& value ); | (1) |  |
| iterator insert( const_iterator pos, T&& value ); | (2) | (since C++11) |
| iterator insert( const_iterator pos,                   size_type count, const T& value ); | (3) |  |
| template< class InputIt >  iterator insert( const_iterator pos, InputIt first, InputIt last ); | (4) |  |
| iterator insert( const_iterator pos, std::initializer_list<T> ilist ); | (5) | (since C++11) |
|  |  |  |

Inserts elements at the specified location in the container.

1) Inserts a copy of value before pos.2) Inserts value before pos, possibly using move semantics.3) Inserts count copies of the value before pos.4) Inserts elements from range ``first`,`last`)` before pos.

|  |  |
| --- | --- |
| This overload has the same effect as overload (3) if `InputIt` is an integral type. | (until C++11) |
| This overload participates in overload resolution only if `InputIt` qualifies as [LegacyInputIterator, to avoid ambiguity with the overload (3). | (since C++11) |

 If first and last are iterators into \*this, the behavior is undefined.5) Inserts elements from initializer list ilist before pos.

No iterators or references are invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator before which the content will be inserted (pos may be the `end()` iterator) |
| value | - | element value to insert |
| count | - | number of elements to insert |
| first, last | - | the range of elements to insert, cannot be iterators into container for which insert is called |
| ilist | - | std::initializer_list to insert the values from |
| Type requirements | | |
| -`T` must meet the requirements of CopyInsertable in order to use overload (1). | | |
| -`T` must meet the requirements of MoveInsertable in order to use overload (2). | | |
| -`T` must meet the requirements of CopyAssignable and CopyInsertable in order to use overload (3). | | |
| -`T` must meet the requirements of EmplaceConstructible in order to use overloads (4,5). | | |

### Return value

1,2) Iterator pointing to the inserted value.3) Iterator pointing to the first element inserted, or pos if count == 0.4) Iterator pointing to the first element inserted, or pos if first == last.5) Iterator pointing to the first element inserted, or pos if ilist is empty.

### Complexity

1,2) Constant.3) Linear in count.4) Linear in std::distance(first, last).5) Linear in ilist.size().

### Exceptions

If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).

### Example

Run this code

```
#include <iostream>
#include <iterator>
#include <string_view>
#include <list>
 
namespace stq {
void println(std::string_view rem, const std::list<int>& container)
{
    std::cout << rem.substr(0, rem.size() - 2) << '[';
    bool first{true};
    for (const int x : container)
        std::cout << (first ? first = false, "" : ", ") << x;
    std::cout << "]\n";
}
}
 
int main()
{
    std::list<int> c1(3, 100);
    stq::println("1. {}", c1);
 
    auto pos = c1.begin();
    pos = c1.insert(pos, 200); // overload (1)
    stq::println("2. {}", c1);
 
    c1.insert(pos, 2, 300); // overload (3)
    stq::println("3. {}", c1);
 
    // reset pos to the begin:
    pos = c1.begin();
 
    std::list<int> c2(2, 400);
    c1.insert(std::next(pos, 2), c2.begin(), c2.end()); // overload (4)
    stq::println("4. {}", c1);
 
    int arr[] = {501, 502, 503};
    c1.insert(c1.begin(), arr, arr + std::size(arr)); // overload (4)
    stq::println("5. {}", c1);
 
    c1.insert(c1.end(), {601, 602, 603}); // overload (5)
    stq::println("6. {}", c1);
}

```

Output:

```
1. [100, 100, 100]
2. [200, 100, 100, 100]
3. [300, 300, 200, 100, 100, 100]
4. [300, 300, 400, 400, 200, 100, 100, 100]
5. [501, 502, 503, 300, 300, 400, 400, 200, 100, 100, 100]
6. [501, 502, 503, 300, 300, 400, 400, 200, 100, 100, 100, 601, 602, 603]

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 149 | C++98 | overloads (3) and (4) returned nothing | returns an iterator |

### See also

|  |  |
| --- | --- |
| emplace(C++11) | constructs element in-place   (public member function) |
| push_front | inserts an element to the beginning   (public member function) |
| push_back | adds an element to the end   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/list/insert&oldid=135232>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 November 2021, at 07:45.