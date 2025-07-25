# std::subtract_with_carry_engine<UIntType,w,s,r>::subtract_with_carry_engine

From cppreference.com
< cpp‎ | numeric‎ | random‎ | subtract with carry engine
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Uniform random bit generators | | | | | | uniform_random_bit_generator(C++20) | | | | | | Random number engines | | | | | | linear_congruential_engine(C++11) | | | | | | mersenne_twister_engine(C++11) | | | | | | subtract_with_carry_engine(C++11) | | | | | | philox_engine(C++26) | | | | | | Random number engine adaptors | | | | | | discard_block_engine(C++11) | | | | | | independent_bits_engine(C++11) | | | | | | shuffle_order_engine(C++11) | | | | | | Predefined random number generators | | | | | | Non-deterministic random numbers | | | | | | random_device(C++11) | | | | | |  | | | | | | Utilities | | | | | | generate_canonical(C++11) | | | | | | seed_seq(C++11) | | | | | |  | | | | | | Random number algorithms | | | | | | ranges::generate_random(C++26) | | | | | |  | | | | | | C random library | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | srand | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | RAND_MAX | | | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random number distributions | | | | | | Uniform distributions | | | | | | uniform_int_distribution(C++11) | | | | | | uniform_real_distribution(C++11) | | | | | | generate_canonical(C++11) | | | | | | Bernoulli distributions | | | | | | bernoulli_distribution(C++11) | | | | | | binomial_distribution(C++11) | | | | | | negative_binomial_distribution(C++11) | | | | | | geometric_distribution(C++11) | | | | | | Poisson distributions | | | | | | poisson_distribution(C++11) | | | | | | exponential_distribution(C++11) | | | | | | gamma_distribution(C++11) | | | | | | weibull_distribution(C++11) | | | | | | extreme_value_distribution(C++11) | | | | | | Normal distributions | | | | | | normal_distribution(C++11) | | | | | | lognormal_distribution(C++11) | | | | | | chi_squared_distribution(C++11) | | | | | | cauchy_distribution(C++11) | | | | | | fisher_f_distribution(C++11) | | | | | | student_t_distribution(C++11) | | | | | | Sampling distributions | | | | | | discrete_distribution(C++11) | | | | | | piecewise_constant_distribution(C++11) | | | | | | piecewise_linear_distribution(C++11) | | | | | |

std::subtract_with_carry_engine

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****subtract_with_carry_engine::subtract_with_carry_engine**** | | | | |
| subtract_with_carry_engine::seed | | | | |
| Generation | | | | |
| subtract_with_carry_engine::operator()") | | | | |
| subtract_with_carry_engine::discard | | | | |
| Characteristics | | | | |
| subtract_with_carry_engine::min | | | | |
| subtract_with_carry_engine::max | | | | |
| Non-member functions | | | | |
| operator==operator!=(C++11)(C++11)(until C++20) | | | | |
| operator<<operator>>(C++11)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| subtract_with_carry_engine() : subtract_with_carry_engine(0u) {} | (1) | (since C++11) |
| explicit subtract_with_carry_engine( result_type value ); | (2) | (since C++11) |
| template< class SeedSeq >  explicit subtract_with_carry_engine( SeedSeq& seq ); | (3) | (since C++11) |
| subtract_with_carry_engine( const subtract_with_carry_engine& other ); | (4) | (since C++11)  (implicitly declared) |
|  |  |  |

Constructs the pseudo-random number engine.

1) The default constructor.

- If the default-constructed engine is of type `std::ranlux24_base`, the 10000th consecutive invocation of it produces the value 7937952.
- If the default-constructed engine is of type `std::ranlux48_base`, the 10000th consecutive invocation of it produces the value 61839128582725.
2) Constructs the engine with a seed value value. The sequence X of the engine's initial state is determined as follows:

1. Constructs a std::linear_congruential_engine<std::uint_least32_t, 40014u, 0u, 2147483563u> object e with argument value == 0u ? default_seed : static_cast<std::uint_least32_t>(value % 2147483563u).
2. Let n be std::size_t(w / 32) + 1.
3. Sets the values of \(\scriptsize X_{-r} \)X-r, ..., \(\scriptsize X_{-1} \)X-1, in that order. Each value \(\scriptsize X_i \)Xi is set as specified below:

:   1. Successively calls e for n times, the return values are denoted as \(\scriptsize z_0 \)z0 ... \(\scriptsize z_{n-1} \)zn-1.
    2. Sets \(\scriptsize X_i \)Xi to \(\scriptsize (\sum^{n-1}_{j=0} z_j \cdot 2^{32j}) \mod m \)(∑n-1  
       j=0 zj·232j  
       ) mod m.

 If \(\scriptsize X_{-1} \)X-1 is ​0​, sets the carry value c of the engine's initial state to 1. Otherwise, sets c to ​0​.3) Constructs the engine with a seed sequence seq. Given std::size_t(w / 32) + 1 as k, the sequence X of the engine's initial state is determined as follows:

1. Creates an invented array object a of length r \* k.
2. Calls seq.generate(a + 0, a + r \* k).
3. For each integer i in `[`-r`,`-1`]`, sets \(\scriptsize X_{i} \)Xi to \(\scriptsize (\sum^{k-1}_{j=0} a_{k(i+r)+j} \cdot 2^{32j}) \mod m \)(∑k-1  
   j=0 ak(i+r)+j·232j  
   ) mod m.
 If \(\scriptsize X_{-1} \)X-1 is ​0​, sets the carry value c of the engine's initial state to 1. Otherwise, sets c to ​0​. This overload participates in overload resolution only if `SeedSeq` meets the requirements of SeedSequence.4) The copy constructor. Upon construction, \*this == other is true.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | seed value to use in the initialization of the internal state |
| seq | - | seed sequence to use in the initialization of the internal state |

### Complexity

1,2) (std::size_t(w / 32) + 1) \* r invocations of e.3) Same as the complexity of the `seq.generate` call.4) \(\scriptsize O(r) \)O(r).

### Exceptions

3) If `SeedSeq` is not std::seed_seq, throws the exceptions thrown by the `seq.generate` call.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: demos for overloads (2-4) required |

Run this code

```
#include <cassert>
#include <random>
 
int main()
{
    std::ranlux24_base gen24; // overload (1)
    std::ranlux48_base gen48; // overload (1)
    gen24.discard(10000 - 1);
    gen48.discard(10000 - 1);
    assert(gen24() == 7'937'952);
    assert(gen48() == 61'839'128'582'725);
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2181 | C++11 | overload (3) would not throw even if the `seq.generate` call throws | propagates the exception |
| LWG 3809 | C++11 | e could not be constructed if `result_type` is std::uint16_t | can be constructed in this case |
| LWG 4014 | C++11 | the resolution of LWG issue 3809 caused the initial seed of the intermediate std::linear_congruential_engine to have a different type from the engine's `result_type` | truncates and converts value |
| P0935R0 | C++11 | the default constructor was explicit | made implicit |

### See also

|  |  |
| --- | --- |
| seed | sets the current state of the engine   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/random/subtract_with_carry_engine/subtract_with_carry_engine&oldid=180216>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 February 2025, at 23:02.