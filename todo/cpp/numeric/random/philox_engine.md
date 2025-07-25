# std::philox_engine

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Uniform random bit generators | | | | | | uniform_random_bit_generator(C++20) | | | | | | Random number engines | | | | | | linear_congruential_engine(C++11) | | | | | | mersenne_twister_engine(C++11) | | | | | | subtract_with_carry_engine(C++11) | | | | | | ****philox_engine****(C++26) | | | | | | Random number engine adaptors | | | | | | discard_block_engine(C++11) | | | | | | independent_bits_engine(C++11) | | | | | | shuffle_order_engine(C++11) | | | | | | Predefined random number generators | | | | | | Non-deterministic random numbers | | | | | | random_device(C++11) | | | | | |  | | | | | | Utilities | | | | | | generate_canonical(C++11) | | | | | | seed_seq(C++11) | | | | | |  | | | | | | Random number algorithms | | | | | | ranges::generate_random(C++26) | | | | | |  | | | | | | C random library | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | srand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | RAND_MAX | | | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random number distributions | | | | | | Uniform distributions | | | | | | uniform_int_distribution(C++11) | | | | | | uniform_real_distribution(C++11) | | | | | | generate_canonical(C++11) | | | | | | Bernoulli distributions | | | | | | bernoulli_distribution(C++11) | | | | | | binomial_distribution(C++11) | | | | | | negative_binomial_distribution(C++11) | | | | | | geometric_distribution(C++11) | | | | | | Poisson distributions | | | | | | poisson_distribution(C++11) | | | | | | exponential_distribution(C++11) | | | | | | gamma_distribution(C++11) | | | | | | weibull_distribution(C++11) | | | | | | extreme_value_distribution(C++11) | | | | | | Normal distributions | | | | | | normal_distribution(C++11) | | | | | | lognormal_distribution(C++11) | | | | | | chi_squared_distribution(C++11) | | | | | | cauchy_distribution(C++11) | | | | | | fisher_f_distribution(C++11) | | | | | | student_t_distribution(C++11) | | | | | | Sampling distributions | | | | | | discrete_distribution(C++11) | | | | | | piecewise_constant_distribution(C++11) | | | | | | piecewise_linear_distribution(C++11) | | | | | |

