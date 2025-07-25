# operator+,-,\*,/,%,&,|,^,<<,>>,&&,|| (std::valarray)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator||**** | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >  std::valarray<T> operator+ ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator- ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator\* ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator/ ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator% ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator& ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator| ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator^ ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator<<( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator>>( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >  std::valarray<bool> operator&&( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T > std::valarray<bool> operator||( const std::valarray<T>& lhs, const std::valarray<T>& rhs ); | (1) |  |
| template< class T >  std::valarray<T> operator+ ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator- ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator\* ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator/ ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator% ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator& ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator| ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator^ ( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator<<( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<T> operator>>( const typename std::valarray<T>::value_type & val,                               const std::valarray<T>& rhs );  template< class T >  std::valarray<bool> operator&&( const typename std::valarray<T>::value_type & val,                                  const std::valarray<T>& rhs );  template< class T >  std::valarray<bool> operator||( const typename std::valarray<T>::value_type & val, const std::valarray<T>& rhs ); | (2) |  |
| template< class T >  std::valarray<T> operator+ ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator- ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator\* ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator/ ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator% ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator& ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator| ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator^ ( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator<<( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<T> operator>>( const std::valarray<T>& lhs,                               const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<bool> operator&&( const std::valarray<T>& lhs,                                  const typename std::valarray<T>::value_type & val );  template< class T >  std::valarray<bool> operator||( const std::valarray<T>& lhs, const typename std::valarray<T>::value_type & val ); | (3) |  |
|  |  |  |

Apply binary operators to each element of two valarrays, or a valarray and a value.

1) The operators works on valarrays of the same size and returns a valarray with the same size as the parameters with the operation applied to every elements of the two arguments.2,3) Applies the operator between each element of the valarray and the scalar.

### Parameters

|  |  |  |
| --- | --- | --- |
| rhs | - | a numeric array |
| lhs | - | a numeric array |
| val | - | a value of type `T` |

### Return value

A valarray with the same size as the parameter.

### Note

The behaviour is undefined when the two arguments are valarrays with different sizes.

The function can be implemented with the return type different from std::valarray. In this case, the replacement type has the following properties:

:   - All const member functions of std::valarray are provided.
    - std::valarray, std::slice_array, std::gslice_array, std::mask_array and std::indirect_array can be constructed from the replacement type.
    - For every function taking a const std::valarray<T>& except begin() and end()(since C++11), identical functions taking the replacement types shall be added;
    - For every function taking two const std::valarray<T>& arguments, identical functions taking every combination of const std::valarray<T>& and replacement types shall be added.
    - The return type does not add more than two levels of template nesting over the most deeply-nested argument type.

### Example

Finds real roots of multiple Quadratic equations.

Run this code

```
#include <cstddef>
#include <iostream>
#include <valarray>
 
int main()
{
    std::valarray<double> a(1, 8);
    std::valarray<double> b{1, 2, 3, 4, 5, 6, 7, 8};
    std::valarray<double> c = -b;
    // literals must also be of type T until LWG3074 (double in this case)
    std::valarray<double> d = std::sqrt(b * b - 4.0 * a * c);
    std::valarray<double> x1 = 2.0 * c / (-b + d);
    std::valarray<double> x2 = 2.0 * c / (-b - d);
    std::cout << "quadratic equation:  root 1:    root 2:   b: c:\n";
    for (std::size_t i = 0; i < a.size(); ++i)
        std::cout << a[i] << "\u00B7x\u00B2 + " << b[i] << "\u00B7x + "
                  << c[i] << " = 0  " << std::fixed << x1[i]
                  << "  " << x2[i] << std::defaultfloat
                  << "  " << -x1[i] - x2[i]
                  << "  " << x1[i] * x2[i] << '\n';
}

```

Output:

```
quadratic equation:  root 1:    root 2:   b: c:
1·x² + 1·x + -1 = 0  -1.618034  0.618034  1  -1
1·x² + 2·x + -2 = 0  -2.732051  0.732051  2  -2
1·x² + 3·x + -3 = 0  -3.791288  0.791288  3  -3
1·x² + 4·x + -4 = 0  -4.828427  0.828427  4  -4
1·x² + 5·x + -5 = 0  -5.854102  0.854102  5  -5
1·x² + 6·x + -6 = 0  -6.872983  0.872983  6  -6
1·x² + 7·x + -7 = 0  -7.887482  0.887482  7  -7
1·x² + 8·x + -8 = 0  -8.898979  0.898979  8  -8

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3074 | C++98 | `T` is deduced from both the scalar and the `valarray` for (2,3), disallowing mixed-type calls | only deduce `T` from the `valarray` |

### See also

|  |  |
| --- | --- |
| operator+operator-operator~operator! | applies a unary arithmetic operator to each element of the valarray   (public member function) |
| operator+=operator-=operator\*=operator/=operator%=operator&=operator|=operator^=operator<<=operator>>= | applies compound assignment operator to each element of the valarray   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/operator_arith3&oldid=160854>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 October 2023, at 14:14.