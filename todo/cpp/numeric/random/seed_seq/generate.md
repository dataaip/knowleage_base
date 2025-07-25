# std::seed_seq::generate

From cppreference.com
< cpp‎ | numeric‎ | random‎ | seed seq
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

std::seed_seq

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| seed_seq::seed_seq | | | | |
| ****seed_seq::generate**** | | | | |
| seed_seq::size | | | | |
| seed_seq::param | | | | |

|  |  |  |
| --- | --- | --- |
| template< class RandomIt >  void generate( RandomIt begin, RandomIt end ); |  | (since C++11) |
|  |  |  |

Generate unbiased seeds by filling the output range ``begin`,`end`)` with 32-bit unsigned integer values, based on the (possibly biased) seeds stored in `v`.

- If begin == end is true, does nothing.
- Otherwise, generates seeds by the generation algorithm described below.

If [std::iterator_traits<RandomIt>::value_type is not an unsigned integer type, or its width is less than 32, the program is ill-formed.

If `RandomIt` does not meet the requirements of LegacyRandomAccessIterator, or it is not mutable, the behavior is undefined.

### Generation algorithm

Given the following values and operations:

|  |  |
| --- | --- |
| Value | Definition |
| z | `v` ﻿.size() |
| n | end - begin |
| m | std::max(z + 1, n) |
| t | (n >= 623) ? 11 : (n >= 68) ? 7 : (n >= 39) ? 5 : (n >= 7) ? 3 : (n - 1) / 2 |
| p | (n - t) / 2 |
| q | p + t |
| Operation | Definition |
| \(\scriptsize \mathsf{xor} \)xor | built-in bitwise XOR |
| \(\scriptsize \mathsf{rshift} \)rshift | built-in bitwise right-shift |
| \(\scriptsize T(x) \)T(x) | \(\scriptsize x\ \mathsf{xor}\ (x\ \mathsf{rshift}\ 27) \)x xor (x rshift 27) |

The generation algorithm consists of the following steps, where \(\scriptsize S_i \)Si denotes begin[i % n], \(\scriptsize V_i \)Vi denotes `v` ﻿[i]:

1) Set each element of the output range to the value 0x8b8b8b8b.2) For each integer k in ``​0​`,`m`)`, performs the following operations in order:1) Let \(\scriptsize r_1 \)r1 be \(\scriptsize 1664525 \cdot T(S_k\ \mathsf{xor}\ S_{k+p}\ \mathsf{xor}\ S_{k-1}) \)1664525·T(Sk xor Sk+p xor Sk-1).2) Let \(\scriptsize r_2 \)r2 be \(\scriptsize r_1 + j \)r1+j, where \(\scriptsize j \)j is:

- \(\scriptsize z \)z, if \(\scriptsize k=0 \)k=0
- \(\scriptsize (k \mod n)+V_{k-1} \)(k mod n)+Vk-1, if \(\scriptsize 0<k⩽z \)0<k⩽z
- \(\scriptsize k \mod n \)k mod n, if \(\scriptsize z<k \)z<k
3) Set \(\scriptsize S_{k+p} \)Sk+p to \(\scriptsize (S_{k+p}+r_1) \mod 2^{32} \)(Sk+p+r1) mod 232  
.4) Set \(\scriptsize S_{k+q} \)Sk+q to \(\scriptsize (S_{k+q}+r_2) \mod 2^{32} \)(Sk+q+r2) mod 232  
.5) Set \(\scriptsize S_k \)Sk to \(\scriptsize r_2 \mod 2^{32} \)r2 mod 232  
.3) For each integer k in `[`m`,`m + n`)`, performs the following operations in order:1) Let \(\scriptsize r_3 \)r3 be \(\scriptsize 1566083941 \cdot T(S_k+S_{k+p}+S_{k-1}) \)1566083941·T(Sk+Sk+p+Sk-1).2) Let \(\scriptsize r_4 \)r4 be \(\scriptsize r_3-(k \mod n) \)r3-(k mod n).3) Set \(\scriptsize S_{k+p} \)Sk+p to \(\scriptsize (S_{k+p}\ \mathsf{xor}\ r_3) \mod 2^{32} \)(Sk+p xor r3) mod 232  
.4) Set \(\scriptsize S_{k+q} \)Sk+q to \(\scriptsize (S_{k+q}\ \mathsf{xor}\ r_4) \mod 2^{32} \)(Sk+q xor r4) mod 232  
.5) Set \(\scriptsize S_k \)Sk to \(\scriptsize r_4 \mod 2^{32} \)r4 mod 232  
.

### Parameters

|  |  |  |
| --- | --- | --- |
| begin, end | - | the iterators denoting the output range |

### Exceptions

Only throws the exceptions thrown by the `RandomIt` operations on begin and end.

### Notes

