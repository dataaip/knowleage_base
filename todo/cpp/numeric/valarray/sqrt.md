# std::sqrt(std::valarray)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | ****sqrt**** | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >  valarray<T> sqrt( const valarray<T>& va ); |  |  |
|  |  |  |

For each element in va computes the square root of the value of the element.

### Parameters

|  |  |  |
| --- | --- | --- |
| va | - | value array to apply the operation to |

### Return value

Value array containing square roots of the values in va.

### Notes

Unqualified function (sqrt) is used to perform the computation. If such function is not available, std::sqrt is used due to argument-dependent lookup.

The function can be implemented with the return type different from std::valarray. In this case, the replacement type has the following properties:

:   - All const member functions of std::valarray are provided.
    - std::valarray, std::slice_array, std::gslice_array, std::mask_array and std::indirect_array can be constructed from the replacement type.
    - For every function taking a const std::valarray<T>& except begin() and end()(since C++11), identical functions taking the replacement types shall be added;
    - For every function taking two const std::valarray<T>& arguments, identical functions taking every combination of const std::valarray<T>& and replacement types shall be added.
    - The return type does not add more than two levels of template nesting over the most deeply-nested argument type.

### Possible implementation

|  |
| --- |
| ```text template<class T> valarray<T> sqrt(const valarray<T>& va) {     valarray<T> other = va;     for (T& i : other)         i = sqrt(i);       return other; // proxy object may be returned } ``` |

### Example

Finds all three roots (two of which can be complex conjugates) of several Cubic equations at once.

Run this code

```
#include <cassert>
#include <complex>
#include <cstddef>
#include <iostream>
#include <numbers>
#include <valarray>
 
using CD = std::complex<double>;
using VA = std::valarray<CD>;
 
// return all n complex roots out of a given complex number x
VA root(CD x, unsigned n)
{
    const double mag = std::pow(std::abs(x), 1.0 / n);
    const double step = 2.0 * std::numbers::pi / n;
    double phase = std::arg(x) / n;
    VA v(n);
    for (std::size_t i{}; i != n; ++i, phase += step)
        v[i] = std::polar(mag, phase);
    return v;
}
 
// return n complex roots of each element in v; in the output valarray first
// goes the sequence of all n roots of v[0], then all n roots of v[1], etc.
VA root(VA v, unsigned n)
{
    VA o(v.size() * n);
    VA t(n);
    for (std::size_t i = 0; i != v.size(); ++i)
    {
        t = root(v[i], n);
        for (unsigned j = 0; j != n; ++j)
            o[n * i + j] = t[j];
    }
    return o;
}
 
// floating-point numbers comparator that tolerates given rounding error
inline bool is_equ(CD x, CD y, double tolerance = 0.000'000'001)
{
    return std::abs(std::abs(x) - std::abs(y)) < tolerance;
}
 
int main()
{
    // input coefficients for polynomial x³ + p·x + q
    const VA p{1, 2, 3, 4, 5, 6, 7, 8};
    const VA q{1, 2, 3, 4, 5, 6, 7, 8};
 
    // the solver
    const VA d = std::sqrt(std::pow(q / 2, 2) + std::pow(p / 3, 3));
    const VA u = root(-q / 2 + d, 3);
    const VA n = root(-q / 2 - d, 3);
 
    // allocate memory for roots: 3 * number of input cubic polynomials
    VA x[3];
    for (std::size_t t = 0; t != 3; ++t)
        x[t].resize(p.size());
 
    auto is_proper_root = [](CD a, CD b, CD p) { return is_equ(a * b + p / 3.0, 0.0); };
 
    // sieve out 6 out of 9 generated roots, leaving only 3 proper roots (per polynomial)
    for (std::size_t i = 0; i != p.size(); ++i)
        for (std::size_t j = 0, r = 0; j != 3; ++j)
            for (std::size_t k = 0; k != 3; ++k)
                if (is_proper_root(u[3 * i + j], n[3 * i + k], p[i]))
                    x[r++][i] = u[3 * i + j] + n[3 * i + k];
 
    std::cout << "Depressed cubic equation:   Root 1: \t\t Root 2: \t\t Root 3:\n";
    for (std::size_t i = 0; i != p.size(); ++i)
    {
        std::cout << "x³ + " << p[i] << "·x + " << q[i] << " = 0  "
                  << std::fixed << x[0][i] << "  " << x[1][i] << "  " << x[2][i]
                  << std::defaultfloat << '\n';
 
        assert(is_equ(std::pow(x[0][i], 3) + x[0][i] * p[i] + q[i], 0.0));
        assert(is_equ(std::pow(x[1][i], 3) + x[1][i] * p[i] + q[i], 0.0));
        assert(is_equ(std::pow(x[2][i], 3) + x[2][i] * p[i] + q[i], 0.0));
    }
}

```

Output:

```
Depressed cubic equation:   Root 1:              Root 2:                 Root 3:
x³ + (1,0)·x + (1,0) = 0  (-0.682328,0.000000)  (0.341164,1.161541)  (0.341164,-1.161541)
x³ + (2,0)·x + (2,0) = 0  (-0.770917,0.000000)  (0.385458,1.563885)  (0.385458,-1.563885)
x³ + (3,0)·x + (3,0) = 0  (-0.817732,0.000000)  (0.408866,1.871233)  (0.408866,-1.871233)
x³ + (4,0)·x + (4,0) = 0  (-0.847708,0.000000)  (0.423854,2.130483)  (0.423854,-2.130483)
x³ + (5,0)·x + (5,0) = 0  (-0.868830,0.000000)  (0.434415,2.359269)  (0.434415,-2.359269)
x³ + (6,0)·x + (6,0) = 0  (-0.884622,0.000000)  (0.442311,2.566499)  (0.442311,-2.566499)
x³ + (7,0)·x + (7,0) = 0  (-0.896922,0.000000)  (0.448461,2.757418)  (0.448461,-2.757418)
x³ + (8,0)·x + (8,0) = 0  (-0.906795,0.000000)  (0.453398,2.935423)  (0.453398,-2.935423)

```

### See also

|  |  |
| --- | --- |
| pow(std::valarray) | applies the function std::pow to two valarrays or a valarray and a value   (function template) |
| sqrtsqrtfsqrtl(C++11)(C++11) | computes square root (\(\small{\sqrt{x}}\)√x)   (function) |
| sqrt(std::complex) | complex square root in the range of the right half-plane   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/sqrt&oldid=160830>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 October 2023, at 10:08.