****std::philox_engine****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| philox_engine::philox_engine | | | | |
| philox_engine::seed | | | | |
| philox_engine::set_counter | | | | |
| Generation | | | | |
| philox_engine::operator()") | | | | |
| philox_engine::discard | | | | |
| Characteristics | | | | |
| philox_engine::min | | | | |
| philox_engine::max | | | | |
| Non-member functions | | | | |
| operator==(C++26) | | | | |
| operator<<operator>>(C++26)(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<random>` |  |  |
| template<  class UIntType, std::size_t w, std::size_t n, std::size_t r,      UIntType... consts  > class philox_engine; |  | (since C++26) |
|  |  |  |

`std::philox_engine` is a counter-based random number engine.

### Template parameters

|  |  |  |
| --- | --- | --- |
| UIntType | - | The result type generated by the generator. The effect is undefined if this is not one of unsigned short, unsigned int, unsigned long, or unsigned long long. |
| w | - | the word size in bits |
| n | - | the word count |
| r | - | the round count |
| consts | - | the sequence of multipliers and round constants used for generating random numbers |

If any of the following values is not true, the program is ill-formed:

- sizeof...(consts) == n
- n == 2 || n == 4 || n == 8 || n == 16
- 0 < r
- 0 < w && w <= std::numeric_limits<UIntType>::digits

### Generator properties

In the following description, let \(\scriptsize Q_i \)Qi denote the ith element of sequence Q, where the subscript starts from zero.

The size of the states of `philox_engine` is \(\scriptsize O(n)\)O(n), each of them consists of four parts:

- A sequence X of n integer values, where each value is in ``​0​`,``2``w`  
  `)`.

:   - This sequence represents a large unsigned integer counter value \(\scriptsize Z=\sum_{j=0}^{n-1} X \cdot 2^{wj} \)Z=∑n-1  
      j=0X⋅2wj  
       of \(\scriptsize n \cdot w \)n⋅w bits.

- A sequence K of n / 2 keys of type `UIntType`.
- A buffer Y of n produced values of type `UIntType`.
- An index j in Y buffer.

The [transition algorithm of `philox_engine` (\(\scriptsize TA(X_i) \)TA(Xi)) is defined as follows:

- If j is not n - 1, increments j by 1.[[1]](philox_engine.html#cite_note-1)
- If j is n - 1, performs the following operations:[[2]](philox_engine.html#cite_note-2)

1. Generates a new sequence of n random values (see below) and stores them in Y.
2. Increments the counter Z by 1.
3. Resets j to ​0​.

The generation algorithm of `philox_engine` is \(\scriptsize GA(X_i)=Y_j \)GA(Xi)=Yj.

1. ↑ In this case, the next generation algorithm call returns the next generated value in the buffer.
2. ↑ In this case, the buffer is refreshed, and the next generation algorithm call returns the first value in the new buffer.

#### Generating random values

Random values are generated from the following parameters:

- the number of rounds r
- the current counter sequence X
- the key sequence K
- the multiplier sequence M
- the round constant sequence C

The sequences M and C are formed from the values from template parameter pack consts, which represents the \(\scriptsize M_k \)Mk and \(\scriptsize C_k \)Ck constants as `[`\(\scriptsize M_0 \)M0`,`\(\scriptsize C_0 \)C0`,`\(\scriptsize M_1 \)M1`,`\(\scriptsize C_1 \)C1`,... , ...,`\(\scriptsize M_{n/2-1} \)Mn/2-1`,`\(\scriptsize C_{n/2-1} \)Cn/2-1`]`.

Random numbers are generated by the following process:

1. Initializes the output sequence S with the elements of X.
2. Updates the elements of S for r rounds.
3. Replaces the values in the buffer Y with the values in S.

#### Updating the output sequence

For each round of update, an intermediate sequence V is initialized with the elements of S in a specified order:

| n | ﻿ ﻿ ﻿\(\scriptsize V_0 \)V0 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_1 \)V1 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_2 \)V2 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_3 \)V3 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_4 \)V4 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_5 \)V5 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_6 \)V6 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_7 \)V7 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_8 \)V8 ﻿ ﻿ ﻿ | ﻿ ﻿ ﻿\(\scriptsize V_9 \)V9 ﻿ ﻿ ﻿ | \(\scriptsize V_{10} \)V10 | \(\scriptsize V_{11} \)V11 | \(\scriptsize V_{12} \)V12 | \(\scriptsize V_{13} \)V13 | \(\scriptsize V_{14} \)V14 | \(\scriptsize V_{15} \)V15 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 2 | \(\scriptsize S_0 \)S0 | \(\scriptsize S_1 \)S1 | N/A | | | | | | | | | | | | | |
| 4 | \(\scriptsize S_0 \)S0 | \(\scriptsize S_3 \)S3 | \(\scriptsize S_2 \)S2 | \(\scriptsize S_1 \)S1 | N/A | | | | | | | | | | | |
| 8 | \(\scriptsize S_2 \)S2 | \(\scriptsize S_1 \)S1 | \(\scriptsize S_4 \)S4 | \(\scriptsize S_7 \)S7 | \(\scriptsize S_6 \)S6 | \(\scriptsize S_5 \)S5 | \(\scriptsize S_0 \)S0 | \(\scriptsize S_3 \)S3 | N/A | | | | | | | |
| 16 | \(\scriptsize S_0 \)S0 | \(\scriptsize S_9 \)S9 | \(\scriptsize S_2 \)S2 | \(\scriptsize S_{13} \)S13 | \(\scriptsize S_6 \)S6 | \(\scriptsize S_{11} \)S11 | \(\scriptsize S_4 \)S4 | \(\scriptsize S_{15} \)S15 | \(\scriptsize S_{10} \)S10 | \(\scriptsize S_7 \)S7 | \(\scriptsize S_{12} \)S12 | \(\scriptsize S_3 \)S3 | \(\scriptsize S_{14} \)S14 | \(\scriptsize S_5 \)S5 | \(\scriptsize S_8 \)S8 | \(\scriptsize S_1 \)S1 |

Given the following operation notations:

- \(\scriptsize \mathsf{xor} \)xor, built-in bitwise XOR.
- \(\scriptsize \mathsf{mullo} \)mullo, it calcuates the low half of modular multiplication and is defined as \(\scriptsize \mathsf{mullo}(a,b,w)=(a \cdot b) \mod 2^w \)mullo(a,b,w)=(a⋅b) mod 2w  
  .
- \(\scriptsize \mathsf{mulhi} \)mulhi, it calcuates the high half of multiplication and is defined as \(\scriptsize \mathsf{mulhi}(a,b,w)=\left\lfloor (a \cdot b)/2^w \right\rfloor \)mulhi(a,b,w)=⌊(a⋅b)/2w  
  ⌋.

Let q be the current round number (starting from zero), for each integer k in ``​0​`,`n / 2`)`, the elements of the output sequence S are updated as follows:

- \(\scriptsize X_{2 \cdot k}=\mathsf{mullo}(V_{2 \cdot k+1},M_k,w) \)X2⋅k=mullo(V2⋅k+1,Mk,w)
- \(\scriptsize X_{2 \cdot k+1}=\mathsf{mulhi}(V_{2 \cdot k+1},M_k,w)\ \mathsf{xor}\ ((K_k+q \cdot C_k) \mod 2^w)\ \mathsf{xor}\ V_{2 \cdot k} \)X2⋅k+1=mulhi(V2⋅k+1,Mk,w) xor ((Kk+q⋅Ck) mod 2w  
  ) xor V2⋅k

### Predefined specializations

The following specializations define the random number engine with two commonly used parameter sets:

|  |  |
| --- | --- |
| Defined in header `<random>` | |
| Type | Definition |
| `philox4x32` (C++26) | std::philox_engine<[std::uint_fast32_t, 32, 4, 10, 0xD2511F53, 0x9E3779B9, 0xCD9E8D57, 0xBB67AE85> |
| `philox4x64` (C++26) | std::philox_engine<std::uint_fast64_t, 64, 4, 10, 0xD2E7470EE14C6C93, 0x9E3779B97F4A7C15, 0xCA5A826395121157, 0xBB67AE8584CAA73B> |

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `result_type` | `UIntType` |

### Data members

|  |  |
| --- | --- |
| constexpr std::size_t word_size[static] | w   (public static member constant) |
| constexpr std::size_t word_count[static] | n   (public static member constant) |
| constexpr std::size_t round_count[static] | r   (public static member constant) |
| constexpr std::array<result_type, word_count / 2> multipliers[static] | the multiplier sequence M   (public static member constant) |
| constexpr std::array<result_type, word_count / 2> round_consts[static] | the round constant sequence C   (public static member constant) |
| constexpr std::uint_least32_t default_seed[static] | 20111115u   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| Construction and Seeding | |
| (constructor) | constructs the engine   (public member function) |
| seed | sets the current state of the engine   (public member function) |
| set_counter | sets the current counter of the engine   (public member function) |
| Generation | |
| operator()") | advances the engine's state and returns the generated value   (public member function) |
| discard | advances the engine's state by a specified amount   (public member function) |
| Characteristics | |
| min[static] | gets the smallest possible value in the output range   (public static member function) |
| max[static] | gets the largest possible value in the output range   (public static member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==(C++26) | compares the internal states of two pseudo-random number engines   (function) |
|  |
| operator<<operator>>(C++26) | performs stream input and output on pseudo-random number engine   (function template) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_philox_engine` | `202406L` | (C++26) | `std::philox_engine` |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/random/philox_engine&oldid=177371>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 October 2024, at 14:44.