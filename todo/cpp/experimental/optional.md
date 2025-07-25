# std::experimental::optional

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
| ****experimental::optional**** | | | | |
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

****std::experimental::optional****

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
| Defined in header `<experimental/optional>` |  |  |
| template< class T >  class optional; |  | (library fundamentals TS) |
|  |  |  |

The class template `std::experimental::optional` manages an **optional** contained value, i.e. a value that may or may not be present.

A common use case for `optional` is the return value of a function that may fail. As opposed to other approaches, such as std::pair<T,bool>, `optional` handles expensive to construct objects well and is more readable, as the intent is expressed explicitly.

Any instance of `optional<T>` at any given point in time either **contains a value** or **does not contain a value**.

If an `optional<T>` **contains a value**, the value is guaranteed to be allocated as part of the `optional` object footprint, i.e. no dynamic memory allocation ever takes place. Thus, an `optional` object models an object, not a pointer, even though the operator\*() and operator->() are defined.

When an object of type optional<T> is contextually converted to bool, the conversion returns true if the object **contains a value** and false if it **does not contain a value**.

The `optional` object **contains a value** in the following conditions:

- The object is initialized with a value of type `T`.
- The object is assigned from another `optional` that **contains a value**.

The object **does not contain a value** in the following conditions:

- The object is default-initialized.
- The object is initialized with a value of std::experimental::nullopt_t or an `optional` object that **does not contain a value**.
- The object is assigned from a value of std::experimental::nullopt_t or from an `optional` that **does not contain a value**.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | the type of the value to manage initialization state for. The type must meet the requirements of Destructible. |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `T` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the optional object   (public member function) |
| (destructor) | destroys the contained value, if there is one   (public member function) |
| operator= | assigns contents   (public member function) |
| Observers | |
| operator->operator\* | accesses the contained value   (public member function) |
| operator bool | checks whether the object contains a value   (public member function) |
| value | returns the contained value   (public member function) |
| value_or | returns the contained value if available, another value otherwise   (public member function) |
| Modifiers | |
| swap | exchanges the contents   (public member function) |
| emplace | constructs the contained value in-place   (public member function) |

### Member objects

|  |  |
| --- | --- |
| Member name | Definition |
| `val` (private) | pointer to the contained value (which points at a data member of the same object), the name is for exposition only |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>= | compares `optional` objects   (function template) |
| make_optional | creates an `optional` object   (function template) |
| std::swap(std::experimental::optional) | specializes the std::swap algorithm   (function) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::experimental::optional> | specializes the std::hash algorithm   (class template specialization) |
| nullopt_t(library fundamentals TS) | indicator of optional type with uninitialized state   (class) |
| in_place_t(library fundamentals TS) | disambiguation tag type for in-place construction of optional types   (class) |
| bad_optional_access(library fundamentals TS) | exception indicating checked access to an optional that doesn't contain a value   (class) |

### Helper objects

|  |  |
| --- | --- |
| nullopt(library fundamentals TS) | an object of type `nullopt_t`   (function) |
| in_place(library fundamentals TS) | an object of type std::experimental::in_place_t   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/optional&oldid=164198>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2023, at 01:34.