# std::shift_left, std::shift_right

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-modifying sequence operations | | | | | | Batch operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_each_n(C++17) | | | | | | | Search operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of(C++11)                (C++11)(C++11) | | | | | | countcount_if | | | | | | mismatch | | | | | | equal | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not(C++11) | | | | | | find_end | | | | | | find_first_of | | | | | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | | Modifying sequence operations | | | | | | Copy operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if(C++11) | | | | | | copy_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copy_n(C++11) | | | | | | move(C++11) | | | | | | move_backward(C++11) | | | | | | | Swap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | iter_swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap_ranges | | | | | |  | | | | | | | Transformation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | transform | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replace_copyreplace_copy_if | | | | | |  | | | | | | | Generation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill | | | | | | fill_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate | | | | | | generate_n | | | | | | | Removing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if | | | | | | unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if | | | | | | unique_copy | | | | | | | Order-changing operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse | | | | | | reverse_copy | | | | | | rotate | | | | | | rotate_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | random_shuffleshuffle(until C++17)(C++11) | | | | | | ****shift_leftshift_right****(C++20)(C++20) | | | | | | | Sampling operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sample(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Sorting and related operations | | | | | | Partitioning operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | partition_copy(C++11) | | | | | | stable_partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned(C++11) | | | | | | partition_point(C++11) | | | | | |  | | | | | | | Sorting operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | partial_sort | | | | | | partial_sort_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted(C++11) | | | | | | is_sorted_until(C++11) | | | | | | nth_element | | | | | |  | | | | | | | Binary search operations (on partitioned ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | binary_search | | | | | | | Set operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes | | | | | | set_union | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_symmetric_difference | | | | | |  | | | | | | | Merge operations (on sorted ranges) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_merge | | | | | | | Heap operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | make_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort_heap | | | | | | is_heap(C++11) | | | | | | is_heap_until(C++11) | | | | | | | Minimum/maximum operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | min | | | | | | minmax(C++11) | | | | | | clamp(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max_element | | | | | | min_element | | | | | | minmax_element(C++11) | | | | | |  | | | | | | | Lexicographical comparison operations | | | | | | lexicographical_compare | | | | | | lexicographical_compare_three_way(C++20) | | | | | | Permutation operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | prev_permutation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation(C++11) | | | | | |  | | | | | |  | | | | | | | C library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | qsort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bsearch | | | | | | |
| Numeric operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| template< class ForwardIt >  constexpr ForwardIt shift_left( ForwardIt first, ForwardIt last,                                  typename std::iterator_traits<ForwardIt>:: difference_type n ); | (1) | (since C++20) |
| template< class ExecutionPolicy, class ForwardIt >  ForwardIt shift_left( ExecutionPolicy&& policy,                        ForwardIt first, ForwardIt last,                        typename std::iterator_traits<ForwardIt>:: difference_type n ); | (2) | (since C++20) |
| template< class ForwardIt >  constexpr ForwardIt shift_right( ForwardIt first, ForwardIt last,                                   typename std::iterator_traits<ForwardIt>:: difference_type n ); | (3) | (since C++20) |
| template< class ExecutionPolicy, class ForwardIt >  ForwardIt shift_right( ExecutionPolicy&& policy,                         ForwardIt first, ForwardIt last,                         typename std::iterator_traits<ForwardIt>:: difference_type n ); | (4) | (since C++20) |
|  |  |  |

Shifts the elements in the range ``first`,`last`)` by n positions.

1) Shifts the elements towards the beginning of the range.

- If n == 0 || n >= last - first, there are no effects.
- Otherwise, for every integer i in `[`​0​`,`last - first - n`)`, moves the element originally at position first + n + i to position first + i.
 The moves are performed in increasing order of `i` starting from ​0​.3) Shifts the elements towards the end of the range.

- If n == 0 || n >= last - first, there are no effects.
- Otherwise, for every integer i in `[`​0​`,`last - first - n`)`, moves the element originally at position first + i to position first + n + i.
 If `ForwardIt` meets the [LegacyBidirectionalIterator requirements, then the moves are performed in decreasing order of i starting from last - first - n - 1.2,4) Same as (1) and (3), respectively, but executed according to policy and the moves may be performed in any order. These overloads participate in overload resolution only if std::is_execution_policy_v<std::remove_cvref_t<ExecutionPolicy>> is true.

Elements that are in the original range but not the new range are left in a valid but unspecified state.

If any of the following conditions is satisfied, the behavior is undefined:

- n >= 0 is not true.
- The type of \*first is not MoveAssignable.
- For `shift_right`, `ForwardIt` is neither LegacyBidirectionalIterator nor ValueSwappable.

### Parameters

|  |  |  |
| --- | --- | --- |
| first | - | the beginning of the original range |
| last | - | the end of the original range |
| n | - | the number of positions to shift |
| policy | - | the execution policy to use |
| Type requirements | | |
| -`ForwardIt` must meet the requirements of LegacyForwardIterator. | | |

### Return value

1,2) The end of the resulting range.

