# std::experimental::parallel::transform_reduce

From cppreference.com
< cpp‎ | experimental
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

Extensions for parallelism

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Execution policies") | | | | |
| parallel::execution_policy") | | | | |
| parallel::sequential_execution_policyparallel::parallel_execution_policyparallel::parallel_vector_execution_policy | | | | |
| parallel::seqparallel::parparallel::par_vec | | | | |
| Parallel algorithms") | | | | |
| Parallel exceptions | | | | |
| parallel::exception_list") | | | | |
| Parallelized version of existing algorithms | | | | |
| New algorithms | | | | |
| parallel::for_eachparallel::for_each_n") | | | | |
| parallel::reduce | | | | |
| parallel::exclusive_scan") | | | | |
| parallel::inclusive_scan") | | | | |
| ****parallel::transform_reduce**** | | | | |
| parallel::transform_exclusive_scan") | | | | |
| parallel::transform_inclusive_scan") | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/numeric>` |  |  |
| template< class InputIt, class UnaryOp, class T, class BinaryOp >  T transform_reduce( InputIt first, InputIt last,                     UnaryOp unary_op, T init, BinaryOp binary_op ); | (1) | (parallelism TS) |
| template< class ExecutionPolicy,  class InputIt, class UnaryOp, class T, class BinaryOp >  T transform_reduce( ExecutionPolicy&& policy,                      InputIt first, InputIt last,                     UnaryOp unary_op, T init, BinaryOp binary_op ); | (2) | (parallelism TS) |
|  |  |  |

Applies unary_op to each element in the range ``first`,`last`)` and reduces the results (possibly permuted and aggregated in unspecified manner) along with the initial value init over binary_op.

The behavior is non-deterministic if binary_op is not associative or not commutative.

The behavior is undefined if unary_op or binary_op modifies any element or invalidates any iterator in `[`first`,`last`)`.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to apply the algorithm to |
| init | - | the initial value of the generalized sum |
| policy | - | the [execution policy |
| unary_op | - | unary FunctionObject that will be applied to each element of the input range. The return type must be acceptable as input to binary_op |
| binary_op | - | binary FunctionObject that will be applied in unspecified order to the results of unary_op, the results of other binary_op and init |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

Generalized sum of init and unary_op(\*first), unary_op(\*(first + 1)), ... unary_op(\*(last - 1)) over binary_op,
where generalized sum GSUM(op, a1, ..., aN) is defined as follows:

- if N = 1, a1,
- if N > 1, op(GSUM(op, b1, ..., bK), GSUM(op, bM, ..., bN)) where

:   - b1, ..., bN may be any permutation of a1, ..., aN and
    - 1 < K + 1 = M ≤ N

in other words, the results of unary_op may be grouped and arranged in arbitrary order.

### Complexity

O(last - first) applications each of unary_op and binary_op.

### Exceptions

- If execution of a function invoked as part of the algorithm throws an exception,

:   - if `policy` is `parallel_vector_execution_policy`, std::terminate is called.
    - if `policy` is `sequential_execution_policy` or `parallel_execution_policy`, the algorithm exits with an exception_list") containing all uncaught exceptions. If there was only one uncaught exception, the algorithm may rethrow it without wrapping in `exception_list`. It is unspecified how much work the algorithm will perform before returning after the first exception was encountered.
    - if `policy` is some other type, the behavior is implementation-defined.

- If the algorithm fails to allocate memory (either for itself or to construct an `exception_list` when handling a user exception), std::bad_alloc is thrown.

### Notes

unary_op is not applied to init.

If the range is empty, init is returned, unmodified.

- If `policy` is an instance of `sequential_execution_policy`, all operations are performed in the calling thread.
- If `policy` is an instance of `parallel_execution_policy`, operations may be performed in unspecified number of threads, indeterminately sequenced with each other.
- If `policy` is an instance of `parallel_vector_execution_policy`, execution may be both parallelized and vectorized: function body boundaries are not respected and user code may be overlapped and combined in arbitrary manner (in particular, this implies that a user-provided Callable must not acquire a mutex to access a shared resource).

### Example

transform_reduce can be used to parallelize std::inner_product:

Run this code

```
#include <boost/iterator/zip_iterator.hpp>
#include <boost/tuple.hpp>
#include <experimental/execution_policy>
#include <experimental/numeric>
#include <functional>
#include <iostream>
#include <iterator>
#include <vector>
 
int main()
{
    std::vector<double> xvalues(10007, 1.0), yvalues(10007, 1.0);
 
    double result = std::experimental::parallel::transform_reduce(
        std::experimental::parallel::par,
        boost::iterators::make_zip_iterator(
            boost::make_tuple(std::begin(xvalues), std::begin(yvalues))),
        boost::iterators::make_zip_iterator(
            boost::make_tuple(std::end(xvalues), std::end(yvalues))),
        [](auto r) { return boost::get<0>(r) * boost::get<1>(r); }
        0.0,
        std::plus<>()
    );
    std::cout << result << '\n';
}

```

Output:

```
10007

```

### See also

|  |  |
| --- | --- |
| accumulate | sums up or folds a range of elements   (function template) |
| transform | applies a function to a range of elements, storing results in a destination range   (function template) |
| reduce(parallelism TS) | similar to std::accumulate, except out of order   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/transform_reduce&oldid=156341>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 August 2023, at 05:21.