# std::is_permutation

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****is_permutation****(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| template< class ForwardIt1, class ForwardIt2 >  bool is_permutation( ForwardIt1 first1, ForwardIt1 last1,                      ForwardIt2 first2 ); | (1) | (since C++11)  (constexpr since C++20) |
| template< class ForwardIt1, class ForwardIt2,  class BinaryPredicate >  bool is_permutation( ForwardIt1 first1, ForwardIt1 last1,                      ForwardIt2 first2, BinaryPredicate p ); | (2) | (since C++11)  (constexpr since C++20) |
| template< class ForwardIt1, class ForwardIt2 >  bool is_permutation( ForwardIt1 first1, ForwardIt1 last1,                      ForwardIt2 first2, ForwardIt2 last2 ); | (3) | (since C++14)  (constexpr since C++20) |
| template< class ForwardIt1, class ForwardIt2,  class BinaryPredicate >  bool is_permutation( ForwardIt1 first1, ForwardIt1 last1,                       ForwardIt2 first2, ForwardIt2 last2,                      BinaryPredicate p ); | (4) | (since C++14)  (constexpr since C++20) |
|  |  |  |

Checks whether ``first1`,`last1`)` is a [permutation of a range starting from first2:

- For overloads (1,2), the second range has std::distance(first1, last1) elements.
- For overloads (3,4), the second range is ``first2`,`last2`)`.

1,3) Elements are compared using operator==.2,4) Elements are compared using the given binary predicate p.

If `ForwardIt1` and `ForwardIt2` have different [value types, the program is ill-formed.

If the comparison function is not an equivalence relation, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| first1, last1 | - | the range of elements to compare |
| first2, last2 | - | the second range to compare |
| p | - | binary predicate which returns ​true if the elements should be treated as equal.   The signature of the predicate function should be equivalent to the following:   bool pred(const Type1 &a, const Type2 &b);  While the signature does not need to have const &, the function must not modify the objects passed to it and must be able to accept all values of type (possibly const) `Type1` and `Type2` regardless of value category (thus, Type1 & is not allowed, nor is Type1 unless for `Type1` a move is equivalent to a copy(since C++11)).  The types Type1 and Type2 must be such that objects of types InputIt1 and InputIt2 can be dereferenced and then implicitly converted to Type1 and Type2 respectively. ​ |
| Type requirements | | |
| -`ForwardIt1, ForwardIt2` must meet the requirements of LegacyForwardIterator. | | |

### Return value

true if the range ``first1`,`last1`)` is a permutation of the range `[`first2`,`last2`)`, false otherwise.

### Complexity

Given \(\scriptsize N\)N as [std::distance(first1, last1):

1) Exactly \(\scriptsize N\)N comparisons using operator== if the two ranges are equal, otherwise \(\scriptsize O(N^2)\)O(N2  
) comparisons in the worst case.2) Exactly \(\scriptsize N\)N applications of the predicate p if the two ranges are equal, otherwise \(\scriptsize O(N^2)\)O(N2  
) applications in the worst case.3,4) If `ForwardIt1` and `ForwardIt2` are both LegacyRandomAccessIterator, and last1 - first1 != last2 - first2 is true, no comparison will be made. Otherwise:3) Exactly \(\scriptsize N\)N comparisons using operator== if the two ranges are equal, otherwise \(\scriptsize O(N^2)\)O(N2  
) comparisons in the worst case.4) Exactly \(\scriptsize N\)N applications of the predicate p if the two ranges are equal, otherwise \(\scriptsize O(N^2)\)O(N2  
) applications in the worst case.

### Possible implementation

|  |
| --- |
| ```text template<class ForwardIt1, class ForwardIt2> bool is_permutation(ForwardIt1 first, ForwardIt1 last,                     ForwardIt2 d_first) {     // skip common prefix     std::tie(first, d_first) = std::mismatch(first, last, d_first);       // iterate over the rest, counting how many times each element     // from first, last) appears in [d_first, d_last)     if (first != last)     {         ForwardIt2 d_last = std::next(d_first, std::distance(first, last));         for (ForwardIt1 i = first; i != last; ++i)         {             if (i != std::find(first, i, *i))                 continue; // this *i has been checked               auto m = std::count(d_first, d_last, *i);             if (m == 0 || std::count(i, last, *i) != m)                 return false;         }     }     return true; } ``` |

### Note

The `std::is_permutation` can be used in **testing**, namely to check the correctness of rearranging algorithms (e.g. sorting, shuffling, partitioning). If `x` is an original range and `y` is a **permuted** range then std::is_permutation(x, y) == true means that `y` consist of **"the same"** elements, maybe staying at other positions.

### Example

Run this code

```
#include <algorithm>
#include <iostream>
 
template<typename Os, typename V>
Os& operator<<(Os& os, const V& v)
{
    os << "{ ";
    for (const auto& e : v)
        os << e << ' ';
    return os << '}';
}
 
int main()
{
    static constexpr auto v1 = {1, 2, 3, 4, 5};
    static constexpr auto v2 = {3, 5, 4, 1, 2};
    static constexpr auto v3 = {3, 5, 4, 1, 1};
 
    std::cout << v2 << " is a permutation of " << v1 << ": " << std::boolalpha
              << std::is_permutation(v1.begin(), v1.end(), v2.begin()) << '\n'
              << v3 << " is a permutation of " << v1 << ": "
              << std::is_permutation(v1.begin(), v1.end(), v3.begin()) << '\n';
}

```

Output:

```
{ 3 5 4 1 2 } is a permutation of { 1 2 3 4 5 }: true
{ 3 5 4 1 1 } is a permutation of { 1 2 3 4 5 }: false

```

### See also

|  |  |
| --- | --- |
| [next_permutation | generates the next greater lexicographic permutation of a range of elements   (function template) |
| prev_permutation | generates the next smaller lexicographic permutation of a range of elements   (function template) |
| equivalence_relation(C++20) | specifies that a `relation` imposes an equivalence relation   (concept) |
| ranges::is_permutation(C++20) | determines if a sequence is a permutation of another sequence (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/is_permutation&oldid=170765>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 April 2024, at 18:50.