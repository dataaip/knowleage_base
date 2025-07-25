# C++ named requirements: Container

From cppreference.com
< cpp‎ | named req
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

C++ named requirements

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | ****Container**** | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

A Container is an object used to store other objects and taking care of the management of the memory used by the objects it contains.

### Requirements

Given the following types and values:

|  |  |
| --- | --- |
| Type | Definition |
| `T` | an object type |
| `C` | a container class containing objects of type `T` |
| Value | Definition |
| u, v | values of type `C` or const C |
| mv | a value of type `C` |
| cv | a value of type const C |
| lhs, rhs | lvalues of type `C` |
| i, j | values of type `C::iterator` or const C::iterator |

`C` satisfies the requirements of Container if the following types, statements, and expressions are well-formed and have the specified semantics:

#### Types

| Type | Definition | Requirements |
| --- | --- | --- |
| typename C::value_type | `T` | `T` is CopyConstructible(until C++11)Erasable from `C`(since C++11). |
| typename C::reference | `T&` | No explicit requirement |
| typename C::const_reference | const T& |
| typename C::iterator | an iterator type | - `C::iterator` is a LegacyForwardIterator, and its value type is `T`. - `C::iterator` is convertible to `C::const_iterator`. |
| typename C::const_iterator | a constant iterator type | `C::const_iterator` is a LegacyForwardIterator, and its value type is `T`. |
| typename C::difference_type | a signed integer type | `C::difference_type` is the same as the difference type of `C::iterator` and `C::const_iterator`. |
| typename C::size_type | an unsigned integer type | `C::size_type` is large enough to represent all non-negative values of `C::difference_type`. |

#### Statements

