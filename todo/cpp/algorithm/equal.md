# std::equal

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | ****equal**** | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | shift_leftshift_right(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| template< class InputIt1, class InputIt2 >  bool equal( InputIt1 first1, InputIt1 last1,             InputIt2 first2 ); | (1) | (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt1, class ForwardIt2 >  bool equal( ExecutionPolicy&& policy,              ForwardIt1 first1, ForwardIt1 last1,             ForwardIt2 first2 ); | (2) | (since C++17) |
| template< class InputIt1, class InputIt2, class BinaryPred >  bool equal( InputIt1 first1, InputIt1 last1,             InputIt2 first2, BinaryPred p ); | (3) | (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt1, class ForwardIt2, class BinaryPred >  bool equal( ExecutionPolicy&& policy,              ForwardIt1 first1, ForwardIt1 last1,             ForwardIt2 first2, BinaryPred p ); | (4) | (since C++17) |
| template< class InputIt1, class InputIt2 >  bool equal( InputIt1 first1, InputIt1 last1,             InputIt2 first2, InputIt2 last2 ); | (5) | (since C++14)  (constexpr since C++20) |
| template< class ExecutionPolicy, class ForwardIt1, class ForwardIt2 >  bool equal( ExecutionPolicy&& policy,              ForwardIt1 first1, ForwardIt1 last1,             ForwardIt2 first2, ForwardIt2 last2 ); | (6) | (since C++17) |
| template< class InputIt1, class InputIt2, class BinaryPred >  bool equal( InputIt1 first1, InputIt1 last1,             InputIt2 first2, InputIt2 last2, BinaryPred p ); | (7) | (since C++14)  (constexpr since C++20) |
| template< class ExecutionPolicy,  class ForwardIt1, class ForwardIt2, class BinaryPred >  bool equal( ExecutionPolicy&& policy,              ForwardIt1 first1, ForwardIt1 last1,             ForwardIt2 first2, ForwardIt2 last2, BinaryPred p ); | (8) | (since C++17) |
|  |  |  |

Checks whether ``first1`,`last1`)` and a range starting from first2 are equal:

- For overloads (1-4), the second range has [std::distance(first1, last1) elements.
- For overloads (5-8), the second range is ``first2`,`last2`)`.

1,5) Elements are compared using operator==.3,7) Elements are compared using the given binary predicate p.2,4,6,8) Same as (1,3,5,7), but executed according to policy. These overloads participate in overload resolution only if all following conditions are satisfied:

|  |  |
| --- | --- |
| [std::is_execution_policy_v<std::decay_t<ExecutionPolicy>> is true. | (until C++20) |
| std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| first1, last1 | - | the first range of the elements to compare |
| first2, last2 | - | the second range of the elements to compare |
| policy | - | the execution policy to use |
| p | - | binary predicate which returns ​true if the elements should be treated as equal.   The signature of the predicate function should be equivalent to the following:   bool pred(const Type1 &a, const Type2 &b);  While the signature does not need to have const &, the function must not modify the objects passed to it and must be able to accept all values of type (possibly const) `Type1` and `Type2` regardless of value category (thus, Type1 & is not allowed, nor is Type1 unless for `Type1` a move is equivalent to a copy(since C++11)).  The types Type1 and Type2 must be such that objects of types InputIt1 and InputIt2 can be dereferenced and then implicitly converted to Type1 and Type2 respectively. ​ |
| Type requirements | | |
| -`InputIt1, InputIt2` must meet the requirements of LegacyInputIterator. | | |
| -`ForwardIt1, ForwardIt2` must meet the requirements of LegacyForwardIterator. | | |
| -`BinaryPred` must meet the requirements of BinaryPredicate. | | |

### Return value

1-4) If each corresponding elements in the two ranges are equal, returns true. Otherwise returns false.5-8) If std::distance(first1, last1) and std::distance(first2, last2) are equal, and each corresponding elements in the two ranges are equal, returns true. Otherwise returns false.

### Complexity

Given \(\scriptsize N_1\)N1 as std::distance(first1, last1) and \(\scriptsize N_2\)N2 as std::distance(first2, last2):

1) At most \(\scriptsize N_1\)N1 comparisons using operator==.2) \(\scriptsize O(N_1)\)O(N1) comparisons using operator==.3) At most \(\scriptsize N_1\)N1 applications of the predicate p.4) \(\scriptsize O(N_1)\)O(N1) applications of the predicate p.5-8) If `InputIt1` and `InputIt2` are both LegacyRandomAccessIterator, and last1 - first1 != last2 - first2 is true, no comparison will be made. Otherwise, given \(\scriptsize N\)N as \(\scriptsize \min(N_1,N_2)\)min(N1,N2):5) At most \(\scriptsize N\)N comparisons using operator==.6) \(\scriptsize O(N)\)O(N) comparisons using operator==.7) At most \(\scriptsize N\)N applications of the predicate p.8) \(\scriptsize O(N)\)O(N) applications of the predicate p.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Possible implementation

