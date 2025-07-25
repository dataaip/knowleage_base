# std::list<T,Allocator>::get_allocator

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | list::list | | | | | | list::~list | | | | | | list::operator= | | | | | | list::assign | | | | | | list::assign_range(C++23) | | | | | | ****list::get_allocator**** | | | | | | Element access | | | | | | list::front | | | | | | list::back | | | | | | Iterators | | | | | | list::beginlist::cbegin(C++11) | | | | | | list::endlist::cend(C++11) | | | | | | list::rbeginlist::crbegin(C++11) | | | | | | list::rendlist::crend(C++11) | | | | | | Capacity | | | | | | list::size | | | | | | list::empty | | | | | | list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | list::clear | | | | | | list::insert | | | | | | list::insert_range(C++23) | | | | | | list::emplace(C++11) | | | | | | list::erase | | | | | | list::push_front | | | | | | list::emplace_front(C++11) | | | | | | list::prepend_range(C++23) | | | | | | list::pop_front | | | | | | list::push_back | | | | | | list::emplace_back(C++11) | | | | | | list::append_range(C++23) | | | | | | list::pop_back | | | | | | list::resize | | | | | | list::swap | | | | | | Operations | | | | | | list::merge | | | | | | list::splice | | | | | | list::removelist::remove_if | | | | | | list::reverse | | | | | | list::unique | | | | | | list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::list) | | | | | | erase(std::list)erase_if(std::list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| allocator_type get_allocator() const; |  | (noexcept since C++11) |
|  |  |  |

Returns the allocator associated with the container.

### Parameters

(none)

### Return value

The associated allocator.

### Complexity

Constant.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/list/get_allocator&oldid=135210>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 November 2021, at 07:24.