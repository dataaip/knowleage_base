# std::experimental::ranges::not_equal_to

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

General utilities library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Utility components | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exchange | | | | | |
| Function objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | invoke | | | | | | identity | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | ****not_equal_to**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater | | | | | | less | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater_equal | | | | | | less_equal | | | | | |
| Metaprogramming and type traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_swappable_withis_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_nothrow_swappable_withis_nothrow_swappable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_reference | | | | | | common_type | | | | | |
| Tagged pairs and tuples | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | TagSpecifier | | | | | | TaggedType | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged | | | | | | tag specifiers | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_pair | | | | | | make_tagged_pair | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_tuple | | | | | | make_tagged_tuple | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/functional>` |  |  |
| template< class T = void >      requires EqualityComparable<T> ||               Same<T, void> ||               /\* == on two const T lvalues invokes a built-in operator comparing pointers \*/ struct not_equal_to; |  | (ranges TS) |
| template<>  struct not_equal_to<void>; |  | (ranges TS) |
|  |  |  |

Function object for performing comparisons. The primary template invokes operator == on const lvalues of type `T` and negates the result. The specialization `not_equal_to<void>` deduces the parameter types of the function call operator from the arguments (but not the return type).

All specializations of `not_equal_to` are `Semiregular`.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `is_transparent` (member only of `not_equal_to<void>` specialization) | /\* unspecified \*/ |

### Member functions

|  |  |
| --- | --- |
| operator() | checks if the arguments are **not equal**   (public member function) |

## std::experimental::ranges::not_equal_to::operator()

|  |  |  |
| --- | --- | --- |
| constexpr bool operator()(const T& x, const T& y) const; | (1) | (member only of primary `not_equal_to<T>` template) |
| template< class T, class U >      requires EqualityComparableWith<T, U> ||               /\* std::declval<T>() == std::declval<U>() resolves to                  a built-in operator comparing pointers \*/ constexpr bool operator()(T&& t, U&& u) const; | (2) | (member only of `not_equal_to<void>` specialization) |
|  |  |  |

1) Compares `x` and `y`. Equivalent to return !ranges::equal_to<>{}(x, y);.2) Compares `t` and `u`. Equivalent to return !ranges::equal_to<>{}(std::forward<T>(t), std::forward<U>(u));.

### Notes

Unlike std::not_equal_to, `ranges::not_equal_to` requires both `==` and `!=` to be valid (via the `EqualityComparable` and `EqualityComparableWith` constraints), and is entirely defined in terms of
ranges::equal_to. However, the implementation is free to use operator!= directly, because those concepts require the results of `==` and `!=` to be consistent.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| not_equal_to | function object implementing x != y   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/functional/not_equal_to&oldid=155354>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 July 2023, at 11:18.