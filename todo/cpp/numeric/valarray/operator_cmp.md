# operator==,!=,<,<=,>,>=(std::valarray)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | ****operator==operator!=operator<operator>operator<=operator>=**** | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<valarray>` |  |  |
| template< class T >   std::valarray<bool> operator==( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator!=( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator< ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator<=( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator> ( const std::valarray<T>& lhs, const std::valarray<T>& rhs );  template< class T > std::valarray<bool> operator>=( const std::valarray<T>& lhs, const std::valarray<T>& rhs ); | (1) |  |
| template< class T >   std::valarray<bool> operator==( const typename std::valarray<T>::value_type & lhsv,                                  const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator!=( const typename std::valarray<T>::value_type & lhsv,                                  const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator< ( const typename std::valarray<T>::value_type & lhsv,                                  const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator<=( const typename std::valarray<T>::value_type & lhsv,                                  const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator> ( const typename std::valarray<T>::value_type & lhsv,                                  const std::valarray<T>& rhs );  template< class T >   std::valarray<bool> operator>=( const typename std::valarray<T>::value_type & lhsv, const std::valarray<T>& rhs ); | (2) |  |
| template< class T >   std::valarray<bool> operator==( const std::valarray<T>& lhs,                                  const typename std::valarray<T>::value_type & rhsv );  template< class T >   std::valarray<bool> operator!=( const std::valarray<T>& lhs,                                  const typename std::valarray<T>::value_type & rhsv );  template< class T >   std::valarray<bool> operator< ( const std::valarray<T>& lhs,                                  const typename std::valarray<T>::value_type & rhsv );  template< class T >   std::valarray<bool> operator<=( const std::valarray<T>& lhs,                                  const typename std::valarray<T>::value_type & rhsv );  template< class T >   std::valarray<bool> operator> ( const std::valarray<T>& lhs,                                  const typename std::valarray<T>::value_type & rhsv );  template< class T >   std::valarray<bool> operator>=( const std::valarray<T>& lhs, const typename std::valarray<T>::value_type & rhsv ); | (3) |  |
|  |  |  |

Compares each value within the numeric array with another value.

1) Returns a numeric array of bool containing elements each of which is obtained by applying the indicated comparison operator to the corresponding values of lhs and rhs.

The behavior is undefined if size() != v.size().

2) Returns a numeric array of bool containing elements each of which is obtained by applying the indicated comparison operator to lhsv and the corresponding value of rhs.3) Returns a numeric array of bool containing elements each of which is obtained by applying the indicated comparison operator to the corresponding value of lhs and rhsv.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | numeric arrays to compare |
| lhsv, rhsv | - | values to compare to each element within a numeric array |

### Return value

A numeric array of bool containing comparison results of corresponding elements.

### Exceptions

May throw implementation-defined exceptions.

### Notes

Each of the operators can only be instantiated if the following requirements are met:

:   - The indicated operator can be applied to type `T`.
    - The result value can be unambiguously converted to bool.

The function can be implemented with the return type different from std::valarray. In this case, the replacement type has the following properties:

:   - All const member functions of std::valarray are provided.
    - std::valarray, std::slice_array, std::gslice_array, std::mask_array and std::indirect_array can be constructed from the replacement type.
    - For every function taking a const std::valarray<T>& except begin() and end()(since C++11), identical functions taking the replacement types shall be added;
    - For every function taking two const std::valarray<T>& arguments, identical functions taking every combination of const std::valarray<T>& and replacement types shall be added.
    - The return type does not add more than two levels of template nesting over the most deeply-nested argument type.

### Example

Run this code

```
#include <iostream>
#include <valarray>
 
int main()
{
    // zero all negatives in a valarray
    std::valarray<int> v = {1, -1, 0, -3, 10, -1, -2};
    std::cout << "Before: ";
    for (auto n : v)
        std::cout << n << ' ';
    std::cout << '\n';
    v[v < 0] = 0;
    std::cout << "After: ";
    for (auto n : v)
        std::cout << n << ' ';
    std::cout << '\n';
 
    // convert the valarray<bool> result of == to a single bool
    std::valarray<int> a = {1, 2, 3};
    std::valarray<int> b = {2, 4, 6};
 
    std::cout << "2*a == b is " << std::boolalpha
              << (2 * a == b).min() << '\n';
}

```

Output:

```
Before: 1 -1 0 -3 10 -1 -2
After: 1 0 0 0 10 0 0
2*a == b is true

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3074 | C++98 | `T` is deduced from both the scalar and the `valarray` for (2,3), disallowing mixed-type calls | only deduce `T` from the `valarray` |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/operator_cmp&oldid=160642>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 October 2023, at 09:04.