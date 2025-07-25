# Concepts library (since C++20)

From cppreference.com
< cpp
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
| ****Concepts library**** (C++20) | | | | |
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

****Concepts library****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | derived_from(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | common_with(C++20) | | | | | | integral(C++20) | | | | | | signed_integral(C++20) | | | | | | unsigned_integral(C++20) | | | | | | floating_point(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | equality_comparableequality_comparable_with(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | semiregular(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

The concepts library provides definitions of fundamental library concepts that can be used to perform compile-time validation of template arguments and perform function dispatch based on properties of types. These concepts provide a foundation for equational reasoning in programs.

Most concepts in the standard library impose both syntactic and semantic requirements. It is said that a standard concept is **satisfied** if its syntactic requirements are met, and is **modeled** if it is satisfied and its semantic requirements (if any) are also met.

In general, only the syntactic requirements can be checked by the compiler. If the validity or meaning of a program depends whether a sequence of template arguments models a concept, and the concept is satisfied but not modeled, or if a semantic requirement is not met at the point of use, the program is ill-formed, no diagnostic required.

### Equality preservation

An expression is **equality-preserving** if it results in equal outputs given equal inputs, where

- the inputs consist of its operands (not neccessarily making the expression semantically valid), and
- the outputs consist of its result and all modifications to the operands by the expression, if any

where, for convenience of wording, its "operands" refer to its largest sub-expressions that consist of an id-expression or invocations of std::move, std::forward, and std::declval.

The cv-qualification and value category of each operand is determined by assuming that each template type parameter in its type denotes a cv-unqualified complete non-array object type.

Every expression required to be equality preserving is further required to be stable, that is, two evaluations of it with the same input objects must have equal outputs without any explicit intervening modification of those input objects.

Unless noted otherwise, every expression used in a requires expression of the standard library concepts is required to be equality preserving, and the evaluation of the expression may modify only its non-constant operands. Operands that are constant must not be modified.

In the standard library, the following concepts are allowed to have non equality-preserving requires expressions:

- `output_iterator`
- `indirectly_writable`
- `invocable`
- `weakly_incrementable`
- `range`

### Implicit expression variations

A requires expression that uses an expression that is non-modifying for some constant lvalue operand also implicitly requires additional variations of that expression that accept a non-constant lvalue or (possibly constant) rvalue for the given operand unless such an expression variation is explicitly required with differing semantics.

These **implicit expression variations** must meet the same semantic requirements of the declared expression. The extent to which an implementation validates the syntax of the variations is unspecified.

```
template<class T>
concept C = requires(T a, T b, const T c, const T d)
{
    c == d;           // expression #1: does not modify the operands
    a = std::move(b); // expression #2: modifies both operands
    a = c;            // expression #3: modifies the left operand `a`
};
 
// Expression #1 implicitly requires additional expression variations that
// meet the requirements for c == d (including non-modification),
// as if the following expressions had been declared as well:
 
// ------ const == const ------- ------ const == non-const ---
//                                         c  ==           b;
//            c == std::move(d);           c  == std::move(b);
// std::move(c) ==           d;  std::move(c) ==           b;
// std::move(c) == std::move(d); std::move(c) == std::move(b);
 
// -- non-const == const ------- -- non-const == non-const ---
//           a  ==           d;            a  ==           b;
//           a  == std::move(d);           a  == std::move(b);
// std::move(a) ==           d;  std::move(a) ==           b;
// std::move(a) == std::move(d); std::move(a) == std::move(b);
 
// Expression #3 implicitly requires additional expression variations that
// meet the requirements for a = c
// (including non-modification of the second operand),
// as if the expressions a = b (non-constant lvalue variation)
// and a = std::move(c) (const rvalue variation) had been declared.
 
// Note: Since expression #2 already requires the non-constant rvalue variation
// (a == std::move(b)) explicitly, expression #3 does not implicitly require it anymore.
 
// The type T meets the explicitly stated syntactic requirements of
// concept C above, but does not meet the additional implicit requirements
// (i.e., T satisfies but does not model C):
// a program requires C<T> is ill-formed (no diagnostic required).
struct T
{
    bool operator==(const T&) const { return true; }
    bool operator==(T&) = delete;
};

```

### Standard library concepts

|  |  |
| --- | --- |
| Defined in namespace `std` | |
| Core language concepts | |
| Defined in header `<concepts>` | |
| same_as(C++20) | specifies that a type is the same as another type   (concept) |
| derived_from(C++20) | specifies that a type is derived from another type   (concept) |
| convertible_to(C++20) | specifies that a type is implicitly convertible to another type   (concept) |
| common_reference_with(C++20) | specifies that two types share a common reference type   (concept) |
| common_with(C++20) | specifies that two types share a common type   (concept) |
| integral(C++20) | specifies that a type is an integral type   (concept) |
| signed_integral(C++20) | specifies that a type is an integral type that is signed   (concept) |
| unsigned_integral(C++20) | specifies that a type is an integral type that is unsigned   (concept) |
| floating_point(C++20) | specifies that a type is a floating-point type   (concept) |
| assignable_from(C++20) | specifies that a type is assignable from another type   (concept) |
| swappableswappable_with(C++20) | specifies that a type can be swapped or that two types can be swapped with each other   (concept) |
| destructible(C++20) | specifies that an object of the type can be destroyed   (concept) |
| constructible_from(C++20) | specifies that a variable of the type can be constructed from or bound to a set of argument types   (concept) |
| default_initializable(C++20) | specifies that an object of a type can be default constructed   (concept) |
| move_constructible(C++20) | specifies that an object of a type can be move constructed   (concept) |
| copy_constructible(C++20) | specifies that an object of a type can be copy constructed and move constructed   (concept) |
| Comparison concepts | |
| Defined in header `<concepts>` | |
| **boolean-testable** ﻿(C++20) | specifies that a type can be used in Boolean contexts (exposition-only concept\*) |
| equality_comparableequality_comparable_with(C++20) | specifies that operator == is an equivalence relation   (concept) |
| totally_orderedtotally_ordered_with(C++20) | specifies that the comparison operators on the type yield a total order   (concept) |
| Defined in header `<compare>` | |
| three_way_comparablethree_way_comparable_with(C++20) | specifies that operator <=> produces consistent result on given types   (concept) |
| Object concepts | |
| Defined in header `<concepts>` | |
| movable(C++20) | specifies that an object of a type can be moved and swapped   (concept) |
| copyable(C++20) | specifies that an object of a type can be copied, moved, and swapped   (concept) |
| semiregular(C++20) | specifies that an object of a type can be copied, moved, swapped, and default constructed   (concept) |
| regular(C++20) | specifies that a type is regular, that is, it is both `semiregular` and `equality_comparable`   (concept) |
| Callable concepts | |
| Defined in header `<concepts>` | |
| invocableregular_invocable(C++20) | specifies that a callable type can be invoked with a given set of argument types   (concept) |
| predicate(C++20) | specifies that a callable type is a Boolean predicate   (concept) |
| relation(C++20) | specifies that a callable type is a binary relation   (concept) |
| equivalence_relation(C++20) | specifies that a `relation` imposes an equivalence relation   (concept) |
| strict_weak_order(C++20) | specifies that a `relation` imposes a strict weak ordering   (concept) |

Additional concepts can be found in the iterators library, the algorithms library, and the ranges library.

### See also

- Named Requirements
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts&oldid=175880>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 September 2024, at 17:31.