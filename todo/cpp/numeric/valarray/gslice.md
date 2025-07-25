# std::gslice

From cppreference.com
< cpp‎ | numeric‎ | valarray
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

Numerics library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Mathematical special functions (C++17) | | | | |
| Mathematical constants (C++20) | | | | |
| Basic linear algebra algorithms (C++26) | | | | |
| Data-parallel types (SIMD) (C++26) | | | | |
| Floating-point environment (C++11) | | | | |
| Complex numbers | | | | |
| Numeric array (`valarray`) | | | | |
| Pseudo-random number generation | | | | |
| Bit manipulation (C++20) | | | | |
| Factor operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | gcd(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lcm(C++17) | | | | | |
| Interpolations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | midpoint(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lerp(C++20) | | | | | |
| Saturation arithmetic | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

std::valarray

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | [valarray::operator[]](operator_at.html "cpp/numeric/valarray/operator at") | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | ****gslice**** | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| class gslice; |  |  |
|  |  |  |

`std::gslice` is the selector class that identifies a subset of std::valarray indices defined by a multi-level set of strides and sizes. Objects of type `std::gslice` can be used as indices with valarray's operator[] to select, for example, columns of a multidimensional array represented as a `valarray`.

Given the starting value s, a list of strides ij and a list of sizes dj, a `std::gslice` constructed from these values selects the set of indices kj=s+Σj(ijdj).

For example, a gslice with starting index `3`, strides `{19,4,1`} and lengths `{2,4,3`} generates the following set of `24=2*4*3` indices:

3 + 0\*19 + 0\*4 + 0\*1 = 3,  
3 + 0\*19 + 0\*4 + 1\*1 = 4,  
3 + 0\*19 + 0\*4 + 2\*1 = 5,  
3 + 0\*19 + 1\*4 + 0\*1 = 7,  
3 + 0\*19 + 1\*4 + 1\*1 = 8,  
3 + 0\*19 + 1\*4 + 2\*1 = 9,  
3 + 0\*19 + 2\*4 + 0\*1 = 11,  
...  
3 + 1\*19 + 3\*4 + 1\*1 = 35,  
3 + 1\*19 + 3\*4 + 2\*1 = 36

It is possible to construct `std::gslice` objects that select some indices more than once: if the above example used the strides `{1,1,1}`, the indices would have been `{3, 4, 5, 4, 5, 6, ...}`. Such gslices may only be used as arguments to the const version of [`std::valarray::operator[]`](operator_at.html "cpp/numeric/valarray/operator at"), otherwise the behavior is undefined.

### Member functions

|  |  |
| --- | --- |
| ****(constructor)**** | constructs a generic slice   (public member function) |
| ****startsizestride**** | returns the parameters of the slice   (public member function) |

## std::gslice::gslice

|  |  |  |
| --- | --- | --- |
| gslice() | (1) |  |
| gslice( std::size_t start, const std::valarray<std::size_t>& sizes,                             const std::valarray<std::size_t>& strides ); | (2) |  |
| gslice( const gslice& other ); | (3) |  |
|  |  |  |

Constructs a new generic slice.

1) Default constructor. Equivalent to gslice(0, std::valarray<std::size_t>(), std::valarray<std::size_t>()). This constructor exists only to allow construction of arrays of slices.2) Constructs a new slice with parameters start, sizes, strides.3) Constructs a copy of other.

### Parameters

|  |  |  |
| --- | --- | --- |
| start | - | the position of the first element |
| sizes | - | an array that defines the number of elements in each dimension |
| strides | - | an array that defines the number of positions between successive elements in each dimension |
| other | - | another slice to copy |

## std::slice::start, size, stride

|  |  |  |
| --- | --- | --- |
| std::size_t start() const; | (1) |  |
| std::valarray<std::size_t> size() const; | (2) |  |
| std::valarray<std::size_t> stride() const; | (3) |  |
|  |  |  |

Returns the parameters passed to the slice on construction - start, sizes and strides respectively.

### Parameters

(none)

### Return value

The parameters of the slice -- start, sizes and strides respectively.

### Complexity

Constant.

### Example

Demonstrates the use of gslices to address columns of a 3D array:

Run this code

```
#include <iostream>
#include <valarray>
 
void test_print(std::valarray<int>& v, int planes, int rows, int cols)
{
    for (int r = 0; r < rows; ++r)
    {
        for (int z = 0; z < planes; ++z)
        {
            for (int c = 0; c < cols; ++c)
                std::cout << v[z * rows * cols + r * cols + c] << ' ';
            std::cout << "  ";
        }
        std::cout << '\n';
    }
}
 
int main()
{
    std::valarray<int> v = // 3d array: 2 x 4 x 3 elements
        {111,112,113 , 121,122,123 , 131,132,133 , 141,142,143,
         211,212,213 , 221,222,223 , 231,232,233 , 241,242,243};
    // int ar3d[2][4][3]
    std::cout << "Initial 2x4x3 array:\n";
    test_print(v, 2, 4, 3);
 
    // update every value in the first columns of both planes
    v[std::gslice(0, {2, 4}, {4 * 3, 3})] = 1; // two level one strides of 12 elements
                                               // then four level two strides of 3 elements
 
    // subtract the third column from the second column in the 1st plane
    v[std::gslice(1, {1, 4}, {4 * 3, 3})] -= v[std::gslice(2, {1, 4}, {4 * 3, 3})];
 
    std::cout << "\n" "After column operations:\n";
    test_print(v, 2, 4, 3);
}

```

Output:

```
Initial 2x4x3 array:
111 112 113   211 212 213
121 122 123   221 222 223
131 132 133   231 232 233
141 142 143   241 242 243
 
After column operations:
1 -1 113   1 212 213
1 -1 123   1 222 223
1 -1 133   1 232 233
1 -1 143   1 242 243

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 543 | C++98 | it was unclear whether a default constructed generic slice is usable | it is usable (as an empty subset) |

### See also

|  |  |
| --- | --- |
| [operator[]](operator_at.html "cpp/numeric/valarray/operator at") | get/set valarray element, slice, or mask   (public member function) |
| slice | BLAS-like slice of a valarray: starting index, length, stride   (class) |
| gslice_array | proxy to a subset of a valarray after applying a gslice   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/gslice&oldid=148641>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 February 2023, at 01:12.