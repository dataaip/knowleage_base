# std::span<T,Extent>::last

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
| ****span::last**** | | | | |
| span::subspan | | | | |
| Non-member functions | | | | |
| as_bytesas_writable_bytes | | | | |
| Non-member constant | | | | |
| dynamic_extent | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< std::size_t Count >  constexpr std::span<element_type, Count> last() const; | (1) | (since C++20) |
| constexpr std::span<element_type, std::dynamic_extent> last( size_type Count ) const; | (2) | (since C++20) |
|  |  |  |

Obtains a span that is a view over the last Count elements of this span. The program is ill-formed if Count > Extent. The behavior is undefined if Count > size().

### Return value

A span `r` that is a view over the last Count elements of \*this, such that r.data() == this->data() + (this->size() - Count) && r.size() == Count.

### Example

Run this code

```
#include <iostream>
#include <span>
#include <string_view>
 
void println(std::string_view const title, auto const& container)
{
    std::cout << title << '[' << std::size(container) << "]{ ";
    for (auto const& elem : container)
        std::cout << elem << ", ";
    std::cout << "};\n";
};
 
void run(std::span<const int> span)
{
    println("span: ", span);
 
    std::span<const int, 3> span_last = span.last<3>();
    println("span.last<3>(): ", span_last);
 
    std::span<const int, std::dynamic_extent> span_last_dynamic = span.last(2);
    println("span.last(2): ", span_last_dynamic);
}
 
int main()
{
    int a[8]{1, 2, 3, 4, 5, 6, 7, 8};
    println("int a", a);
    run(a);
}

```

Output:

```
int a[8]{ 1, 2, 3, 4, 5, 6, 7, 8, };
span: [8]{ 1, 2, 3, 4, 5, 6, 7, 8, };
span.last<3>(): [3]{ 6, 7, 8, };
span.last(2): [2]{ 7, 8, };

```

### See also

|  |  |
| --- | --- |
| first | obtains a subspan consisting of the first `N` elements of the sequence   (public member function) |
| subspan | obtains a subspan   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/span/last&oldid=162036>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 November 2023, at 07:36.