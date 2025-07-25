# std::literals::complex_literals::operator""i, operator""if, operator""il

From cppreference.com
< cpp‎ | numeric‎ | complex
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

std::complex

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::complex | | | | | | complex::operator= | | | | | | complex::real | | | | | | complex::imag | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::operator+=complex::operator-=complex::operator\*=complex::operator/= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator- | | | | | | operator+operator-operator\*operator/ | | | | | | operator==operator!=(until C++20) | | | | | | operator<<operator>> | | | | | | get(std::complex)(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | real | | | | | | imag | | | | | | abs | | | | | | arg | | | | | | norm | | | | | | conj | | | | | | proj(C++11) | | | | | | polar | | | | | | ****operator""ioperator""ifoperator""il****(C++14)(C++14)(C++14) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log10 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | |
| Power functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pow | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asin(C++11) | | | | | | acos(C++11) | | | | | | atan(C++11) | | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex>` |  |  |
| constexpr complex<double> operator""i( long double arg );  constexpr complex<double> operator""i( unsigned long long arg ); | (1) | (since C++14) |
| constexpr complex<float> operator""if( long double arg );  constexpr complex<float> operator""if( unsigned long long arg ); | (2) | (since C++14) |
| constexpr complex<long double> operator""il( long double arg );  constexpr complex<long double> operator""il( unsigned long long arg ); | (3) | (since C++14) |
|  |  |  |

Forms a std::complex literal representing an imaginary number.

1) Forms a literal std::complex<double> with the real part zero and imaginary part arg.2) Forms a literal std::complex<float> with the real part zero and imaginary part arg.3) Forms a literal std::complex<long double> with the real part zero and imaginary part arg.

### Parameters

|  |  |  |
| --- | --- | --- |
| arg | - | the value of the imaginary number |

### Return value

The std::complex literal with the real part zero and imaginary part arg.

### Notes

These operators are declared in the namespace std::literals::complex_literals, where both `literals` and `complex_literals` are inline namespaces. Access to these operators can be gained with either:

- using namespace std::literals,
- using namespace std::complex_literals, or
- using namespace std::literals::complex_literals.

Even though if is a keyword in C++, it is a ud-suffix of the literal operator of the form operator ""if and in the literal expressions such as 1if or 1.0if because it is not separated by whitespace and is not a standalone token.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_complex_udls` | `201309L` | (C++14) | User-Defined Literals for std::complex |

### Possible implementation

| operator""i |
| --- |
| ```text constexpr std::complex<double> operator""i(unsigned long long d) {     return std::complex<double> {0.0, static_cast<double>(d)}; }   constexpr std::complex<double> operator""i(long double d) {     return std::complex<double> {0.0, static_cast<double>(d)}; } ``` |
| operator""if |
| ```text constexpr std::complex<float> operator""if(unsigned long long d) {     return std::complex<float> {0.0f, static_cast<float>(d)}; }   constexpr std::complex<float> operator""if(long double d) {     return std::complex<float> {0.0f, static_cast<float>(d)}; } ``` |
| operator""il |
| ```text constexpr std::complex<long double> operator""il(unsigned long long d) {     return std::complex<long double> {0.0L, static_cast<long double>(d)}; }   constexpr std::complex<long double> operator""il(long double d) {     return std::complex<long double> {0.0L, d}; } ``` |

### Example

Run this code

```
#include <complex>
#include <iostream>
 
int main()
{
    using namespace std::complex_literals;
 
    std::complex<double> c = 1.0 + 1i;
    std::cout << "abs" << c << " = " << std::abs(c) << '\n';
 
    std::complex<float> z = 3.0f + 4.0if;
    std::cout << "abs" << z << " = " << std::abs(z) << '\n';
}

```

Output:

```
abs(1,1) = 1.41421
abs(3,4) = 5

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a complex number   (public member function) |
| operator= | assigns the contents   (public member function) |
| C documentation for I | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/operator%22%22i&oldid=150866>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 April 2023, at 06:51.