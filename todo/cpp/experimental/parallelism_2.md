# Extensions for parallelism, version 2

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
| ****Extensions for parallelism 2**** (parallelism TS v2) | | | | |
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

****Extensions for parallelism v2****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Parallel exceptions | | | | |
| exception_list") | | | | |
| Additional execution policies | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::vector_policy") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | execution::unsequenced_policy") | | | | | |
| Algorithms | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | induction") | | | | | | reductionreduction_plusreduction_minusreduction_multiplies") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduction_bit_andreduction_bit_orreduction_bit_xorreduction_minreduction_max") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | for_loopfor_loop_stridedfor_loop_nfor_loop_n_strided") | | | | | |  | | | | | |  | | | | | |
| execution::no_vec") | | | | |
| execution::ordered_update_t") | | | | |
| Task blocks | | | | |
| task_block") | | | | |
| task_cancelled_exception") | | | | |
| define_task_blockdefine_task_block_restore_thread") | | | | |
| Data-parallel vectors | | | | |

The C++ Extensions for Parallelism Version 2, ISO/IEC TS 19570:2018 defines the following new components for the C++ standard library:

### Parallel exceptions

|  |  |
| --- | --- |
| Defined in header `<experimental/exception_list>` | |
| exception_list") | exceptions raised during parallel executions   (class) |

### Execution policies

|  |  |
| --- | --- |
| Defined in header `<experimental/execution_policy>` | |
| unsequenced_policyvector_policy") | execution policy types   (class) |
| unseqvec") | global execution policy objects   (constant) |

### Parallel algorithms

|  |  |
| --- | --- |
|  | This section is incomplete |

### Task Block

|  |  |
| --- | --- |
|  | This section is incomplete |

### Data-Parallel Types

|  |  |
| --- | --- |
| simd(parallelism TS v2) | data-parallel vector type   (class template) |
| simd_mask(parallelism TS v2) | data-parallel type with the element type bool   (class template) |

### Feature test macros

|  |  |
| --- | --- |
| Defined in header `<experimental/task_block>` | |
| __cpp_lib_experimental_parallel_task_block | a value of at least 201711 indicates that the task block functionality is supported   (macro constant) |
| Defined in header `<experimental/execution>` | |
| __cpp_lib_experimental_execution_vector_policy | a value of at least 201711 indicates that the vector and wavefront policies are supported   (macro constant) |
| Defined in header `<experimental/algorithm>` | |
| __cpp_lib_experimental_parallel_for_loop | a value of at least 201711 indicates that the `for_loop` class of algorithms is supported   (macro constant) |
| Defined in header `<experimental/simd>` | |
| __cpp_lib_experimental_parallel_simd | a value of at least 201803 indicates that the data-parallel types library is supported   (macro constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/parallelism_2&oldid=111580>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 July 2019, at 23:20.