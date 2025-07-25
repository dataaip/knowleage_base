# std::tuple_size<std::experimental::ranges::tagged>

From cppreference.com
< cpp‎ | experimental‎ | ranges‎ | utility/tagged
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

General utilities library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Utility components | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exchange | | | | | |
| Function objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | invoke | | | | | | identity | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | not_equal_to | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater | | | | | | less | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater_equal | | | | | | less_equal | | | | | |
| Metaprogramming and type traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_swappable_withis_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_nothrow_swappable_withis_nothrow_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_reference | | | | | | common_type | | | | | |
| Tagged pairs and tuples | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | TagSpecifier | | | | | | TaggedType | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged | | | | | | tag specifiers | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_pair | | | | | | make_tagged_pair | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_tuple | | | | | | make_tagged_tuple | | | | | |  | | | | | |

std::experimental::ranges::tagged

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| tagged::tagged | | | | |
| tagged::operator= | | | | |
| tagged::swap | | | | |
| Named accessors | | | | |
| Non-member functions | | | | |
| ranges::swap(ranges::tagged) | | | | |
| Helper classes | | | | |
| ****tuple_size**** | | | | |
| tuple_element | | | | |

|  |  |  |
| --- | --- | --- |
| template< class Base, class... Tags >  struct tuple_size<std::experimental::ranges::tagged<Base, Tags...>> : std::tuple_size<Base> {}; |  | (ranges TS) |
|  |  |  |

The partial specialization of std::tuple_size for `tagged` provides the ability to obtain the number of elements in a `tagged` object using tuple-like syntax. It simply forwards to std::tuple_size<Base>.

## Inherited from std::integral_constant

### Member constants

|  |  |
| --- | --- |
| value[static] | std::tuple_size<Base>::value   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| operator std::size_t | converts the object to std::size_t, returns value   (public member function) |
| operator()(C++14) | returns value   (public member function) |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `value_type` | std::size_t |
| `type` | std::integral_constant<std::size_t, value> |

### See also

|  |  |
| --- | --- |
| std::tuple_size<std::tuple>(C++11) | obtains the size of a `tuple`   (class template specialization) |
| std::tuple_size<std::array>(C++11) | obtains the size of an `array`   (class template specialization) |
| std::tuple_size<std::pair>(C++11) | obtains the size of a `pair`   (class template specialization) |
| std::tuple_element<std::experimental::ranges::tagged> | obtains the types of the elements of a `tagged`   (class template specialization) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/utility/tagged/tuple_size&oldid=155632>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 July 2023, at 22:40.