# std::forward_list<T,Allocator>::emplace_after

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_list::forward_list | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | forward_list::clear | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | forward_list::insert_after | | | | | | ****forward_list::emplace_after**** | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | forward_list::merge | | | | | | forward_list::splice_after | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | erase(std::forward_list)erase_if(std::forward_list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< class... Args >  iterator emplace_after( const_iterator pos, Args&&... args ); |  | (since C++11) |
|  |  |  |

Inserts a new element into a position after the specified position in the container. The element is constructed in-place, i.e. no copy or move operations are performed. The constructor of the element is called with exactly the same arguments, as supplied to the function.

No iterators or references are invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator after which the new element will be constructed |
| args | - | arguments to forward to the constructor of the element |

### Return value

Iterator to the new element.

### Complexity

Constant.

### Exceptions

If an exception is thrown for any reason, this function has no effect (strong exception safety guarantee).

### Example

The example demonstrates a canonical filling of a single-linked list in natural (as opposed to reverse) order.

Run this code

```
#include <forward_list>
#include <iostream>
#include <string>
 
struct Sum
{
    std::string remark;
    int sum;
 
    Sum(std::string remark, int sum)
        : remark{std::move(remark)}, sum{sum} {}
 
    void print() const
    {
        std::cout << remark << " = " << sum << '\n';
    }
};
 
int main()
{
    std::forward_list<Sum> list;
 
    auto iter = list.before_begin();
    std::string str{"1"};
 
    for (int i{1}, sum{1}; i != 10; sum += i)
    {
        iter = list.emplace_after(iter, str, sum);
        ++i;
        str += " + " + std::to_string(i);
    }
 
    for (const Sum& s : list)
        s.print();
}

```

Output:

```
1 = 1
1 + 2 = 3
1 + 2 + 3 = 6
1 + 2 + 3 + 4 = 10
1 + 2 + 3 + 4 + 5 = 15
1 + 2 + 3 + 4 + 5 + 6 = 21
1 + 2 + 3 + 4 + 5 + 6 + 7 = 28
1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 = 36
1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 = 45

```

### See also

|  |  |
| --- | --- |
| insert_after | inserts elements after an element   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list/emplace_after&oldid=159707>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 September 2023, at 09:12.