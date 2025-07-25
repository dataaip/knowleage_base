# std::partial_sum

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****partial_sum**** | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | ****partial_sum**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<numeric>` |  |  |
| template< class InputIt, class OutputIt >  OutputIt partial_sum( InputIt first, InputIt last,                       OutputIt d_first ); | (1) | (constexpr since C++20) |
| template< class InputIt, class OutputIt, class BinaryOp >  OutputIt partial_sum( InputIt first, InputIt last,                       OutputIt d_first, BinaryOp op ); | (2) | (constexpr since C++20) |
|  |  |  |

1) If ``first`,`last`)` is empty, does nothing. Otherwise, performs the following operations in order:

1. Creates an accumulator acc, whose type is the [value type of `InputIt`, and initializes it with \*first.
2. Assigns acc to \*d_first.
3. For each integer i in ``1`,`[std::distance(first, last)`)`, performs the following operations in order:
a) Computes acc + \*iter(until C++20)std::move(acc) + \*iter(since C++20), where iter is the next ith iterator of first.b) Assigns the result to acc.c) Assigns acc[[1]](partial_sum.html#cite_note-1) to \*dest, where dest is the next ith iterator of d_first.2) Same as (1), but computes op(acc, \*iter)(until C++20)op(std::move(acc), \*iter)(since C++20) instead.

Given binary_op as the actual binary operation:

- If any of the following conditions is satisfied, the program is ill-formed:

:   - The value type of `InputIt` is not constructible from \*first.
    - acc is not writable to d_first.
    - The result of binary_op(acc, \*iter)(until C++20)binary_op(std::move(acc), \*iter)(since C++20) is not implicitly convertible to the value type of `InputIt`.

- Given d_last as the iterator to be returned, if any of the following conditions is satisfied, the behavior is undefined:

:   - binary_op modifies any element of `[`first`,`last`)` or `[`d_first`,`d_last`)`.
    - binary_op invalidates any iterator or subrange in `[`first`,`last`]` or `[`d_first`,`d_last`]`.

1. ↑ The actual value to be assigned is the result of the assignment in the previous step. We assume the assignment result is acc here.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to sum |
| d_first | - | the beginning of the destination range; may be equal to first |
| op | - | binary operation function object that will be applied.   The signature of the function should be equivalent to the following:   Ret fun(const Type1 &a, const Type2 &b);  The signature does not need to have const &.  The type  Type1 must be such that an object of type std::iterator_traits<InputIt>::value_type can be implicitly converted to  Type1. The type  Type2 must be such that an object of type InputIt can be dereferenced and then implicitly converted to  Type2. The type Ret must be such that an object of type InputIt can be dereferenced and assigned a value of type Ret. ​ |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`OutputIt` must meet the requirements of LegacyOutputIterator. | | |

### Return value

Iterator to the element past the last element written, or d_first if ``first`,`last`)` is empty.

### Complexity

Given \(\scriptsize N\)N as [std::distance(first, last):

1) Exactly \(\scriptsize N-1\)N-1 applications of operator+.2) Exactly \(\scriptsize N-1\)N-1 applications of the binary function op.

### Possible implementation

| partial_sum (1) |
| --- |
| ```text template<class InputIt, class OutputIt> constexpr // since C++20 OutputIt partial_sum(InputIt first, InputIt last, OutputIt d_first) {     if (first == last)         return d_first;       typename std::iterator_traits<InputIt>::value_type sum = *first;     *d_first = sum;       while (++first != last)     {         sum = std::move(sum) + *first; // std::move since C++20         *++d_first = sum;     }       return ++d_first;       // or, since C++14:     // return std::partial_sum(first, last, d_first, std::plus<>()); } ``` |
| partial_sum (2) |
| ```text template<class InputIt, class OutputIt, class BinaryOp> constexpr // since C++20 OutputIt partial_sum(InputIt first, InputIt last,                       OutputIt d_first, BinaryOp op) {     if (first == last)         return d_first;       typename std::iterator_traits<InputIt>::value_type acc = *first;     *d_first = acc;       while (++first != last)     {         acc = op(std::move(acc), *first); // std::move since C++20         *++d_first = acc;     }       return ++d_first; } ``` |

### Notes

acc was introduced because of the resolution of LWG issue 539. The reason of using acc rather than directly summing up the results (i.e. \*(d_first + 2) = (\*first + \*(first + 1)) + \*(first + 2);) is because the semantic of the latter is confusing if the following types mismatch:

- the value type of `InputIt`
- the writable type(s) of `OutputIt`
- the types of the parameters of operator+ or op
- the return type of operator+ or op

acc serves as the intermediate object to store and provide the values for each step of the computation:

- its type is the value type of `InputIt`
- it is written to d_first
- its value is passed to operator+ or op
- it stores the return value of operator+ or op

```
enum not_int { x = 1, y = 2 };
 
char i_array[4] = {100, 100, 100, 100};
not_int e_array[4] = {x, x, y, y};
int  o_array[4];
 
// OK: uses operator+(char, char) and assigns char values to int array
std::partial_sum(i_array, i_array + 4, o_array);
 
// Error: cannot assign not_int values to int array
std::partial_sum(e_array, e_array + 4, o_array);
 
// OK: performs conversions when needed
// 1. creates “acc” of type char (the value type)
// 2. the char arguments are used for long multiplication (char -> long)
// 3. the long product is assigned to “acc” (long -> char)
// 4. “acc” is assigned to an element of “o_array” (char -> int)
// 5. go back to step 2 to process the remaining elements in the input range
std::partial_sum(i_array, i_array + 4, o_array, std::multiplies<long>{});

```

### Example

Run this code

```
#include <functional>
#include <iostream>
#include <iterator>
#include <numeric>
#include <vector>
 
int main()
{
    std::vector<int> v(10, 2); // v = {2, 2, 2, 2, 2, 2, 2, 2, 2, 2}
 
    std::cout << "The first " << v.size() << " even numbers are: ";
    // write the result to the cout stream
    std::partial_sum(v.cbegin(), v.cend(), 
                     std::ostream_iterator<int>(std::cout, " "));
    std::cout << '\n';
 
    // write the result back to the vector v
    std::partial_sum(v.cbegin(), v.cend(),
                     v.begin(), std::multiplies<int>());
 
    std::cout << "The first " << v.size() << " powers of 2 are: ";
    for (int n : v)
        std::cout << n << ' ';
    std::cout << '\n';
}

```

Output:

```
The first 10 even numbers are: 2 4 6 8 10 12 14 16 18 20 
The first 10 powers of 2 are: 2 4 8 16 32 64 128 256 512 1024

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 242 | C++98 | op could not have side effects | it cannot modify the ranges involved |
| LWG 539 | C++98 | the type requirements needed for the result evaluations and assignments to be valid were missing | added |

### See also

|  |  |
| --- | --- |
| adjacent_difference | computes the differences between adjacent elements in a range   (function template) |
| accumulate | sums up or folds a range of elements   (function template) |
| inclusive_scan(C++17) | similar to ****std::partial_sum****, includes the ith input element in the ith sum   (function template) |
| exclusive_scan(C++17) | similar to ****std::partial_sum****, excludes the ith input element from the ith sum   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/partial_sum&oldid=176154>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 September 2024, at 05:02.