# std::cosh(std::valarray)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | ****cosh**** | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >  valarray<T> cosh( const valarray<T>& va ); |  |  |
|  |  |  |

For each element in va computes hyperbolic cosine of the value of the element.

### Parameters

|  |  |  |
| --- | --- | --- |
| va | - | value array to apply the operation to |

### Return value

Value array containing hyperbolic cosine of the values in va.

### Notes

Unqualified function (cosh) is used to perform the computation. If such function is not available, std::cosh is used due to argument-dependent lookup.

The function can be implemented with the return type different from std::valarray. In this case, the replacement type has the following properties:

:   - All const member functions of std::valarray are provided.
    - std::valarray, std::slice_array, std::gslice_array, std::mask_array and std::indirect_array can be constructed from the replacement type.
    - For every function taking a const std::valarray<T>& except begin() and end()(since C++11), identical functions taking the replacement types shall be added;
    - For every function taking two const std::valarray<T>& arguments, identical functions taking every combination of const std::valarray<T>& and replacement types shall be added.
    - The return type does not add more than two levels of template nesting over the most deeply-nested argument type.

### Possible implementation

|  |
| --- |
| ```text template<class T> valarray<T> cosh(const valarray<T>& va) {     valarray<T> other = va;     for (T& i : other)         i = cosh(i);       return other; // proxy object may be returned } ``` |

### Example

Run this code

```
#include <cmath>
#include <iomanip>
#include <iostream>
#include <valarray>
 
void show(const char* title, const std::valarray<float>& data)
{
    const int w{9};
    std::cout << std::setw(w) << title << " | ";
    for (float x : data)
        std::cout << std::setw(w) << x << " | ";
    std::cout << '\n';
}
 
int main()
{
    const std::valarray<float> x{.1, .2, .3, .4};
    const auto sinh = std::sinh(x);
    const auto cosh = std::cosh(x);
    const auto z = (cosh * cosh) - (sinh * sinh);
 
    show("x", x);
    show("sinh(x)", sinh);
    show("cosh(x)", cosh);
    show("z", z);
}

```

Output:

```

        x |       0.1 |       0.2 |       0.3 |       0.4 | 
  sinh(x) |  0.100167 |  0.201336 |   0.30452 |  0.410752 | 
  cosh(x) |     1.005 |   1.02007 |   1.04534 |   1.08107 | 
        z |         1 |         1 |         1 |         1 |

```

### See also

|  |  |
| --- | --- |
| sinh(std::valarray) | applies the function std::sinh to each element of valarray   (function template) |
| tanh(std::valarray) | applies the function std::tanh to each element of valarray   (function template) |
| coshcoshfcoshl(C++11)(C++11) | computes hyperbolic cosine (\({\small\cosh{x}}\)cosh(x))   (function) |
| cosh(std::complex) | computes hyperbolic cosine of a complex number (\({\small\cosh{z}}\)cosh(z))   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/cosh&oldid=160803>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 October 2023, at 01:00.