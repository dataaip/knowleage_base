# std::reduce

From cppreference.com
< cpp‎ | algorithm
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

Algorithm library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Constrained algorithms and algorithms on ranges (C++20) | | | | |
| Constrained algorithms, e.g. ranges::copy, ranges::sort, ... | | | | |
| Execution policies (C++17) | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_execution_policy(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::seqexecution::parexecution::par_unseqexecution::unseq(C++17)    (C++17)(C++17)(C++20) | | | | | | | |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::sequenced_policyexecution::parallel_policyexecution::parallel_unsequenced_policyexecution::parallel_unsequenced(C++17)(C++17)(C++17)(C++20) | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | ****reduce****(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****reduce****(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<numeric>` |  |  |
| template< class InputIt >  typename std::iterator_traits<InputIt>::value_type     reduce( InputIt first, InputIt last ); | (1) | (since C++17)  (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt >  typename std::iterator_traits<ForwardIt>::value_type      reduce( ExecutionPolicy&& policy,             ForwardIt first, ForwardIt last ); | (2) | (since C++17) |
| template< class InputIt, class T >  T reduce( InputIt first, InputIt last, T init ); | (3) | (since C++17)  (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt, class T >  T reduce( ExecutionPolicy&& policy,           ForwardIt first, ForwardIt last, T init ); | (4) | (since C++17) |
| template< class InputIt, class T, class BinaryOp >  T reduce( InputIt first, InputIt last, T init, BinaryOp op ); | (5) | (since C++17)  (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt, class T, class BinaryOp >  T reduce( ExecutionPolicy&& policy,           ForwardIt first, ForwardIt last, T init, BinaryOp op ); | (6) | (since C++17) |
|  |  |  |

1) Equivalent to reduce(first, last, typename std::iterator_traits<InputIt>::value_type{}).3) Equivalent to reduce(first, last, init, std::plus<>()).5) Reduces the range ``first`,`last`)`, possibly permuted and aggregated in unspecified manner, along with the initial value init over op.2,4,6) Same as (1,3,5), but executed according to policy. These overloads participate in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| [std::is_execution_policy_v<std::decay_t<ExecutionPolicy>> is true. | (until C++20) |
| std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true. | (since C++20) |

Given binary_op as the actual binary operation:

- The result is non-deterministic if the binary_op is not associative or not commutative (such as floating-point addition).

- If any of the following values is not convertible to `T`, the program is ill-formed:

:   - binary_op(init, \*first)
    - binary_op(\*first, init)
    - binary_op(init, init)
    - binary_op(\*first, \*first)

- If any of the following conditions is satisfied, the behavior is undefined:

:   - `T` is not MoveConstructible.
    - binary_op modifies any element of `[`first`,`last`)`.
    - binary_op invalidates any iterator or subrange of `[`first`,`last`]`.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to apply the algorithm to |
| init | - | the initial value of the generalized sum |
| policy | - | the execution policy to use |
| op | - | binary FunctionObject that will be applied in unspecified order to the result of dereferencing the input iterators, the results of other op and init. |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`ForwardIt` must meet the requirements of LegacyForwardIterator. | | |

### Return value

1-4) The generalized sum of init and the elements of ``first`,`last`)` over [std::plus<>().5,6) The generalized sum of init and the elements of ``first`,`last`)` over op.

The **generalized sum** of a group of elements over an binary operation binary_op is defined as follows:

- If the group only has one element, the sum is the value of the element.
- Otherwise, performs the following operations in order:

1. Takes any two elements elem1 and elem2 from the group.
2. Calculates binary_op(elem1, elem2) and puts the result back to the group.
3. Repeats steps 1 and 2 until there is only one element in the group.

### Complexity

Given \(\scriptsize N\)N as [std::distance(first, last):

1-4) \(\scriptsize O(N)\)O(N) applications of std::plus<>().5,6) \(\scriptsize O(N)\)O(N) applications of op.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Notes

`std::reduce` behaves like std::accumulate except the elements of the range may be grouped and rearranged in arbitrary order.

### Example

Side-by-side comparison between `std::reduce` and std::accumulate:

Run this code

```
#if PARALLEL
#include <execution>
#define SEQ std::execution::seq,
#define PAR std::execution::par,
#else
#define SEQ
#define PAR
#endif
 
#include <chrono>
#include <iomanip>
#include <iostream>
#include <locale>
#include <numeric>
#include <utility>
#include <vector>
 
int main()
{
    std::cout.imbue(std::locale("en_US.UTF-8"));
    std::cout << std::fixed << std::setprecision(1);
 
    auto eval = [](auto fun)
    {
        const auto t1 = std::chrono::high_resolution_clock::now();
        const auto [name, result] = fun();
        const auto t2 = std::chrono::high_resolution_clock::now();
        const std::chrono::duration<double, std::milli> ms = t2 - t1;
        std::cout << std::setw(28) << std::left << name << "sum: "
                  << result << '\t' << "time: " << ms.count() << " ms\n";
    };
 
    {
        const std::vector<double> v(100'000'007, 0.1);
 
        eval([&v]{ return std::pair{"std::accumulate (double)",
            std::accumulate(v.cbegin(), v.cend(), 0.0)}; });
        eval([&v]{ return std::pair{"std::reduce (seq, double)",
            std::reduce(SEQ v.cbegin(), v.cend())}; });
        eval([&v]{ return std::pair{"std::reduce (par, double)",
            std::reduce(PAR v.cbegin(), v.cend())}; });
    }
 
    {
        const std::vector<long> v(100'000'007, 1);
 
        eval([&v]{ return std::pair{"std::accumulate (long)",
            std::accumulate(v.cbegin(), v.cend(), 0l)}; });
        eval([&v]{ return std::pair{"std::reduce (seq, long)",
            std::reduce(SEQ v.cbegin(), v.cend())}; });
        eval([&v]{ return std::pair{"std::reduce (par, long)",
            std::reduce(PAR v.cbegin(), v.cend())}; });
    }
}

```

Possible output:

```
// POSIX: g++ -std=c++23 ./example.cpp -ltbb -O3; ./a.out
std::accumulate (double)    sum: 10,000,000.7	time: 356.9 ms
std::reduce (seq, double)   sum: 10,000,000.7	time: 140.1 ms
std::reduce (par, double)   sum: 10,000,000.7	time: 140.1 ms
std::accumulate (long)      sum: 100,000,007	time: 46.0 ms
std::reduce (seq, long)     sum: 100,000,007	time: 67.3 ms
std::reduce (par, long)     sum: 100,000,007	time: 63.3 ms
 
// POSIX: g++ -std=c++23 ./example.cpp -ltbb -O3 -DPARALLEL; ./a.out
std::accumulate (double)    sum: 10,000,000.7	time: 353.4 ms
std::reduce (seq, double)   sum: 10,000,000.7	time: 140.7 ms
std::reduce (par, double)   sum: 10,000,000.7	time: 24.7 ms
std::accumulate (long)      sum: 100,000,007	time: 42.4 ms
std::reduce (seq, long)     sum: 100,000,007	time: 52.0 ms
std::reduce (par, long)     sum: 100,000,007	time: 23.1 ms

```

### See also

|  |  |
| --- | --- |
| accumulate | sums up or folds a range of elements   (function template) |
| transform | applies a function to a range of elements, storing results in a destination range   (function template) |
| transform_reduce(C++17) | applies an invocable, then reduces out of order   (function template) |
| ranges::fold_left(C++23) | left-folds a range of elements (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/reduce&oldid=180244>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 February 2025, at 17:09.