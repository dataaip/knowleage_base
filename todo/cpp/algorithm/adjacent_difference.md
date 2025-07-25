# std::adjacent_difference

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | ****adjacent_difference**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | ****adjacent_difference**** | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<numeric>` |  |  |
| template< class InputIt, class OutputIt >  OutputIt adjacent_difference( InputIt first, InputIt last,                               OutputIt d_first ); | (1) | (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt1, class ForwardIt2 >  ForwardIt2 adjacent_difference( ExecutionPolicy&& policy,                                  ForwardIt1 first, ForwardIt1 last,                                 ForwardIt2 d_first ); | (2) | (since C++17) |
| template< class InputIt, class OutputIt, class BinaryOp >  OutputIt adjacent_difference( InputIt first, InputIt last,                               OutputIt d_first, BinaryOp op ); | (3) | (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt1, class ForwardIt2, class BinaryOp >  ForwardIt2 adjacent_difference( ExecutionPolicy&& policy,                                  ForwardIt1 first, ForwardIt1 last,                                 ForwardIt2 d_first, BinaryOp op ); | (4) | (since C++17) |
|  |  |  |

Let `T` be the value type of decltype(first).

1) If ``first`,`last`)` is empty, does nothing. Otherwise, performs the following operations in order:

1. Creates an accumulator acc of type `T`, and initializes it with \*first.
2. Assigns acc to \*d_first.
3. For each iterator iter in `[`++first`,`last`)` in order, performs the following operations in order:
a) Creates an object val of type `T`, and initializes it with \*iter.b) Computes val - acc(until C++20)val - std::move(acc)(since C++20).c) Assigns the result to \*++d_first.d) Copy(until C++20)Move(since C++20) assigns from val to acc.2) If `[`first`,`last`)` is empty, does nothing. Otherwise, performs the following operations in order:

1. Assigns \*first to \*d_first.
2. For each integer i in `[`1`,`[std::distance(first, last)`)`, performs the following operations in order:
a) Computes curr - prev, where curr is the next ith iterator of first, and prev is the next i - 1th iterator of first.b) Assigns the result to \*dest, where dest is the next ith iterator of d_first.3) Same as (1), but computes op(val, acc)(until C++20)op(val, std::move(acc))(since C++20) instead.4) Same as (2), but computes op(curr, prev) instead.

Given binary_op as the actual binary operation:

- If any of the following conditions is satisfied, the program is ill-formed:

:   - For overloads (1,3):

    :   - `T` is not constructible from \*first.
        - acc is not writable to d_first.
        - The result of binary_op(val, acc)(until C++20)binary_op(val, std::move(acc))(since C++20) is not writable to d_first.

    - For overloads (2,4):

    :   - \*first is not writable to d_first.
        - The result of binary_op(\*first, \*first) is not writable to d_first.

- Given d_last as the iterator to be returned, if any of the following conditions is satisfied, the behavior is undefined:

|  |  |
| --- | --- |
| - For overloads (1,3), `T` is not MoveAssignable. | (since C++20) |

:   - For overloads (2,4), `[`first`,`last`)` and `[`d_first`,`d_last`)` overlaps.
    - binary_op modifies any element of `[`first`,`last`)` or `[`d_first`,`d_last`)`.
    - binary_op invalidates any iterator or subrange in `[`first`,`last`]` or `[`d_first`,`d_last`]`.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements |
| d_first | - | the beginning of the destination range |
| policy | - | the execution policy to use |
| op | - | binary operation function object that will be applied.   The signature of the function should be equivalent to the following:   Ret fun(const Type1 &a, const Type2 &b);  The signature does not need to have const &.  The types  Type1 and  Type2 must be such that an object of type iterator_traits<InputIt>::value_type can be implicitly converted to both of them. The type Ret must be such that an object of type OutputIt can be dereferenced and assigned a value of type Ret. ​ |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`OutputIt` must meet the requirements of LegacyOutputIterator. | | |
| -`ForwardIt1, ForwardIt2` must meet the requirements of LegacyForwardIterator. | | |

### Return value

Iterator to the element past the last element written, or d_first if ``first`,`last`)` is empty.

### Complexity

Given \(\scriptsize N\)N as [std::distance(first, last):

1,2) Exactly \(\scriptsize N-1\)N-1 applications of operator-.3,4) Exactly \(\scriptsize N-1\)N-1 applications of the binary function op.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Possible implementation

| adjacent_difference (1) |
| --- |
| ```text template<class InputIt, class OutputIt> constexpr // since C++20 OutputIt adjacent_difference(InputIt first, InputIt last, OutputIt d_first) {     if (first == last)         return d_first;       typedef typename std::iterator_traits<InputIt>::value_type value_t;     value_t acc = *first;     *d_first = acc;       while (++first != last)     {         value_t val = *first;         *++d_first = val - std::move(acc); // std::move since C++20         acc = std::move(val);     }       return ++d_first; } ``` |
| adjacent_difference (3) |
| ```text template<class InputIt, class OutputIt, class BinaryOp> constexpr // since C++20 OutputIt adjacent_difference(InputIt first, InputIt last,                               OutputIt d_first, BinaryOp op) {     if (first == last)         return d_first;       typedef typename std::iterator_traits<InputIt>::value_type value_t;     value_t acc = *first;     *d_first = acc;       while (++first != last)     {         value_t val = *first;         *++d_first = op(val, std::move(acc)); // std::move since C++20         acc = std::move(val);     }       return ++d_first; } ``` |

