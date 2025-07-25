# std::experimental::ranges::is_swappable_with, std::experimental::ranges::is_swappable, std::experimental::ranges::is_nothrow_swappable_with, std::experimental::ranges::is_nothrow_swappable

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | invoke | | | | | | identity | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | not_equal_to | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater | | | | | | less | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | greater_equal | | | | | | less_equal | | | | | |
| Metaprogramming and type traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****is_swappable_withis_swappable**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****is_nothrow_swappable_withis_nothrow_swappable**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_reference | | | | | | common_type | | | | | |
| Tagged pairs and tuples | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | TagSpecifier | | | | | | TaggedType | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged | | | | | | tag specifiers | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_pair | | | | | | make_tagged_pair | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tagged_tuple | | | | | | make_tagged_tuple | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/type_traits>` |  |  |
| template< class T, class U >  struct is_swappable_with; | (1) | (ranges TS) |
| template< class T >  struct is_swappable; | (2) | (ranges TS) |
| template< class T, class U >  struct is_nothrow_swappable_with; | (3) | (ranges TS) |
| template< class T >  struct is_nothrow_swappable; | (4) | (ranges TS) |
|  |  |  |

1) If the expressions ranges::swap(std::declval<T>(), std::declval<U>()) and ranges::swap(std::declval<U>(), std::declval<T>()) are both well-formed when treated as an unevaluated operand, provides the member constant `value` equal true. Otherwise, `value` is false. Access checks are performed as if from a context unrelated to either type.2) If `T` is not a referenceable type (i.e., possibly cv-qualified void or a function type with a **cv-qualifier-seq** or a **ref-qualifier**), provides a member constant `value` equal to false. Otherwise, provides a member constant `value` equal to ranges::is_swappable_with<T&, T&>::value.3) Same as (1), but evaluations of both expressions from (1) are known not to throw exceptions.4) Same as (2), but uses is_nothrow_swappable_with.

`T` and `U` shall each be a complete type, (possibly cv-qualified) void, or an array of unknown bound. Otherwise, the behavior is undefined.

### Helper variable templates

|  |  |  |
| --- | --- | --- |
| template< class T, class U >  constexpr bool is_swappable_with_v = is_swappable_with<T, U>::value; | (1) | (ranges TS) |
| template< class T >  constexpr bool is_swappable_v = is_swappable<T>::value; | (2) | (ranges TS) |
| template< class T, class U >  constexpr bool is_nothrow_swappable_with_v = is_nothrow_swappable_with<T, U>::value; | (3) | (ranges TS) |
| template< class T >  constexpr bool is_nothrow_swappable_v = is_nothrow_swappable<T>::value; | (4) | (ranges TS) |
|  |  |  |

## Inherited from std::integral_constant

### Member constants

|  |  |
| --- | --- |
| value[static] | true if `T` is swappable with `U`, false otherwise   (public static member constant) |

### Member functions

|  |  |
| --- | --- |
| operator bool | converts the object to bool, returns value   (public member function) |
| operator()(C++14) | returns value   (public member function) |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `value_type` | bool |
| `type` | std::integral_constant<bool, value> |

### Notes

This trait does not check anything outside the immediate context of the swap expressions: if the use of `T` or `U` would trigger template specializations, generation of implicitly-defined special member functions etc, and those have errors, the actual swap may not compile even if `ranges::is_swappable_with<T,U>::value` compiles and evaluates to true.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| SwappableSwappableWith | specifies that a type can be swapped or that two types can be swapped with each other   (concept) |
| is_swappable_withis_swappableis_nothrow_swappable_withis_nothrow_swappable(C++17)(C++17)(C++17)(C++17) | checks if objects of a type can be swapped with objects of same or different type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/type_traits/is_swappable&oldid=159308>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2023, at 01:54.