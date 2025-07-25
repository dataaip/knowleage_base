# C++ named requirements: CharTraits

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Basic | | | | | | DefaultConstructible | | | | | | MoveConstructible(C++11) | | | | | | CopyConstructible | | | | | | CopyAssignable | | | | | | MoveAssignable(C++11) | | | | | | Destructible | | | | | | Type properties | | | | | | ScalarType | | | | | | PODType | | | | | | TriviallyCopyable(C++11) | | | | | | TrivialType(C++11) | | | | | | StandardLayoutType(C++11) | | | | | | ImplicitLifetimeType | | | | | | Library-wide | | | | | | BooleanTestable | | | | | | EqualityComparable | | | | | | LessThanComparable | | | | | | Swappable | | | | | | ValueSwappable(C++11) | | | | | | NullablePointer(C++11) | | | | | | Hash(C++11) | | | | | | Allocator | | | | | | FunctionObject | | | | | | Callable | | | | | | Predicate | | | | | | BinaryPredicate | | | | | | Compare | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Container | | | | | | Container | | | | | | ReversibleContainer | | | | | | AllocatorAwareContainer | | | | | | SequenceContainer | | | | | | ContiguousContainer(C++17) | | | | | | AssociativeContainer | | | | | | UnorderedAssociativeContainer(C++11) | | | | | | Container element | | | | | | DefaultInsertable(C++11) | | | | | | CopyInsertable(C++11) | | | | | | MoveInsertable(C++11) | | | | | | EmplaceConstructible(C++11) | | | | | | Erasable(C++11) | | | | | | Iterator | | | | | | LegacyIterator | | | | | | LegacyInputIterator | | | | | | LegacyOutputIterator | | | | | | LegacyForwardIterator | | | | | | LegacyBidirectionalIterator | | | | | | LegacyRandomAccessIterator | | | | | | LegacyContiguousIterator(C++17) | | | | | | ConstexprIterator(C++20) | | | | | | Stream I/O | | | | | | FormattedInputFunction | | | | | | UnformattedInputFunction | | | | | | FormattedOutputFunction | | | | | | UnformattedOutputFunction | | | | | | Formatters | | | | | | BasicFormatter(C++20) | | | | | | Formatter(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Random Numbers | | | | | | SeedSequence(C++11) | | | | | | RandomNumberEngine(C++11) | | | | | | RandomNumberDistribution(C++11) | | | | | | UniformRandomBitGenerator(C++11) | | | | | | RandomNumberEngineAdaptor(C++11) | | | | | | Concurrency | | | | | | BasicLockable(C++11) | | | | | | Lockable(C++11) | | | | | | TimedLockable(C++11) | | | | | | SharedLockable(C++14) | | | | | | SharedTimedLockable(C++14) | | | | | | Mutex(C++11) | | | | | | TimedMutex(C++11) | | | | | | SharedMutex(C++17) | | | | | | SharedTimedMutex(C++14) | | | | | | Ranges | | | | | | RangeAdaptorObject(C++20) | | | | | | RangeAdaptorClosureObject(C++20) | | | | | | Multidimensional View | | | | | | LayoutMapping(C++23) | | | | | | LayoutMappingPolicy(C++23) | | | | | | AccessorPolicy(C++23) | | | | | | Other | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****CharTraits**** | | | | | | RegexTraits(C++11) | | | | | | BitmaskType | | | | | | LiteralType(C++11) | | | | | | NumericType | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | UnaryTypeTrait(C++11) | | | | | | BinaryTypeTrait(C++11) | | | | | | TransformationTrait(C++11) | | | | | | Clock(C++11) | | | | | | TrivialClock(C++11) | | | | | | |  | | | | | |

****CharTraits**** is a traits class that abstracts basic character and string operations for a given character type. Most standard library string and input/output classes require a CharTraits template type parameter alongside a corresponding character template type parameter.

### Requirements

No operation listed below on CharTraits may throw an exception.

Given

- `CharT`, a character type
- `X`, a CharTraits type for type `CharT`
- c, d, values of type `CharT`
- p, q, values of type const CharT\*
- s, a value of type `CharT*`
- n, i, j, values of type std::size_t
- e, f, values of type `X::int_type`
- pos, a value of type `X::pos_type`
- state, a value of type `X::state_type`
- r, an lvalue of type `CharT`

### Types

| Type | Semantics |
| --- | --- |
| `X::char_type` | `CharT` |
| `X::int_type` | A type that can hold all valid values of `X::char_type` plus X::eof() |
| `X::off_type` | Invokes implementation-defined behavior if not std::streamoff when `X` is used as the traits template parameter in input/output classes. |
| `X::pos_type` | - Functions in input/output classes returning this type use X::pos_type(X::off_type(-1)) as an invalid value to signal an error - Use of this invalid value as an argument to any std::istream, std::ostream or std::streambuf member taking a value of this type is undefined behavior - Invokes implementation-defined behavior if this type is not std::streampos when `X` is used as the traits template parameter in input/output classes |
| `X::state_type` | Destructible, CopyAssignable, CopyConstructible, DefaultConstructible |

### Expressions

| Expression | Return type | Semantics | Complexity |
| --- | --- | --- | --- |
| X::eq(c, d) | bool | Returns: whether c is to be treated as equal to d | Constant |
| X::lt(c, d) | bool | Returns: whether c is to be treated as less than d | Constant |
| X::compare(p, q, n) | int | Returns:  - ​0​ if for each i in `[`​0​`,`n`)`, X::eq(p[i], q[i]) is true - Else, a negative value if   - For some j in `[`​0​`,`n`)`, X::lt(p[j], q[j]) is true and   - For each i in `[`​0​`,`j`)`, X::eq(p[i], q[i]) is true - Else a positive value | Linear |
| X::length(p) | std::size_t | Returns: the smallest i such that X::eq(p[i], CharT()) is true | Linear |
| X::find(p, n, c) | const X::char_type\* | Returns:  - The smallest q in `[`p`,`p + n`)` such that X::eq(\*q, c) is true - ​0​ otherwise | Linear |
| X::move(s, p, n) | `X::char_type*` | - For each i in `[`​0​`,`n`)`, performs X::assign(s[i], p[i]) - Copies correctly even where the ranges `[`p`,`p + n`)` and `[`s`,`s + n`)` overlap - Returns: s | Linear |
| X::copy(s, p, n) | `X::char_type*` | - Requires: `[`p`,`p + n`)` and `[`s`,`s + n`)` do not overlap - Returns: s - For each i in `[`​0​`,`n`)`, performs X::assign(s[i], p[i]) | Linear |
| X::assign(r, d) | (Not used) | Assigns r = d | Constant |
| X::assign(s, n, c) | `X::char_type*` | - For each i in `[`​0​`,`n`)`, performs X::assign(s[i], c). - Returns: s | Linear |
| X::not_eof(e) | `X::int_type` | Returns:  - e if X::eq_int_type(e, X::eof()) is false - Otherwise a value f such that X::eq_int_type(f, X::eof()) is false | Constant |
| X::to_char_type(e) | `X::char_type` | Returns:  - If for some c, X::eq_int_type(e, X::to_int_type(c)) is true, c - Else some unspecified value | Constant |
| X::to_int_type(c) | `X::int_type` | Returns: some value e, constrained by the definitions of `X::to_char_type` and `X::eq_int_type` | Constant |
| X::eq_int_type(e, f) | bool | - For all c and d, X::eq(c, d) is equal to X::eq_int_type(X::to_int_type(c),                X::to_int_type(d)) - Returns:   - Yields X::eq(c, d) if for some c and d, e == X::to_int_type(c) and f == X::to_int_type(d)   - Otherwise, yields true if e and f are both copies of X::eof()   - Otherwise, yields false if one of e and f is a copy of X::eof() and the other is not   - Otherwise the value is unspecified | Constant |
| X::eof() | `X::int_type` | Returns: a value e such that X::eq_int_type(e, X::to_int_type(c)) is false for all values c | Constant |

### Standard library

CharTraits is required by the following standard library class templates as a template type parameter:

|  |  |
| --- | --- |
| Strings | |
| basic_string | stores and manipulates sequences of characters   (class template) |
| basic_string_view(C++17) | read-only string view   (class template) |
| Streams | |
| basic_ios | manages an arbitrary stream buffer   (class template) |
| basic_istream | wraps a given abstract device (std::basic_streambuf) and provides high-level input interface   (class template) |
| basic_ifstream | implements high-level file stream input operations   (class template) |
| basic_istringstream | implements high-level string stream input operations   (class template) |
| basic_ispanstream(C++23) | implements fixed character buffer input operations   (class template) |
| basic_ostream | wraps a given abstract device (std::basic_streambuf) and provides high-level output interface   (class template) |
| basic_ofstream | implements high-level file stream output operations   (class template) |
| basic_ostringstream | implements high-level string stream output operations   (class template) |
| basic_osyncstream(C++20) | synchronized output stream wrapper   (class template) |
| basic_ospanstream(C++23) | implements fixed character buffer output operations   (class template) |
| basic_iostream | wraps a given abstract device (std::basic_streambuf) and provides high-level input/output interface   (class template) |
| basic_fstream | implements high-level file stream input/output operations   (class template) |
| basic_stringstream | implements high-level string stream input/output operations   (class template) |
| basic_spanstream(C++23) | implements fixed character buffer input/output operations   (class template) |
| Stream iterators | |
| istream_iterator | input iterator that reads from std::basic_istream   (class template) |
| ostream_iterator | output iterator that writes to std::basic_ostream   (class template) |
| Stream buffers | |
| basic_streambuf | abstracts a raw device   (class template) |
| basic_filebuf | implements raw file device   (class template) |
| basic_stringbuf | implements raw string device   (class template) |
| basic_syncbuf(C++20) | synchronized output device wrapper   (class template) |
| basic_spanbuf(C++23) | implements raw fixed character buffer device   (class template) |
| Stream buffer iterators | |
| istreambuf_iterator | input iterator that reads from std::basic_streambuf   (class template) |
| ostreambuf_iterator | output iterator that writes to std::basic_streambuf   (class template) |

CharTraits is satisfied by the following standard library explicit specializations of std::char_traits:

|  |  |  |
| --- | --- | --- |
| template<> class char_traits<char>;  template<> class char_traits<wchar_t>;  template<> class char_traits<char8_t>;  template<> class char_traits<char16_t>; template<> class char_traits<char32_t>; |  | (since C++20) (since C++11) (since C++11) |
|  |  |  |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 335 | C++98 | the requirements on the binary overload of `assign` did not prevent assignments to rvalues | its first argument can only be an lvalue |
| LWG 352 | C++98 | `X::state_type` was only required to be CopyConstructible | it is also required to be CopyAssignable and DefaultConstructible |
| LWG 3085 | C++98 | X::copy(s, p, n) only required p not in `[`s`,`s + n`)`, which is too weak[[1]](CharTraits.html#cite_note-1) | requires ``p`,`p + n`)` and `[`s`,`s + n`)` not to overlap |

1. [↑ ``p`,`p + n`)` and `[`s`,`s + n`)` can overlap, using [std::memcpy to implement `X::copy` results in undefined behavior in this case.
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/named_req/CharTraits&oldid=158844>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 21:56.