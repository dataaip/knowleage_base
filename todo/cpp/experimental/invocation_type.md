# std::experimental::invocation_type, std::experimental::raw_invocation_type

From cppreference.com
< cpp‎ | experimental
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
| ****experimental::invocation_typeexperimental::raw_invocation_type**** | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/type_traits>` |  |  |
| template< class >  struct raw_invocation_type; //undefined    template< class Fn, class... ArgTypes > struct raw_invocation_type<Fn(ArgTypes...)>; | (1) | (library fundamentals TS) |
| template< class >  struct invocation_type; //undefined    template< class Fn, class... ArgTypes > struct invocation_type<Fn(ArgTypes...)>; | (2) | (library fundamentals TS) |
|  |  |  |

Computes the **invocation parameters** when `Fn` is called with the arguments `ArgTypes...`, as in INVOKE(std::declval<Fn>(), std::declval<ArgTypes>()...), where INVOKE is the operation defined in Callable.

The **invocation parameters** of the expression INVOKE(f, t1, t2, ..., tN) is defined as follows, where `T1` is the (possibly cv-qualified) type of `t1` and `U1` is `T1&` if `t1` is an lvalue and `T1&&` otherwise:

- If `f` is a pointer to a member function of a class `T`, then the invocation parameters are `U1` followed by the parameters of `f` matched by `t2, ..., tN`.
- If `N == 1` and `f` is a pointer to member data of a class `T`, then the invocation parameter is `U1`.
- If `f` is an object of class type, the invocation parameters are the parameters matching `t1, ..., tN` of the best viable function for the arguments `t1, ..., tN` among the function call operators and surrogate call functions of `f`.
- In all other cases, the invocations parameters are the parameters of `f` matching `t1, ..., tN`.

If an argument `tI` matches an ellipsis in the function's parameter list, the corresponding invocation parameter is the result of applying the default argument promotions to `tI`.

`Fn` and all types in `ArgTypes` can be any complete type, array of unknown bound, or (possibly cv-qualified) `void`.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| raw_invocation_type<Fn(ArgTypes...)>::type | R(T1, T2, ...), where:  - `R` is std::result_of_t<Fn(ArgTypes...)>. - `T1, T2, ...` are the **invocation parameters** of INVOKE(std::declval<Fn>(), std::declval<ArgTypes>()...) as defined above.   Only defined if `Fn` can be called with the arguments `ArgTypes...` in unevaluated context. |
| invocation_type<Fn(ArgTypes...)>::type | R(U1, U2, ...), where  - `R` is std::result_of_t<Fn(ArgTypes...)>. - `T1, T2, ...` are the **invocation parameters** of INVOKE(std::declval<Fn>(), std::declval<ArgTypes>()...) as defined above. - `A1, A2, ...` denotes `ArgTypes...` - `Ui` is std::decay_t<Ai> if std::declval<Ai>() is an rvalue and `Ti` otherwise.   Only defined if `Fn` can be called with the arguments `ArgTypes...` in unevaluated context. |

### Helper types

|  |  |  |
| --- | --- | --- |
| template< class T >  using raw_invocation_type_t = typename raw_invocation_type<T>::type; |  | (library fundamentals TS) |
| template< class T >  using invocation_type_t = typename invocation_type<T>::type; |  | (library fundamentals TS) |
|  |  |  |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| C++ documentation for Reflection TS | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/invocation_type&oldid=154971>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 July 2023, at 00:52.