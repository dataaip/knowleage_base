# std::multiset<Key,Compare,Allocator>::rbegin, std::multiset<Key,Compare,Allocator>::crbegin

From cppreference.com
< cpp‎ | container‎ | multiset
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

std::multiset

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::multiset | | | | | | multiset::~multiset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::operator= | | | | | | multiset::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multiset::beginmultiset::cbegin(C++11) | | | | | | multiset::endmultiset::cend(C++11) | | | | | | ****multiset::rbeginmultiset::crbegin****(C++11) | | | | | | multiset::rendmultiset::crend(C++11) | | | | | | Capacity | | | | | | multiset::size | | | | | | multiset::max_size | | | | | | multiset::empty | | | | | | Observers | | | | | | multiset::key_comp | | | | | | multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multiset::clear | | | | | | multiset::erase | | | | | | multiset::swap | | | | | | multiset::extract(C++17) | | | | | | multiset::merge(C++17) | | | | | | multiset::insert | | | | | | multiset::insert_range(C++23) | | | | | | multiset::emplace(C++11) | | | | | | multiset::emplace_hint(C++11) | | | | | | Lookup | | | | | | multiset::count | | | | | | multiset::find | | | | | | multiset::contains(C++20) | | | | | | multiset::equal_range | | | | | | multiset::lower_bound | | | | | | multiset::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::multiset) | | | | | | erase_if(std::multiset)(C++20) | | | | | | operator==operator<=>(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| reverse_iterator rbegin(); | (1) | (noexcept since C++11) |
| const_reverse_iterator rbegin() const; | (2) | (noexcept since C++11) |
| const_reverse_iterator crbegin() const noexcept; | (3) | (since C++11) |
|  |  |  |

Returns a reverse iterator to the first element of the reversed `multiset`. It corresponds to the last element of the non-reversed `multiset`. If the `multiset` is empty, the returned iterator is equal to rend().

!range-rbegin-rend.svg

### Parameters

(none)

### Return value

Reverse iterator to the first element.

### Complexity

Constant.

### Notes

Because both `iterator` and `const_iterator` are constant iterators (and may in fact be the same type), it is not possible to mutate the elements of the container through an iterator returned by any of these member functions.

The underlying iterator of the returned reverse iterator is the end iterator. Hence the returned iterator is invalidated if and when the end iterator is invalidated.

libc++ backports `crbegin()` to C++98 mode.

### Example

Run this code

```
#include <iostream>
#include <set>
 
int main()
{
    std::multiset<unsigned> rep{1, 2, 3, 4, 1, 2, 3, 4};
 
    for (auto it = rep.crbegin(); it != rep.crend(); ++it)
    {
        for (auto n = *it; n > 0; --n)
            std::cout << "⏼" << ' ';
        std::cout << '\n';
    }
}

```

Output:

```
⏼ ⏼ ⏼ ⏼
⏼ ⏼ ⏼ ⏼
⏼ ⏼ ⏼
⏼ ⏼ ⏼
⏼ ⏼
⏼ ⏼
⏼
⏼

```

### See also

|  |  |
| --- | --- |
| rendcrend(C++11) | returns a reverse iterator to the end   (public member function) |
| rbegincrbegin(C++14) | returns a reverse iterator to the beginning of a container or array   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multiset/rbegin&oldid=135721>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2021, at 06:40.