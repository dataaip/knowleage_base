# std::piecewise_linear_distribution

From cppreference.com
< cpp‎ | numeric‎ | random
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

Pseudo-random number generation

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Uniform random bit generators | | | | | | uniform_random_bit_generator(C++20) | | | | | | Random number engines | | | | | | linear_congruential_engine(C++11) | | | | | | mersenne_twister_engine(C++11) | | | | | | subtract_with_carry_engine(C++11) | | | | | | philox_engine(C++26) | | | | | | Random number engine adaptors | | | | | | discard_block_engine(C++11) | | | | | | independent_bits_engine(C++11) | | | | | | shuffle_order_engine(C++11) | | | | | | Predefined random number generators | | | | | | Non-deterministic random numbers | | | | | | random_device(C++11) | | | | | |  | | | | | | Utilities | | | | | | generate_canonical(C++11) | | | | | | seed_seq(C++11) | | | | | |  | | | | | | Random number algorithms | | | | | | ranges::generate_random(C++26) | | | | | |  | | | | | | C random library | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | srand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | RAND_MAX | | | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random number distributions | | | | | | Uniform distributions | | | | | | uniform_int_distribution(C++11) | | | | | | uniform_real_distribution(C++11) | | | | | | generate_canonical(C++11) | | | | | | Bernoulli distributions | | | | | | bernoulli_distribution(C++11) | | | | | | binomial_distribution(C++11) | | | | | | negative_binomial_distribution(C++11) | | | | | | geometric_distribution(C++11) | | | | | | Poisson distributions | | | | | | poisson_distribution(C++11) | | | | | | exponential_distribution(C++11) | | | | | | gamma_distribution(C++11) | | | | | | weibull_distribution(C++11) | | | | | | extreme_value_distribution(C++11) | | | | | | Normal distributions | | | | | | normal_distribution(C++11) | | | | | | lognormal_distribution(C++11) | | | | | | chi_squared_distribution(C++11) | | | | | | cauchy_distribution(C++11) | | | | | | fisher_f_distribution(C++11) | | | | | | student_t_distribution(C++11) | | | | | | Sampling distributions | | | | | | discrete_distribution(C++11) | | | | | | piecewise_constant_distribution(C++11) | | | | | | ****piecewise_linear_distribution****(C++11) | | | | | |

****std::piecewise_linear_distribution****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| piecewise_linear_distribution::piecewise_linear_distribution | | | | |
| piecewise_linear_distribution::reset | | | | |
| Generation | | | | |
| piecewise_linear_distribution::operator()") | | | | |
| Characteristics | | | | |
| piecewise_linear_distribution::intervalspiecewise_linear_distribution::densities | | | | |
| piecewise_linear_distribution::param | | | | |
| piecewise_linear_distribution::min | | | | |
| piecewise_linear_distribution::max | | | | |
| Non-member functions | | | | |
| operator==operator!=(C++11)(C++11)(until C++20) | | | | |
| operator<<operator>>(C++11)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<random>` |  |  |
| template< class RealType = double >  class piecewise_linear_distribution; |  | (since C++11) |
|  |  |  |

`std::piecewise_linear_distribution` produces random floating-point numbers, which are distributed according to a linear probability density function within each of the several subintervals \(\small{b_i, b_{i+1})}\)[bi, bi+1). The distribution is such that the probability density at each interval boundary is exactly the predefined value \(\small{p_i}\)pi.

The probability density for any \(\small{ b_i \le x < b_{i+1} }\)bi≤x<bi+1 is \(\small{p_i\frac{b_{i+1}-x}{b_{i+1}-b_i} + p_{i+1}\frac{x-b_i}{b_{i+1}-b_i} }\)pi

|  |
| --- |
| bi+1-x |
| bi+1-bi |

 + pi+1

|  |
| --- |
| x-bi |
| bi+1-bi |

, where probability densities at interval boundaries \(\small{p_k}\)pk are calculated as \(\small{w_k/S}\)wk/S where \(\small{S}\)S is the sum of all \(\small{\frac{1}{2}(w_k + w_{k+1})(b_{k+1} - b_k)}\)

|  |
| --- |
| 1 |
| 2 |

(wk+wk+1)(bk+1−bk).

The set of interval boundaries \(\small{b_i}\)bi and the set of weights at boundaries \(\small{w_i}\)wi are the parameters of this distribution.

[`std::piecewise_linear_distribution` satisfies all requirements of RandomNumberDistribution.

### Template parameters

|  |  |  |
| --- | --- | --- |
| RealType | - | The result type generated by the generator. The effect is undefined if this is not one of float, double, or long double. |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `result_type` (C++11) | RealType |
| `param_type` (C++11) | the type of the parameter set, see RandomNumberDistribution. |

### Member functions

|  |  |
| --- | --- |
| (constructor)(C++11) | constructs new distribution   (public member function) |
| reset(C++11) | resets the internal state of the distribution   (public member function) |
| Generation | |
| operator()")(C++11) | generates the next random number in the distribution   (public member function) |
| Characteristics | |
| intervalsdensities(C++11) | returns the distribution parameters   (public member function) |
| param(C++11) | gets or sets the distribution parameter object   (public member function) |
| min(C++11) | returns the minimum potentially generated value   (public member function) |
| max(C++11) | returns the maximum potentially generated value   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares two distribution objects   (function) |
| operator<<operator>>(C++11) | performs stream input and output on pseudo-random number distribution   (function template) |

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <map>
#include <random>
#include <string>
 
int main()
{
    std::random_device rd;
    std::mt19937 gen{rd()};
    // increase the probability from 0 to 5
    // remain flat from 5 to 10
    // decrease from 10 to 15 at the same rate
    std::vector<double> i{0, 5, 10, 15};
    std::vector<double> w{0, 1, 1, 0};
    std::piecewise_linear_distribution<> d{i.begin(), i.end(), w.begin()};
 
    std::map<int, int> hist;
    for (int n{}; n < 1e4; ++n)
        ++hist[d(gen)];
 
    for (auto [x, y] : hist)
        std::cout << std::setw(2) << std::setfill('0') << x
                  << ' ' << std::string(y / 100, '*') << '\n';
}

```

Possible output:

```
00 *
01 ***
02 ****
03 ******
04 *********
05 *********
06 *********
07 **********
08 *********
09 **********
10 *********
11 *******
12 ****
13 ***
14 *

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/random/piecewise_linear_distribution&oldid=166819>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 December 2023, at 01:17.