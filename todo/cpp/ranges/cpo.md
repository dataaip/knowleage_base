# Customization point object (since C++20)

From cppreference.com
< cpp‎ | standard library
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

Standard library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****Customization point object**** (C++20) | | | | |
| Exposition-only entities | | | | |
| **decay-copy**(C++11) | | | | |
| **synth-three-way****synth-three-way-result**(C++20)(C++20) | | | | |

### Explanation

The name `cpo` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__cpo_fn`.

All instances of `__cpo_fn` are equal. The effects of invoking different instances of type `__cpo_fn` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `cpo` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `cpo` above, `__cpo_fn` models

- std::invocable<__cpo_fn, Args...>,
- std::invocable<const __cpo_fn, Args...>,
- std::invocable<__cpo_fn&, Args...>, and
- std::invocable<const __cpo_fn&, Args...>.

Otherwise, no function call operator of `__cpo_fn` participates in overload resolution.

### See also

- RangeAdaptorObject (RAO)
- RangeAdaptorClosureObject (RACO)
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/standard_library/cpo&oldid=174139>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 August 2024, at 08:05.