# std::experimental::ranges::tagged<Base,Tags...>::operator=

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
| ****tagged::operator=**** | | | | |
| tagged::swap | | | | |
| Named accessors | | | | |
| Non-member functions | | | | |
| ranges::swap(ranges::tagged) | | | | |
| Helper classes | | | | |
| tuple_size | | | | |
| tuple_element | | | | |

|  |  |  |
| --- | --- | --- |
| tagged &operator=( tagged&& that ) = default; | (1) |  |
| tagged &operator=( const tagged& that ) = default; | (2) |  |
| template< class Other >      requires Assignable<Base&, Other>  constexpr tagged& operator=( ranges::tagged<Other, Tags...>&& that ) noexcept(std::is_nothrow_assignable<Base&, Other>::value); | (3) |  |
| template< class Other >      requires Assignable<Base&, const Other&> constexpr tagged& operator=( const ranges::tagged<Other, Tags...>& that ); | (4) |  |
| template< class U >      requires Assignable<Base&, U> && !Same<std::decay_t<U>, tagged> constexpr tagged& operator=( U&& that ) noexcept(std::is_nothrow_assignable<Base&, U>::value); | (5) |  |
|  |  |  |

Assigns the contents of that to \*this.

1,2) `tagged` has defaulted copy and move assignment operators that invoke the corresponding assignment operator of `Base`.3) Converting move assignment from a different `tagged` specialization with matching tags. Equivalent to static_cast<Base&>(\*this) = static_cast<Other&&>(that);.4) Converting copy assignment from a different `tagged` specialization with matching tags. Equivalent to static_cast<Base&>(\*this) = static_cast<const Other&>(that);.5) Assigns that to the `Base` subobject. Equivalent to static_cast<Base&>(\*this) = std::forward<U>(that);.

### Return value

\*this.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/utility/tagged/operator%3D&oldid=157772>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 September 2023, at 09:22.