# std::mersenne_twister_engine

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Uniform random bit generators | | | | | | uniform_random_bit_generator(C++20) | | | | | | Random number engines | | | | | | linear_congruential_engine(C++11) | | | | | | ****mersenne_twister_engine****(C++11) | | | | | | subtract_with_carry_engine(C++11) | | | | | | philox_engine(C++26) | | | | | | Random number engine adaptors | | | | | | discard_block_engine(C++11) | | | | | | independent_bits_engine(C++11) | | | | | | shuffle_order_engine(C++11) | | | | | | Predefined random number generators | | | | | | Non-deterministic random numbers | | | | | | random_device(C++11) | | | | | |  | | | | | | Utilities | | | | | | generate_canonical(C++11) | | | | | | seed_seq(C++11) | | | | | |  | | | | | | Random number algorithms | | | | | | ranges::generate_random(C++26) | | | | | |  | | | | | | C random library | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | srand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | RAND_MAX | | | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random number distributions | | | | | | Uniform distributions | | | | | | uniform_int_distribution(C++11) | | | | | | uniform_real_distribution(C++11) | | | | | | generate_canonical(C++11) | | | | | | Bernoulli distributions | | | | | | bernoulli_distribution(C++11) | | | | | | binomial_distribution(C++11) | | | | | | negative_binomial_distribution(C++11) | | | | | | geometric_distribution(C++11) | | | | | | Poisson distributions | | | | | | poisson_distribution(C++11) | | | | | | exponential_distribution(C++11) | | | | | | gamma_distribution(C++11) | | | | | | weibull_distribution(C++11) | | | | | | extreme_value_distribution(C++11) | | | | | | Normal distributions | | | | | | normal_distribution(C++11) | | | | | | lognormal_distribution(C++11) | | | | | | chi_squared_distribution(C++11) | | | | | | cauchy_distribution(C++11) | | | | | | fisher_f_distribution(C++11) | | | | | | student_t_distribution(C++11) | | | | | | Sampling distributions | | | | | | discrete_distribution(C++11) | | | | | | piecewise_constant_distribution(C++11) | | | | | | piecewise_linear_distribution(C++11) | | | | | |

