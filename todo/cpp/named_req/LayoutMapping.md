# C++ named requirements: LayoutMapping (since C++23)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | ****LayoutMapping****(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

****LayoutMapping**** controls the mapping of a multidimensional index to a one-dimensional offset to data handle in std::mdspan.

### Requirements

A type `M` satisfies LayoutMapping if it models `copyable` and `equality_comparable`, and the following are true:

- std::is_nothrow_move_constructible_v<M>
- std::is_nothrow_move_assignable_v<M>
- std::is_nothrow_swappable_v<M>

And, given the following types and values, the expressions shown in the table below are valid and have the indicated semantics:

#### Legend

|  |  |
| --- | --- |
| Type | Definition |
| `M` | a layout mapping class |
| Value | Definition |
| m | a value of type (possibly const-qualified) `M` |
| i, j | packs of (possibly const-qualified) integers that are multidimensional indices in m.extents() |
| r | a (possibly const-qualified) rank index of typename M​::​extents_type |
| d_r | a pack of (possibly const-qualified) integers for which sizeof...(d_r) == M​::​extents_type​::​rank() is true, the element at rank index r is equal to 1, and all other elements are equal to ​0​ |

#### Member types

| Name | Type | Requirements |
| --- | --- | --- |
| `M::extents_type` | Specialization of class template std::extents |  |
| `M::index_type` | typename M::extents_type::index_type |  |
| `M::rank_type` | typename M::extents_type::rank_type |  |
| `M::layout_type` | Layout mapping policy `MP` where typename MP::template mapping<E> is `M` for some extents type `E` | LayoutMappingPolicy for which `M` is mapping type of `MP` |

#### Member functions and operators

| Expression | Return type | Semantics |
| --- | --- | --- |
| m.extents() | const typename M​::​extents_type& | Returns constant reference to associated multidimensional index space |
| m(i...) | typename M​::​index_type | - Returns a nonnegative integer o such that o < std::numeric_limits<typename M​::​index_type>​::​max() and o <= std::numeric_limits<std::size_t>​::​max() are both true. - Such expression is equivalent to m(static_cast<typename M::index_type>(i)...). |
| m.required_span_size() | typename M​::​index_type | - Returns 1 plus the maximum value of m(i...) for all i if the size of the multidimensional index space m.extents() is not 0. - Otherwise, returns ​0​. |
| m.is_unique() | bool | Returns true only if for every i and j where (i != j || ...) is true, m(i...) != m(j...) is true. [[note 1]](LayoutMapping.html#cite_note-1) |
| m.is_exhaustive() | bool | Returns true only if for all k in the range `[`​0​`,`m.required_span_size()`)`, there exists an i such that m(i...) equals k. [[note 2]](LayoutMapping.html#cite_note-2) |
| m.is_strided() | bool | Returns true only if for every rank index r of m.extents(), there exists an integer s_r such that, for all i where (i + d_r) is a multidimensional index in m.extents(), m((i + d_r)...) - m(i...) equals s_r. [[note 3]](LayoutMapping.html#cite_note-3) |
| m.stride(r) | typename M​::​index_type | - The precondition is that m.is_strided() is true. - Returns a stride s_r at rank index r as defined in m.is_strided() above. |
| M::is_always_unique() | bool | - Returns true only if m.is_unique() is true for all possible objects m of type `M`. [[note 4]](LayoutMapping.html#cite_note-4) - The return value is always a constant expression. |
| M::is_always_exhaustive() | bool | - Returns true only if m.is_exhaustive() is true for all possible objects m of type `M`. [[note 5]](LayoutMapping.html#cite_note-5) - The return value is always a constant expression. |
| M::is_always_strided() | bool | - Returns true only if m.is_strided() is true for all possible objects m of type `M`. [[note 6]](LayoutMapping.html#cite_note-6) - The return value is always a constant expression. |

1. ↑ A mapping can return false even if the condition is met. For certain layouts, it is possibly not feasible to determine efficiently whether the layout is unique.
2. ↑ Same as above, but in the case of exhaustive layouts.
3. ↑ Same as above, but in the case of strided layouts.
4. ↑ A mapping can return false even if the condition is met. For certain layout mappings, it is possibly not feasible to determine whether every instance is unique.
5. ↑ Same as above, but in the case of exhaustive instances.
6. ↑ Same as above, but in the case of strided instances.

### Concept

For the constraints uses under std::layout_stride::mapping, the following exposition-only concept is defined.

|  |  |  |
| --- | --- | --- |
| template< class M >  concept /\*layout-mapping-alike\*/ = requires   {      requires /\*is-extents\*/<typename M::extents_type>;      { M::is_always_strided() }    -> std::same_as<bool>;      { M::is_always_exhaustive() } -> std::same_as<bool>;      { M::is_always_unique() }     -> std::same_as<bool>;      std::bool_constant<M::is_always_strided()>::value;      std::bool_constant<M::is_always_exhaustive()>::value;      std::bool_constant<M::is_always_unique()>::value; }; |  | (exposition only\*) |
|  |  |  |

Defines the minimal usability constraints of the LayoutMapping requirement. This concept checks that the predicate mapping trait functions above exist, are constant expressions, and have a return type of bool.

/\*is-extents\*/<E> is true if and only if `E` is a specialization of std::extents.

### Standard library

The following standard library types satisfy LayoutMapping requirements:

|  |  |
| --- | --- |
| mapping | a layout mapping of layout_left (public member class template of `std::layout_left`) |
| mapping | a layout mapping of layout_right (public member class template of `std::layout_right`) |
| mapping | a layout mapping of layout_stride (public member class template of `std::layout_stride`) |
| mapping") | a layout mapping of layout_left_padded (public member class template of `std::layout_left_padded<PaddingValue>`) |
| mapping") | a layout mapping of layout_right_padded (public member class template of `std::layout_right_padded<PaddingValue>`) |

### See also

- LayoutMappingPolicy
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/LayoutMapping&oldid=178868>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 December 2024, at 06:41.