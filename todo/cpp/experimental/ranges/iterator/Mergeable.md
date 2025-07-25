# std::experimental::ranges::Mergeable

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

Iterators library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Readable | | | | | | Writable | | | | | | WeaklyIncrementable | | | | | | Incrementable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator | | | | | | Sentinel | | | | | | SizedSentinel | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | InputIterator | | | | | | ForwardIterator | | | | | | BidirectionalIterator | | | | | | RandomAccessIterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | OutputIterator | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Indirect callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectUnaryInvocableIndirectRegularUnaryInvocable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectUnaryPredicate | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectRelation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectStrictWeakOrder | | | | | |  | | | | | |
| Common algorithm requirements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectlyMovable | | | | | | IndirectlyMovableStorable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectlyCopyable | | | | | | IndirectlyCopyableStorable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | IndirectlySwappable | | | | | | IndirectlyComparable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Permutable | | | | | | ****Mergeable**** | | | | | | Sortable | | | | | |
| Concept utilities | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_result_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected | | | | | |
| Iterator utilities and operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_move") | | | | | | iter_swap") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | next | | | | | | prev | | | | | |
| Iterator traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | difference_type | | | | | | value_type | | | | | | reference_trvalue_reference_titer_common_reference_t | | | | | | iterator_category | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tag | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::iterator_traits") | | | | | | std::iterator_traits<InputIterator>std::iterator_traits<OutputIterator>") | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Iterator adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator") | | | | | | move_iterator") | | | | | | move_sentinel") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | back_insert_iterator") | | | | | | front_insert_iterator") | | | | | | insert_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator") | | | | | | counted_iterator") | | | | | | default_sentinel") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | danglingborrowed_iterator_t | | | | | | unreachable") | | | | | |
| Stream iterators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ostream_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ostreambuf_iterator") | | | | | |

|  |  |  |
| --- | --- | --- |
| template< class I1, class I2, class Out, class R = ranges::less<>,  class P1 = ranges::identity, class P2 = ranges::identity >  concept bool Mergeable =      InputIterator<I1> &&      InputIterator<I2> &&      WeaklyIncrementable<Out> &&      IndirectlyCopyable<I1, Out> &&      IndirectlyCopyable<I2, Out> &&     IndirectStrictWeakOrder<R, ranges::projected<I1, P1>, ranges::projected<I2, P2>>; |  | (ranges TS) |
|  |  |  |

The `Mergeable` concept specifies the common requirements of algorithms that merge sorted sequences into an output sequence by copying the elements (for example, ranges::merge")).

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/iterator/Mergeable&oldid=155540>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 July 2023, at 22:44.