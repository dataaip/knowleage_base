# std::mdspan

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
| ****mdspan****(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

****std::mdspan****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | mdspan::mdspan | | | | | | mdspan::operator= | | | | | | Element access | | | | | | [mdspan::operator[]](mdspan/operator_at.html "cpp/container/mdspan/operator at") | | | | | | Observers | | | | | | mdspan::rank | | | | | | mdspan::rank_dynamic | | | | | | mdspan::static_extent | | | | | | mdspan::extent | | | | | | mdspan::size | | | | | | mdspan::empty | | | | | | mdspan::stride | | | | | | mdspan::extents | | | | | | mdspan::data_handle | | | | | | mdspan::mapping | | | | | | mdspan::accessor | | | | | | mdspan::is_uniquemdspan::is_exhaustivemdspan::is_stridedmdspan::is_always_uniquemdspan::is_always_exhaustivemdspan::is_always_strided | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-member functions | | | | | | swap(std::mdspan) | | | | | | Subviews | | | | | | submdspan")(C++26) | | | | | | submdspan_extents")(C++26) | | | | | | Helper types and templates | | | | | | extentsdextents | | | | | | dims(C++26) | | | | | | default_accessor | | | | | | aligned_accessor")(C++26) | | | | | | Layout mapping policies | | | | | | layout_left | | | | | | layout_right | | | | | | layout_stride | | | | | | layout_left_padded(C++26) | | | | | | layout_right_padded(C++26) | | | | | | Subviews helpers | | | | | | full_extent(C++26) | | | | | | strided_slice(C++26) | | | | | | submdspan_mapping_result(C++26) | | | | | | Deduction guides | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<mdspan>` |  |  |
| template<  class T,      class Extents,      class LayoutPolicy = std::layout_right,      class AccessorPolicy = std::default_accessor<T> > class mdspan; |  | (since C++23) |
|  |  |  |

`std::mdspan` is a multidimensional array view that maps a multidimensional index to an element of the array. The mapping and element access policies are configurable, and the underlying array need not be contiguous or even exist in memory at all.

Each specialization `MDS` of `mdspan` models `copyable` and satisfies:

:   - std::is_nothrow_move_constructible_v<MDS> is true,
    - std::is_nothrow_move_assignable_v<MDS> is true, and
    - std::is_nothrow_swappable_v<MDS> is true.

A specialization of `mdspan` is a TriviallyCopyable type if its `accessor_type`, `mapping_type` and `data_handle_type` are TriviallyCopyable types.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | element type; a complete object type that is neither an abstract class type nor an array type. |
| Extents | - | specifies number of dimensions, their sizes, and which are known at compile time. Must be a specialization of std::extents. |
| LayoutPolicy | - | specifies how to convert multidimensional index to underlying 1D index (column-major 3D array, symmetric triangular 2D matrix, etc). Must satisfy the requirements of LayoutMappingPolicy. |
| AccessorPolicy | - | specifies how to convert underlying 1D index to a reference to T. Must satisfy the constraint that std::is_same_v<T, typename AccessorPolicy​::​element_type> is true. Must satisfy the requirements of AccessorPolicy. |

### Member types

|  |  |
| --- | --- |
| Member | Definition |
| `extents_type` | `Extents` |
| `layout_type` | `LayoutPolicy` |
| `accessor_type` | `AccessorPolicy` |
| `mapping_type` | LayoutPolicy::mapping<Extents> |
| `element_type` | `T` |
| `value_type` | std::remove_cv_t<T> |
| `index_type` | Extents::index_type |
| `size_type` | Extents::size_type |
| `rank_type` | Extents::rank_type |
| `data_handle_type` | AccessorPolicy::data_handle_type |
| `reference` | AccessorPolicy::reference |

### Data members