****std::mersenne_twister_engine****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| mersenne_twister_engine::mersenne_twister_engine | | | | |
| mersenne_twister_engine::seed | | | | |
| Generation | | | | |
| mersenne_twister_engine::operator()") | | | | |
| mersenne_twister_engine::discard | | | | |
| Characteristics | | | | |
| mersenne_twister_engine::min | | | | |
| mersenne_twister_engine::max | | | | |
| Non-member functions | | | | |
| operator==operator!=(C++11)(C++11)(until C++20) | | | | |
| operator<<operator>>(C++11)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<random>` |  |  |
| template<  class UIntType, std::size_t w, std::size_t n, std::size_t m, std::size_t r,      UIntType a, std::size_t u, UIntType d, std::size_t s,      UIntType b, std::size_t t, UIntType c, std::size_t l, UIntType f > class mersenne_twister_engine; |  | (since C++11) |
|  |  |  |

`mersenne_twister_engine` is a random number engine based on Mersenne Twister algorithm. It produces high quality, but not cryptographically secure, unsigned integer random numbers of type `UIntType` on the interval \(\scriptsize {[0,2^w)}\)[0, 2w  
).

### Template parameters

|  |  |  |
| --- | --- | --- |
| UIntType | - | The result type generated by the generator. The effect is undefined if this is not one of unsigned short, unsigned int, unsigned long, or unsigned long long. |
| w | - | the power of two that determines the range of values generated by the engine |
| n | - | the degree of recurrence |
| m | - | the middle word, an offset used in the recurrence relation defining the state |
| r | - | the number of bits of the lower bit-mask, also known as the twist value |
| a | - | the conditional xor-mask, i.e. the coefficients of the rational normal form twist matrix |
| u, d, s, b, t, c, l | - | the 1st to 7th components of the bit-scrambling (tempering) matrix |
| f | - | the initialization multiplier |

If any of the following restrictions is violated, the program is ill-formed:

- m is in `[`1`,`n`]`.
- The following expressions are all true:

:   - w >= 3
    - w >= r
    - w >= u
    - w >= s
    - w >= t
    - w >= l
    - w <= std::numeric_limits<UIntType>::digits

- Given (1u << w) - 1u as w1, the following expressions are all true:

:   - a <= w1
    - b <= w1
    - c <= w1
    - d <= w1
    - f <= w1

### Generator properties

The size of the states of `mersenne_twister_engine` is n, each of them consists of a sequence X of n values of type `result_type`. \(\scriptsize X_j\)Xj stands for the \(\scriptsize j\mod n\)j mod nth value (starting from 0) of X.

Given the following bitwise operation notations:

- \(\scriptsize \mathsf{bitand}\)bitand, built-in bitwise AND.
- \(\scriptsize \mathsf{xor}\)xor, built-in bitwise XOR.
- \(\scriptsize \mathsf{lshift}\)lshift, built-in bitwise left-shift.
- \(\scriptsize \mathsf{rshift}\)rshift, built-in bitwise right-shift.

The transition algorithm of `mersenne_twister_engine` (\(\scriptsize TA(x_i)\)TA(xi)) is defined as follows:

1. Concatenate the upper w - r bits of \(\scriptsize X_{i-n}\)Xi-n with the lower r bits of \(\scriptsize X_{i+1-n}\)Xi+1-n to obtain an unsigned integer value Y.
2. Let y be \(\scriptsize a \cdot (Y\ \mathsf{bitand}\ 1)\)a·(Y bitand 1), and set \(\scriptsize X_i\)Xi to \(\scriptsize X_{i+m−n}\ \mathsf{xor}\ (Y\ \mathsf{rshift}\ 1)\ \mathsf{xor}\ y\)Xi+m−n xor (Y rshift 1) xor y.

The generation algorithm of `mersenne_twister_engine` (\(\scriptsize GA(x_i)\)GA(xi)) is defined as follows:

1. Let \(\scriptsize z_1\)z1 be \(\scriptsize X_i\ \mathsf{xor}\ ((X_i\ \mathsf{rshift}\ u)\ \mathsf{bitand}\ d)\)Xi xor ((Xi rshift u) bitand d).
2. Let \(\scriptsize z_2\)z2 be \(\scriptsize z_1\ \mathsf{xor}\ (((z_1\ \mathsf{lshift}\ s)\mod 2^w)\ \mathsf{bitand}\ b)\)Xi xor (((Xi lshift s) mod 2w  
   ) bitand b).
3. Let \(\scriptsize z_3\)z3 be \(\scriptsize z_2\ \mathsf{xor}\ (((z_2\ \mathsf{lshift}\ t)\mod 2^w)\ \mathsf{bitand}\ c)\)Xi xor (((Xi lshift t) mod 2w  
   ) bitand c).
4. Let \(\scriptsize z_4\)z4 be \(\scriptsize z_3\ \mathsf{xor}\ (z_3\ \mathsf{rshift}\ l)\)z3 xor (z3 rshift l).
5. Deliver \(\scriptsize z_4\)z4 as the result (i.e. \(\scriptsize GA(x_i)=z_4\)GA(xi)=z4).

### Predefined specializations

The following specializations define the random number engine with two commonly used parameter sets:

|  |  |
| --- | --- |
| Defined in header `<random>` | |
| Type | Definition |
| `mt19937` (C++11) | std::mersenne_twister_engine<std::uint_fast32_t,  32, 624, 397, 31,  0x9908b0df, 11,  0xffffffff, 7,  0x9d2c5680, 15,  0xefc60000, 18, 1812433253>  32-bit Mersenne Twister by Matsumoto and Nishimura, 1998 |
| `mt19937_64` (C++11) | std::mersenne_twister_engine<std::uint_fast64_t,  64, 312, 156, 31,  0xb5026f5aa96619e9, 29,  0x5555555555555555, 17,  0x71d67fffeda60000, 37,  0xfff7eee000000000, 43,  6364136223846793005>  64-bit Mersenne Twister by Matsumoto and Nishimura, 2000 |

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `result_type` | `UIntType` |

### Data members

|  |  |
| --- | --- |
| constexpr size_t word_size[static] | w   (public static member constant) |
| constexpr size_t state_size[static] | n   (public static member constant) |
| constexpr size_t shift_size[static] | m   (public static member constant) |
| constexpr size_t mask_bits[static] | r   (public static member constant) |
| constexpr UIntType xor_mask[static] | a   (public static member constant) |
| constexpr size_t tempering_u[static] | u   (public static member constant) |
| constexpr UIntType tempering_d[static] | d   (public static member constant) |
| constexpr size_t tempering_s[static] | s   (public static member constant) |
| constexpr UIntType tempering_b[static] | b   (public static member constant) |
| constexpr size_t tempering_t[static] | t   (public static member constant) |
| constexpr UIntType tempering_c[static] | c   (public static member constant) |
| constexpr size_t tempering_l[static] | l   (public static member constant) |
| constexpr UIntType initialization_multiplier[static] | f   (public static member constant) |
| constexpr UIntType default_seed[static] | 5489u   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| Construction and Seeding | |
| (constructor) | constructs the engine   (public member function) |
| seed | sets the current state of the engine   (public member function) |
| Generation | |
| operator()") | advances the engine's state and returns the generated value   (public member function) |
| discard | advances the engine's state by a specified amount   (public member function) |
| Characteristics | |
| min[static] | gets the smallest possible value in the output range   (public static member function) |
| max[static] | gets the largest possible value in the output range   (public static member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=(C++11)(C++11)(removed in C++20) | compares the internal states of two pseudo-random number engines   (function) |
|  |
| operator<<operator>>(C++11) | performs stream input and output on pseudo-random number engine   (function template) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/random/mersenne_twister_engine&oldid=175348>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 August 2024, at 22:19.