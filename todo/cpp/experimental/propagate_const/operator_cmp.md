# operator==,!=,<,<=,>,>=(std::experimental::propagate_const)

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
| ****operator==operator!=operator<operator>operator<=operator>operator>=**** | | | | |
| swap | | | | |
| get_underlying | | | | |
| Helper classes | | | | |
| std::hash | | | | |
| std::equal_tostd::not_equal_tostd::lessstd::greaterstd::less_equalstd::greater_equal | | | | |

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr bool operator==( const propagate_const<T>& pt, nullptr_t ); | (1) | (library fundamentals TS v2) |
| template< class T >  constexpr bool operator==( nullptr_t, const propagate_const<T>& pt ); | (2) | (library fundamentals TS v2) |
| template< class T >  constexpr bool operator!=( const propagate_const<T>& pt, nullptr_t ); | (3) | (library fundamentals TS v2) |
| template< class T >  constexpr bool operator!=( nullptr_t, const propagate_const<T>& pt ); | (4) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator==( const propagate_const<T>& pt, const propagate_const<U>& pu ); | (5) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator!=( const propagate_const<T>& pt, const propagate_const<U>& pu ); | (6) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator<( const propagate_const<T>& pt, const propagate_const<U>& pu ); | (7) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator>( const propagate_const<T>& pt, const propagate_const<U>& pu ); | (8) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator<=( const propagate_const<T>& pt, const propagate_const<U>& pu ); | (9) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator>=( const propagate_const<T>& pt, const propagate_const<U>& pu ); | (10) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator==( const propagate_const<T>& pt, const U& u ); | (11) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator!=( const propagate_const<T>& pt, const U& u ); | (12) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator==( const T& t, const propagate_const<U>& pu ); | (13) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator!=( const T& t, const propagate_const<U>& pu ); | (14) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator<( const propagate_const<T>& pt, const U& u ); | (15) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator>( const propagate_const<T>& pt, const U& u ); | (16) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator<=( const propagate_const<T>& pt, const U& u ); | (17) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator>=( const propagate_const<T>& pt, const U& u ); | (18) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator<( const T& t, const propagate_const<U>& pu ); | (19) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator>( const T& t, const propagate_const<U>& pu ); | (20) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator<=( const T& t, const propagate_const<U>& pu ); | (21) | (library fundamentals TS v2) |
| template< class T, class U >  constexpr bool operator>=( const T& t, const propagate_const<U>& pu ); | (22) | (library fundamentals TS v2) |
|  |  |  |

Compares the wrapped pointers of two `propagate_const`s, or between a `propagate_const` and nullptr, or between a `propagate_const` and another object.

1-4) Equality comparison for a `propagate_const` and nullptr.5,6) Equality comparison for two `propagate_const`s.7-10) Ordered comparison for two `propagate_const`s.11-14) Equality comparison for a `propagate_const` and another object.15-22) Ordered comparison for a `propagate_const` and another object.

### Parameters

|  |  |  |
| --- | --- | --- |
| pt, pu | - | `propagate_const`s to compare |
| t, u | - | other objects to compare |

### Return value

Let `t_` denote the underlying pointer-like object wrapped by a `propagate_const`.

1) pt.t_ == nullptr2) nullptr == pt.t_3) pt.t_ != nullptr4) nullptr != pt.t_5) pt.t_ == pu.t_6) pt.t_ != pu.t_7) pt.t_ < pu.t_8) pt.t_ > pu.t_9) pt.t_ <= pu.t_10) pt.t_ >= pu.t_11) pt.t_ == u12) pt.t_ != u13) t == pu.t_14) t != pu.t_15) pt.t_ < u16) pt.t_ > u17) pt.t_ <= u18) pt.t_ >= u19) t < pu.t_20) t > pu.t_21) t <= pu.t_22) t >= pu.t_
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/propagate_const/operator_cmp&oldid=157748>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 23:16.