### Notes

acc was introduced because of the resolution of LWG issue 539. The reason of using acc rather than directly calculating the differences is because the semantic of the latter is confusing if the following types mismatch:

- the value type of `InputIt`
- the writable type(s) of `OutputIt`
- the types of the parameters of operator- or op
- the return type of operator- or op

acc serves as the intermediate object to cache values of the iterated elements:

- its type is the value type of `InputIt`
- the value written to d_first (which is the return value of operator- or op) is assigned to it
- its value is passed to operator- or op

```
char i_array[4] = {100, 100, 100, 100};
int  o_array[4];
 
// OK: performs conversions when needed
// 1. creates “acc” of type char (the value type)
// 2. “acc” is assigned to the first element of “o_array”
// 3. the char arguments are used for long multiplication (char -> long)
// 4. the long product is assigned to the output range (long -> int)
// 5. the next value of “i_array” is assigned to “acc”
// 6. go back to step 3 to process the remaining elements in the input range
std::adjacent_difference(i_array, i_array + 4, o_array, std::multiplies<long>{});

```

### Example

Run this code

```
#include <array>
#include <functional>
#include <iostream>
#include <iterator>
#include <numeric>
#include <vector>
 
void println(auto comment, const auto& sequence)
{
    std::cout << comment;
    for (const auto& n : sequence)
        std::cout << n << ' ';
    std::cout << '\n';
};
 
int main()
{
    // Default implementation - the difference between two adjacent items
    std::vector v{4, 6, 9, 13, 18, 19, 19, 15, 10};
    println("Initially, v = ", v);
    std::adjacent_difference(v.begin(), v.end(), v.begin());
    println("Modified v = ", v);
 
    // Fibonacci
    std::array<int, 10> a {1};
    std::adjacent_difference(std::begin(a), std::prev(std::end(a)),
                             std::next(std::begin(a)), std::plus<>{});
    println("Fibonacci, a = ", a);
}

```

Output:

```
Initially, v = 4 6 9 13 18 19 19 15 10 
Modified v = 4 2 3 4 5 1 0 -4 -5 
Fibonacci, a = 1 1 2 3 5 8 13 21 34 55

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 242 | C++98 | op could not have side effects | it cannot modify the ranges involved |
| LWG 539 | C++98 | the type requirements needed for the result evaluations and assignments to be valid were missing | added |
| LWG 3058 | C++17 | for overloads (2,4), the result of each invocation of operator- or op was assigned to a temporary object, and that object is assigned to the output range | assign the results to the output range directly |

### See also

|  |  |
| --- | --- |
| partial_sum | computes the partial sum of a range of elements   (function template) |
| accumulate | sums up or folds a range of elements   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/adjacent_difference&oldid=176954>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 October 2024, at 02:16.