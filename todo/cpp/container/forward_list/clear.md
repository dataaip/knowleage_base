# std::forward_list<T,Allocator>::clear

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_list::forward_list | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | ****forward_list::clear**** | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | forward_list::insert_after | | | | | | forward_list::emplace_after | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | forward_list::merge | | | | | | forward_list::splice_after | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | erase(std::forward_list)erase_if(std::forward_list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void clear() noexcept; |  | (since C++11) |
|  |  |  |

Erases all elements from the container.

Invalidates any references, pointers, and iterators referring to contained elements.
Any past-the-end iterator remains valid.

### Parameters

(none)

### Return value

(none)

### Complexity

Linear in the size of the container, i.e., the number of elements.

### Example

Run this code

```
#include <iostream>
#include <string_view>
#include <forward_list>
 
void print_info(std::string_view rem, const std::forward_list<int>& v)
{
    std::cout << rem << "{ ";
    for (const auto& value : v)
        std::cout << value << ' ';
    std::cout << "}\n";
}
 
int main()
{
    std::forward_list<int> container{1, 2, 3};
    print_info("Before clear: ", container);
    container.clear();
    print_info("After clear: ", container);
}

```

Output:

```
Before clear: { 1 2 3 }
After clear: { }

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2231 | C++11 | complexity guarantee was mistakenly omitted in C++11 | complexity reaffirmed as linear |

### See also

|  |  |
| --- | --- |
| erase_after | erases an element after an element   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list/clear&oldid=156306>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 August 2023, at 14:00.