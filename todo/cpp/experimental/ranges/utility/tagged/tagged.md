# std::experimental::ranges::tagged<Base,Tags...>::tagged

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
| ****tagged::tagged**** | | | | |
| tagged::operator= | | | | |
| tagged::swap | | | | |
| Named accessors | | | | |
| Non-member functions | | | | |
| ranges::swap(ranges::tagged) | | | | |
| Helper classes | | | | |
| tuple_size | | | | |
| tuple_element | | | | |

|  |  |  |
| --- | --- | --- |
| using Base::Base; | (1) |  |
| tagged() = default; | (2) |  |
| tagged( tagged&& that ) = default; | (3) |  |
| tagged( const tagged& that ) = default; | (4) |  |
| tagged( Base&& that ) noexcept(std::is_nothrow_move_constructible<Base>::value)      requires MoveConstructible<Base>; | (5) |  |
| tagged( const Base& that ) noexcept(std::is_nothrow_copy_constructible<Base>::value)      requires CopyConstructible<Base>; | (6) |  |
| template< class Other >      requires Constructible<Base, Other>  constexpr tagged( ranges::tagged<Other, Tags...> && that ) noexcept(std::is_nothrow_constructible<Base, Other>::value); | (7) |  |
| template< class Other >      requires Constructible<Base, const Other&> constexpr tagged( const ranges::tagged<Other, Tags...> &that ); | (8) |  |
|  |  |  |

Constructs a `tagged` object.

1) `tagged<Base, Tags...>` inherits the constructors of `Base`.2-4) `tagged` has defaulted default, copy, and move constructors that invoke the corresponding constructor of `Base`.5) Converting move constructor from `Base`. Initializes the `Base` subobject with std::move(that).6) Converting copy constructor from `Base`. Initializes the `Base` subobject with that.7) Converting move constructor from a different `tagged` specialization with matching tags. Initializes the `Base` subobject with static_cast<Other&&>(that).8) Converting copy constructor from a different `tagged` specialization with matching tags. Initializes the `Base` subobject with static_cast<const Other&>(that).
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/utility/tagged/tagged&oldid=155630>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 July 2023, at 22:37.