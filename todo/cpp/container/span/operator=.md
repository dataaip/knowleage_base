# std::span<T,Extent>::operator=

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
| ****span::operator=**** | | | | |
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
| dynamic_extent | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr span& operator=( const span& other ) noexcept = default; |  | (since C++20) |
|  |  |  |

Assigns other to \*this. This defaulted assignment operator performs a shallow copy of the data pointer and the size, i.e., after a call to this function, data() == other.data() and size() == other.size().

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another span to copy from |

### Return value

\*this

### Example

Run this code

```
#include <algorithm>
#include <array>
#include <cassert>
#include <cstddef>
#include <iostream>
#include <span>
#include <string_view>
 
void print(std::string_view info = "", std::span<const int> span = {},
           std::size_t extent = 0, std::size_t size_of = 0)
{
    if (span.empty())
    {
        std::cout << info << '\n';
        return;
    }
 
    std::cout << info << '[' << span.size() << "] {";
    std::ranges::for_each(span, [](const int x) { std::cout << ' ' << x; });
    std::cout << " }";
 
    if (extent)
    {
        std::cout << " extent = ";
        if (extent == std::dynamic_extent)
            std::cout << "dynamic";
        else
            std::cout << extent;
    }
 
    if (size_of)
        std::cout << ", sizeof = " << size_of;
 
    std::cout << '\n';
}
 
int main()
{
    std::array<int,6> a1;
    std::array<int,6> a2;
    a1.fill(3);
    a2.fill(4);
 
    auto s1 = std::span(a1);
    auto s2 = std::span(a2);
    print("s1", s1, s1.extent, sizeof(s1));
    print("s2", s2, s2.extent, sizeof(s2));
 
    // Check that assignment performs a shallow copy.
    s1 = s2;
    (s1.data() == s2.data() && s1.size() == s2.size())
        ? print("s1 = s2; is a shallow copy!")
        : print("s1 = s2; is a deep copy!");
    print("s1", s1);
 
    print("Fill s1 with 5:");
    std::ranges::fill(s1, 5);
    // s2 is also 'updated' since s1 and s2 point to the same data
    assert(std::ranges::equal(s1, s2));
    print("s1", s1);
    print("s2", s2);
    print();
 
    int a3[]{1, 2, 3, 4};
    int a4[]{2, 3, 4, 5};
    int a5[]{3, 4, 5};
 
    std::span<int, std::dynamic_extent> dynamic_1{a3};
    std::span<int, std::dynamic_extent> dynamic_2{a4, 3};
    std::span<int, 4> static_1{a3};
    std::span<int, 4> static_2{a4};
    std::span<int, 3> static_3{a5};
 
    print("dynamic_1", dynamic_1, dynamic_1.extent, sizeof(dynamic_1));
    print("dynamic_2", dynamic_2, dynamic_2.extent, sizeof(dynamic_2));
    print("static_1", static_1, static_1.extent, sizeof(static_1));
    print("static_2", static_2, static_2.extent, sizeof(static_2));
    print("static_3", static_3, static_3.extent, sizeof(static_3));
 
    dynamic_1 = dynamic_2; // OK
    dynamic_1 = static_1;  // OK
//  static_1 = dynamic_1;  // ERROR: no match for ‘operator=’
    static_1 = static_2;   // OK: same extents = 4
//  static_1 = static_3;   // ERROR: different extents: 4 and 3
}

```

Output:

```
s1[6] { 3 3 3 3 3 3 } extent = 6, sizeof = 8
s2[6] { 4 4 4 4 4 4 } extent = 6, sizeof = 8
s1 = s2; is a shallow copy!
s1[6] { 4 4 4 4 4 4 }
Fill s1 with 5:
s1[6] { 5 5 5 5 5 5 }
s2[6] { 5 5 5 5 5 5 }
 
dynamic_1[4] { 1 2 3 4 } extent = dynamic, sizeof = 16
dynamic_2[3] { 2 3 4 } extent = dynamic, sizeof = 16
static_1[4] { 1 2 3 4 } extent = 4, sizeof = 8
static_2[4] { 2 3 4 5 } extent = 4, sizeof = 8
static_3[3] { 3 4 5 } extent = 3, sizeof = 8

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs the `span`   (public member function) |
| data | direct access to the underlying contiguous storage   (public member function) |
| size | returns the number of elements   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/span/operator%3D&oldid=166668>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2023, at 14:08.