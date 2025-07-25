# C++ named requirements: Mutex (since C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | ****Mutex****(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | CharTraits | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

The ****Mutex**** requirements extends the Lockable requirements to include inter-thread synchronization.

### Requirements

- Lockable
- DefaultConstructible
- Destructible
- not copyable
- not movable

For an object `m` of Mutex type:

- The expression m.lock() has the following properties

:   - Behaves as an atomic operation.
    - Blocks the calling thread until exclusive ownership of the mutex can be obtained.
    - Prior m.unlock() operations on the same mutex **synchronize-with** this lock operation (equivalent to release-acquire std::memory_order).
    - The behavior is undefined if the calling thread already owns the mutex (except if m is std::recursive_mutex or std::recursive_timed_mutex).
    - Exception of type std::system_error may be thrown on errors, with the following error codes:

    :   - std::errc::operation_not_permitted if the calling thread does not have required privileges.
        - std::errc::resource_deadlock_would_occur if the implementation detects that this operation would lead to deadlock.

- The expression m.try_lock() has the following properties

:   - Behaves as an atomic operation.
    - Attempts to obtain exclusive ownership of the mutex for the calling thread without blocking. If ownership is not obtained, returns immediately. The function is allowed to spuriously fail and return even if the mutex is not currently owned by another thread.
    - If `try_lock()` succeeds, prior `unlock()` operations on the same object **synchronize-with** this operation (equivalent to release-acquire std::memory_order). `lock()` does not synchronize with a failed `try_lock()`.
    - Does not throw exceptions.

- The expression m.unlock() has the following properties

:   - Behaves as an atomic operation.
    - Releases the calling thread's ownership of the mutex and **synchronizes-with** the subsequent successful lock operations on the same object.
    - The behavior is undefined if the calling thread does not own the mutex.
    - Does not throw exceptions.

- All lock and unlock operations on a single mutex occur in a single total order that can be viewed as modification order of an atomic variable: the order is specific to this individual mutex.

### Standard library

The following standard library types satisfy Mutex requirements:

|  |  |
| --- | --- |
| mutex(C++11) | provides basic mutual exclusion facility   (class) |
| recursive_mutex(C++11) | provides mutual exclusion facility which can be locked recursively by the same thread   (class) |
| recursive_timed_mutex(C++11) | provides mutual exclusion facility which can be locked recursively by the same thread and implements locking with a timeout   (class) |
| shared_mutex(C++17) | provides shared mutual exclusion facility   (class) |
| shared_timed_mutex(C++14) | provides shared mutual exclusion facility and implements locking with a timeout   (class) |
| timed_mutex(C++11) | provides mutual exclusion facility which implements locking with a timeout   (class) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2309 | C++11 | `lock` might throw std::system_error with error code std::errc::device_or_resource_busy | not allowed |

### See also

- Thread support library
- Lockable
- TimedMutex
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/Mutex&oldid=177788>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 November 2024, at 11:49.