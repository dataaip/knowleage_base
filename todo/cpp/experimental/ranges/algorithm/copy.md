# std::experimental::ranges::copy, std::experimental::ranges::copy_if

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****copycopy_if**** | | | | | | copy_n") | | | | | | copy_backward") | | | | | | move") | | | | | | move_backward") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fill") | | | | | | fill_n") | | | | | | generate") | | | | | | generate_n") | | | | | | swap_ranges") | | | | | | shuffle") | | | | | | transform") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | removeremove_if") | | | | | | replacereplace_if") | | | | | | reverse") | | | | | | rotate") | | | | | | unique") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_copyremove_copy_if") | | | | | | replace_copyreplace_copy_if") | | | | | | reverse_copy") | | | | | | rotate_copy") | | | | | | unique_copy") | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_permutation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next_permutation") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | prev_permutation") | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/algorithm>` |  |  |
| template< InputIterator I, Sentinel<I> S, WeaklyIncrementable O >      requires IndirectlyCopyable<I, O>  ranges::tagged_pair<tag::in(I), tag::out(O)>     copy( I first, S last, O result ); | (1) | (ranges TS) |
| template< InputRange R, WeaklyIncrementable O >      requires IndirectlyCopyable<ranges::iterator_t<R>, O>  ranges::tagged_pair<tag::in(ranges::safe_iterator_t<R>), tag::out(O)>     copy( R&& r, O result ); | (2) | (ranges TS) |
| template< InputIterator I, Sentinel<I> S, WeaklyIncrementable O,  class Proj = ranges::identity,            IndirectUnaryPredicate<projected<I, Proj>> Pred >      requires IndirectlyCopyable<I, O>  ranges::tagged_pair<tag::in(I), tag::out(O)>     copy_if( I first, S last, O result, Pred pred, Proj proj = Proj{} ); | (3) | (ranges TS) |
| template< InputRange R, WeaklyIncrementable O,  class Proj = ranges::identity,            IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred >      requires IndirectlyCopyable<iterator_t<R>, O>  ranges::tagged_pair<tag::in(ranges::safe_iterator_t<R>), tag::out(O)>     copy_if( R&& r, O result, Pred pred, Proj proj = Proj{} ); | (4) | (ranges TS) |
|  |  |  |

Copies elements in the source range (``first`,`last`)` or r) into the destination range beginning at result, starting from the first element in the source range and proceeding to the last one.

1) Copies all elements in the range `[`first`,`last`)`. For each non-negative integer `n < (last - first)`, performs \*(result + n) = \*(first + n). The behavior is undefined if result is within the range `[`first`,`last`)`. In this case, [ranges::copy_backward may be used instead.2) Same as (1), but uses r as the source range, as if by ranges::copy(ranges::begin(r), ranges::end(r), result); except that result may not be copied.3) Only copies the elements for which the predicate pred returns true when applied to the element's value as projected by the projection proj. The order of the elements that are copied is preserved. The behavior is undefined if the source and the destination ranges overlap.4) Same as (3), but uses r as the source range, as if by ranges::copy_if(ranges::begin(r), ranges::end(r), result, pred, proj); except that result, pred and proj may not be copied.

Notwithstanding the declarations depicted above, the actual number and order of template parameters for algorithm declarations is unspecified. Thus, if explicit template arguments are used when calling an algorithm, the program is probably non-portable.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to copy |
| r | - | the range of elements to copy |
| result | - | the beginning of the destination range |
| pred | - | predicate to apply to the projected elements |
| proj | - | projection to apply to the elements |

### Return value

A `tagged_pair` object containing the following two members:

- The first member, with the tag `tag::in`, is the past-the-end iterator of the source range (that is, an iterator of type `I` that compares equal to the sentinel last).
- The second member, with the tag `tag::out`, is the past-the-end iterator of the result range.

### Complexity

1) Exactly ranges::distance(first, last) assignments.2) Exactly ranges::distance(r) assignments.3) Exactly ranges::distance(first, last) applications of the corresponding projection and predicate.4) Exactly ranges::distance(r) applications of the corresponding projection and predicate.

### Possible implementations

| First version |
| --- |
| ```text template<InputIterator I, Sentinel<I> S, WeaklyIncrementable O>     requires IndirectlyCopyable<I, O>() ranges::tagged_pair<tag::in(I), tag::out(O)>     copy(I first, S last, O result) {     for (; first != last; ++first, (void)++result)         *result = *first;     return {first, result}; } ``` |
| Second version |
| ```text template<InputRange R, WeaklyIncrementable O>     requires IndirectlyCopyable<ranges::iterator_t<R>, O>() ranges::tagged_pair<tag::in(ranges::safe_iterator_t<R>), tag::out(O)>     copy(R&& r, O result) {    return ranges::copy(ranges::begin(r), ranges::end(r), result); } ``` |
| Third version |
| ```text template<InputIterator I, Sentinel<I> S, WeaklyIncrementable O,          class Proj = ranges::identity,          IndirectUnaryPredicate<projected<I, Proj>> Pred>     requires IndirectlyCopyable<I, O>() ranges::tagged_pair<tag::in(I), tag::out(O)>     copy_if(I first, S last, O result, Pred pred, Proj proj = Proj{}) {     for (; first != last; ++first)         if (ranges::invoke(pred, ranges::invoke(proj, *first)))         {             *result = *first;             ++result;         }     return {first, result}; } ``` |
| Fourth version |
| ```text template<InputRange R, WeaklyIncrementable O,          class Proj = ranges::identity,          IndirectUnaryPredicate<projected<ranges::iterator_t<R>, Proj>> Pred>     requires IndirectlyCopyable<ranges::iterator_t<R>, O>() ranges::tagged_pair<tag::in(ranges::safe_iterator_t<R>), tag::out(O)>     copy_if(R&& r, O result, Pred pred, Proj proj = Proj{}) {     return ranges::copy_if(ranges::begin(r), ranges::end(r), result, pred, proj); } ``` |

### Example

The following code uses copy to both copy the contents of one vector to another and to display the resulting vector:

Run this code

```
#include <experimental/ranges/algorithm>
#include <experimental/ranges/iterator>
#include <iostream>
#include <numeric>
#include <vector>
 
int main()
{
    // see https://en.cppreference.com/w/cpp/language/namespace_alias
    namespace ranges = std::experimental::ranges;
 
    std::vector<int> from_vector(10);
    std::iota(from_vector.begin(), from_vector.end(), 0);
 
    std::vector<int> to_vector;
    ranges::copy_if(from_vector.begin(), from_vector.end(),
                    ranges::back_inserter(to_vector),
                    [](const auto i)
                    {
                       return i % 3;
                    });
// or, alternatively,
//  std::vector<int> to_vector(from_vector.size());
//  std::copy(from_vector, to_vector.begin());
 
    std::cout << "to_vector contains: ";
 
    ranges::copy(to_vector, ranges::ostream_iterator<int>(std::cout, " "));
    std::cout << '\n';
}

```

Output:

```
to_vector contains: 1 2 4 5 7 8

```

### See also

|  |  |
| --- | --- |
| copycopy_if(C++11) | copies a range of elements to a new location   (function template) |
| copy_backward") | copies a range of elements in backwards order   (function template) |
| reverse_copy") | creates a copy of a range that is reversed   (function template) |
| copy_n") | copies a number of elements to a new location   (function template) |
| fill") | assigns a range of elements a certain value   (function template) |
| remove_copyremove_copy_if") | copies a range of elements omitting those that satisfy specific criteria   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/algorithm/copy&oldid=155239>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 July 2023, at 01:13.