|  |  |
| --- | --- |
| Member | Description |
| `accessor_type` `acc_` (private) | the accessor (exposition-only member object\*) |
| `mapping_type` `map_` (private) | the layout mapping (exposition-only member object\*) |
| `data_handle_type` `ptr_` (private) | the underlying data handle (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an `mdspan`   (public member function) |
| operator= | assigns an `mdspan`   (public member function) |
| Element access | |
| [operator[]](mdspan/operator_at.html "cpp/container/mdspan/operator at") | accesses an element at the specified multidimensional index   (public member function) |
| Observers | |
| rank[static] | returns the rank of a `mdspan`   (public static member function) |
| rank_dynamic[static] | returns the dynamic rank of a `mdspan`   (public static member function) |
| static_extent[static] | returns the static extent size of a `mdspan` at a given rank index   (public static member function) |
| extent | returns the extent of a `mdspan` at a given rank index   (public member function) |
| size | returns the size of the multidimensional index space   (public member function) |
| empty | checks if the size of the index space is zero   (public member function) |
| stride | obtains the stride along the specified dimension   (public member function) |
| extents | obtains the extents object   (public member function) |
| data_handle | obtains the pointer to the underlying 1D sequence   (public member function) |
| mapping | obtains the mapping object   (public member function) |
| accessor | obtains the accessor policy object   (public member function) |
| is_unique | determines if this mdspan's mapping is unique (every combination of indices maps to a different underlying element)   (public member function) |
| is_exhaustive | determines if this mdspan's mapping is exhaustive (every underlying element can be accessed with some combination of indices)   (public member function) |
| is_strided | determines if this mdspan's mapping is strided (in each dimension, incrementing an index jumps over the same number of underlying elements every time)   (public member function) |
| is_always_unique[static] | determines if this mdspan's layout mapping is always unique   (public static member function) |
| is_always_exhaustive[static] | determines if this mdspan's layout mapping is always exhaustive   (public static member function) |
| is_always_strided[static] | determines if this mdspan's layout mapping is always strided   (public static member function) |

### Non-member functions

|  |  |
| --- | --- |
| std::swap(std::mdspan)(C++23) | specializes the std::swap algorithm for mdspan   (function template) |
| Subviews | |
| submdspan")(C++26) | returns a view of a subset of an existing `mdspan`   (function template) |
| submdspan_extents")(C++26) | creates new extents from the existing extents and slice specifiers   (function template) |

### Helper types and templates

|  |  |
| --- | --- |
| extents(C++23) | a descriptor of a multidimensional index space of some rank   (class template) |
| dextentsdims(C++23)(C++26) | convenience alias template for an all-dynamic std::extents (alias template) |
| default_accessor(C++23) | a type for indexed access to elements of `mdspan`   (class template) |
| aligned_accessor")(C++26) | a type for aligned access to elements of `mdspan`   (class template) |
| Layout mapping policies | |
| layout_left(C++23) | column-major multidimensional array layout mapping policy; leftmost extent has stride `1`   (class) |
| layout_right(C++23) | row-major multidimensional array layout mapping policy; rightmost extent has stride `1`   (class) |
| layout_stride(C++23) | a layout mapping policy with user-defined strides   (class) |
| layout_left_padded(C++26) | column-major layout mapping policy with padding stride that can be greater than or equal to the leftmost extent   (class template) |
| layout_right_padded(C++26) | row-major layout mapping policy with padding stride that can be greater than or equal to the rightmost extent   (class template) |
| Subviews helpers | |
| full_extentfull_extent_t(C++26) | a slice specifier tag describing full range of indices in the specified extent. (tag) |
| strided_slice(C++26) | a slice specifier representing a set of regularly spaced indices as indicated by an offset, an extent, and a stride   (class template) |
| submdspan_mapping_result(C++26) | a return type of the overloads of `submdspan_mapping`   (class template) |

### Deduction guides

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_mdspan` | `202207L` | (C++23) | `std::mdspan` |
| `__cpp_lib_submdspan` | `202306L` | (C++26) | std::submdspan |
| `202403L` | (C++26) | `std::mdspan` padded layouts |
| `__cpp_lib_aligned_accessor` | `202411L` | (C++26) | std::aligned_accessor |

### Example

Can be previewed on Compiler Explorer.

Run this code

```
#include <cstddef>
#include <mdspan>
#include <print>
#include <vector>
 
int main()
{
    std::vector v{1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12};
 
    // View data as contiguous memory representing 2 rows of 6 ints each
    auto ms2 = std::mdspan(v.data(), 2, 6);
    // View the same data as a 3D array 2 x 3 x 2
    auto ms3 = std::mdspan(v.data(), 2, 3, 2);
 
    // Write data using 2D view
    for (std::size_t i = 0; i != ms2.extent(0); i++)
        for (std::size_t j = 0; j != ms2.extent(1); j++)
            ms2[i, j] = i * 1000 + j;
 
    // Read back using 3D view
    for (std::size_t i = 0; i != ms3.extent(0); i++)
    {
        std::println("slice @ i = {}", i);
        for (std::size_t j = 0; j != ms3.extent(1); j++)
        {
            for (std::size_t k = 0; k != ms3.extent(2); k++)
                std::print("{} ", ms3[i, j, k]);
            std::println("");
        }
    }
}

```

Output:

```
slice @ i = 0
0 1
2 3
4 5
slice @ i = 1
1000 1001
1002 1003
1004 1005

```

### See also

|  |  |
| --- | --- |
| span(C++20) | a non-owning view over a contiguous sequence of objects   (class template) |
| valarray | numeric arrays, array masks and array slices   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan&oldid=180236>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 February 2025, at 14:43.