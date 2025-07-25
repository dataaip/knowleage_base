# std::span<T,Extent>::operator[]

From cppreference.com
< cpp‎ | container‎ | span
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

std::span

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| span::span | | | | |
| span::operator= | | | | |
| Element access | | | | |
| span::front | | | | |
| span::back | | | | |
| span::at(C++26) | | | | |
| ****span::operator[]**** | | | | |
| span::data | | | | |
| Iterators | | | | |
| span::beginspan::cbegin(C++23) | | | | |
| span::endspan::cend(C++23) | | | | |
| span::rbeginspan::crbegin(C++23) | | | | |
| span::rendspan::crend(C++23) | | | | |
| Observers | | | | |
| span::empty | | | | |
| span::size | | | | |
| span::size_bytes | | | | |
| Subviews | | | | |
| span::first | | | | |
| span::last | | | | |
| span::subspan | | | | |
| Non-member functions | | | | |
| as_bytesas_writable_bytes | | | | |
| Non-member constant | | | | |
| dynamic_extent | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr reference operator[]( size_type idx ) const; |  | (since C++20) |
|  |  |  |

Returns a reference to the idxth element of the sequence. The behavior is undefined if idx is out of range (i.e., if it is greater than or equal to size()).

### Parameters

|  |  |  |
| --- | --- | --- |
| idx | - | the index of the element to access |

### Return value

A reference to the idxth element of the sequence, i.e., data()[idx].

### Exceptions

Throws nothing.

### Example

Run this code

```
#include <cstddef>
#include <iostream>
#include <span>
#include <utility>
 
void reverse(std::span<int> span)
{
    for (std::size_t i = 0, j = std::size(span); i < j; ++i)
    {
        --j;
        std::swap(span[i], span[j]);
    }
}
 
void print(std::span<const int> const span)
{
    for (int element : span)
        std::cout << element << ' ';
    std::cout << '\n';
}
 
int main()
{
    int data[]{1, 2, 3, 4, 5};
    print(data);
    reverse(data);
    print(data);
}

```

Output:

```
1 2 3 4 5
5 4 3 2 1

```

### See also

|  |  |
| --- | --- |
| at(C++26) | access specified element with bounds checking   (public member function) |
| data | direct access to the underlying contiguous storage   (public member function) |
| size | returns the number of elements   (public member function) |
| as_bytesas_writable_bytes(C++20) | converts a `span` into a view of its underlying bytes   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/span/operator_at&oldid=166666>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2023, at 14:03.