# std::experimental::ranges::DerivedFrom

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

Concepts library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Core language concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Same | | | | | | ****DerivedFrom**** | | | | | | ConvertibleTo | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CommonReference | | | | | | Common | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integral | | | | | | SignedIntegral | | | | | | UnsignedIntegral | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignable | | | | | | SwappableSwappableWith | | | | | |
| Object concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Destructible | | | | | | Constructible | | | | | | DefaultConstructible | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MoveConstructible | | | | | | CopyConstructible | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Movable | | | | | | Copyable | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Semiregular | | | | | | Regular | | | | | |  | | | | | |
| Comparison concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Boolean | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | WeaklyEqualityComparableWith | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | EqualityComparableEqualityComparableWith | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | StrictTotallyOrderedStrictTotallyOrderedWith | | | | | |
| Callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | InvocableRegularInvocable | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Predicate | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Relation | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | StrictWeakOrder | | | | | |  | | | | | |
| URNG concept | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | UniformRandomNumberGenerator | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/ranges/concepts>` |  |  |
| template< class T, class U >  concept bool DerivedFrom =      std::is_base_of<U, T>::value && std::is_convertible<std::remove_cv_t<T>\*, std::remove_cv_t<U>\*>::value; |  | (ranges TS) |
|  |  |  |

The concept DerivedFrom<T, U> is satisfied if and only if `U` is a class type that is either `T` or a public and unambiguous base of `T`.

Despite the use of std::is_base_of and std::is_convertible in its description above, `DerivedFrom` is not required to use it in its implementation. Thus, there need not be any subsumption relationship between DerivedFrom<T, U> and std::is_base_of<U,T>::value or std::is_convertible<std::remove_cv_t<T>\*, std::remove_cv_t<U>\*>::value.

### See also

|  |  |
| --- | --- |
| is_base_of(C++11) | checks if a type is a base of the other type   (class template) |
| is_convertibleis_nothrow_convertible(C++11)(C++20) | checks if a type can be converted to the other type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/concepts/DerivedFrom&oldid=155301>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 July 2023, at 00:26.