| equal (1) |
| --- |
| ```text template<class InputIt1, class InputIt2> constexpr //< since C++20 bool equal(InputIt1 first1, InputIt1 last1, InputIt2 first2) {     for (; first1 != last1; ++first1, ++first2)         if (!(*first1 == *first2))             return false;       return true; } ``` |
| equal (3) |
| ```text template<class InputIt1, class InputIt2, class BinaryPred> constexpr //< since C++20 bool equal(InputIt1 first1, InputIt1 last1,            InputIt2 first2, BinaryPred p) {     for (; first1 != last1; ++first1, ++first2)         if (!p(*first1, *first2))             return false;       return true; } ``` |
| equal (5) |
| ```text namespace detail {     // random-access iterator implementation (allows quick range size detection)     template<class RandomIt1, class RandomIt2>     constexpr //< since C++20     bool equal(RandomIt1 first1, RandomIt1 last1, RandomIt2 first2, RandomIt2 last2,                std::random_access_iterator_tag, std::random_access_iterator_tag)     {         if (last1 - first1 != last2 - first2)             return false;           for (; first1 != last1; ++first1, ++first2)             if (!(*first1 == *first2))                 return false;           return true;     }       // input iterator implementation (needs to manually compare with “last2”)     template<class InputIt1, class InputIt2>     constexpr //< since C++20     bool equal(InputIt1 first1, InputIt1 last1, InputIt2 first2, InputIt2 last2,                std::input_iterator_tag, std::input_iterator_tag)     {         for (; first1 != last1 && first2 != last2; ++first1, ++first2)             if (!(*first1 == *first2))                 return false;           return first1 == last1 && first2 == last2;     } }   template<class InputIt1, class InputIt2> constexpr //< since C++20 bool equal(InputIt1 first1, InputIt1 last1, InputIt2 first2, InputIt2 last2) {     details::equal(first1, last1, first2, last2,                    typename std::iterator_traits<InputIt1>::iterator_category(),                    typename std::iterator_traits<InputIt2>::iterator_category()); } ``` |
| equal (7) |
| ```text namespace detail {     // random-access iterator implementation (allows quick range size detection)     template<class RandomIt1, class RandomIt2, class BinaryPred>     constexpr //< since C++20     bool equal(RandomIt1 first1, RandomIt1 last1,                RandomIt2 first2, RandomIt2 last2, BinaryPred p,                std::random_access_iterator_tag, std::random_access_iterator_tag)     {         if (last1 - first1 != last2 - first2)             return false;           for (; first1 != last1; ++first1, ++first2)             if (!p(*first1, *first2))                 return false;           return true;     }       // input iterator implementation (needs to manually compare with “last2”)     template<class InputIt1, class InputIt2, class BinaryPred>     constexpr //< since C++20     bool equal(InputIt1 first1, InputIt1 last1,                InputIt2 first2, InputIt2 last2, BinaryPred p,                std::input_iterator_tag, std::input_iterator_tag)     {         for (; first1 != last1 && first2 != last2; ++first1, ++first2)             if (!p(*first1, *first2))                 return false;           return first1 == last1 && first2 == last2;     } }   template<class InputIt1, class InputIt2, class BinaryPred> constexpr //< since C++20 bool equal(InputIt1 first1, InputIt1 last1,            InputIt2 first2, InputIt2 last2, BinaryPred p) {     details::equal(first1, last1, first2, last2, p,                    typename std::iterator_traits<InputIt1>::iterator_category(),                    typename std::iterator_traits<InputIt2>::iterator_category()); } ``` |

### Notes

`std::equal` should not be used to compare the ranges formed by the iterators from std::unordered_set, std::unordered_multiset, std::unordered_map, or std::unordered_multimap because the order in which the elements are stored in those containers may be different even if the two containers store the same elements.

When comparing entire containers or string views(since C++17) for equality, operator== for the corresponding type are usually preferred.

Sequential `std::equal` is not guaranteed to be short-circuit. E.g. if the first pair elements of both ranges do not compare equal, the rest of elements may also be compared. Non-short-circuit comparison may happen when the ranges are compared with std::memcmp or implementation-specific vectorized algorithms.

### Example

The following code uses `std::equal` to test if a string is a palindrome.

Run this code

```
#include <algorithm>
#include <iomanip>
#include <iostream>
#include <string_view>
 
constexpr bool is_palindrome(const std::string_view& s)
{
    return std::equal(s.cbegin(), s.cbegin() + s.size() / 2, s.crbegin());
}
 
void test(const std::string_view& s)
{
    std::cout << std::quoted(s)
              << (is_palindrome(s) ? " is" : " is not")
              << " a palindrome\n";
}
 
int main()
{
    test("radar");
    test("hello");
}

```

Output:

```
"radar" is a palindrome
"hello" is not a palindrome

```

### See also

|  |  |
| --- | --- |
| findfind_iffind_if_not(C++11) | finds the first element satisfying specific criteria   (function template) |
| lexicographical_compare | returns true if one range is lexicographically less than another   (function template) |
| mismatch | finds the first position where two ranges differ   (function template) |
| search | searches for the first occurrence of a range of elements   (function template) |
| ranges::equal(C++20) | determines if two sets of elements are the same (algorithm function object) |
| equal_to | function object implementing x == y   (class template) |
| equal_range | returns range of elements matching a specific key   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/equal&oldid=177606>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 November 2024, at 18:45.