# std::inplace_vector

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
| ****inplace_vector****(C++26) | | | | |
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

****std::inplace_vector****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](inplace_vector/operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<inplace_vector>` |  |  |
| template<  class T,      std::size_t N > struct inplace_vector; |  | (since C++26) |
|  |  |  |

`inplace_vector` is a dynamically-resizable array with contiguous inplace storage. The elements of type `T` are stored and properly aligned within the object itself. The capacity of the internal storage is fixed at compile-time and is equal to N.

The elements are stored contiguously, which means that elements can be accessed not only through iterators or random-access operator[], but also using offsets to regular pointers to elements. A pointer to an element of an `inplace_vector` may be passed to any function that expects a pointer to an element of a C-array.

The `inplace_vector` models Container, ReversibleContainer, ContiguousContainer, and SequenceContainer, including most of the optional sequence container requirements, except that the `push_front`, `emplace_front`, `pop_front`, and `prepend_range` member functions are not provided.

For any positive N, `std::inplace_vector<T, N>::iterator` and `std::inplace_vector<T, N>::const_iterator` meet the ConstexprIterator requirements.

For any positive N, if `T` is not TriviallyCopyable or std::is_trivially_default_constructible_v<T> is false, then member functions of `inplace_vector` are not usable in constant expressions.

The specialization std::inplace_vector<T, 0> is TriviallyCopyable and is empty. std::is_trivially_default_constructible_v<std::inplace_vector<T, 0>> is also true.

Any member function of std::inplace_vector<T, N> that would cause insertion beyond the capacity N throws std::bad_alloc.

The complexity of common operations on `inplace_vector`s is as follows:

- Random access to an element via [`operator[]`](inplace_vector/operator_at.html "cpp/container/inplace vector/operator at") or `at()` – constant: 𝓞(1).
- Insertion or removal of an element at the end – constant: 𝓞(1).
- Insertion or removal of elements at the end – linear in the number of elements inserted/removed: 𝓞(n).
- Insertion or removal of elements in the beginning or in the middle – linear in the number of elements inserted/removed plus the distance to the end of the vector: 𝓞(n).

### Iterator invalidation

`std::inplace_vector` iterator invalidation guarantees differ from std::vector:

- moving an `inplace_vector` invalidates all iterators;
- swapping two `inplace_vector`s invalidates all iterators (during swap, the iterator will continue to point to the same array element, and may thus change its value).

The following member functions potentially invalidate iterators:
`operator=`,
`assign`,
`assign_range`,
`clear`,
`emplace`,
`erase`,
`insert`,
`insert_range`,
`pop_back`,
`resize`, and
`swap`.

The following member functions potentially invalidate `end` iterator only:
`append_range`,
`emplace_back`,
`push_back`,
`try_append_range`,
`try_emplace_back`,
`try_push_back`,
`unchecked_emplace_back`, and
`unchecked_push_back`.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | element type. Must be MoveConstructible and MoveAssignable. |
| N | - | capacity, i.e. the maximum number of elements in the `inplace_vector` (might be ​0​). |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `value_type` | `T` |
| `size_type` | std::size_t |
| `difference_type` | std::ptrdiff_t |
| `reference` | value_type& |
| `const_reference` | const value_type& |
| `pointer` | value_type\* |
| `const_pointer` | const value_type\* |
| `iterator` | implementation-defined LegacyRandomAccessIterator and `random_access_iterator` to `value_type` |
| `const_iterator` | implementation-defined LegacyRandomAccessIterator and `random_access_iterator` to const value_type |
| `reverse_iterator` | std::reverse_iterator<iterator> |
| `const_reverse_iterator` | std::reverse_iterator<const_iterator> |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `inplace_vector`   (public member function) |
| (destructor) | destructs the `inplace_vector`   (public member function) |
| operator= | assigns values to the container   (public member function) |
| assign | assigns values to the container   (public member function) |
| assign_range | assigns a range of values to the container   (public member function) |
| Element access | |
| at | access specified element with bounds checking   (public member function) |
| [operator[]](inplace_vector/operator_at.html "cpp/container/inplace vector/operator at") | access specified element   (public member function) |
| front | access the first element   (public member function) |
| back | access the last element   (public member function) |
| data | direct access to the underlying contiguous storage   (public member function) |
| Iterators | |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend | returns an iterator to the end   (public member function) |
| rbegincrbegin | returns a reverse iterator to the beginning   (public member function) |
| rendcrend | returns a reverse iterator to the end   (public member function) |
| Size and capacity | |
| empty | checks whether the container is empty   (public member function) |
| size | returns the number of elements   (public member function) |
| max_size[static] | returns the maximum possible number of elements   (public static member function) |
| capacity[static] | returns the number of elements that can be held in currently allocated storage   (public static member function) |
| resize | changes the number of elements stored   (public member function) |
| reserve[static] | reserves storage   (public static member function) |
| shrink_to_fit[static] | reduces memory usage by freeing unused memory   (public static member function) |
| Modifiers | |
| insert | inserts elements   (public member function) |
| insert_range | inserts a range of elements   (public member function) |
| emplace | constructs element in-place   (public member function) |
| emplace_back | constructs an element in-place at the end   (public member function) |
| try_emplace_back | tries to construct an element in-place at the end   (public member function) |
| unchecked_emplace_back | unconditionally constructs an element in-place at the end   (public member function) |
| push_back | adds an element to the end   (public member function) |
| try_push_back | tries to add an element to the end   (public member function) |
| unchecked_push_back | unconditionally adds an element to the end   (public member function) |
| pop_back | removes the last element   (public member function) |
| append_range | adds a range of elements to the end   (public member function) |
| try_append_range | tries to add a range of elements to the end   (public member function) |
| clear | clears the contents   (public member function) |
| erase | erases elements   (public member function) |
| swap | swaps the contents   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| std::swap(std::inplace_vector)(C++26) | specializes the std::swap algorithm   (function template) |
| erase(std::inplace_vector)erase_if(std::inplace_vector)(C++26) | erases all elements satisfying specific criteria   (function template) |
| operator==operator<=>(C++26) | lexicographically compares the values of two `inplace_vector`s   (function template) |

### Notes

The number of elements in a `inplace_vector` may vary dynamically up to a fixed capacity because elements are stored within the object itself similarly to std::array. However, objects are initialized as they are inserted into `inplace_vector` unlike C arrays or std::array , which must construct all elements on instantiation.

`inplace_vector` is useful in environments where dynamic memory allocations are undesired.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_inplace_vector` | `202406L` | (C++26) | `std::inplace_vector`: dynamically-resizable vector with fixed capacity inplace storage |

### Example

Run this code

```
#include <algorithm>
#include <array>
#include <cassert>
#include <inplace_vector>
 
int main()
{
    std::inplace_vector<int, 4> v1{0, 1, 2};
    assert(v1.max_size() == 4);
    assert(v1.capacity() == 4);
    assert(v1.size() == 3);
    assert(std::ranges::equal(v1, std::array{0, 1, 2}));
    assert(v1[0] == 0);
    assert(v1.at(0) == 0);
    assert(v1.front() == 0);
    assert(*v1.begin() == 0);
    assert(v1.back() == 2);
    v1.push_back(3);
    assert(v1.back() == 3);
    assert(std::ranges::equal(v1, std::array{0, 1, 2, 3}));
    v1.resize(3);
    assert(std::ranges::equal(v1, std::array{0, 1, 2}));
    assert(v1.try_push_back(3) != nullptr);
    assert(v1.back() == 3);
    assert(v1.size() == 4);
    assert(v1.try_push_back(13) == nullptr); // no place
    assert(v1.back() == 3);
    assert(v1.size() == 4);
    v1.clear();
    assert(v1.size() == 0);
    assert(v1.empty());
}

```

### See also

|  |  |
| --- | --- |
| vector | dynamic contiguous array   (class template) |
| array(C++11) | fixed-sized inplace contiguous array   (class template) |
| deque | double-ended queue   (class template) |

### External links

|  |  |
| --- | --- |
| 1. | `inplace_vector` — A reference implementation of P0843R14 (`std::inplace_vector`). |
| 2. | `static_vector` — Boost.Container implements inplace vector as a standalone type with its own guarantees. |
| 3. | `fixed_vector` — EASTL implements inplace vector via an extra template parameter. |
| 4. | `small_vector` — Folly also implements inplace vector via an extra template parameter. |
| 5. | `stack_alloc` — Howard Hinnant's Custom allocators that emulate `std::inplace_vector` on top of std::vector. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector&oldid=179337>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 January 2025, at 18:50.