| Statement | Semantics | | Complexity |
| --- | --- | --- | --- |
| C c; C c = C(); | Postcondition | c.empty() is true. | constant |
| C c(v); C c = C(v); | Precondition | |  |  | | --- | --- | | If v is not an rvalue of type `C`, `T` is CopyInsertable into `C`. | (since C++11) | | linear[[1]](Container.html#cite_note-1) |
| Postcondition | - If v is an lvalue, c == v is true. - If v is an rvalue, and c and v do not refer to the same object(since C++11), c is equal to the value that v had before this construction. |
| Notes | | | |
| 1. ↑ If v is an rvalue of type `C`, and `C` is not a specialization of std::array or std::inplace_vector, the complexity is constant. | | | |

#### Expressions

| Expression | Type | Semantics | | Complexity |
| --- | --- | --- | --- | --- |
| C() | `C` | Postcondition | C().empty() is true. | constant |
| C(v) | `C` | Precondition | |  |  | | --- | --- | | If v is not an rvalue of type `C`, `T` is CopyInsertable into `C`. | (since C++11) | | constant[[1]](Container.html#cite_note-2) |
| Postcondition | - If v is an lvalue, C(v) == v is true. - If v is an rvalue, and C(v) and v do not refer to the same object(since C++11), C(v) is equal to the value that v had before this construction. |
| lhs = v | `C&` | Postcondition | - If v is an lvalue, lhs == v is true. - If v is an rvalue, and lv and v do not refer to the same object(since C++11), lhs is equal to the value that v had before this assignment. | linear |
| v.~C() | void | Effect | Destroys all elements of v and deallocates all memory obtained. | linear |
| mv.begin() | `C::iterator` | Effect | Returns an iterator pointing to the first element of mv. | constant |
| cv.begin() | `C::const_iterator` | Effect | Returns an iterator pointing to the first element of cv. | constant |
| mv.end() | `C::iterator` | Effect | Returns the past-the-end iterator of mv. | constant |
| cv.end() | `C::const_iterator` | Effect | Returns the past-the-end iterator of cv. | constant |
| v.cbegin() (since C++11) | `C::const_iterator` | Effect | Returns const_cast<const C&>(v).begin(). | constant |
| v.cend() (since C++11) | `C::const_iterator` | Effect | Returns const_cast<const C&>(v).end(). | constant |
| i <=> j (since C++20) | std::strong_ordering | Constraint | This expression is only required to be well-formed if `C::iterator` satisfies the random access iterator requirements. | constant |
| u == v | bool | Effect | Returns  |  |  | | --- | --- | | u.size() == v.size() &&     std::equal(u.begin(),          u.end(), v.begin()) | (until C++14) | | std::equal(u.begin(), u.end(),            v.begin(), v.end()) | (since C++14) |  . | linear[[2]](Container.html#cite_note-3) |
| u != v |  | Effect | Equivalent to !(u == v). |
| lhs.swap(rhs) swap(lhs, rhs) | void | Effect | Exchanges the contents of lhs and rhs. | constant[[3]](Container.html#cite_note-4) |
| v.size() | `C::size_type` | Effect | Returns the number of elements[[4]](Container.html#cite_note-5) of v. | constant |
| v.max_size() | `C::size_type` | Effect | Returns the number of elements of the largest possible container of type `C`. | constant |
| v.empty() | bool | Effect | Returns v.begin() == v.end(). | constant |
| Optional container requirements (only provided for some types of containers) | | | | |
| u <=> v (since C++20) | **synth-three-way-result** <C::value_type> | Precondition | Either `T` models `three_way_comparable`, or operator< is a total ordering relationship defined for values of type `T` and const T. | linear |
| Effect | Returns std::lexicographical_compare_three_way (u.begin(), u.end(), v.begin(), v.end(), **synth-three-way** ﻿)[[5]](Container.html#cite_note-6). |
| Notes | | | | |
| 1. ↑ If v is an rvalue of type `C`, and `C` is a specialization of std::array or std::inplace_vector, the complexity is linear. 2. ↑ If u.size() != v.size() is true, the complexity is constant. 3. ↑ If `C` is a specialization of std::array or std::inplace_vector, the complexity is linear. 4. ↑ The number of elements is defined by the rules of constructors, inserts, and erases. It is equal to the value of std::distance(v.begin(), v.end()). 5. ↑ If the iterators passed to std::lexicographical_compare_three_way are ConstexprIterators, the operation is implemented by constexpr functions. | | | | |

In the expressions i == j, i != j, i < j, i <= j, i >= j, i > j and i - j, if i and/or j are replaced by iterators of type `C::const_iterator` pointing to the same element respectively, the semantics remain the same.

### Container data races

See container thread safety.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 179 | C++98 | `iterator` and `const_iterator` types might be incomparable | required to be comparable |
| LWG 276 | C++98 | `T` was required to be CopyAssignable | `T` is required to be CopyConstructible |
| LWG 322 | C++98 | the value types of `iterator` and `const_iterator` were not specified | specified as `T` |
| LWG 774 | C++98 | there was no requirement on swap(a, b) | added |
| LWG 883 | C++98 | a.swap(b) was defined as swap(a, b), resulted in circular definition | defined as exchanging the values of a and b |
| LWG 1319 | C++98 | `iterator` and `const_iterator` might not have multipass guarantee | they are required to satisfy the requirements of LegacyForwardIterator |
| LWG 2114 (P2167R3) | C++98 | non-bool return types of some functions were allowed | disallowed |
| LWG 2182 | C++98 | the types deonted by `reference` and `const_reference` were poorly specified | improved wording |
| LWG 2257 | C++98 | two containers required linear time to compare equal even if they have different sizes | only requires constant time in this case |
| LWG 2263 | C++11 | the resolution of LWG issue 179 was accidentally dropped in C++11 | restored |
| LWG 2839 | C++11 | self move assignment of standard containers was not allowed | allowed but the result is unspecified |
| N3346 | C++11 | `C::value_type` was required to be Destructible | required to be Erasable from `C` |

### See also

|  |  |
| --- | --- |
| C++ documentation for Containers library | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/Container&oldid=177547>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 November 2024, at 17:45.