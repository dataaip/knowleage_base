# std::count, std::count_if

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | ****countcount_if**** | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class InputIt, class T >  typename std::iterator_traits<InputIt>::difference_type     count( InputIt first, InputIt last, const T& value ); |  | (constexpr since C++20)  (until C++26) |
| template< class InputIt, class T = typename std::iterator_traits  <InputIt>::value_type >  constexpr typename std::iterator_traits<InputIt>::difference_type     count( InputIt first, InputIt last, const T& value ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class ExecutionPolicy, class ForwardIt, class T >  typename std::iterator_traits<ForwardIt>::difference_type      count( ExecutionPolicy&& policy,            ForwardIt first, ForwardIt last, const T& value ); |  | (since C++17)  (until C++26) |
| template< class ExecutionPolicy,  class ForwardIt, class T = typename std::iterator_traits                                           <ForwardIt>::value_type >  typename std::iterator_traits<ForwardIt>::difference_type      count( ExecutionPolicy&& policy,            ForwardIt first, ForwardIt last, const T& value ); |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt, class UnaryPred >  typename std::iterator_traits<InputIt>::difference_type     count_if( InputIt first, InputIt last, UnaryPred p ); | (3) | (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt, class UnaryPred >  typename std::iterator_traits<ForwardIt>::difference_type      count_if( ExecutionPolicy&& policy,               ForwardIt first, ForwardIt last, UnaryPred p ); | (4) | (since C++17) |
|  |  |  |

Returns the number of elements in the range ``first`,`last`)` satisfying specific criteria.

1) Counts the elements that are equal to value (using operator==).3) Counts elements for which predicate p returns true.2,4) Same as (1,3), but executed according to policy. These overloads participate in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| [std::is_execution_policy_v<std::decay_t<ExecutionPolicy>> is true. | (until C++20) |
| std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to examine |
| value | - | the value to search for |
| policy | - | the execution policy to use |
| p | - | unary predicate which returns ​true for the required elements.   The expression p(v) must be convertible to bool for every argument `v` of type (possibly const) `VT`, where `VT` is the value type of `InputIt`, regardless of value category, and must not modify `v`. Thus, a parameter type of VT&is not allowed, nor is VT unless for `VT` a move is equivalent to a copy(since C++11). ​ |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`ForwardIt` must meet the requirements of LegacyForwardIterator. | | |
| -`UnaryPred` must meet the requirements of Predicate. | | |

### Return value

The number of iterators it in the range ``first`,`last`)` satisfying the following condition:

1,2) \*it == value is true.3,4) p(\*it) != false is true.

### Complexity

Given \(\scriptsize N\)N as [std::distance(first, last):

1,2) Exactly \(\scriptsize N\)N comparisons with value using operator==.3,4) Exactly \(\scriptsize N\)N applications of the predicate p.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Notes

For the number of elements in the range ``first`,`last`)` without any additional criteria, see [std::distance.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_algorithm_default_value_type` | `202403` | (C++26) | List-initialization for algorithms (1,2) |

### Possible implementation

See also the implementations of `count` in libstdc++ and libc++.

See also the implementations of `count_if` in libstdc++ and libc++.

| count |
| --- |
| ```text template<class InputIt, class T = typename std::iterator_traits<InputIt>::value_type> typename std::iterator_traits<InputIt>::difference_type     count(InputIt first, InputIt last, const T& value) {     typename std::iterator_traits<InputIt>::difference_type ret = 0;     for (; first != last; ++first)         if (*first == value)             ++ret;     return ret; } ``` |
| count_if |
| ```text template<class InputIt, class UnaryPred> typename std::iterator_traits<InputIt>::difference_type     count_if(InputIt first, InputIt last, UnaryPred p) {     typename std::iterator_traits<InputIt>::difference_type ret = 0;     for (; first != last; ++first)         if (p(*first))             ++ret;     return ret; } ``` |

### Example

Run this code

```
#include <algorithm>
#include <array>
#include <cassert>
#include <complex>
#include <iostream>
#include <iterator>
 
int main()
{
    constexpr std::array v{1, 2, 3, 4, 4, 3, 7, 8, 9, 10};
    std::cout << "v: ";
    std::copy(v.cbegin(), v.cend(), std::ostream_iterator<int>(std::cout, " "));
    std::cout << '\n';
 
    // Determine how many integers match a target value.
    for (const int target : {3, 4, 5})
    {
        const int num_items = std::count(v.cbegin(), v.cend(), target);
        std::cout << "number: " << target << ", count: " << num_items << '\n';
    }
 
    // Use a lambda expression to count elements divisible by 4.
    int count_div4 = std::count_if(v.begin(), v.end(), [](int i) { return i % 4 == 0; });
    std::cout << "numbers divisible by four: " << count_div4 << '\n';
 
    // A simplified version of `distance` with O(N) complexity:
    auto distance = [](auto first, auto last)
    {
        return std::count_if(first, last, [](auto) { return true; });
    };
    static_assert(distance(v.begin(), v.end()) == 10);
 
    std::array<std::complex<double>, 3> nums{{{4, 2}, {1, 3}, {4, 2}}};
    #ifdef __cpp_lib_algorithm_default_value_type
        // T gets deduced making list-initialization possible
        auto c = std::count(nums.cbegin(), nums.cend(), {4, 2});
    #else
        auto c = std::count(nums.cbegin(), nums.cend(), std::complex<double>{4, 2});
    #endif
    assert(c == 2);
}

```

Output:

```
v: 1 2 3 4 4 3 7 8 9 10
number: 3, count: 2
number: 4, count: 2
number: 5, count: 0
numbers divisible by four: 3

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 283 | C++98 | `T` was required to be EqualityComparable, but the value type of `InputIt` is not always `T` | removed the requirement |

### See also

|  |  |
| --- | --- |
| distance | returns the distance between two iterators   (function template) |
| ranges::countranges::count_if(C++20)(C++20) | returns the number of elements satisfying specific criteria (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/count&oldid=171908>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 May 2024, at 21:15.