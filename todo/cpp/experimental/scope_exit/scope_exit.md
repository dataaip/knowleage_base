# std::experimental::scope_exit<EF>::scope_exit

From cppreference.com
< cpp‎ | experimental‎ | scope exit
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

Library fundamentals v3

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::scope_exit | | | | |
| experimental::scope_fail | | | | |
| experimental::scope_success | | | | |
| experimental::unique_resource | | | | |

std::experimental::scope_exit

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****scope_exit::scope_exit**** | | | | |
| scope_exit::~scope_exit | | | | |
| Modifiers | | | | |
| scope_exit::release | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< class Fn >  explicit scope_exit( Fn&& fn ) noexcept(/\*see below\*/); | (1) | (library fundamentals TS v3) |
| scope_exit( scope_exit&& other ) noexcept(/\*see below\*/); | (2) | (library fundamentals TS v3) |
| scope_exit( const scope_exit& ) = delete; | (3) | (library fundamentals TS v3) |
|  |  |  |

Creates a `scope_exit` from a function, a function object or another `scope_exit`.

1) Initializes the exit function with a function or function object. The constructed `scope_exit` is active. If `Fn` is not an lvalue reference type and std::is_nothrow_constructible_v<EF, Fn> is true, the stored `EF` is initialized with std::forward<Fn>(fn); otherwise it is initialized with fn. If initialization of the stored `EF` throws an exception, calls fn(). This overload participates in overload resolution only if std::is_same_v<std::remove_cvref_t<Fn>, scope_exit> is false and std::is_constructible_v<EF, Fn> is true. The program is ill-formed if function call expression fn() is ill-formed. The behavior is undefined if calling fn() throws an exception or results in undefined behavior, even if fn has not been called.2) Move constructor. Initializes the stored `EF` with the one in other. The constructed `scope_exit` is active if and only if other is active before the construction. If std::is_nothrow_move_constructible_v<EF> is true, initializes stored `EF` (denoted by `exitfun`) with std::forward<EF>(other.exitfun), otherwise initializes it with other.exitfun. After successful move construction, other.release() is called and other becomes inactive. This overload participates in overload resolution only if std::is_nothrow_move_constructible_v<EF> is true or std::is_copy_constructible_v<EF> is true. The behavior is undefined if

- std::is_nothrow_move_constructible_v<EF> is true and `EF` does not meet the requirements of MoveConstructible, or
- std::is_nothrow_move_constructible_v<EF> is false and `EF` does not meet the requirements of CopyConstructible.
3) `scope_exit` is not CopyConstructible.

### Parameters

|  |  |  |
| --- | --- | --- |
| fn | - | function or function object used for initializing the stored `EF` |
| other | - | `scope_exit` to move from |

### Exceptions

Any exception thrown during the initialization of the stored `EF`.

1)noexcept specification:noexcept(std::is_nothrow_constructible_v<EF, Fn> ||  
         std::is_nothrow_constructible_v<EF, Fn&>)2)noexcept specification:noexcept(std::is_nothrow_move_constructible_v<EF> ||  
         std::is_nothrow_copy_constructible_v<EF>)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| release | makes the `scope_exit` inactive   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/scope_exit/scope_exit&oldid=115129>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 January 2020, at 22:35.