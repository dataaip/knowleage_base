# std::experimental::ranges::ConvertibleTo

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Same | | | | | | DerivedFrom | | | | | | ****ConvertibleTo**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CommonReference | | | | | | Common | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integral | | | | | | SignedIntegral | | | | | | UnsignedIntegral | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignable | | | | | | SwappableSwappableWith | | | | | |
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
| template< class From, class To >  concept bool ConvertibleTo =      std::is_convertible<From, To>::value &&      requires(From (&f)()) {          static_cast<To>(f()); }; |  | (ranges TS) |
|  |  |  |

The concept ConvertibleTo<From, To> specifies that an expression of the type and value category specified by `From` can be implicitly and explicitly converted to the type `To`, and the two forms of conversion are equivalent.

Specifically, ConvertibleTo<From, To> is satisfied only if, given the invented function
To test(From (&f)()) { return f(); } and a function `f` of type From () such that the expression f() is equality-preserving (see below),

- Either
  - `To` is neither an object type nor a reference-to-object type, or
  - static_cast<To>(f()) is equal to `test(f)`, and

- One of the following is true:
  - `From` is not a reference-to-object type, or
  - `From` is an rvalue reference to a non-const-qualified type, and the resulting state of the object referenced by f() is valid but unspecified after either expression above; or
  - the object referred to by `f()` is not modified by either expression above.

There need not be any subsumption relationship between ConvertibleTo<From, To> and std::is_convertible<From, To>::value.

### Equality preservation

An expression is **equality preserving** if it results in equal outputs given equal inputs.

- The inputs to an expression consist of its operands.
- The outputs of an expression consist of its result and all operands modified by the expression (if any).

Every expression required to be equality preserving is further required to be **stable**: two evaluations of such an expression with the same input objects must have equal outputs absent any explicit intervening modification of those input objects.

Unless noted otherwise, every expression used in a **requires-expression** is required to be equality preserving and stable, and the evaluation of the expression may only modify its non-constant operands. Operands that are constant must not be modified.

### See also

|  |  |
| --- | --- |
| is_convertibleis_nothrow_convertible(C++11)(C++20) | checks if a type can be converted to the other type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ranges/concepts/ConvertibleTo&oldid=155297>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 July 2023, at 00:20.