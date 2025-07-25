# std::forward_list

From cppreference.com
< cpp‎ | container
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
| ****forward_list****(C++11) | | | | |
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

****std::forward_list****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_list::forward_list | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | forward_list::clear | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | forward_list::insert_after | | | | | | forward_list::emplace_after | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | forward_list::merge | | | | | | forward_list::splice_after | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | erase(std::forward_list)erase_if(std::forward_list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<forward_list>` |  |  |
| template<  class T,      class Allocator = std::allocator<T> > class forward_list; | (1) | (since C++11) |
| namespace pmr {  template< class T >      using forward_list = std::forward_list<T, std::pmr::polymorphic_allocator<T>>; } | (2) | (since C++17) |
|  |  |  |

`std::forward_list` is a container that supports fast insertion and removal of elements from anywhere in the container. Fast random access is not supported. It is implemented as a singly-linked list. Compared to std::list this container provides more space efficient storage when bidirectional iteration is not needed.

Adding, removing and moving the elements within the list, or across several lists, does not invalidate the iterators currently referring to other elements in the list. However, an iterator or reference referring to an element is invalidated when the corresponding element is removed (via erase_after) from the list.

`std::forward_list` meets the requirements of Container (except for the size member function and that `operator==`'s complexity is always linear), AllocatorAwareContainer and SequenceContainer.

### Template parameters

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| T | - | The type of the elements.  |  |  | | --- | --- | | The requirements that are imposed on the elements depend on the actual operations performed on the container. Generally, it is required that element type is a complete type and meets the requirements of Erasable, but many member functions impose stricter requirements. | (until C++17) | | The requirements that are imposed on the elements depend on the actual operations performed on the container. Generally, it is required that element type meets the requirements of Erasable, but many member functions impose stricter requirements. This container (but not its members) can be instantiated with an incomplete element type if the allocator satisfies the allocator completeness requirements.   | Feature-test macro | Value | Std | Feature | | --- | --- | --- | --- | | `__cpp_lib_incomplete_container_elements` | `201505L` | (C++17) | Minimal incomplete type support | | (since C++17) | |
| Allocator | - | An allocator that is used to acquire/release memory and to construct/destroy the elements in that memory. The type must meet the requirements of Allocator. The behavior is undefined(until C++20)The program is ill-formed(since C++20) if `Allocator::value_type` is not the same as `T`. |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `T` |
| `allocator_type` | `Allocator` |
| `size_type` | Unsigned integer type (usually std::size_t) |
| `difference_type` | Signed integer type (usually std::ptrdiff_t) |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `pointer` | std::allocator_traits<Allocator>::pointer |
| `const_pointer` | std::allocator_traits<Allocator>::const_pointer |
| `iterator` | LegacyForwardIterator to `value_type` |
| `const_iterator` | LegacyForwardIterator to const value_type |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `forward_list`   (public member function) |
| (destructor) | destructs the `forward_list`   (public member function) |
| operator= | assigns values to the container   (public member function) |
| assign | assigns values to the container   (public member function) |
| assign_range(C++23) | assigns a range of values to the container   (public member function) |
| get_allocator | returns the associated allocator   (public member function) |
| Element access | |
| front | access the first element   (public member function) |
| Iterators | |
| before_begincbefore_begin | returns an iterator to the element before beginning   (public member function) |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend | returns an iterator to the end   (public member function) |
| Capacity | |
| empty | checks whether the container is empty   (public member function) |
| max_size | returns the maximum possible number of elements   (public member function) |
| Modifiers | |
| clear | clears the contents   (public member function) |
| insert_after | inserts elements after an element   (public member function) |
| emplace_after | constructs elements in-place after an element   (public member function) |
| insert_range_after(C++23) | inserts a range of elements after an element   (public member function) |
| erase_after | erases an element after an element   (public member function) |
| push_front | inserts an element to the beginning   (public member function) |
| emplace_front | constructs an element in-place at the beginning   (public member function) |
| prepend_range(C++23) | adds a range of elements to the beginning   (public member function) |
| pop_front | removes the first element   (public member function) |
| resize | changes the number of elements stored   (public member function) |
| swap | swaps the contents   (public member function) |
| Operations | |
| merge | merges two sorted lists   (public member function) |
| splice_after | moves elements from another `forward_list`   (public member function) |
| removeremove_if | removes elements satisfying specific criteria   (public member function) |
| reverse | reverses the order of the elements   (public member function) |
| unique | removes consecutive duplicate elements   (public member function) |
| sort | sorts the elements   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++20) | lexicographically compares the values of two `forward_list`s   (function template) |
| std::swap(std::forward_list)(C++11) | specializes the std::swap algorithm   (function template) |
| erase(std::forward_list)erase_if(std::forward_list)(C++20) | erases all elements satisfying specific criteria   (function template) |

|  |  |
| --- | --- |
| Deduction guides | (since C++17) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges construction and insertion for containers |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| list | doubly-linked list   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list&oldid=174035>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 August 2024, at 20:53.