# std::pow(std::valarray)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | ****pow**** | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >   std::valarray<T> pow( const std::valarray<T>& base, const std::valarray<T>& exp ); | (1) |  |
| template< class T >   std::valarray<T> pow( const std::valarray<T>& base, const typename std::valarray<T>::value_type& vexp ); | (2) |  |
| template< class T >   std::valarray<T> pow( const typename std::valarray<T>::value_type& vbase, const std::valarray<T>& exp ); | (3) |  |
|  |  |  |

Raises a value to a power.

1) Computes the values of each element in the numeric array base raised to the power specified by the corresponding element from the numeric array exp.

The behavior is undefined if base.size() != exp.size().

2) Computes the values of each element in the numeric array base raised to the power vexp.3) Computes the values of vbase raised to the power defined by the elements in the numeric array exp.

### Parameters

|  |  |  |
| --- | --- | --- |
| base | - | numeric array containing the values of the base |
| exp | - | numeric array containing the values of the exponent |
| vbase | - | a value defining the base |
| vexp | - | a value defining the exponent |

### Return value

A numeric array containing the results of exponentiation.

### Notes

Unqualified function (pow) is used to perform the computation. If such function is not available, std::pow is used due to argument-dependent lookup.

The function can be implemented with the return type different from std::valarray. In this case, the replacement type has the following properties:

:   - All const member functions of std::valarray are provided.
    - std::valarray, std::slice_array, std::gslice_array, std::mask_array and std::indirect_array can be constructed from the replacement type.
    - For every function taking a const std::valarray<T>& except begin() and end()(since C++11), identical functions taking the replacement types shall be added;
    - For every function taking two const std::valarray<T>& arguments, identical functions taking every combination of const std::valarray<T>& and replacement types shall be added.
    - The return type does not add more than two levels of template nesting over the most deeply-nested argument type.

### Example

Run this code

```
#include <cmath>
#include <cstddef>
#include <iomanip>
#include <iostream>
#include <valarray>
 
class show
{
    friend std::ostream& operator<<(std::ostream& os, show const& r)
    {
        constexpr char const* sup[]
        {
            "\u2070", "\u00B9", "\u00B2", "\u00B3", "\u2074",
            "\u2075", "\u2076", "\u2077", "\u2078", "\u2079"
        };
 
        for (std::size_t n = 0; n != r.bases.size(); ++n)
        {
            os << std::left << r.bases[n] << std::left;
            if (n < r.exponents.size())
                os << sup[r.exponents[n] % 10] << ' ';
            else
                os << "  ";
        }
 
        if (r.results.size() != 0)
        {
            os << '=';
            for (std::size_t n = 0; n != r.results.size(); ++n)
                os << ' ' << r.results[n];
        }
 
        return os << '\n';
    }
 
public:
    std::valarray<int> bases{}, exponents{}, results{};
};
 
int main()
{
    constexpr int base{2};
    constexpr int exponent{5};
    const std::valarray<int> bases{1, 2, 3, 4, 5, 6, 7};
    const std::valarray<int> exponents{0, 1, 2, 3, 4, 5, 6};
    const std::valarray<int> powers1 = std::pow(bases, exponents);
    const std::valarray<int> powers2 = std::pow(bases, exponent);
    const std::valarray<int> powers3 = std::pow(base, exponents);
 
    std::cout
        << "pow(const std::valarray<T>& base, const std::valarray<T>& exp); (1)\n"
        << "base : " << show{bases}
        << "exp  : " << show{exponents}
        << "pow  : " << show{bases, exponents, powers1}
        << '\n'
        << "pow(const std::valarray<T>& base, const value_type& vexp); (2)\n"
        << "base : " << show{bases}
        << "vexp : " << exponent << '\n'
        << "pow  : " << show{bases, std::valarray<int>(exponent, bases.size()), powers2}
        << '\n'
        << "pow(const value_type& vbase, const std::valarray<T>& exp); (3)\n"
        << "vbase: " << base << '\n'
        << "exp  : " << show{exponents}
        << "pow  : " << show{std::valarray<int>(base, bases.size()), exponents, powers3};
}

```

Output:

```
pow(const std::valarray<T>& base, const std::valarray<T>& exp); (1)
base : 1  2  3  4  5  6  7
exp  : 0  1  2  3  4  5  6
pow  : 1⁰ 2¹ 3² 4³ 5⁴ 6⁵ 7⁶ = 1 2 9 64 625 7776 117649
 
pow(const std::valarray<T>& base, const value_type& vexp); (2)
base : 1  2  3  4  5  6  7
vexp : 5
pow  : 1⁵ 2⁵ 3⁵ 4⁵ 5⁵ 6⁵ 7⁵ = 1 32 243 1024 3125 7776 16807
 
pow(const value_type& vbase, const std::valarray<T>& exp); (3)
vbase: 2
exp  : 0  1  2  3  4  5  6
pow  : 2⁰ 2¹ 2² 2³ 2⁴ 2⁵ 2⁶ = 1 2 4 8 16 32 64

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3074 | C++98 | `T` is deduced from both the scalar and the `valarray` for (2,3), disallowing mixed-type calls | only deduce `T` from the `valarray` |

### See also

|  |  |
| --- | --- |
| sqrt(std::valarray) | applies the function std::sqrt to each element of valarray   (function template) |
| powpowfpowl(C++11)(C++11) | raises a number to the given power (\(\small{x^y}\)xy)   (function) |
| pow(std::complex) | complex power, one or both arguments may be a complex number   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/pow&oldid=160828>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 October 2023, at 09:55.