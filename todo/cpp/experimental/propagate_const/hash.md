# std::hash(std::experimental::propagate_const)

From cppreference.com
< cpp‎ | experimental‎ | propagate const
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

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::propagate_const | | | | |
| experimental::not_fn | | | | |
| experimental::observer_ptr | | | | |
| experimental::make_array | | | | |
| experimental::to_array | | | | |
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

std::experimental::propagate_const

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| propagate_const::propagate_const | | | | |
| propagate_const::operator= | | | | |
| propagate_const::swap | | | | |
| Observers | | | | |
| propagate_const::get | | | | |
| propagate_const::operator bool | | | | |
| propagate_const::operator\*propagate_const::operator-> | | | | |
| propagate_const::operator element_type\*propagate_const::operator const element_type\* | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator>operator<=operator>operator>= | | | | |
| swap | | | | |
| get_underlying | | | | |
| Helper classes | | | | |
| ****std::hash**** | | | | |
| std::equal_tostd::not_equal_tostd::lessstd::greaterstd::less_equalstd::greater_equal | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/propagate_const>` |  |  |
| template< class T > struct hash<std::experimental::propagate_const<T>>; |  | (library fundamentals TS v2) |
|  |  |  |

The template specialization of std::hash for std::experimental::propagate_const<T> allows users to obtain hashes of objects of type std::experimental::propagate_const<T>.

For a given std::experimental::propagate_const<T> p, this specialization ensures that std::hash<std::experimental::propagate_const<T>>()(p) == std::hash<T>()(p.t_), where p.t_ is the pointer-like object wrapped by `p`.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| hash(C++11) | hash function object   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/propagate_const/hash&oldid=155162>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 July 2023, at 01:04.