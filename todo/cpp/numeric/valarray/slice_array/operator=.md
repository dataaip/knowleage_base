# std::slice_array<T>::operator=

From cppreference.com
< cpp‎ | numeric‎ | valarray‎ | slice array
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | [valarray::operator[]](../operator_at.html "cpp/numeric/valarray/operator at") | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

std::slice_array

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| slice_array::slice_array | | | | |
| slice_array::~slice_array | | | | |
| ****slice_array::operator=**** | | | | |
| slice_array::operator+=slice_array::operator-=slice_array::operator\*=slice_array::operator/=slice_array::operator%=slice_array::operator&=slice_array::operator|=slice_array::operator^=slice_array::operator<<=slice_array::operator>>= | | | | |

|  |  |  |
| --- | --- | --- |
| void operator=( const T& value ) const; | (1) |  |
| void operator=( const std::valarray<T>& val_arr ) const; | (2) |  |
| const slice_array& operator=( const slice_array& other_arr ) const; | (3) |  |
|  |  |  |

Assigns values to all referred elements.

1) Assigns value to all of the elements.2) Assigns the elements of val_arr to the referred to elements of \*this.3) Assigns the selected elements from other_arr to the referred to elements of \*this.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | a value to assign to all of the referred elements |
| val_arr | - | std::valarray to assign |
| other_arr | - | std::slice_array to assign |

### Return value

1,2) (none)3) \*this

### Example

Run this code

```
#include <iostream>
#include <valarray>
 
void print(char const* remark, std::valarray<int> const& v = {})
{
    std::cout << remark;
    if (v.size() != 0)
    {
        std::cout << ':';
        for (int e : v)
            std::cout << ' ' << e;
    }
    std::cout << '\n';
}
 
int main()
{
    std::valarray<int> v1{1, 2, 3, 4, 5, 6, 7, 8};
    std::slice_array<int> s1 = v1[std::slice(1, 4, 2)];
    print("v1", v1);
    print("s1", s1);
 
    print("\n(1) operator=( const T& )");
    print("s1 = 42");
    s1 = 42; // (1)
    print("s1", s1);
    print("v1", v1);
 
    print("\n(2) operator=( const std::valarray<T>& )");
    std::valarray<int> v2{10, 11, 12, 13, 14, 15};
    print("v2", v2);
    print("s1 = v2");
    s1 = v2; // (2)
    print("s1", s1);
    print("v1", v1);
 
    print("\n(3) operator=( const slice_array& )");
    v1 = {1, 2, 3, 4, 5, 6, 7, 8};
    std::slice_array<int> s2 = v1[std::slice(0, 4, 1)];
    std::slice_array<int> s3 = v2[std::slice(1, 4, 1)];
    print("v1", v1);
    print("v2", v2);
    print("s2", s2);
    print("s3", s3);
    print("s2 = s3");
    s2 = s3; // (3) Note: LHS and RHS must have same size.
    print("s2", s2);
    print("v1", v1);
}

```

Output:

```
v1: 1 2 3 4 5 6 7 8
s1: 2 4 6 8
 
(1) operator=( const T& )
s1 = 42
s1: 42 42 42 42
v1: 1 42 3 42 5 42 7 42
 
(2) operator=( const std::valarray<T>& )
v2: 10 11 12 13 14 15
s1 = v2
s1: 10 11 12 13
v1: 1 10 3 11 5 12 7 13
 
(3) operator=( const slice_array& )
v1: 1 2 3 4 5 6 7 8
v2: 10 11 12 13 14 15
s2: 1 2 3 4
s3: 11 12 13 14
s2 = s3
s2: 11 12 13 14
v1: 11 12 13 14 5 6 7 8

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 123 | C++98 | overload (2) was non-const | made const |
| LWG 253 | C++98 | the copy assignment operator was private | made public |
| LWG 621 | C++98 | the copy assignment operator was non-const | made const |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/slice_array/operator%3D&oldid=120737>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 July 2020, at 07:16.