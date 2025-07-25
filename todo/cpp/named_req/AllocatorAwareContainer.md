# C++ named requirements: AllocatorAwareContainer (since C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | ****AllocatorAwareContainer**** | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

An ****AllocatorAwareContainer**** is a Container that holds an instance of an Allocator and uses that instance in all its member functions to allocate and deallocate memory and to construct and destroy objects in that memory (such objects may be container elements, nodes, or, for unordered containers, bucket arrays), except that std::basic_string specializations do not use the allocators for construction/destruction of their elements(since C++23).

The following rules apply to container construction:

- Copy constructors of AllocatorAwareContainers obtain their instances of the allocator by calling std::allocator_traits<allocator_type>::select_on_container_copy_construction on the allocator of the container being copied.
- Move constructors obtain their instances of allocators by move-constructing from the allocator belonging to the old container.
- All other constructors take a const allocator_type& parameter.

The only way to replace an allocator is copy-assignment, move-assignment, and swap:

- Copy-assignment will replace the allocator only if std::allocator_traits<allocator_type>::propagate_on_container_copy_assignment::value is true.
- Move-assignment will replace the allocator only if std::allocator_traits<allocator_type>::propagate_on_container_move_assignment::value is true.
- Swap will replace the allocator only if std::allocator_traits<allocator_type>::propagate_on_container_swap::value is true. Specifically, it will exchange the allocator instances through an unqualified call to the non-member function swap, see Swappable.

Note: The behavior of swapping two containers with unequal allocators if `propagate_on_container_swap` is false is undefined.

- The accessor `get_allocator()` obtains a copy of the allocator that was used to construct the container or installed by the most recent allocator replacement operation.

### Requirements

A type satisfies AllocatorAwareContainer if it satisfies Container and, given the following types and values, the semantic and complexity requirements in the tables below are satisfied:

|  |  |
| --- | --- |
| Type | Definition |
| `X` | an AllocatorAwareContainer type |
| `T` | the `value_type` of `X` |
| `A` | the allocator type used by `X` |
| Value | Definition |
| a, b | non-const lvalues of type `X` |
| c | an lvalue of type const X |
| t | an lvalue or a const rvalue of type `X` |
| rv | a non-const rvalue of type `X` |
| m | a value of type `A` |

#### Types

| Name | Type | Requirement |
| --- | --- | --- |
| typename X::allocator_type | `A` | `X::allocator_type::value_type` and `X::value_type` are the same. |

#### Statements

| Statement | Semantics | | Complexity |
| --- | --- | --- | --- |
| X u; X u = X(); | Precondition | `A` is DefaultConstructible. | Constant |
| Postcondition | u.empty() and u.get_allocator() == A() are both true. |
| X u(m); | Postcondition | u.empty() and u.get_allocator() == m are both true. | Constant |
| X u(t, m); | Precondition | `T` is CopyInsertable into `X`. | Linear |
| Postcondition | u == t and u.get_allocator() == m are both true. |
| X u(rv); | Postcondition | - u has the same elements as rv had before this construction. - The value of u.get_allocator() is the same as the value of rv.get_allocator() before this construction. | Constant |
| X u(rv, m); | Precondition | `T` is MoveInsertable into `X`. | - Constant if m == rv.get_allocator() is true. - Otherwise linear. |
| Postcondition | - u has the same elements, or copies of the elements, that rv had before this construction. - u.get_allocator() == m is true. |

#### Expressions

| Expression | Type | Semantics | | Complexity |
| --- | --- | --- | --- | --- |
| c.get_allocator() | `A` | No direct semantic requirement. | | Constant |
| a = t | `X&` | Precondition | `T` is CopyInsertable into `X` and CopyAssignable. | Linear |
| Postcondition | a == t is true. |
| a = rv | `X&` | Precondition | If the allocator will ****not**** be replaced by move-assignment (see above), then `T` is MoveInsertable into `X` and MoveAssignable. | Linear |
| Effect | All existing elements of a are either move assigned to or destroyed. |
| Postcondition | If a and rv do not refer the same object, a is equal to the value that rv had before the assignment. |
| a.swap(b) | void | Effect | Exchanges the contents of a and b. | Constant |

### Notes

AllocatorAwareContainers always call std::allocator_traits<A>::construct(m, p, args) to construct an object of type `T` at p using args, with m == get_allocator(). The default `construct` in std::allocator calls ::new((void\*)p) T(args)(until C++20)std::allocator has no `construct` member and std::construct_at(p, args) is called when constructing elements(since C++20), but specialized allocators may choose a different definition.

### Standard library

All standard library string types and containers (except std::array and std::inplace_vector) are AllocatorAwareContainers:

|  |  |
| --- | --- |
| basic_string | stores and manipulates sequences of characters   (class template) |
| deque | double-ended queue   (class template) |
| forward_list(C++11) | singly-linked list   (class template) |
| list | doubly-linked list   (class template) |
| vector | dynamic contiguous array   (class template) |
| map | collection of key-value pairs, sorted by keys, keys are unique   (class template) |
| multimap | collection of key-value pairs, sorted by keys   (class template) |
| set | collection of unique keys, sorted by keys   (class template) |
| multiset | collection of keys, sorted by keys   (class template) |
| unordered_map(C++11) | collection of key-value pairs, hashed by keys, keys are unique   (class template) |
| unordered_multimap(C++11) | collection of key-value pairs, hashed by keys   (class template) |
| unordered_set(C++11) | collection of unique keys, hashed by keys   (class template) |
| unordered_multiset(C++11) | collection of keys, hashed by keys   (class template) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2839 | C++11 | self move assignment of standard containers was not allowed | allowed but the result is unspecified |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/AllocatorAwareContainer&oldid=178187>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 December 2024, at 19:52.