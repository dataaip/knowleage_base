# std::experimental::parallel::seq, std::experimental::parallel::par, std::experimental::parallel::par_vec

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
| ****parallel::seqparallel::parparallel::par_vec**** | | | | |
| Parallel algorithms") | | | | |
| Parallel exceptions | | | | |
| parallel::exception_list") | | | | |
| Parallelized version of existing algorithms | | | | |
| New algorithms | | | | |
| parallel::for_eachparallel::for_each_n") | | | | |
| parallel::reduce | | | | |
| parallel::exclusive_scan") | | | | |
| parallel::inclusive_scan") | | | | |
| parallel::transform_reduce | | | | |
| parallel::transform_exclusive_scan") | | | | |
| parallel::transform_inclusive_scan") | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/execution_policy>` |  |  |
| constexpr sequential_execution_policy seq{}; |  | (parallelism TS) |
| constexpr parallel_execution_policy par{}; |  | (parallelism TS) |
| constexpr parallel_vector_execution_policy par_vec{}; |  | (parallelism TS) |
|  |  |  |

`seq`, `par` and `par_vec` are instances of the execution policy types `sequential_execution_policy`, `parallel_execution_policy` and `parallel_vector_execution_policy` respectively. They are used to specify the execution policy of parallel algorithms - i.e., the kinds of parallelism allowed.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/execution_policy_tag&oldid=80070>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 July 2015, at 21:07.