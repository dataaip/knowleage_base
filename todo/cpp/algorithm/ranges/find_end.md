# std::ranges::find_end

From cppreference.com
< cpp‎ | algorithm‎ | ranges
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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | inner_product | | | | | | adjacent_difference | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | accumulate | | | | | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sum | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |  | | | | | | |
| Operations on uninitialized memory | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n(C++11) | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_fill_n | | | | | |  | | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | destroy(C++17) | | | | | | destroy_n(C++17) | | | | | | destroy_at(C++17) | | | | | | construct_at(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | |

Constrained algorithmsAll names in this menu belong to namespace `std::ranges`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Non-modifying sequence operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of | | | | | | for_each | | | | | | for_each_n | | | | | | countcount_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_find | | | | | | mismatch | | | | | | equal | | | | | | lexicographical_compare | | | | | | containscontains_subrange(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not | | | | | | find_lastfind_last_iffind_last_if_not(C++23)(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****find_end**** | | | | | | find_first_of | | | | | | search | | | | | | search_n | | | | | | starts_with(C++23) | | | | | | ends_with(C++23) | | | | | |  | | | | | | |
| Modifying sequence operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if | | | | | | copy_n | | | | | | copy_backward | | | | | | move | | | | | | move_backward | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | shift_leftshift_right(C++23)(C++23) | | | | | | fill | | | | | | fill_n | | | | | | generate | | | | | | generate_n | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | transform | | | | | | swap_ranges | | | | | | shuffle | | | | | | sample | | | | | | removeremove_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | replacereplace_if | | | | | | reverse | | | | | | rotate | | | | | | remove_copyremove_copy_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | unique | | | | | | replace_copyreplace_copy_if | | | | | | reverse_copy | | | | | | rotate_copy | | | | | | unique_copy | | | | | | |
| Partitioning operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition_point | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition_copy | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stable_partition | | | | | | |
| Sorting operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted | | | | | | is_sorted_until | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sort | | | | | | nth_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sort_copy | | | | | |  | | | | | | |
| Binary search operations (on sorted ranges) | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binary_search | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range | | | | | | |
| Set operations (on sorted ranges) | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge | | | | | | inplace_merge | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference | | | | | | set_intersection | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_union | | | | | | includes | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_symmetric_difference | | | | | |  | | | | | | |
| Heap operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_heap | | | | | | is_heap_until | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make_heap | | | | | | sort_heap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap | | | | | | pop_heap | | | | | | |
| Minimum/maximum operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | max | | | | | | max_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | min | | | | | | min_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | minmax | | | | | | minmax_element | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clamp | | | | | |  | | | | | | |
| Permutation operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | prev_permutation | | | | | | |
| Fold operations | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fold_left(C++23) | | | | | | fold_left_first(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fold_right(C++23) | | | | | | fold_right_last(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fold_left_with_iter(C++23) | | | | | | fold_left_first_with_iter(C++23) | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Numeric operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++23) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random number generation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | generate_random(C++26) | | | | | | | |
| Operations on uninitialized storage | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | construct_at | | | | | | destroy | | | | | | destroy_n | | | | | | destroy_at | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy | | | | | | uninitialized_move | | | | | | uninitialized_fill | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_copy_n | | | | | | uninitialized_move_n | | | | | | uninitialized_fill_n | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uninitialized_default_construct | | | | | | uninitialized_default_construct_n | | | | | | uninitialized_value_construct | | | | | | uninitialized_value_construct_n | | | | | | |
| Return types | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | in_fun_result | | | | | | in_in_result | | | | | | in_found_result | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | in_out_result | | | | | | in_in_out_result | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | in_out_out_result | | | | | | min_max_result | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | out_value_result(C++23) | | | | | | in_value_result(C++23) | | | | | |  | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<algorithm>` |  |  |
| Call signature |  |  |
| template< std::forward_iterator I1, std::sentinel_for<I1> S1,  std::forward_iterator I2, std::sentinel_for<I2> S2,            class Pred = ranges::equal_to,            class Proj1 = std::identity,            class Proj2 = std::identity >  requires std::indirectly_comparable<I1, I2, Pred, Proj1, Proj2>  constexpr ranges::subrange<I1>      find_end( I1 first1, S1 last1, I2 first2, S2 last2,               Pred pred = {}, Proj1 proj1 = {}, Proj2 proj2 = {} ); | (1) | (since C++20) |
| template< ranges::forward_range R1, ranges::forward_range R2,  class Pred = ranges::equal_to,            class Proj1 = std::identity,            class Proj2 = std::identity >  requires std::indirectly_comparable<ranges::iterator_t<R1>,                                      ranges::iterator_t<R2>,                                      Pred, Proj1, Proj2>  constexpr ranges::borrowed_subrange_t<R1>      find_end( R1&& r1, R2&& r2, Pred pred = {},               Proj1 proj1 = {}, Proj2 proj2 = {} ); | (2) | (since C++20) |
|  |  |  |

1) Searches for the **last** occurrence of the sequence ``first2`,`last2`)` in the range `[`first1`,`last1`)`, after projection with proj1 and proj2 respectively. The projected elements are compared using the binary predicate pred.2) Same as (1), but uses r1 as the first source range and r2 as the second source range, as if using [ranges::begin(r1) as first1, ranges::end(r1) as last1, ranges::begin(r2) as first2, and ranges::end(r2) as last2.

The function-like entities described on this page are **algorithm function objects** (informally known as **niebloids**), that is:

- Explicit template argument lists cannot be specified when calling any of them.
- None of them are visible to argument-dependent lookup.
- When any of them are found by normal unqualified lookup as the name to the left of the function-call operator, argument-dependent lookup is inhibited.

### Parameters

|  |  |  |
| --- | --- | --- |
| first1, last1 | - | the range of elements to examine (aka **haystack**) |
| first2, last2 | - | the range of elements to search for (aka **needle**) |
| r1 | - | the range of elements to examine (aka **haystack**) |
| r2 | - | the range of elements to search for (aka **needle**) |
| pred | - | binary predicate to compare the elements |
| proj1 | - | projection to apply to the elements in the first range |
| proj2 | - | projection to apply to the elements in the second range |

### Return value

1) ranges::subrange<I1>{} value initialized with expression {i, i + (i == last1 ? 0 : ranges::distance(first2, last2))} that denotes the last occurrence of the sequence ``first2`,`last2`)` in range `[`first1`,`last1`)` (after projections with proj1 and proj2). If `[`first2`,`last2`)` is empty or if no such sequence is found, the return value is effectively initialized with {last1, last1}.2) Same as (1), except that the return type is [ranges::borrowed_subrange_t<R1>.

### Complexity

At most \(\scriptsize S\cdot(N-S+1)\)S·(N-S+1) applications of the corresponding predicate and each projection, where \(\scriptsize S\)S is ranges::distance(first2, last2) and \(\scriptsize N\)N is ranges::distance(first1, last1) for (1), or \(\scriptsize S\)S is ranges::distance(r2) and \(\scriptsize N\)N is ranges::distance(r1) for (2).

### Notes

An implementation can improve efficiency of the search if the input iterators model std::bidirectional_iterator by searching from the end towards the begin. Modelling the std::random_access_iterator may improve the comparison speed. All this however does not change the theoretical complexity of the worst case.

### Possible implementation

|  |
| --- |
| ```text struct find_end_fn {     template<std::forward_iterator I1, std::sentinel_for<I1> S1,              std::forward_iterator I2, std::sentinel_for<I2> S2,              class Pred = ranges::equal_to,              class Proj1 = std::identity, class Proj2 = std::identity>     requires std::indirectly_comparable<I1, I2, Pred, Proj1, Proj2>     constexpr ranges::subrange<I1>         operator()(I1 first1, S1 last1,                    I2 first2, S2 last2, Pred pred = {},                    Proj1 proj1 = {}, Proj2 proj2 = {}) const     {         if (first2 == last2)         {             auto last_it = ranges::next(first1, last1);             return {last_it, last_it};         }         auto result = ranges::search(             std::move(first1), last1, first2, last2, pred, proj1, proj2);           if (result.empty())             return result;           for (;;)         {             auto new_result = ranges::search(                 std::next(result.begin()), last1, first2, last2, pred, proj1, proj2);             if (new_result.empty())                 return result;             else                 result = std::move(new_result);         }     }       template<ranges::forward_range R1, ranges::forward_range R2,              class Pred = ranges::equal_to,              class Proj1 = std::identity,              class Proj2 = std::identity>     requires std::indirectly_comparable<ranges::iterator_t<R1>,                                         ranges::iterator_t<R2>,                                         Pred, Proj1, Proj2>     constexpr ranges::borrowed_subrange_t<R1>         operator()(R1&& r1, R2&& r2, Pred pred = {},                    Proj1 proj1 = {}, Proj2 proj2 = {}) const     {         return (*this)(ranges::begin(r1), ranges::end(r1),                        ranges::begin(r2), ranges::end(r2),                        std::move(pred),                        std::move(proj1), std::move(proj2));     } };   inline constexpr find_end_fn find_end {}; ``` |

### Example

Run this code

```
#include <algorithm>
#include <array>
#include <cctype>
#include <iostream>
#include <ranges>
#include <string_view>
 
void print(const auto haystack, const auto needle)
{
    const auto pos = std::distance(haystack.begin(), needle.begin());
    std::cout << "In \"";
    for (const auto c : haystack)
        std::cout << c;
    std::cout << "\" found \"";
    for (const auto c : needle)
        std::cout << c;
    std::cout << "\" at position " << pos << ".." << pos + needle.size() << ")\n"
        << std::string(4 + pos, ' ') << std::string(needle.size(), '^') << '\n';
}
 
int main()
{
    using namespace std::literals;
    constexpr auto secret{"password password word..."sv};
    constexpr auto wanted{"password"sv};
 
    constexpr auto found1 = std::ranges::find_end(
        secret.cbegin(), secret.cend(), wanted.cbegin(), wanted.cend());
    print(secret, found1);
 
    constexpr auto found2 = std::ranges::find_end(secret, "word"sv);
    print(secret, found2);
 
    const auto found3 = std::ranges::find_end(secret, "ORD"sv,
        [ { // uses a binary predicate
            return std::tolower(x) == std::tolower(y);
        });
    print(secret, found3);
 
    const auto found4 = std::ranges::find_end(secret, "SWORD"sv, {}, {},
        [](char c) { return std::tolower(c); }); // projects the 2nd range
    print(secret, found4);
 
    static_assert(std::ranges::find_end(secret, "PASS"sv).empty()); // => not found
}

```

Output:

```
In "password password word..." found "password" at position 9..17)
             ^^^^^^^^
In "password password word..." found "word" at position [18..22)
                      ^^^^
In "password password word..." found "ord" at position [19..22)
                       ^^^
In "password password word..." found "sword" at position [12..17)
                ^^^^^

```

### See also

|  |  |
| --- | --- |
| [ranges::find_lastranges::find_last_ifranges::find_last_if_not(C++23)(C++23)(C++23) | finds the last element satisfying specific criteria (algorithm function object) |
| ranges::findranges::find_ifranges::find_if_not(C++20)(C++20)(C++20) | finds the first element satisfying specific criteria (algorithm function object) |
| ranges::find_first_of(C++20) | searches for any one of a set of elements (algorithm function object) |
| ranges::adjacent_find(C++20) | finds the first two adjacent items that are equal (or satisfy a given predicate) (algorithm function object) |
| ranges::search(C++20) | searches for the first occurrence of a range of elements (algorithm function object) |
| ranges::search_n(C++20) | searches for the first occurrence of a number consecutive copies of an element in a range (algorithm function object) |
| find_end | finds the last sequence of elements in a certain range   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/algorithm/ranges/find_end&oldid=159507>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 September 2023, at 06:21.