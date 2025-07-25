# std::experimental::optional<T>::emplace

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
| ****optional::emplace**** | | | | |
| optional::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator<=operator>operator>= | | | | |
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
| template< class... Args >   void emplace( Args&&... args ); |  | (library fundamentals TS) |
| template< class U, class... Args >   void emplace( std::initializer_list<U> ilist, Args&&... args ); |  | (library fundamentals TS) |
|  |  |  |

Constructs the contained value in-place. If \*this already contains a value before the call, the contained value is destroyed by calling its destructor.

1) Initializes the contained value by direct-initializing (but not direct-list-initializing) with std::forward<Args>(args)... as parameters.2) Initializes the contained value by calling its constructor with ilist, std::forward<Args>(args)... as parameters. This overload participates in overload resolution only if std::is_constructible<T, std::initializer_list<U>&, Args&&...>::value is true.

### Parameters

|  |  |  |
| --- | --- | --- |
| args... | - | the arguments to pass to the constructor |
| ilist | - | the initializer list to pass to the constructor |
| Type requirements | | |
| -`T` must be constructible from `Args...` | | |
| -`T` must be constructible from std::initializer_list and `Args...` | | |

### Return value

(none)

### Exceptions

Any exception thrown by the selected constructor of `T`. If an exception is thrown, \*this does not contain a value after this call (the previously contained value, if any, had been destroyed).

### See also

|  |  |
| --- | --- |
| operator= | assigns contents   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/optional/emplace&oldid=78317>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 May 2015, at 22:22.