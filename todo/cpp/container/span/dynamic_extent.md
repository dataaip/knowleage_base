# std::dynamic_extent

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
| span::subspan | | | | |
| Non-member functions | | | | |
| as_bytesas_writable_bytes | | | | |
| Non-member constant | | | | |
| ****dynamic_extent**** | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<span>` |  |  |
| inline constexpr std::size_t dynamic_extent = std::numeric_limits<std::size_t>::max(); |  | (since C++20) |
|  |  |  |

`std::dynamic_extent` is a constant of type std::size_t that is generally used to indicate that any type using `std::dynamic_extent` will **dynamically** store its value (e.g., size) rather than having the value **statically** known in the type.

It is being used in several contexts:

- To differentiate std::span of static and dynamic extent.

|  |  |
| --- | --- |
| - To indicate that the extent at a certain rank index will be stored dynamically in std::extents. | (since C++23) |

|  |  |
| --- | --- |
| - To indicate that the padded layouts for std::mdspan will dynamically store its padding value. | (since C++26) |

### Note

Since std::size_t is an unsigned type, an equivalent definition is:

```
inline constexpr std::size_t dynamic_extent = -1;

```

See integral conversions.

### Example

Run this code

```
#include <array>
#include <cassert>
#include <cstddef>
#include <iostream>
#include <span>
#include <string_view>
#include <vector>
 
int main()
{
    auto print = [](std::string_view const name, std::size_t ex)
    {
        std::cout << name << ", ";
        if (std::dynamic_extent == ex)
            std::cout << "dynamic extent\n";
        else
            std::cout << "static extent = " << ex << '\n';
    };
 
    int a[]{1, 2, 3, 4, 5};
 
    std::span span1{a};
    print("span1", span1.extent);
 
    std::span<int, std::dynamic_extent> span2{a};
    print("span2", span2.extent);
 
    std::array ar{1, 2, 3, 4, 5};
    std::span span3{ar};
    print("span3", span3.extent);
 
    std::vector v{1, 2, 3, 4, 5};
    std::span span4{v};
    print("span4", span4.extent);
}

```

Output:

```
span1, static extent = 5
span2, dynamic extent
span3, static extent = 5
span4, dynamic extent

```

### See also

|  |  |
| --- | --- |
| span(C++20) | a non-owning view over a contiguous sequence of objects   (class template) |
| extents(C++23) | a descriptor of a multidimensional index space of some rank   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/span/dynamic_extent&oldid=170829>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 April 2024, at 21:35.