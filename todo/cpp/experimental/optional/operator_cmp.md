# operator==, !=, <, <=, >, >=(std::experimental::optional)

From cppreference.com
< cpp‎ | experimental‎ | optional
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

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

std::experimental::optional

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| optional::optional | | | | |
| optional::~optional | | | | |
| optional::operator= | | | | |
| Observers | | | | |
| optional::operator->optional::operator\* | | | | |
| optional::operator bool | | | | |
| optional::value | | | | |
| optional::value_or | | | | |
| Modifiers | | | | |
| optional::emplace | | | | |
| optional::swap | | | | |
| Non-member functions | | | | |
| ****operator==operator!=operator<operator<=operator>operator>=**** | | | | |
| make_optional | | | | |
| swap | | | | |
| Helper classes | | | | |
| hash | | | | |
| nullopt_t | | | | |
| in_place_t | | | | |
| bad_optional_access | | | | |
| Helper objects | | | | |
| nullopt | | | | |
| in_place | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/optional>` |  |  |
| Compare two `optional` objects |  |  |
| template< class T >   constexpr bool operator==( const optional<T>& lhs, const optional<T>& rhs ); | (1) | (library fundamentals TS) |
| template< class T >   constexpr bool operator!=( const optional<T>& lhs, const optional<T>& rhs ); | (2) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<( const optional<T>& lhs, const optional<T>& rhs ); | (3) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<=( const optional<T>& lhs, const optional<T>& rhs ); | (4) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>( const optional<T>& lhs, const optional<T>& rhs ); | (5) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>=( const optional<T>& lhs, const optional<T>& rhs ); | (6) | (library fundamentals TS) |
| Compare an `optional` object with a `nullopt` |  |  |
| template< class T >   constexpr bool operator==( const optional<T>& opt, std::nullopt_t ) noexcept; | (7) | (library fundamentals TS) |
| template< class T >   constexpr bool operator==( std::nullopt_t, const optional<T>& opt ) noexcept; | (8) | (library fundamentals TS) |
| template< class T >   constexpr bool operator!=( const optional<T>& opt, std::nullopt_t ) noexcept; | (9) | (library fundamentals TS) |
| template< class T >   constexpr bool operator!=( std::nullopt_t, const optional<T>& opt ) noexcept; | (10) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<( const optional<T>& opt, std::nullopt_t ) noexcept; | (11) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<( std::nullopt_t, const optional<T>& opt ) noexcept; | (12) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<=( const optional<T>& opt, std::nullopt_t ) noexcept; | (13) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<=( std::nullopt_t, const optional<T>& opt ) noexcept; | (14) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>( const optional<T>& opt, std::nullopt_t ) noexcept; | (15) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>( std::nullopt_t, const optional<T>& opt ) noexcept; | (16) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>=( const optional<T>& opt, std::nullopt_t ) noexcept; | (17) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>=( std::nullopt_t, const optional<T>& opt ) noexcept; | (18) | (library fundamentals TS) |
| Compare an `optional` object with a `T` |  |  |
| template< class T >   constexpr bool operator==( const optional<T>& opt, const T& value ); | (19) | (library fundamentals TS) |
| template< class T >   constexpr bool operator==( const T& value, const optional<T>& opt ); | (20) | (library fundamentals TS) |
| template< class T >   constexpr bool operator!=( const optional<T>& opt, const T& value ); | (21) | (library fundamentals TS) |
| template< class T >   constexpr bool operator!=( const T& value, const optional<T>& opt ); | (22) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<( const optional<T>& opt, const T& value ); | (23) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<( const T& value, const optional<T>& opt ); | (24) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<=( const optional<T>& opt, const T& value ); | (25) | (library fundamentals TS) |
| template< class T >   constexpr bool operator<=( const T& value, const optional<T>& opt ); | (26) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>( const optional<T>& opt, const T& value ); | (27) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>( const T& value, const optional<T>& opt ); | (28) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>=( const optional<T>& opt, const T& value ); | (29) | (library fundamentals TS) |
| template< class T >   constexpr bool operator>=( const T& value, const optional<T>& opt ); | (30) | (library fundamentals TS) |
|  |  |  |

Performs comparison operations on `optional` objects.

1-6) Compares two `optional` objects, lhs and rhs. The contained values are compared (using operator== for (1,2) and operator< for (3-6)) only if both lhs and rhs contain values. Otherwise,

:   :   - lhs is considered **equal to** rhs if, and only if, both lhs and rhs do not contain a value.
        - lhs is considered **less than** rhs if, and only if, rhs contains a value and lhs does not.

7-18) Compares opt with a nullopt. Equivalent to (1-6) when comparing to an `optional` that does not contain a value.19-30) Compares opt with a value. The values are compared (using operator== for (19-22) and operator< for (23-30)) only if opt contains a value. Otherwise, opt is considered **less than** value.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs, opt | - | an `optional` object to compare |
| value | - | value to compare to the contained value |
| Type requirements | | |
| -`T` must meet the requirements of EqualityComparable in order to use overloads (1,2). | | |

### Return value

1) If bool(lhs) != bool(rhs), returns false. Otherwise, if bool(lhs) == false (and so bool(rhs) == false as well), returns true. Otherwise, returns \*lhs == \*rhs.2) Returns !(lhs == rhs).3) If bool(rhs) == false returns false. Otherwise, if bool(lhs) == false, returns true. Otherwise returns \*x < \*y.4) Returns !(rhs < lhs).5) Returns rhs < lhs.6) Returns !(lhs < rhs).7,8) Returns !opt.9,10) Returns bool(opt).11) Returns false.12) Returns bool(opt).13) Returns !opt.14) Returns true.15) Returns bool(opt).16) Returns false.17) Returns true.18) Returns !opt.19) Returns bool(opt) ? \*opt == value : false.20) Returns bool(opt) ? value == \*opt : false.21) Returns bool(opt) ? !(\*opt == value) : true.22) Returns bool(opt) ? !(value == \*opt) : true.23) Returns bool(opt) ? \*opt < value : true.24) Returns bool(opt) ? value < \*opt : false.25) Returns !(opt > value).26) Returns !(value > opt).27) Returns bool(opt) ? value < \*opt : false.28) Returns bool(opt) ? \*opt < value : true.29) Returns !(opt < value).30) Returns !(value < opt).

### Exceptions

1-6) (none)19-30) (none)
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/optional/operator_cmp&oldid=157743>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 22:57.