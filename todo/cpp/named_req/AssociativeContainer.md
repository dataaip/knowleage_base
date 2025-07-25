# C++ named requirements: AssociativeContainer

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | ****AssociativeContainer**** | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

An ****AssociativeContainer**** is an ordered Container that provides fast lookup of objects based on keys.

An associative container supports **unique keys** if it may contain at most one element for each key. Otherwise, it supports **equivalent keys**.

### Requirements

|  |  |
| --- | --- |
| Legend | |
| `X` | An associative container class |
| `T` | The element type of `X` |
| `A` | The allocator type of `X`: `X::allocator_type` if it exists, otherwise std::allocator<X::value_type> |
| a | A value of type `X` |
| a2 | A value of a type `Y` whose node handles are compatible with `X` |
| b | A value of type `X` or const X |
| u | A name of a variable beging declared |
| a_uniq | A value of type `X` when `X` supports unique keys |
| a_eq | A value of type `X` when `X` supports equivalent keys |
| a_tran | A value of type `X` or const X when type `X::key_compare::is_transparent` exists |
| i, j | The LegacyInputIterators referring to elements implicitly convertible to `X::value_type` |
| ``i`,`j`)` | A valid range |
| rg (since C++23) | A value of a type `R` that models [**container-compatible-range**`<value_type>` |
| p | A valid constant iterator to a |
| q | A valid dereferenceable constant iterator to a |
| r | A valid dereferenceable iterator to a |
| q1, q2 | A valid range of const iterators in a |
| il | An object of type std::initializer_list<X::value_type> |
| t | A value of type `X::value_type` |
| k | A value of type `X::key_type` |
| c | A value of type `X::key_compare` or const X::key_compare |
| kl | A value such that a is partitioned with respect to c(x, kl), with x the key value of e and e in a |
| ku | A value such that a is partitioned with respect to !c(ku, x), with x the key value of e and e in a |
| ke | A value such that a is partitioned with respect to c(x, ke) and !c(ke, x), with c(x, ke) implying !c(ke, x) and with x the key value of e and e in a |
| kx (since C++23) | A value such that:  - a is partitioned with respect to c(x, kx) and !c(kx, x), with c(x, kx) implying !c(kx, x) and with x the key value of e and e in a, and - kx is not convertible to either `X::iterator` or `X::const_iterator` |
| m | An allocator of a type convertible to `A` |
| nh | A non-const rvalue of type `X::node_type` |

The type `X` satisfies AssociativeContainer if

- The type `X` satisfies Container(until C++11)AllocatorAwareContainer(since C++11),
- Is parameterized on `Key` and an ordering relation `Compare` that induces a strict weak ordering on elements of `Key`, and
  - In addition, std::map and std::multimap associate an arbitrary **mapped type** `T` with the `Key`.
  - The object of type `Compare` is called the **comparison object** of a container of type `X`.
- The following expressions must be valid and have their specified effects for all associative containers:

#### Types

| Name | Type | Requirements |
| --- | --- | --- |
| `key_type` | `Key` |  |
| `mapped_type` | `T` (for std::map and std::multimap only) |  |
| `value_type` | - `Key` (for std::set and std::multiset only) - std::pair<const Key, T>(for std::map and std::multimap only) | Erasable from `X` |
| `key_compare` | `Compare` | CopyConstructible |
| `value_compare` | - same as `key_compare` (for std::set and std::multiset) - an ordering relation on pairs induced by the first component (i.e. `Key`) (for std::map and std::multimap) | BinaryPredicate |
| `node_type` | A specialization of the node-handle class template, such that the public nested types are the same types as the corresponding types in `X`. |  |

#### Member functions and operators

| Expression | Result | Preconditions | Effects | Returns | Complexity |
| --- | --- | --- | --- | --- | --- |
| X(c) |  |  | Constructs an empty container. Uses a copy of c as a comparison object |  | Constant |
| X u = X(); X u; |  | `key_compare` meets the DefaultConstructible requirements | Constructs an empty container. Uses Compare() as a comparison object |  | Constant |
| X(i, j, c) |  | `value_type` is EmplaceConstructible into `X` from \*i | Constructs an empty container and inserts elements from the range ``i`,`j`)` into it; uses c as a comparison object |  | N·log(N) in general, where `N` has the value [std::distance(i, j); linear if ``i`,`j`)` is sorted with respect to value_comp() |
| X(i, j) |  | `key_compare` meets the [DefaultConstructible requirements. `value_type` is EmplaceConstructible into `X` from \*i | Constructs an empty container and inserts elements from the range ``i`,`j`)` into it; uses Compare() as a comparison object |  |
| X(from_range, rg, c) (since C++23) |  | `value_type` is [EmplaceConstructible into `X` from \*ranges::begin(rg) | Constructs an empty container and inserts each element from rg into it. Uses c as the comparison object |  | N·log(N) in general, where `N` has the value ranges::distance(rg); linear if rg is sorted with respect to value_comp() |
| X(from_range, rg) (since C++23) |  | `key_compare` meets the DefaultConstructible requirements. `value_type` is EmplaceConstructible into `X` from \*ranges::begin(rg) | Constructs an empty container and inserts each element from rg into it. Uses Compare() as the comparison object |  |
| X(il, c) |  |  | X(il.begin(), il.end(), c) |  |  |
| X(il) |  |  | X(il.begin(), il.end()) |  |  |
| a = il | X& | `value_type` is CopyInsertable into `X` and CopyAssignable | Assigns the range ``il.begin()`,`il.end()`)` into a. All existing elements of a are either assigned to or destroyed |  | N·log(N) in general, where `N` has the value il.size() + a.size(); linear if `[`il.begin()`,`il.end()`)` is sorted with respect to value_comp() |
| b.key_comp() | `X::key_compare` |  |  | The comparison object out of which b was constructed | Constant |
| b.value_comp() | `X::value_compare` |  |  | An object of `value_compare` constructed out of the comparison object | Constant |
| a_uniq.emplace(args) | [std::pair<   iterator,   bool> | `value_type` is EmplaceConstructible into `X` from args | Inserts a `value_type` object t constructed with std::forward<Args>(args)... if and only if there is no element in the container with key equivalent to the key of t | The bool component of the returned pair is true if and only if the insertion takes place, and the iterator component of the pair points to the element with key equivalent to the key of t | Logarithmic |
| a_eq.emplace(args) | `iterator` | `value_type` is EmplaceConstructible into `X` from args | Inserts a `value_type` object t constructed with std::forward<Args>(args).... If a range containing elements equivalent to t exists in a_eq, t is inserted at the end of that range | An iterator pointing to the newly inserted element | Logarithmic |
| a.emplace_hint(p, args) | `iterator` |  | Equivalent to a.emplace(   std::forward<Args>(args)...), except that the element is inserted as close as possible to the position just prior to p | An iterator pointing to the element with the key equivalent to the newly inserted element | Logarithmic in general, but amortized constant if the element is inserted right before p |
| a_uniq.insert(t) | std::pair<   iterator,   bool> | If t is a non-const rvalue, `value_type` is MoveInsertable into `X`; otherwise, `value_type` is CopyInsertable into `X` | Inserts t if and only if there is no element in the container with key equivalent to the key of t | The bool component of the returned pair is true if and only if the insertion takes place, and the `iterator` component of the pair points to the element with key equivalent to the key of t | Logarithmic |
| a_eq.insert(t) | `iterator` | If t is a non-const rvalue, `value_type` is MoveInsertable into `X`; otherwise, `value_type` is CopyInsertable into `X` | Inserts t and returns the iterator pointing to the newly inserted element. If a range containing elements equivalent to t exists in a_eq, t is inserted at the end of that range |  | Logarithmic |
| a.insert(p, t) | `iterator` | If t is a non-const rvalue, `value_type` is MoveInsertable into `X`; otherwise, `value_type` is CopyInsertable into `X` | Inserts t if and only if there is no element with key equivalent to the key of t in containers with unique keys; always inserts t in containers with equivalent keys. t is inserted as close as possible to the position just prior to p | An iterator pointing to the element with key equivalent to the key of t | Logarithmic in general, but amortized constant if t is inserted right before p |
| a.insert(i, j) | void | `value_type` is EmplaceConstructible into `X` from \*i. Neither i nor j are iterators into a | Inserts each element from the range ``i`,`j`)` if and only if there is no element with key equivalent to the key of that element in containers with unique keys; always inserts that element in containers with equivalent keys |  | N·log(a.size() + N), where `N` has the value [std::distance(i, j) |
| a.insert_range(rg) (since C++23) | void | `value_type` is EmplaceConstructible into `X` from \*ranges::begin(rg). rg and a do not overlap | Inserts each element from rg if and only if there is no element with key equivalent to the key of that element in containers with unique keys; always inserts that element in containers with equivalent keys |  | N·log(a.size() + N), where `N` has the value ranges::distance(rg) |
| a.insert(il) |  |  | a.insert(il.begin(), il.end()) |  |  |
| a_uniq.insert(nh) | `insert_return_type` | nh is empty or a_uniq.get_allocator() == nh.get_allocator() is true | If nh is empty, has no effect. Otherwise, inserts the element owned by nh if and only if there is no element in the container with a key equivalent to nh.key() | If nh is empty, `inserted` is false, `position` is end(), and `node` is empty. Otherwise if the insertion took place, `inserted` is true, `position` points to the inserted element, and `node` is empty; if the insertion failed, `inserted` is false, `node` has the previous value of nh, and `position` points to an element with a key equivalent to nh.key() | Logarithmic |
| a_eq.insert(nh) | `iterator` | nh is empty or a_eq.get_allocator() == nh.get_allocator() is true | If nh is empty, has no effect and returns a_eq.end(). Otherwise, inserts the element owned by nh and returns an iterator pointing to the newly inserted element. If a range containing elements with keys equivalent to nh.key() exists in a_eq, the element is inserted at the end of that range. Ensures: nh is empty |  | Logarithmic |
| a.insert(p, nh) | `iterator` | nh is empty or a.get_allocator() == nh.get_allocator() is true | If nh is empty, has no effect and returns a.end(). Otherwise, inserts the element owned by nh if and only if there is no element with key equivalent to nh.key() in containers with unique keys; always inserts the element owned by nh in containers with equivalent keys. The element is inserted as close as possible to the position just prior to p. Ensures: nh is empty if insertion succeeds, unchanged if insertion fails | An iterator pointing to the element with key equivalent to nh.key() | Logarithmic in general, but amortized constant if the element is inserted right before p |
| a.extract(k) | `node_type` |  | Removes the first element in the container with key equivalent to k | A `node_type` owning the element if found, otherwise an empty `node_type` | log(a.size()) |
| a_tran.extract(kx) (since C++23) | `node_type` |  | Removes the first element in the container with key r such that !c(r, kx) && !c(kx, r) is true | A `node_type` owning the element if found, otherwise an empty `node_type` | log(a_tran.size()) |
| a.extract(q) | `node_type` |  | Removes the element pointed to by q | A `node_type` owning that element | Amortized constant |
| a.merge(a2) | void | a.get_allocator() == a2.get_allocator() | Attempts to extract each element in a2 and insert it into a using the comparison object of a. In containers with unique keys, if there is an element in a with key equivalent to the key of an element from a2, then that element is not extracted from a2. Ensures: Pointers and references to the transferred elements of a2 refer to those same elements but as members of a. Iterators referring to the transferred elements will continue to refer to their elements, but they now behave as iterators into a, not into a2. Throws: Nothing unless the comparison object throws |  | N·log(a.size() + N), where `N` has the value a2.size() |
| a.erase(k) | `size_type` |  | Erases all elements in the container with key equivalent to k | The number of erased elements | log(a.size()) + a.count(k) |
| a_tran.erase(kx) (since C++23) | `size_type` |  | Erases all elements in the container with key r such that !c(r, kx) && !c(kx, r) is true | The number of erased elements | log(a_tran.size()) + a_tran.count(kx) |
| a.erase(q) | `iterator` |  | Erases the element pointed to by q | An iterator pointing to the element immediately following q prior to the element being erased. If no such element exists, returns a.end() | Amortized constant |
| a.erase(r) | `iterator` |  | Erases the element pointed to by r | An iterator pointing to the element immediately following r prior to the element being erased. If no such element exists, returns a.end() | Amortized constant |
| a.erase(q1, q2) | `iterator` |  | Erases all the elements in the range ``q1`,`q2`)` | An iterator pointing to the element pointed to by q2 prior to any elements being erased. If no such element exists, a.end() is returned | log(a.size()) + N, where `N` has the value [std::distance(q1, q2) |
| a.clear() |  |  | a.erase(a.begin(), a.end()). Ensures: a.empty() is true |  | Linear in a.size() |
| b.find(k) | `iterator`; `const_iterator` for constant b |  |  | An iterator pointing to an element with the key equivalent to k, or b.end() if such an element is not found | Logarithmic |
| a_tran.find(ke) | `iterator`; `const_iterator` for constant a_tran |  |  | An iterator pointing to an element with key r such that !c(r, ke) && !c(ke, r) is true, or a_tran.end() if such an element is not found | Logarithmic |
| b.count(k) | `size_type` |  |  | The number of elements with key equivalent to k | log(b.size()) + b.count(k) |
| a_tran.count(ke) | `size_type` |  |  | The number of elements with key r such that !c(r, ke) && !c(ke, r) | log(a_tran.size()) + a_tran.count(ke) |
| b.contains(k) | bool |  | return b.find(k) != b.end(); |  |  |
| a_tran.contains(ke) | bool |  | return   a_tran.find(ke) !=   a_tran.end(); |  |  |
| b.lower_bound(k) | `iterator`; `const_iterator` for constant b |  |  | An iterator pointing to the first element with key not less than k, or b.end() if such an element is not found | Logarithmic |
| a_tran.lower_bound(kl) | `iterator`; `const_iterator` for constant a_tran |  |  | An iterator pointing to the first element with key r such that !c(r, kl), or a_tran.end() if such an element is not found | Logarithmic |
| b.upper_bound(k) | `iterator`; `const_iterator` for constant b |  |  | An iterator pointing to the first element with key greater than k, or b.end() if such an element is not found | Logarithmic |
| a_tran.upper_bound(ku) | `iterator`; `const_iterator` for constant a_tran |  |  | An iterator pointing to the first element with key r such that c(ku, r), or a_tran.end() if such an element is not found | Logarithmic |
| b.equal_range(k) | std::pair<   iterator,   iterator>; std::pair<   const_iterator,   const_iterator> for constant b |  | Equivalent to: return   std::make_pair(     b.lower_bound(k),     b.upper_bound(k)); |  | Logarithmic |
| a_tran.equal_range(ke) | std::pair<   iterator,   iterator>; std::pair<   const_iterator,   const_iterator> for constant a_tran |  | Equivalent to: return   std::make_pair(     a_tran.lower_bound(ke),     a_tran.upper_bound(ke)); |  | Logarithmic |

#### Iterators

Iterators of associative containers satisfy the requirements of LegacyBidirectionalIterator.

For associative containers where `value_type` is the same as `key_type`, both `iterator` and `const_iterator` are constant iterators. It is unspecified whether or not `iterator` and `const_iterator` are the same type.

Iterators of associative containers iterate through the containers in the non-descending order of keys where non-descending is defined by the comparison that was used to construct the containers. That is, given

- a, an associative container
- i and j, dereferenceable iterators to a.

If the distance from i to j is positive, then a.value_comp()(\*j, \*i) == false. Additionally, if a is an associative container with unique keys, the stronger condition a.value_comp()(\*i, \*j) != false holds.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Finish requirements. |

### Standard library

The following standard library containers satisfy the AssociativeContainer requirements:

|  |  |
| --- | --- |
| set | collection of unique keys, sorted by keys   (class template) |
| multiset | collection of keys, sorted by keys   (class template) |
| map | collection of key-value pairs, sorted by keys, keys are unique   (class template) |
| multimap | collection of key-value pairs, sorted by keys   (class template) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 354 | C++98 | `lower_bound` and `upper_bound` did not return the end iterator if no element is found | they return the end iterator in this case |
| LWG 589 | C++98 | the elements that i and j refer to had the type `X::value_type` | the elements are implicitly convertible to `X::value_type` |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/AssociativeContainer&oldid=177963>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 November 2024, at 14:17.