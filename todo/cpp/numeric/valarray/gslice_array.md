# std::gslice_array

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | ****gslice_array**** | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

****std::gslice_array****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| gslice_array::gslice_array | | | | |
| gslice_array::~gslice_array | | | | |
| gslice_array::operator= | | | | |
| gslice_array::operator+=gslice_array::operator-=gslice_array::operator\*=gslice_array::operator/=gslice_array::operator%=gslice_array::operator&=gslice_array::operator|=gslice_array::operator^=gslice_array::operator<<=gslice_array::operator>>= | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >  class gslice_array; |  |  |
|  |  |  |

`std::gslice_array` is a helper template used by the valarray subscript operator with std::gslice argument. It has reference semantics to a subset of the array specified by the std::gslice object.

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `value_type` | `T` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `gslice_array`   (public member function) |
| (destructor) | destroys a `gslice_array`   (public member function) |
| operator= | assigns contents   (public member function) |
| operator+=operator-=operator\*=operator/=operator%=operator&=operator|=operator^=operator<<=operator>>= | performs arithmetic operation on the array referred by generic slice.   (public member function) |

### Example

Run this code

```
#include <cassert>
#include <cstddef>
#include <iomanip>
#include <iostream>
#include <numeric>
#include <valarray>
 
int main()
{
    std::valarray<int> data(32);
    std::iota(std::begin(data), std::end(data), 0);
 
    const std::size_t offset = 1, z = 2, y = 3, x = 4;
    const std::valarray<std::size_t> sizes{z, y, x};
    const std::valarray<std::size_t> strides{15, 5, 1};
    const std::gslice gslice = std::gslice(offset, sizes, strides);
    // Indices are generated according to the formula:
    // index[k] = offset + [0,1,2)*15 + [0,1,2,3)*5 + [0,1,2,3,4)*1
    //          = offset + inner_product(sizes[k], strides);
    // where sizes[k] = {[0,z), [0,y), [0,x)}, while the rightmost index (x)
    // runs fastest. As a result we have following set of indices:
    //  index[0]  = 1 + 0*15 + 0*5 + 0*1 = 1
    //  index[1]  = 1 + 0*15 + 0*5 + 1*1 = 2
    //  index[2]  = 1 + 0*15 + 0*5 + 2*1 = 3
    //  index[3]  = 1 + 0*15 + 0*5 + 3*1 = 4
    //  index[4]  = 1 + 0*15 + 1*5 + 0*1 = 6
    //  index[5]  = 1 + 0*15 + 1*5 + 1*1 = 7
    //  index[6]  = 1 + 0*15 + 1*5 + 2*1 = 8
    //  index[7]  = 1 + 0*15 + 1*5 + 3*1 = 9
    //  ...
    //  index[22] = 1 + 1*15 + 2*5 + 2*1 = 28
    //  index[23] = 1 + 1*15 + 2*5 + 3*1 = 29
 
    const std::valarray<int> indices = data[gslice];
    for (unsigned i = 0; i != indices.size(); ++i)
        std::cout << std::setfill('0') << std::setw(2) << indices[i] << ' ';
    std::cout << "\nTotal indices: " << indices.size() << '\n';
    assert(indices.size() == x * y * z);
 
    data = 0;
    std::gslice_array<int> gslice_array = data[gslice];
    gslice_array = 1;
    // Cells that correspond to generated indices = '1', skipped cells = '0'.
    for (auto i : data)
        std::cout << i << ' ';
    std::cout << "\nSum of ones = " << data.sum() << '\n';
}

```

Output:

```
01 02 03 04 06 07 08 09 11 12 13 14 16 17 18 19 21 22 23 24 26 27 28 29 
Total indices: 24
0 1 1 1 1 0 1 1 1 1 0 1 1 1 1 0 1 1 1 1 0 1 1 1 1 0 1 1 1 1 0 0 
Sum of ones = 24

```

### See also

|  |  |
| --- | --- |
| slice_array | proxy to a subset of a valarray after applying a slice   (class template) |
| mdspan(C++23) | a multi-dimensional non-owning array view   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/gslice_array&oldid=178691>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2024, at 15:40.