- If n is less than std::distance(first, last), returns an iterator equal to std::next(first, (std::distance(first, last) - n)).
- Otherwise, returns first.
3,4) The beginning of the resulting range.

- If n is less than std::distance(first, last), returns an iterator equal to std::next(first, n).
- Otherwise, returns last.

### Complexity

1,2) At most std::distance(first, last) - n assignments.3,4) At most std::distance(first, last) - n assignment or swaps.

### Exceptions

The overloads with a template parameter named `ExecutionPolicy` report errors as follows:

- If execution of a function invoked as part of the algorithm throws an exception and `ExecutionPolicy` is one of the standard policies, std::terminate is called. For any other `ExecutionPolicy`, the behavior is implementation-defined.
- If the algorithm fails to allocate memory, std::bad_alloc is thrown.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_shift` | `201806L` | (C++20) | `std::shift_left` and `std::shift_right` |

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <string>
#include <type_traits>
#include <vector>
 
struct S
{
    int value{0};
    bool specified_state{true};
 
    S(int v = 0) : value{v} {}
    S(S const& rhs) = default;
    S(S&& rhs) { *this = std::move(rhs); }
    S& operator=(S const& rhs) = default;
    S& operator=(S&& rhs)
    {
        if (this != &rhs)
        {
            value = rhs.value;
            specified_state = rhs.specified_state;
            rhs.specified_state = false;
        }
        return *this;
    }
};
 
template<typename T>
std::ostream& operator<<(std::ostream& os, std::vector<T> const& v)
{
    for (const auto& s : v)
    {
        if constexpr (std::is_same_v<T, S>)
            s.specified_state ? os << s.value << ' ' : os << ". ";
        else if constexpr (std::is_same_v<T, std::string>)
            os << (s.empty() ? "." : s) << ' ';
        else
            os << s << ' ';
    }
    return os;
}
 
int main()
{
    std::cout << std::left;
 
    std::vector<S>           a{1, 2, 3, 4, 5, 6, 7};
    std::vector<int>         b{1, 2, 3, 4, 5, 6, 7};
    std::vector<std::string> c{"α", "β", "γ", "δ", "ε", "ζ", "η"};
 
    std::cout << "vector<S> \tvector<int> \tvector<string>\n";
    std::cout << a << "  " << b << "  " << c << '\n';
 
    std::shift_left(begin(a), end(a), 3);
    std::shift_left(begin(b), end(b), 3);
    std::shift_left(begin(c), end(c), 3);
    std::cout << a << "  " << b << "  " << c << '\n';
 
    std::shift_right(begin(a), end(a), 2);
    std::shift_right(begin(b), end(b), 2);
    std::shift_right(begin(c), end(c), 2);
    std::cout << a << "  " << b << "  " << c << '\n';
 
    std::shift_left(begin(a), end(a), 8); // has no effect: n >= last - first
    std::shift_left(begin(b), end(b), 8); // ditto
    std::shift_left(begin(c), end(c), 8); // ditto
    std::cout << a << "  " << b << "  " << c << '\n';
 
//  std::shift_left(begin(a), end(a), -3); // UB, e.g. segfault
}

```

Possible output:

```
vector<S>       vector<int>     vector<string>
1 2 3 4 5 6 7   1 2 3 4 5 6 7   α β γ δ ε ζ η
4 5 6 7 . . .   4 5 6 7 5 6 7   δ ε ζ η . . .
. . 4 5 6 7 .   4 5 4 5 6 7 5   . . δ ε ζ η .
. . 4 5 6 7 .   4 5 4 5 6 7 5   . . δ ε ζ η .

```

### See also

|  |  |
| --- | --- |
| move(C++11) | moves a range of elements to a new location   (function template) |
| move_backward(C++11) | moves a range of elements to a new location in backwards order   (function template) |
| rotate | rotates the order of elements in a range   (function template) |
| ranges::shift_leftranges::shift_right(C++23) | shifts elements in a range (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/shift&oldid=170518>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 March 2024, at 22:53.