# std::strided_slice

From cppreference.com
< cpp‎ | container‎ | mdspan
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

std::mdspan

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | mdspan::mdspan | | | | | | mdspan::operator= | | | | | | Element access | | | | | | [mdspan::operator[]](operator_at.html "cpp/container/mdspan/operator at") | | | | | | Observers | | | | | | mdspan::rank | | | | | | mdspan::rank_dynamic | | | | | | mdspan::static_extent | | | | | | mdspan::extent | | | | | | mdspan::size | | | | | | mdspan::empty | | | | | | mdspan::stride | | | | | | mdspan::extents | | | | | | mdspan::data_handle | | | | | | mdspan::mapping | | | | | | mdspan::accessor | | | | | | mdspan::is_uniquemdspan::is_exhaustivemdspan::is_stridedmdspan::is_always_uniquemdspan::is_always_exhaustivemdspan::is_always_strided | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-member functions | | | | | | swap(std::mdspan) | | | | | | Subviews | | | | | | submdspan")(C++26) | | | | | | submdspan_extents")(C++26) | | | | | | Helper types and templates | | | | | | extentsdextents | | | | | | dims(C++26) | | | | | | default_accessor | | | | | | aligned_accessor")(C++26) | | | | | | Layout mapping policies | | | | | | layout_left | | | | | | layout_right | | | | | | layout_stride | | | | | | layout_left_padded(C++26) | | | | | | layout_right_padded(C++26) | | | | | | Subviews helpers | | | | | | full_extent(C++26) | | | | | | ****strided_slice****(C++26) | | | | | | submdspan_mapping_result(C++26) | | | | | | Deduction guides | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<mdspan>` |  |  |
| template< class OffsetType, class ExtentType, class StrideType >  struct strided_slice; |  | (since C++26) |
|  |  |  |

An instance of every specialization of `strided_slice` is a slice specifier used in std::submdspan to select a subset of elements using a set of regularly spaced indices at a specified dimension in `std::mdspan`.

Each `strided_slice` object s is characterized by three data members: the offset index s.offset, the extent s.extent, and the stride s.stride.

Given that s.stride is greater than zero, the number of selected indices denoted by N is determined by 1 + (s.extent - 1) / s.stride if s.extent is nonzero, otherwise ​0​. The half-open interval from which indices will be selected is given by ``s.offset`,`s.offset + s.extent`)`. The sequence of selected indices is produced as follows: s.offset, ..., s.offset + (N - 1) \* s.stride.

This class template has no base classes or declared members other than those shown below.

### Template parameters

|  |  |  |
| --- | --- | --- |
| OffsetType | - | the type of offset |
| ExtentType | - | the type of extent |
| StrideType | - | the type of stride |
| Type requirements | | |
| -All template parameters must be unsigned or signed integer types or must satisfy [**integral-constant-like** | | |

The program is ill-formed if the type requirement is not satisfied.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `offset_type` | `OffsetType` |
| `extent_type` | `ExtentType` |
| `stride_type` | `StrideType` |

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| offset | a starting index of type `offset_type`   (public member object) |
| extent | a value of type `extent_type` added to offset used to define the upper bound of indices   (public member object) |
| stride | an increment value of type `stride_type` which is equivalent to the distance between two indices   (public member object) |

All these members are declared with `[[no_unique_address]]` attribute and have default member initializers where each data member is value initialized.

### Notes

Every specialization of `strided_slice` is an aggregate class which allows aggregate initialization (including designated initialization) of data members (for instance, std::strided_slice{.offset = 2, .extent = 10, .stride = 3}).

The slice specification of `strided_slice` takes advantage of the data member extent, as opposed to other slice specifications that use end to indicate the upper bound value. This is because it can directly generate a static extent for subview of std::mdspan if both extent and stride are of types that satisfy **integral-constant-like**. This enables efficient extraction of subviews with static extents by mixing compile time values with a runtime value of `offset`.

### Example

Run this code

```
#include <mdspan>
#include <print>
 
template <typename View, typename O = int, typename E = int, typename S = int>
    requires (View::extents_type::rank() == 1)
void print_sliced_view(View v, std::strided_slice<O, E, S> s)
{
    using index_type = View::index_type;
    auto subview = std::submdspan(v, s);
    const auto& submap = subview.mapping();
 
    std::print("[");
    bool uses_comma = false;
    for (index_type i = 0; i != subview.extent(0); ++i)
    {
        if (uses_comma)
            std::print(", ");
        std::print("{}", subview[i]);
        uses_comma = true;
    }
    uses_comma = false;
    std::print("] extracted from indices [");
    for (index_type i = 0; i != subview.extent(0); ++i)
    {
        if (uses_comma)
            std::print(", ");
        std::print("{}", submap(i) + s.offset);
        uses_comma = true;
    }
    std::println("]");
}
 
int main()
{
    static constexpr char letters[]
    {
        'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J',
        'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T',
        'U', 'V', 'W', 'X', 'Y', 'Z'
    };
    constexpr std::mdspan md(letters, 26);
    print_sliced_view(md, {.offset = 0, .extent = 10, .stride = 1});
    print_sliced_view(md, {.offset = 2, .extent = 10, .stride = 1});
    print_sliced_view(md, {.offset = 0, .extent = 5,  .stride = 1});
    print_sliced_view(md, {.offset = 2, .extent = 5,  .stride = 1});
    print_sliced_view(md, {.offset = 0, .extent = 10, .stride = 2});
    print_sliced_view(md, {.offset = 2, .extent = 10, .stride = 3});
    print_sliced_view(md, {.offset = 0, .extent = 15, .stride = 5});
    print_sliced_view(md, {.offset = 6, .extent = 15, .stride = 5});
}

```

Output:

```
[A, B, C, D, E, F, G, H, I, J] extracted from indices [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[C, D, E, F, G, H, I, J, K, L] extracted from indices [2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
[A, B, C, D, E] extracted from indices [0, 1, 2, 3, 4]
[C, D, E, F, G] extracted from indices [2, 3, 4, 5, 6]
[A, C, E, G, I] extracted from indices [0, 2, 4, 6, 8]
[C, F, I, L] extracted from indices [2, 5, 8, 11]
[A, F, K] extracted from indices [0, 5, 10]
[G, L, Q] extracted from indices [6, 11, 16]

```

### See also

|  |  |
| --- | --- |
| slice | BLAS-like slice of a valarray: starting index, length, stride   (class) |
| submdspan")(C++26) | returns a view of a subset of an existing `mdspan`   (function template) |

|  |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan/strided_slice&oldid=173448>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 July 2024, at 00:05.