The generation algorithm is adapted from the initialization sequence of the Mersenne Twister generator by [Makoto Matsumoto and Takuji Nishimura, incorporating the improvements made by Mutsuo Saito in 2007.

### Example

Run this code

```
#include <algorithm>
#include <cassert>
#include <cstdint>
#include <iostream>
#include <random>
 
// Prototyping the main part of std::seed_seq...
struct seed_seq
{
    std::vector<std::uint32_t> v;
 
    seed_seq(std::initializer_list<std::uint32_t> const il) : v{il} {}
 
    template<typename RandomIt>
    void generate(RandomIt first, RandomIt last)
    {
        if (first == last)
            return;
        //
        // Assuming v = {1, 2, 3, 4, 5} and distance(first, last) == 10.
        //
        // Step 1: fill with 0x8b8b8b8b
        // seeds = {2341178251, 2341178251, 2341178251, 2341178251, 2341178251,
        //          2341178251, 2341178251, 2341178251, 2341178251, 2341178251}
        //
        std::fill(first, last, 0x8b8b8b8b);
        //
        // Step 2:
        // n = 10, s = 5, t = 3, p = 3, q = 6, m = 10
        //
        const std::uint32_t n = last - first;
        const std::uint32_t s = v.size();
        const std::uint32_t t = (n < 7) ? (n - 1) / 2
                              : (n < 39) ? 3
                              : (n < 68) ? 5
                              : (n < 623) ? 7
                              : 11;
        const std::uint32_t p = (n - t) / 2;
        const std::uint32_t q = p + t;
        const std::uint32_t m = std::max(s + 1, n);
        //
        // First iteration, k = 0; r1 = 1371501266, r2 = 1371501271
        //
        // seeds = {1371501271, 2341178251, 2341178251, 3712679517, 2341178251,
        //          2341178251, 3712679522, 2341178251, 2341178251, 2341178251}
        //
        // Iterations from k = 1 to k = 5 (r2 = r1 + k % n + v[k - 1])
        //
        // r1 = 2786190137, 3204727651, 4173325571, 1979226628, 401983366
        // r2 = 2786190139, 3204727655, 4173325577, 1979226636, 401983376
        //
        // seeds = {3350727907, 3188173515, 3204727655, 4173325577, 1979226636,
        //           401983376, 3591037797, 2811627722, 1652921976, 2219536532}
        //
        // Iterations from k = 6 to k = 9 (r2 = r1 + k % n)
        //
        // r1 = 2718637909, 1378394210, 2297813071, 1608643617
        // r2 = 2718637915, 1378394217, 2297813079, 1608643626
        //
        // seeds = { 434154821, 1191019290, 3237041891, 1256752498, 4277039715,
        //          2010627002, 2718637915, 1378394217, 2297813079, 1608643626}
        //
        auto begin_mod = first, n -> decltype(*first)&
        {
            return first[u % n]; // i.e. begin[x] is taken modulo n
        };
        auto T = [](std::uint32_t x) { return x ^ (x >> 27); };
 
        for (std::uint32_t k = 0, r1, r2; k < m; ++k)
        {
            r1 = 1664525 * T(begin_mod(k) ^ begin_mod(k + p) ^ begin_mod(k - 1));
            r2 = (k == 0) ? r1 + s
               : (k <= s) ? r1 + k % n + v[k - 1]
               :            r1 + k % n;
            begin_mod(k + p) += r1;
            begin_mod(k + q) += r2;
            begin_mod(k) = r2;
        }
        //
        // Step 3
        // iterations from k = 10 to k = 19, using ^= to modify the output
        //
        // r1 = 1615303485, 3210438310, 893477041, 2884072672, 1918321961,
        // r2 = 1615303485, 3210438309, 893477039, 2884072669, 1918321957
        //
        // seeds = { 303093272, 3210438309,  893477039, 2884072669, 1918321957,
        //          1117182731, 1772877958, 2669970405, 3182737656, 4094066935}
        //
        // r1 =  423054846, 46783064, 3904109085, 1534123446, 1495905687
        // r2 =  423054841, 46783058, 3904109078, 1534123438, 1495905678
        //
        // seeds = { 4204997637, 4246533866, 1856049002, 1129615051, 690460811,
        //           1075771511,   46783058, 3904109078, 1534123438, 1495905678}
        //
        for (std::uint32_t k = m, r3, r4; k < m + n; ++k)
        {
            r3 = 1566083941 * T(begin_mod(k) + begin_mod(k + p) + begin_mod(k - 1));
            r4 = r3 - k % n;
            begin_mod(k+p) ^= r3;
            begin_mod(k+q) ^= r4;
            begin_mod(k) = r4;
        }
    }
};
 
int main()
{
    const auto input = std::initializer_list<std::uint32_t>{1, 2, 3, 4, 5};
    const auto output_size = 10;
 
    // using std version of seed_seq
    std::seed_seq seq(input);
    std::vector<std::uint32_t> seeds(output_size);
    seq.generate(seeds.begin(), seeds.end());
    for (const std::uint32_t n : seeds)
        std::cout << n << '\n';
 
    // using custom version of seed_seq
    seed_seq seq2(input);
    std::vector<std::uint32_t> seeds2(output_size);
    seq2.generate(seeds2.begin(), seeds2.end());
 
    assert(seeds == seeds2);
}

```

Output:

```
4204997637
4246533866
1856049002
1129615051
690460811
1075771511
46783058
3904109078
1534123438
1495905678

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2180 | C++11 | `seed_seq::generate` is non-throwing | it may throw exceptions |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/random/seed_seq/generate&oldid=177248>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 October 2024, at 18:40.