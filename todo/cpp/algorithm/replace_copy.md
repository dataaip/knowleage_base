# std::replace_copy, std::replace_copy_if

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****replace_copyreplace_copy_if**** | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| template< class InputIt, class OutputIt, class T >  OutputIt replace_copy( InputIt first, InputIt last, OutputIt d_first, const T& old_value, const T& new_value ); | (1) | (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt1, class ForwardIt2, class T >  ForwardIt2 replace_copy      ( ExecutionPolicy&& policy,        ForwardIt1 first, ForwardIt1 last, ForwardIt2 d_first, const T& old_value, const T& new_value ); | (2) | (since C++17) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class InputIt, class OutputIt, class UnaryPred, class T >  OutputIt replace_copy_if      ( InputIt first, InputIt last, OutputIt d_first,       UnaryPred p, const T& new_value ); |  | (constexpr since C++20)  (until C++26) |
| template< class InputIt, class OutputIt, class UnaryPred,  class T = typename std::iterator_traits                          <OutputIt>::value_type >  constexpr OutputIt replace_copy_if      ( InputIt first, InputIt last, OutputIt d_first,       UnaryPred p, const T& new_value ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class ExecutionPolicy, class ForwardIt1, class ForwardIt2,  class UnaryPred, class T >  ForwardIt2 replace_copy_if      ( ExecutionPolicy&& policy,        ForwardIt1 first, ForwardIt1 last, ForwardIt2 d_first,       UnaryPred p, const T& new_value ); |  | (since C++17)  (until C++26) |
| template< class ExecutionPolicy, class ForwardIt1, class ForwardIt2,  class UnaryPred, class T = typename std::iterator_traits                                           <ForwardIt2>::value_type >  ForwardIt2 replace_copy_if      ( ExecutionPolicy&& policy,        ForwardIt1 first, ForwardIt1 last, ForwardIt2 d_first,       UnaryPred p, const T& new_value ); |  | (since C++26) |
|  |  |  |

Copies the elements from the range ``first`,`last`)` to another range beginning at d_first, while replacing all elements satisfying specific criteria with new_value.

1) Replaces all elements that are equal to old_value (using operator==).3) Replaces all elements for which predicate p returns true.2,4) Same as (1,3), but executed according to policy. These overloads participate in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| [std::is_execution_policy_v<std::decay_t<ExecutionPolicy>> is true. | (until C++20) |
| std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true. | (since C++20) |

If any of the results of the expressions \*first and new_value is not writable to d_first, the program is ill-formed.

If the source and destination ranges overlap, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to copy |
| d_first | - | the beginning of the destination range |
| old_value | - | the value of elements to replace |
| policy | - | the execution policy to use |
| p | - | unary predicate which returns ​true if the element value should be replaced.   The expression p(v) must be convertible to bool for every argument `v` of type (possibly const) `VT`, where `VT` is the value type of `InputIt`, regardless of value category, and must not modify `v`. Thus, a parameter type of VT&is not allowed, nor is VT unless for `VT` a move is equivalent to a copy(since C++11). ​ |
| new_value | - | the value to use as replacement |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`OutputIt` must meet the requirements of LegacyOutputIterator. | | |
| -`ForwardIt1, ForwardIt2` must meet the requirements of LegacyForwardIterator. | | |

### Return value

Iterator to the element past the last element copied.

### Complexity

Given \(\scriptsize N\)N as std::distance(first, last):

1,2) Exactly \(\scriptsize N\)N comparisons using operator==.3,4) Exactly \(\scriptsize N\)N applications of the predicate p.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Possible implementation

| replace_copy |
| --- |
| ```text template<class InputIt, class OutputIt, class T> OutputIt replace_copy(InputIt first, InputIt last, OutputIt d_first,                       const T& old_value, const T& new_value) {     for (; first != last; ++first)         *d_first++ = (*first == old_value) ? new_value : *first;     return d_first; } ``` |
| replace_copy_if |
| ```text template<class InputIt, class OutputIt, class UnaryPred,          class T = typename std::iterator_traits<ForwardIt>::value_type> OutputIt replace_copy_if(InputIt first, InputIt last, OutputIt d_first,                          UnaryPred p, const T& new_value) {     for (; first != last; ++first)         *d_first++ = p(*first) ? new_value : *first;     return d_first; } ``` |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_algorithm_default_value_type` | `202403` | (C++26) | List-initialization for algorithms (3,4) |

### Example

Run this code

```
#include <algorithm>
#include <complex>
#include <iostream>
#include <vector>
 
void println(const auto& seq)
{
    for (const auto& e : seq)
        std::cout << e << ' ';
    std::cout << '\n';
}
 
int main()
{
    std::vector<short> src{3, 1, 4, 1, 5, 9, 2, 6, 5};
    println(src);
    std::vector<int> dst(src.size());
    std::replace_copy_if(src.cbegin(), src.cend(),
                         dst.begin(),
                         [](short n){ return n > 5; }, 0);
    println(dst);
 
    std::vector<std::complex<double>> src2{{1, 3}, {2, 4}, {3, 5}},
                                      dst2(src2.size());
    println(src2);
    #ifdef __cpp_lib_algorithm_default_value_type
        std::replace_copy_if(src2.cbegin(), src2.cend(), dst2.begin(),
            [](std::complex<double> z){ return std::abs(z) < 5; },
            {4, 2}); // Possible, since the T is deduced.
    #else
        std::replace_copy_if(src2.cbegin(), src2.cend(), dst2.begin(),
            [](std::complex<double> z){ return std::abs(z) < 5; },
            std::complex<double>{4, 2});
    #endif
    println(dst2);
}

```

Output:

```
3 1 4 1 5 9 2 6 5 
3 1 4 1 5 0 2 0 5 
(1,3) (2,4) (3,5) 
(4,2) (4,2) (3,5)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 283 | C++98 | `T` was required to be CopyAssignable (and EqualityComparable for `replace_copy`), but the value type of `InputIt` is not always `T` | removed the requirement |
| LWG 337 | C++98 | `replace_copy_if` only required `InputIt` to meet the requirements of LegacyIterator[[1]](replace_copy.html#cite_note-1) | corrected to LegacyInputIterator |

1. ↑ The actual defect in the C++ standard is that the template parameter `InputIterator` was misspecified as `Iterator`. This affects the type requirements because the C++ standard states that for the function templates in the algorithms library, the template type parameters whose name ends with `Iterator` imply the type requirements of the corresponding iterator categories.

### See also

|  |  |
| --- | --- |
| replacereplace_if | replaces all values satisfying specific criteria with another value   (function template) |
| removeremove_if | removes elements satisfying specific criteria   (function template) |
| ranges::replace_copyranges::replace_copy_if(C++20)(C++20) | copies a range, replacing elements satisfying specific criteria with another value (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/replace_copy&oldid=171916>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 May 2024, at 21:22.