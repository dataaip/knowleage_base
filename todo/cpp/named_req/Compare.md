# C++ named requirements: Compare

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | ****Compare**** | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

****Compare**** is a set of requirements expected by some of the standard library facilities from the user-provided function object types.

The return value of the function call operation applied to an object of a type satisfying Compare, when converted to bool, yields true if the first argument of the call appears before the second in the strict weak ordering relation induced by this type, and false otherwise.

As with any BinaryPredicate, evaluation of that expression is not allowed to call non-const functions through the dereferenced iterators and, syntactically, the function call operation must accept const object arguments, with the same behavior regardless of whether the arguments are const or non-const.

### Requirements

The type `T` satisfies Compare if

- The type `T` satisfies BinaryPredicate, and

Given

- `comp`, an object of type `T`,
- equiv(a, b), an expression-equivalent to !comp(a, b) && !comp(b, a).

The following expressions must be valid and have their specified effects:

| Expression | Return type | Requirements |
| --- | --- | --- |
| comp(a, b) | |  |  | | --- | --- | | meets BooleanTestable | (until C++20) | | models **boolean-testable** | (since C++20) | | Establishes strict weak ordering relation with the following properties:  - For all `a`, comp(a, a) == false. - If comp(a, b) == true then comp(b, a) == false. - if comp(a, b) == true and comp(b, c) == true then comp(a, c) == true. |
| equiv(a, b) | bool | Establishes equivalence relationship with the following properties:  - For all `a`, equiv(a, a) == true. - If equiv(a, b) == true, then equiv(b, a) == true. - If equiv(a, b) == true and equiv(b, c) == true, then equiv(a, c) == true. |

Note: `comp` induces a strict total ordering on the equivalence classes determined by `equiv`.

### Standard library

The following standard library facilities expect a Compare type.

|  |  |
| --- | --- |
| set | collection of unique keys, sorted by keys   (class template) |
| map | collection of key-value pairs, sorted by keys, keys are unique   (class template) |
| multiset | collection of keys, sorted by keys   (class template) |
| multimap | collection of key-value pairs, sorted by keys   (class template) |
| priority_queue | adapts a container to provide priority queue   (class template) |
| sort | sorts a range into ascending order   (function template) |
| sort | sorts the elements   (public member function of `std::forward_list<T,Allocator>`) |
| sort | sorts the elements   (public member function of `std::list<T,Allocator>`) |
| stable_sort | sorts a range of elements while preserving order between equal elements   (function template) |
| partial_sort | sorts the first N elements of a range   (function template) |
| partial_sort_copy | copies and partially sorts a range of elements   (function template) |
| is_sorted(C++11) | checks whether a range is sorted into ascending order   (function template) |
| is_sorted_until(C++11) | finds the largest sorted subrange   (function template) |
| nth_element | partially sorts the given range making sure that it is partitioned by the given element   (function template) |
| lower_bound | returns an iterator to the first element **not less** than the given value   (function template) |
| upper_bound | returns an iterator to the first element **greater** than a certain value   (function template) |
| binary_search | determines if an element exists in a partially-ordered range   (function template) |
| equal_range | returns range of elements matching a specific key   (function template) |
| merge | merges two sorted ranges   (function template) |
| merge | merges two sorted lists   (public member function of `std::forward_list<T,Allocator>`) |
| merge | merges two sorted lists   (public member function of `std::list<T,Allocator>`) |
| inplace_merge | merges two ordered ranges in-place   (function template) |
| includes | returns true if one sequence is a subsequence of another   (function template) |
| set_difference | computes the difference between two sets   (function template) |
| set_intersection | computes the intersection of two sets   (function template) |
| set_symmetric_difference | computes the symmetric difference between two sets   (function template) |
| set_union | computes the union of two sets   (function template) |
| push_heap | adds an element to a max heap   (function template) |
| pop_heap | removes the largest element from a max heap   (function template) |
| make_heap | creates a max heap out of a range of elements   (function template) |
| sort_heap | turns a max heap into a range of elements sorted in ascending order   (function template) |
| is_heap(C++11) | checks if the given range is a max heap   (function template) |
| is_heap_until(C++11) | finds the largest subrange that is a max heap   (function template) |
| max | returns the greater of the given values   (function template) |
| max_element | returns the largest element in a range   (function template) |
| min | returns the smaller of the given values   (function template) |
| min_element | returns the smallest element in a range   (function template) |
| minmax(C++11) | returns the smaller and larger of two elements   (function template) |
| minmax_element(C++11) | returns the smallest and the largest elements in a range   (function template) |
| lexicographical_compare | returns true if one range is lexicographically less than another   (function template) |
| next_permutation | generates the next greater lexicographic permutation of a range of elements   (function template) |
| prev_permutation | generates the next smaller lexicographic permutation of a range of elements   (function template) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2114 (P2167R3) | C++98 | contextual convertibility of return types to bool did not reflect the practice of implementations | requirements corrected |
| LWG 3031 | C++98 | requirements on const values were insufficent | requirements strengthened |

### See also

|  |  |
| --- | --- |
| strict_weak_order(C++20) | specifies that a `relation` imposes a strict weak ordering   (concept) |
| ****Comparison operators**** | `<`, `<=`, `>`, `>=`, `==`, `!=`, and `<=>` (C++20), compare the arguments |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/Compare&oldid=175974>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2024, at 07:54.