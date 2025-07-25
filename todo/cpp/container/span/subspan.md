# std::span<T,Extent>::subspan

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
| [span::operator[]](operator_at.html "cpp/container/span/operator at") | | | | |
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
| ****span::subspan**** | | | | |
| Non-member functions | | | | |
| as_bytesas_writable_bytes | | | | |
| Non-member constant | | | | |
| dynamic_extent | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< std::size_t Offset,  std::size_t Count = std::dynamic_extent >  constexpr std::span<element_type, E /\* see below \*/>     subspan() const; | (1) | (since C++20) |
| constexpr std::span<element_type, std::dynamic_extent>      subspan( size_type Offset,              size_type Count = std::dynamic_extent ) const; | (2) | (since C++20) |
|  |  |  |

Obtains a span that is a view over the Count elements of this span starting at offset Offset. If Count is std::dynamic_extent, the number of elements in the subspan is size() - offset (i.e., it ends at the end of \*this).

1) Is ill-formed if

- Offset is greater than Extent, or
- Count is not std::dynamic_extent and Count is greater than Extent - Offset.

The behavior is undefined if either Offset or Count is out of range. This happens if

- Offset is greater than size(), or
- Count is not std::dynamic_extent and Count is greater than size() - Offset.

The extent `E` of the span returned by (1) is determined as follows:

- If Count is not std::dynamic_extent, Count;
- Otherwise, if `Extent` is not std::dynamic_extent, Extent - Offset;
- Otherwise, std::dynamic_extent.

### Return value

The requested subspan `r`, such that r.data() == this->data() + Offset. If Count is std::dynamic_extent, r.size() == this->size() - Offset; otherwise r.size() == Count.

### Example

Run this code

```
#include <algorithm>
#include <cstdio>
#include <numeric>
#include <ranges>
#include <span>
 
void display(std::span<const char> abc)
{
    const auto columns{20U};
    const auto rows{abc.size() - columns + 1};
 
    for (auto offset{0U}; offset < rows; ++offset)
    {
        std::ranges::for_each(abc.subspan(offset, columns), std::putchar);
        std::putchar('\n');
    }
}
 
int main()
{
    char abc[26];
    std::iota(std::begin(abc), std::end(abc), 'A');
    display(abc);
}

```

Output:

```
ABCDEFGHIJKLMNOPQRST
BCDEFGHIJKLMNOPQRSTU
CDEFGHIJKLMNOPQRSTUV
DEFGHIJKLMNOPQRSTUVW
EFGHIJKLMNOPQRSTUVWX
FGHIJKLMNOPQRSTUVWXY
GHIJKLMNOPQRSTUVWXYZ

```

### See also

|  |  |
| --- | --- |
| first | obtains a subspan consisting of the first `N` elements of the sequence   (public member function) |
| last | obtains a subspan consisting of the last `N` elements of the sequence   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/span/subspan&oldid=162015>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 November 2023, at 04:34.