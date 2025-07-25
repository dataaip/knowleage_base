# std::experimental::ranges::is_permutation

From cppreference.com
< cpp‎ | experimental‎ | ranges
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Ranges

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Concepts | | | | |
| General utilities | | | | |
| Iterators | | | | |
| Ranges | | | | |
| Algorithms | | | | |

Algorithms library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Non-modifying sequence operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | all_ofany_ofnone_of | | | | | | countcount_if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | findfind_iffind_if_not | | | | | | find_end | | | | | | find_first_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_find | | | | | | search | | | | | | search_n | | | | | | mismatch | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal | | | | | | for_each | | | | | | lexicographical_compare | | | | | |  | | | | | |  | | | | | |
| Modifying sequence operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | copycopy_if | | | | | | copy_n") | | | | | | copy_backward") | | | | | | move") | | | | | | move_backward") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill") | | | | | | fill_n") | | | | | | generate") | | | | | | generate_n") | | | | | | swap_ranges") | | | | | | shuffle") | | | | | | transform") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if") | | | | | | replacereplace_if") | | | | | | reverse") | | | | | | rotate") | | | | | | unique") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if") | | | | | | replace_copyreplace_copy_if") | | | | | | reverse_copy") | | | | | | rotate_copy") | | | | | | unique_copy") | | | | | |
| Partitioning operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_partitioned") | | | | | | partition_point") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partition") | | | | | | partition_copy") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stable_partition") | | | | | |  | | | | | |
| Sorting operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_sorted") | | | | | | is_sorted_until") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sort | | | | | | stable_sort") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | partial_sort") | | | | | | partial_sort_copy") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nth_element") | | | | | |  | | | | | |
| Binary search operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | lower_bound") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | upper_bound") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binary_search") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_range") | | | | | |
| Set operations (on sorted ranges) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | merge") | | | | | | inplace_merge") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | includes") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_difference") | | | | | | set_intersection") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set_symmetric_difference") | | | | | | set_union") | | | | | |
| Heap operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_heap") | | | | | | is_heap_until") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | make_heap") | | | | | | sort_heap") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | push_heap") | | | | | | pop_heap") | | | | | |
| Minimum/maximum operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | max") | | | | | | max_element") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | min") | | | | | | min_element") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | minmax") | | | | | | minmax_element") | | | | | |
| Permutations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****is_permutation**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | prev_permutation") | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/algorithm>` |  |  |
| template< ForwardIterator I1, Sentinel<I1> S1, ForwardIterator I2, Sentinel<I2> S2,  class Pred = ranges::equal_to<>,             class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires IndirectlyComparable<I1, I2, Pred, Proj1, Proj2>  bool is_permutation( I1 first1, S1 last1, I2 first2, S2 last2, Pred pred = Pred{},                      Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (1) | (ranges TS) |
| template< ForwardRange R1, ForwardRange R2, class Pred = ranges::equal_to<>,  class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires IndirectlyComparable<ranges::iterator_t<R1>, ranges::iterator_t<R2>,                                    Pred, Proj1, Proj2>  bool is_permutation( R1&& r1, R2&& r2, Pred pred = Pred{},                      Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (2) | (ranges TS) |
| template< ForwardIterator I1, Sentinel<I1> S1, class I2,  class Pred = ranges::equal_to<>,             class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires ForwardIterator<std::decay_t<I2>> && !Range<I2> &&               IndirectlyComparable<I1, std::decay_t<I2>, Pred, Proj1, Proj2>  bool is_permutation( I1 first1, S1 last1, I2&& first2_, Pred pred = Pred{},                      Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (3) | (ranges TS)  (deprecated) |
| template< ForwardRange R1, class I2, class Pred = ranges::equal_to<>,  class Proj1 = ranges::identity, class Proj2 = ranges::identity >      requires ForwardIterator<std::decay_t<I2>> && !Range<I2> &&               IndirectlyComparable<ranges::iterator_t<R1>, std::decay_t<I2>, Pred, Proj1, Proj2>  bool is_permutation( R1&& r1, I2&& first2_, Pred pred = Pred{},                      Proj1 proj1 = Proj1{}, Proj2 proj2 = Proj2{} ); | (4) | (ranges TS)  (deprecated) |
|  |  |  |

1) Returns true if there exists a permutation of the elements in range ``first1`,`last1`)` that makes the range equal to `[`first2`,`last2`)`, and false otherwise.2) Same as (1), but uses r1 as the first source range and r2 as the second source range, as if using [ranges::begin(r1) as first1, ranges::end(r1) as last1, ranges::begin(r2) as first2, and ranges::end(r2) as last2.3) Same as (1), except that first2 is defined as if by std::decay_t<I2> first2 = std::forward<I2>(first2_); and last2 is first2 + (last1 - first1).4) Same as (3), but uses r1 as the first source range, as if using ranges::begin(r1) as first1 and ranges::end(r1) as last1.

Two ranges are considered equal if they have the same number of elements and, for every iterator `i` in the range ``first1`,`last1`)`, [ranges::invoke(pred, ranges::invoke(proj1, \*i), ranges::invoke(proj2, \*(first2 + (i - first1)))) is true.

Notwithstanding the declarations depicted above, the actual number and order of template parameters for algorithm declarations is unspecified. Thus, if explicit template arguments are used when calling an algorithm, the program is probably non-portable.

### Parameters

|  |  |  |
| --- | --- | --- |
| first1, last1 | - | the first range of the elements |
| r1 | - | the first range of the elements |
| first2, last2 | - | the second range of the elements |
| r2 | - | the second range of the elements |
| first2_ | - | the beginning of the second range of the elements |
| pred | - | predicate to apply to the projected elements |
| proj1 | - | projection to apply to the elements in the first range |
| proj2 | - | projection to apply to the elements in the second range |

### Return value

true if the range ``first1`,`last1`)` is a permutation of the range `[`first2`,`last2`)`.

### Complexity

At most O(N2) applications of the predicate and each projection, or exactly N if the sequences are already equal, where N = last1 - first1.

However if SizedSentinel<S1, I1> && SizedSentinel<S2, I2> is satisfied and last1 - first1 != last2 - first2, no applications of the predicate and projections are made.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| [is_permutation(C++11) | determines if a sequence is a permutation of another sequence   (function template) |
| next_permutation") | generates the next greater lexicographic permutation of a range of elements   (function template) |
| prev_permutation") | generates the next smaller lexicographic permutation of a range of elements   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/algorithm/is_permutation&oldid=155253>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 July 2023, at 02:40.