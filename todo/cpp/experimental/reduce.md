# std::experimental::parallel::reduce

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
| ****parallel::reduce**** | | | | |
| parallel::exclusive_scan") | | | | |
| parallel::inclusive_scan") | | | | |
| parallel::transform_reduce | | | | |
| parallel::transform_exclusive_scan") | | | | |
| parallel::transform_inclusive_scan") | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/numeric>` |  |  |
| template< class InputIt >  typename std::iterator_traits<InputIt>::value_type reduce(     InputIt first, InputIt last ); | (1) | (parallelism TS) |
| template< class ExecutionPolicy, class InputIterator >  typename std::iterator_traits<InputIt>::value_type reduce(     ExecutionPolicy&& policy, InputIt first, InputIt last ); | (2) | (parallelism TS) |
| template< class InputIt, class T >  T reduce( InputIt first, InputIt last, T init ); | (3) | (parallelism TS) |
| template< class ExecutionPolicy, class InputIt, class T >  T reduce( ExecutionPolicy&& policy, InputIt first, InputIt last, T init ); | (4) | (parallelism TS) |
| template< class InputIt, class T, class BinaryOp >  T reduce( InputIt first, InputIt last, T init, BinaryOp binary_op ); | (5) | (parallelism TS) |
| template< class ExecutionPolicy, class InputIt, class T, class BinaryOp >  T reduce( ExecutionPolicy&& policy,           InputIt first, InputIt last, T init, BinaryOp binary_op ); | (6) | (parallelism TS) |
|  |  |  |

1) Same as reduce(first, last, typename std::iterator_traits<InputIt>::value_type{}).3) Same as reduce(first, last, init, std::plus<>()).5) Reduces the range ``first`,`last`)`, possibly permuted and aggregated in unspecified manner, along with the initial value init over binary_op.2,4,6) Same as (1,3,5), but executed according to policy.

The behavior is non-deterministic if binary_op is not associative or not commutative.

The behavior is undefined if binary_op modifies any element or invalidates any iterator in `[`first`,`last`)`.

### Parameters

|  |  |  |
| --- | --- | --- |
| first, last | - | the range of elements to apply the algorithm to |
| init | - | the initial value of the generalized sum |
| policy | - | the [execution policy |
| binary_op | - | binary FunctionObject that will be applied in unspecified order to the result of dereferencing the input iterators, the results of other binary_op and init |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

Generalized sum of init and \*first, \*(first + 1), ... \*(last - 1) over binary_op,

where generalized sum GSUM(op, a1, ..., aN) is defined as follows:

- if N=1, a1
- if N > 1, op(GSUM(op, b1, ..., bK), GSUM(op, bM, ..., bN)) where

:   - b1, ..., bN may be any permutation of a1, ..., aN and
    - 1 < K+1 = M ≤ N

in other words, the elements of the range may be grouped and rearranged in arbitrary order.

### Complexity

O(last - first) applications of binary_op.

### Exceptions

- If execution of a function invoked as part of the algorithm throws an exception,

:   - if `policy` is `parallel_vector_execution_policy`, std::terminate is called.
    - if `policy` is `sequential_execution_policy` or `parallel_execution_policy`, the algorithm exits with an exception_list") containing all uncaught exceptions. If there was only one uncaught exception, the algorithm may rethrow it without wrapping in `exception_list`. It is unspecified how much work the algorithm will perform before returning after the first exception was encountered.
    - if `policy` is some other type, the behavior is implementation-defined.

- If the algorithm fails to allocate memory (either for itself or to construct an `exception_list` when handling a user exception), std::bad_alloc is thrown.

### Notes

If the range is empty, init is returned, unmodified.

- If `policy` is an instance of `sequential_execution_policy`, all operations are performed in the calling thread.
- If `policy` is an instance of `parallel_execution_policy`, operations may be performed in unspecified number of threads, indeterminately sequenced with each other.
- If `policy` is an instance of `parallel_vector_execution_policy`, execution may be both parallelized and vectorized: function body boundaries are not respected and user code may be overlapped and combined in arbitrary manner (in particular, this implies that a user-provided Callable must not acquire a mutex to access a shared resource).

### Example

reduce is the out-of-order version of std::accumulate:

Run this code

```
#include <chrono>
#include <experimental/execution_policy>
#include <experimental/numeric>
#include <iostream>
#include <numeric>
#include <vector>
 
int main()
{
    std::vector<double> v(10'000'007, 0.5);
 
    {
        auto t1 = std::chrono::high_resolution_clock::now();
        double result = std::accumulate(v.begin(), v.end(), 0.0);
        auto t2 = std::chrono::high_resolution_clock::now();
        std::chrono::duration<double, std::milli> ms = t2 - t1;
        std::cout << std::fixed << "std::accumulate result " << result
                  << " took " << ms.count() << " ms\n";
    }
 
    {
        auto t1 = std::chrono::high_resolution_clock::now();
        double result = std::experimental::parallel::reduce(
                            std::experimental::parallel::par,
                            v.begin(), v.end());
        auto t2 = std::chrono::high_resolution_clock::now();
        std::chrono::duration<double, std::milli> ms = t2 - t1;
        std::cout << "parallel::reduce result "
                  << result << " took " << ms.count() << " ms\n";
    }
}

```

Possible output:

```
std::accumulate result 5000003.50000 took 12.7365 ms
parallel::reduce result 5000003.50000 took 5.06423 ms

```

### See also

|  |  |
| --- | --- |
| accumulate | sums up or folds a range of elements   (function template) |
| transform | applies a function to a range of elements, storing results in a destination range   (function template) |
| transform_reduce(parallelism TS) | applies a functor, then reduces out of order   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/reduce&oldid=155635>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 July 2023, at 00:07.