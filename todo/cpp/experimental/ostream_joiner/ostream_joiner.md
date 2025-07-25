# std::experimental::ostream_joiner<DelimT,CharT,Traits>::ostream_joiner

From cppreference.com
< cpp‎ | experimental‎ | ostream joiner
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

std::experimental::ostream_joiner

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****ostream_joiner::ostream_joiner**** | | | | |
| ostream_joiner::operator= | | | | |
| ostream_joiner::operator\* | | | | |
| ostream_joiner::operator++ostream_joiner::operator++(int) | | | | |
| Non-member functions | | | | |
| make_ostream_joiner | | | | |

|  |  |  |
| --- | --- | --- |
| ostream_joiner( ostream_type& stream, const DelimT& delimiter ); | (1) | (library fundamentals TS v2) |
| ostream_joiner( ostream_type& stream, DelimT&& delimiter ); | (2) | (library fundamentals TS v2) |
| ostream_joiner( const ostream_joiner& other ) = default; | (3) | (library fundamentals TS v2)  (implicitly declared) |
| ostream_joiner( ostream_joiner&& other ) = default; | (4) | (library fundamentals TS v2)  (implicitly declared) |
|  |  |  |

1) Constructs the iterator with the private ostream_type\* member initialized with std::addressof(stream), the private delimiter member initialized with delimiter, and the private "first element" flag set to true.2) Constructs the iterator with the private ostream_type\* member initialized with std::addressof(stream), the private delimiter member initialized with `std::move(delimiter)`, and the private "first element" flag set to true.3,4) Implicitly declared copy/move constructor that copy/move constructs the private stream pointer, delimiter, and "first element" flag members.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | the output stream to be accessed by this iterator |
| delimiter | - | the delimiter to be inserted into the stream in between two outputs |
| other | - | the `ostream_joiner` object from which this object is to be copy- or move-constructed |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ostream_joiner/ostream_joiner&oldid=157746>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 23:11.