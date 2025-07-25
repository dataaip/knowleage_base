# Standard library header <iterator>

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | ****<iterator>**** | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the iterator library.

|  |  |
| --- | --- |
| This header is a partial freestanding header. Everything inside this header is freestanding beside stream iterators. | (since C++23) |

|  |  |
| --- | --- |
| Concepts | |
| Iterator concepts | |
| indirectly_readable(C++20) | specifies that a type is indirectly readable by applying operator `*`   (concept) |
| indirectly_writable(C++20) | specifies that a value can be written to an iterator's referenced object   (concept) |
| weakly_incrementable(C++20) | specifies that a `semiregular` type can be incremented with pre- and post-increment operators   (concept) |
| incrementable(C++20) | specifies that the increment operation on a `weakly_incrementable` type is equality-preserving and that the type is `equality_comparable`   (concept) |
| input_or_output_iterator(C++20) | specifies that objects of a type can be incremented and dereferenced   (concept) |
| sentinel_for(C++20) | specifies a type is a sentinel for an `input_or_output_iterator` type   (concept) |
| sized_sentinel_for(C++20) | specifies that the - operator can be applied to an iterator and a sentinel to calculate their difference in constant time   (concept) |
| input_iterator(C++20) | specifies that a type is an input iterator, that is, its referenced values can be read and it can be both pre- and post-incremented   (concept) |
| output_iterator(C++20) | specifies that a type is an output iterator for a given value type, that is, values of that type can be written to it and it can be both pre- and post-incremented   (concept) |
| forward_iterator(C++20) | specifies that an `input_iterator` is a forward iterator, supporting equality comparison and multi-pass   (concept) |
| bidirectional_iterator(C++20) | specifies that a `forward_iterator` is a bidirectional iterator, supporting movement backwards   (concept) |
| random_access_iterator(C++20) | specifies that a `bidirectional_iterator` is a random-access iterator, supporting advancement in constant time and subscripting   (concept) |
| contiguous_iterator(C++20) | specifies that a `random_access_iterator` is a contiguous iterator, referring to elements that are contiguous in memory   (concept) |
| Indirect callable concepts | |
| indirectly_unary_invocableindirectly_regular_unary_invocable(C++20)(C++20) | specifies that a callable type can be invoked with the result of dereferencing an `indirectly_readable` type   (concept) |
| indirect_unary_predicate(C++20) | specifies that a callable type, when invoked with the result of dereferencing an `indirectly_readable` type, satisfies `predicate`   (concept) |
| indirect_binary_predicate(C++20) | specifies that a callable type, when invoked with the result of dereferencing two `indirectly_readable` types, satisfies `predicate`   (concept) |
| indirect_equivalence_relation(C++20) | specifies that a callable type, when invoked with the result of dereferencing two `indirectly_readable` types, satisfies `equivalence_relation`   (concept) |
| indirect_strict_weak_order(C++20) | specifies that a callable type, when invoked with the result of dereferencing two `indirectly_readable` types, satisfies `strict_weak_order`   (concept) |
| Common algorithm requirements | |
| indirectly_movable(C++20) | specifies that values may be moved from an `indirectly_readable` type to an `indirectly_writable` type   (concept) |
| indirectly_movable_storable(C++20) | specifies that values may be moved from an `indirectly_readable` type to an `indirectly_writable` type and that the move may be performed via an intermediate object   (concept) |
| indirectly_copyable(C++20) | specifies that values may be copied from an `indirectly_readable` type to an `indirectly_writable` type   (concept) |
| indirectly_copyable_storable(C++20) | specifies that values may be copied from an `indirectly_readable` type to an `indirectly_writable` type and that the copy may be performed via an intermediate object   (concept) |
| indirectly_swappable(C++20) | specifies that the values referenced by two `indirectly_readable` types can be swapped   (concept) |
| indirectly_comparable(C++20) | specifies that the values referenced by two `indirectly_readable` types can be compared   (concept) |
| permutable(C++20) | specifies the common requirements of algorithms that reorder elements in place   (concept) |
| mergeable(C++20) | specifies the requirements of algorithms that merge sorted sequences into an output sequence by copying elements   (concept) |
| sortable(C++20) | specifies the common requirements of algorithms that permute sequences into ordered sequences   (concept) |
| Classes | |
| Algorithm utilities | |
| indirect_result_t(C++20) | computes the result of invoking a callable object on the result of dereferencing some set of `indirectly_readable` types (alias template) |
| projected(C++20) | helper template for specifying the constraints on algorithms that accept projections   (class template) |
| projected_value_t(C++26) | computes the value type of an `indirectly_readable` type by projection (alias template) |
| Associated types | |
| incrementable_traits(C++20) | computes the difference type of a `weakly_incrementable` type   (class template) |
| indirectly_readable_traits(C++20) | computes the value type of an `indirectly_readable` type   (class template) |
| iter_value_titer_reference_titer_const_reference_titer_difference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++23)(C++20)(C++20)(C++20) | computes the associated types of an iterator (alias template) |
| Primitives | |
| iterator_traits | provides uniform interface to the properties of an iterator   (class template) |
| input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | empty class types used to indicate iterator categories   (class) |
| iterator(deprecated in C++17) | base class to ease the definition of required types for simple iterators   (class template) |
| Adaptors | |
| reverse_iterator | iterator adaptor for reverse-order traversal   (class template) |
| move_iterator(C++11) | iterator adaptor which dereferences to an rvalue   (class template) |
| move_sentinel(C++20) | sentinel adaptor for std::move_iterator   (class template) |
| basic_const_iterator(C++23) | iterator adaptor that converts an iterator into a constant iterator   (class template) |
| const_iterator(C++23) | computes a constant iterator type for a given type (alias template) |
| const_sentinel(C++23) | computes a sentinel type to be used with constant iterators (alias template) |
| common_iterator(C++20) | adapts an iterator type and its sentinel into a common iterator type   (class template) |
| default_sentinel_t(C++20) | default sentinel for use with iterators that know the bound of their range   (class) |
| counted_iterator(C++20) | iterator adaptor that tracks the distance to the end of the range   (class template) |
| unreachable_sentinel_t(C++20) | sentinel that always compares unequal to any `weakly_incrementable` type   (class) |
| back_insert_iterator | iterator adaptor for insertion at the end of a container   (class template) |
| front_insert_iterator | iterator adaptor for insertion at the front of a container   (class template) |
| insert_iterator | iterator adaptor for insertion into a container   (class template) |
| Stream Iterators | |
| istream_iterator | input iterator that reads from std::basic_istream   (class template) |
| ostream_iterator | output iterator that writes to std::basic_ostream   (class template) |
| istreambuf_iterator | input iterator that reads from std::basic_streambuf   (class template) |
| ostreambuf_iterator | output iterator that writes to std::basic_streambuf   (class template) |
| Customization point objects | |
| Defined in namespace `std::ranges` | |
| iter_move(C++20) | casts the result of dereferencing an object to its associated rvalue reference type (customization point object) |
| iter_swap(C++20) | swaps the values referenced by two dereferenceable objects (customization point object) |
| Constants | |
| unreachable_sentinel(C++20) | an object of type `unreachable_sentinel_t` that always compares unequal to any `weakly_incrementable` type   (constant) |
| default_sentinel(C++20) | an object of type `default_sentinel_t` used with iterators that know the bound of their range   (constant) |
| Functions | |
| Adaptors | |
| make_reverse_iterator(C++14) | creates a std::reverse_iterator of type inferred from the argument   (function template) |
| make_move_iterator(C++11) | creates a std::move_iterator of type inferred from the argument   (function template) |
| make_const_iterator(C++23) | creates a std::const_iterator of type inferred from the argument   (function template) |
| make_const_sentinel(C++23) | creates a std::const_sentinel of type inferred from the argument   (function template) |
| front_inserter | creates a std::front_insert_iterator of type inferred from the argument   (function template) |
| back_inserter | creates a std::back_insert_iterator of type inferred from the argument   (function template) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |
| Non-member operators | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(C++11)(C++11)(C++11)(C++20) | compares the underlying iterators   (function template) |
| operator+(C++11) | advances the iterator   (function template) |
| operator-(C++11) | computes the distance between two iterator adaptors   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | compares the underlying iterators   (function template) |
| operator+ | advances the iterator   (function template) |
| operator- | computes the distance between two iterator adaptors   (function template) |
| operator==operator<=>(C++20) | compares the distances to the end   (function template) |
| operator+(C++20) | advances the iterator   (function template) |
| operator-(C++20) | computes the distance between two iterator adaptors   (function template) |
| operator==operator!=(removed in C++20) | compares two `istream_iterator`s   (function template) |
| operator==operator!=(removed in C++20) | compares two `istreambuf_iterator`s   (function template) |
| Operations | |
| advance | advances an iterator by given distance   (function template) |
| distance | returns the distance between two iterators   (function template) |
| next(C++11) | increment an iterator   (function template) |
| prev(C++11) | decrement an iterator   (function template) |
| ranges::advance(C++20) | advances an iterator by given distance or to a given bound (algorithm function object) |
| ranges::distance(C++20) | returns the distance between an iterator and a sentinel, or between the beginning and end of a range (algorithm function object) |
| ranges::next(C++20) | increment an iterator by a given distance or to a bound (algorithm function object) |
| ranges::prev(C++20) | decrement an iterator by a given distance or to a bound (algorithm function object) |
| Range access | |
| begincbegin(C++11)(C++14) | returns an iterator to the beginning of a container or array   (function template) |
| endcend(C++11)(C++14) | returns an iterator to the end of a container or array   (function template) |
| rbegincrbegin(C++14) | returns a reverse iterator to the beginning of a container or array   (function template) |
| rendcrend(C++14) | returns a reverse end iterator for a container or array   (function template) |
| sizessize(C++17)(C++20) | returns the size of a container or array   (function template) |
| empty(C++17) | checks whether the container is empty   (function template) |
| data(C++17) | obtains the pointer to the underlying array   (function template) |

### Synopsis

```
#include <compare>
#include <concepts>
 
namespace std {
  template<class T> using /* with-reference */ = T&;  // exposition only
  template<class T> concept /* can-reference */       // exposition only
    = requires { typename /* with-reference */<T>; };
  template<class T> concept /* dereferenceable */     // exposition only
    = requires(T& t) {
      { *t } -> /* can-reference */;  // not required to be equality-preserving
    };
 
  // associated types
  // incrementable traits
  template<class> struct incrementable_traits;
  template<class T>
    using iter_difference_t = /* see description */;
 
  // indirectly readable traits
  template<class> struct indirectly_readable_traits;
  template<class T>
    using iter_value_t = /* see description */;
 
  // iterator traits
  template<class I> struct iterator_traits;
  template<class T> requires is_object_v<T> struct iterator_traits<T*>;
 
  template</* dereferenceable */ T>
    using iter_reference_t = decltype(*declval<T&>());
 
  namespace ranges {
    // customization point objects
    inline namespace /* unspecified */ {
      // ranges::iter_move
      inline constexpr /* unspecified */ iter_move = /* unspecified */;
 
      // ranges::iter_swap
      inline constexpr /* unspecified */ iter_swap = /* unspecified */;
    }
  }
 
  template</* dereferenceable */ T>
    requires requires(T& t) {
      { ranges::iter_move(t) } -> /* can-reference */;
    }
  using iter_rvalue_reference_t
    = decltype(ranges::iter_move(declval<T&>()));
 
  // iterator concepts
  // concept indirectly_readable
  template<class In>
    concept indirectly_readable = /* see description */;
 
  template<indirectly_readable T>
    using iter_common_reference_t =
      common_reference_t<iter_reference_t<T>, iter_value_t<T>&>;
 
  // concept indirectly_writable
  template<class Out, class T>
    concept indirectly_writable = /* see description */;
 
  // concept weakly_incrementable
  template<class I>
    concept weakly_incrementable = /* see description */;
 
  // concept incrementable
  template<class I>
    concept incrementable = /* see description */;
 
  // concept input_or_output_iterator
  template<class I>
    concept input_or_output_iterator = /* see description */;
 
  // concept sentinel_for
  template<class S, class I>
    concept sentinel_for = /* see description */;
 
  // concept sized_sentinel_for
  template<class S, class I>
    inline constexpr bool disable_sized_sentinel_for = false;
 
  template<class S, class I>
    concept sized_sentinel_for = /* see description */;
 
  // concept input_iterator
  template<class I>
    concept input_iterator = /* see description */;
 
  // concept output_iterator
  template<class I, class T>
    concept output_iterator = /* see description */;
 
  // concept forward_iterator
  template<class I>
    concept forward_iterator = /* see description */;
 
  // concept bidirectional_iterator
  template<class I>
    concept bidirectional_iterator = /* see description */;
 
  // concept random_access_iterator
  template<class I>
    concept random_access_iterator = /* see description */;
 
  // concept contiguous_iterator
  template<class I>
    concept contiguous_iterator = /* see description */;
 
  // indirect callable requirements
  // indirect callables
  template<class F, class I>
    concept indirectly_unary_invocable = /* see description */;
 
  template<class F, class I>
    concept indirectly_regular_unary_invocable = /* see description */;
 
  template<class F, class I>
    concept indirect_unary_predicate = /* see description */;
 
  template<class F, class I1, class I2>
    concept indirect_binary_predicate = /* see description */;
 
  template<class F, class I1, class I2 = I1>
    concept indirect_equivalence_relation = /* see description */;
 
  template<class F, class I1, class I2 = I1>
    concept indirect_strict_weak_order = /* see description */;
 
  template<class F, class... Is>
    requires (indirectly_readable<Is> && ...) && invocable<F, iter_reference_t<Is>...>
      using indirect_result_t = invoke_result_t<F, iter_reference_t<Is>...>;
 
  // projected
  template<indirectly_readable I, indirectly_regular_unary_invocable<I> Proj>
    struct projected;
 
  template<weakly_incrementable I, class Proj>
    struct incrementable_traits<projected<I, Proj>>;
 
  template<indirectly_­readable I, indirectly_­regular_­unary_­invocable<I> Proj>
    using projected_value_t = remove_cvref_t<invoke_result_t<Proj&, iter_value_t<I>&>>;
 
  // common algorithm requirements
  // concept indirectly_movable
  template<class In, class Out>
    concept indirectly_movable = /* see description */;
 
  template<class In, class Out>
    concept indirectly_movable_storable = /* see description */;
 
  // concept indirectly_copyable
  template<class In, class Out>
    concept indirectly_copyable = /* see description */;
 
  template<class In, class Out>
    concept indirectly_copyable_storable = /* see description */;
 
  // concept indirectly_swappable
  template<class I1, class I2 = I1>
    concept indirectly_swappable = /* see description */;
 
  // concept indirectly_comparable
  template<class I1, class I2, class R, class P1 = identity, class P2 = identity>
    concept indirectly_comparable = /* see description */;
 
  // concept permutable
  template<class I>
    concept permutable = /* see description */;
 
  // concept mergeable
  template<class I1, class I2, class Out,
      class R = ranges::less, class P1 = identity, class P2 = identity>
    concept mergeable = /* see description */;
 
  // concept sortable
  template<class I, class R = ranges::less, class P = identity>
    concept sortable = /* see description */;
 
  // primitives
  // iterator tags
  struct input_iterator_tag { };
  struct output_iterator_tag { };
  struct forward_iterator_tag: public input_iterator_tag { };
  struct bidirectional_iterator_tag: public forward_iterator_tag { };
  struct random_access_iterator_tag: public bidirectional_iterator_tag { };
  struct contiguous_iterator_tag: public random_access_iterator_tag { };
 
  // iterator operations
  template<class InputIt, class Distance>
    constexpr void advance(InputIt& i, Distance n);
  template<class InputIt>
    constexpr typename iterator_traits<InputIt>::difference_type
      distance(InputIt first, InputIt last);
  template<class InputIt>
    constexpr InputIt
      next(InputIt x, typename iterator_traits<InputIt>::difference_type n = 1);
  template<class BidirIt>
    constexpr BidirIt
      prev(BidirIt x, typename iterator_traits<BidirIt>::difference_type n = 1);
 
  // range iterator operations
  namespace ranges {
    // ranges::advance
    template<input_or_output_iterator I>
      constexpr void advance(I& i, iter_difference_t<I> n);
    template<input_or_output_iterator I, sentinel_for<I> S>
      constexpr void advance(I& i, S bound);
    template<input_or_output_iterator I, sentinel_for<I> S>
      constexpr iter_difference_t<I> advance(I& i, iter_difference_t<I> n, S bound);
 
    // ranges::distance
    template<class I, sentinel_for<I> S>
      requires (!sized_sentinel_for<S, I>)
      constexpr iter_difference_t<I> distance(I first, S last);
    template<class I, sized_sentinel_for<decay_t<I>> S>
      constexpr iter_difference_t<decay_t<I>> distance(I&& first, S last);
    template<range R>
      constexpr range_difference_t<R> distance(R&& r);
 
    // ranges::next
    template<input_or_output_iterator I>
      constexpr I next(I x);
    template<input_or_output_iterator I>
      constexpr I next(I x, iter_difference_t<I> n);
    template<input_or_output_iterator I, sentinel_for<I> S>
      constexpr I next(I x, S bound);
    template<input_or_output_iterator I, sentinel_for<I> S>
      constexpr I next(I x, iter_difference_t<I> n, S bound);
 
    // ranges::prev
    template<bidirectional_iterator I>
      constexpr I prev(I x);
    template<bidirectional_iterator I>
      constexpr I prev(I x, iter_difference_t<I> n);
    template<bidirectional_iterator I>
      constexpr I prev(I x, iter_difference_t<I> n, I bound);
  }
 
  // predefined iterators and sentinels
  // reverse iterators
  template<class It> class reverse_iterator;
 
  template<class It1, class It2>
    constexpr bool operator==(const reverse_iterator<It1>& x,
                              const reverse_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator!=(const reverse_iterator<It1>& x,
                              const reverse_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator<(const reverse_iterator<It1>& x,
                             const reverse_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator>(const reverse_iterator<It1>& x,
                             const reverse_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator<=(const reverse_iterator<It1>& x,
                              const reverse_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator>=(const reverse_iterator<It1>& x,
                              const reverse_iterator<It2>& y);
  template<class It1, three_way_comparable_with<It1> It2>
    constexpr compare_three_way_result_t<It1, It2>
      operator<=>(const reverse_iterator<It1>& x, const reverse_iterator<It2>& y);
 
  template<class It1, class It2>
    constexpr auto operator-(const reverse_iterator<It1>& x,
                             const reverse_iterator<It2>& y)
      -> decltype(y.base() - x.base());
  template<class It>
    constexpr reverse_iterator<It> operator+(iter_difference_t<It> n,
                                             const reverse_iterator<It>& x);
 
  template<class It>
    constexpr reverse_iterator<It> make_reverse_iterator(It i);
 
  template<class It1, class It2>
      requires (!sized_sentinel_for<It1, It2>)
    inline constexpr bool disable_sized_sentinel_for<reverse_iterator<It1>,
                                                     reverse_iterator<It2>> = true;
 
  // insert iterators
  template<class Container> class back_insert_iterator;
  template<class Container>
    constexpr back_insert_iterator<Container> back_inserter(Container& x);
 
  template<class Container> class front_insert_iterator;
  template<class Container>
    constexpr front_insert_iterator<Container> front_inserter(Container& x);
 
  template<class Container> class insert_iterator;
  template<class Container>
    constexpr insert_iterator<Container>
      inserter(Container& x, ranges::iterator_t<Container> i);
 
  // move iterators and sentinels
  template<class It> class move_iterator;
 
  template<class It1, class It2>
    constexpr bool operator==(const move_iterator<It1>& x, const move_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator<(const move_iterator<It1>& x, const move_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator>(const move_iterator<It1>& x, const move_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator<=(const move_iterator<It1>& x, const move_iterator<It2>& y);
  template<class It1, class It2>
    constexpr bool operator>=(const move_iterator<It1>& x, const move_iterator<It2>& y);
  template<class It1, three_way_comparable_with<It1> It2>
    constexpr compare_three_way_result_t<It1, It2>
      operator<=>(const move_iterator<It1>& x, const move_iterator<It2>& y);
 
  template<class It1, class It2>
    constexpr auto operator-(const move_iterator<It1>& x, const move_iterator<It2>& y)
      -> decltype(x.base() - y.base());
  template<class It>
    constexpr move_iterator<It>
      operator+(iter_difference_t<It> n, const move_iterator<It>& x);
 
  template<class It>
    constexpr move_iterator<It> make_move_iterator(It i);
 
  template<semiregular S> class move_sentinel;
 
  // common iterators
  template<input_or_output_iterator I, sentinel_for<I> S>
    requires (!same_as<I, S> && copyable<I>)
      class common_iterator;
 
  template<class I, class S>
    struct incrementable_traits<common_iterator<I, S>>;
 
  template<input_iterator I, class S>
    struct iterator_traits<common_iterator<I, S>>;
 
  // default sentinel
  struct default_sentinel_t;
  inline constexpr default_sentinel_t default_sentinel{};
 
  // counted iterators
  template<input_or_output_iterator I> class counted_iterator;
 
  template<input_iterator I>
    requires /* see description */
    struct iterator_traits<counted_iterator<I>>;
 
  // unreachable sentinel
  struct unreachable_sentinel_t;
  inline constexpr unreachable_sentinel_t unreachable_sentinel{};
 
  // stream iterators
  template<class T, class CharT = char, class Traits = char_traits<CharT>,
           class Distance = ptrdiff_t>
  class istream_iterator;
  template<class T, class CharT, class Traits, class Distance>
    bool operator==(const istream_iterator<T, CharT, Traits, Distance>& x,
                    const istream_iterator<T, CharT, Traits, Distance>& y);
 
  template<class T, class CharT = char, class traits = char_traits<CharT>>
      class ostream_iterator;
 
  template<class CharT, class Traits = char_traits<CharT>>
    class istreambuf_iterator;
  template<class CharT, class Traits>
    bool operator==(const istreambuf_iterator<CharT, Traits>& a,
                    const istreambuf_iterator<CharT, Traits>& b);
 
  template<class CharT, class Traits = char_traits<CharT>>
    class ostreambuf_iterator;
 
  // range access
  template<class C> constexpr auto begin(C& c) -> decltype(c.begin());
  template<class C> constexpr auto begin(const C& c) -> decltype(c.begin());
  template<class C> constexpr auto end(C& c) -> decltype(c.end());
  template<class C> constexpr auto end(const C& c) -> decltype(c.end());
  template<class T, size_t N> constexpr T* begin(T (&a)[N]) noexcept;
  template<class T, size_t N> constexpr T* end(T (&a)[N]) noexcept;
  template<class C> constexpr auto cbegin(const C& c) noexcept(noexcept(std::begin(c)))
    -> decltype(std::begin(c));
  template<class C> constexpr auto cend(const C& c) noexcept(noexcept(std::end(c)))
    -> decltype(std::end(c));
  template<class C> constexpr auto rbegin(C& c) -> decltype(c.rbegin());
  template<class C> constexpr auto rbegin(const C& c) -> decltype(c.rbegin());
  template<class C> constexpr auto rend(C& c) -> decltype(c.rend());
  template<class C> constexpr auto rend(const C& c) -> decltype(c.rend());
  template<class T, size_t N> constexpr reverse_iterator<T*> rbegin(T (&a)[N]);
  template<class T, size_t N> constexpr reverse_iterator<T*> rend(T (&a)[N]);
  template<class E> constexpr reverse_iterator<const E*> rbegin(initializer_list<E> il);
  template<class E> constexpr reverse_iterator<const E*> rend(initializer_list<E> il);
  template<class C> constexpr auto crbegin(const C& c) -> decltype(std::rbegin(c));
  template<class C> constexpr auto crend(const C& c) -> decltype(std::rend(c));
 
  template<class C> constexpr auto size(const C& c) -> decltype(c.size());
  template<class T, size_t N> constexpr size_t size(const T (&a)[N]) noexcept;
  template<class C> constexpr auto ssize(const C& c)
    -> common_type_t<ptrdiff_t, make_signed_t<decltype(c.size())>>;
  template<class T, ptrdiff_t N> constexpr ptrdiff_t ssize(const T (&a)[N]) noexcept;
  template<class C> constexpr auto empty(const C& c) -> decltype(c.empty());
  template<class T, size_t N> constexpr bool empty(const T (&a)[N]) noexcept;
  template<class E> constexpr bool empty(initializer_list<E> il) noexcept;
  template<class C> constexpr auto data(C& c) -> decltype(c.data());
  template<class C> constexpr auto data(const C& c) -> decltype(c.data());
  template<class T, size_t N> constexpr T* data(T (&a)[N]) noexcept;
  template<class E> constexpr const E* data(initializer_list<E> il) noexcept;
}

```

#### Concept `indirectly_readable`

```
namespace std {
  template<class In>
    concept __indirectlyReadableImpl = // exposition only
      requires(const In in) {
        typename iter_value_t<In>;
        typename iter_reference_t<In>;
        typename iter_rvalue_reference_t<In>;
        { *in } -> same_as<iter_reference_t<In>>
        { iter_move(in) } -> same_as<iter_rvalue_reference_t<In>>
      } &&
      common_reference_with<iter_reference_t<In>&&, iter_value_t<In>&> &&
      common_reference_with<iter_reference_t<In>&&, iter_rvalue_reference_t<In>&&> &&
      common_reference_with<iter_rvalue_reference_t<In>&&, const iter_value_t<In>&>;
 
  template<class In>
    concept indirectly_readable =
      __indirectlyReadableImpl<remove_cvref_t<In>>
}

```

#### Concept `indirectly_writable`

```
namespace std {
  template<class Out, class T>
    concept indirectly_writable =
      requires(Out&& o, T&& t) {
        *o = std::forward<T>(t); // not required to be equality-preserving
        *std::forward<Out>(o) = std::forward<T>(t);
        // not required to be equality-preserving
        const_cast<const iter_reference_t<Out>&&>(*o) =
        std::forward<T>(t); // not required to be equality-preserving
        const_cast<const iter_reference_t<Out>&&>(*std::forward<Out>(o)) =
        std::forward<T>(t); // not required to be equality-preserving
      };
}

```

#### Concept `weakly_incrementable`

```
namespace std {
  template<class T>
    inline constexpr bool __is_integer_like = /* see description */; // exposition only
 
  template<class T>
    inline constexpr bool __is_signed_integer_like =  // exposition only
      /* see description */;
 
  template<class I>
    concept weakly_incrementable =
      default_initializable<I> && movable<I> &&
      requires(I i) {
        typename iter_difference_t<I>;
        requires __is_signed_integer_like<iter_difference_t<I>>;
        { ++i } -> same_as<I&>;   // not required to be equality-preserving
        i++;                      // not required to be equality-preserving
      };
}

```

#### Concept `incrementable`

```
namespace std {
  template<class I>
    concept incrementable =
      regular<I> &&
      weakly_incrementable<I> &&
      requires(I i) {
        { i++ } -> same_as<I>;
      };
}

```

#### Concept `input_or_output_iterator`

```
namespace std {
  template<class I>
    concept input_or_output_iterator =
      requires(I i) {
        { *i } -> can-reference;
      } &&
      weakly_incrementable<I>;
}

```

#### Concept `sentinel_for`

```
namespace std {
  template<class S, class I>
    concept sentinel_for =
      semiregular<S> &&
      input_or_output_iterator<I> &&
      __WeaklyEqualityComparableWith<S, I>;
}

```

#### Concept `sized_sentinel_for`

```
namespace std {
  template<class S, class I>
    concept sized_sentinel_for =
      sentinel_for<S, I> &&
      !disable_sized_sentinel<remove_cv_t<S>, remove_cv_t<I>> &&
      requires(const I& i, const S& s) {
        { s - i } -> same_as<iter_difference_t<I>>;
        { i - s } -> same_as<iter_difference_t<I>>;
      };
}

```

#### Concept `input_iterator`

```
namespace std {
  template<class I>
    concept input_iterator =
      input_or_output_iterator<I> &&
      indirectly_readable<I> &&
      requires { typename /* ITER_CONCEPT */(I); } &&
      derived_from</* ITER_CONCEPT */(I), input_iterator_tag>;
}

```

#### Concept `output_iterator`

```
namespace std {
  template<class I, class T>
    concept output_iterator =
      input_or_output_iterator<I> &&
      indirectly_writable<I, T> &&
      requires(I i, T&& t) {
        *i++ = std::forward<T>(t); // not required to be equality-preserving
      };
}

```

#### Concept `forward_iterator`

```
namespace std {
  template<class I>
    concept forward_iterator =
      input_iterator<I> &&
      derived_from</* ITER_CONCEPT */(I), forward_iterator_tag> &&
      incrementable<I> &&
      sentinel_for<I, I>;
}

```

#### Concept `bidirectional_iterator`

```
namespace std {
  template<class I>
    concept bidirectional_iterator =
      forward_iterator<I> &&
      derived_from</* ITER_CONCEPT */(I), bidirectional_iterator_tag> &&
      requires(I i) {
        { --i } -> same_as<I&>;
        { i-- } -> same_as<I>;
      };
}

```

#### Concept `random_access_iterator`

```
namespace std {
  template<class I>
    concept random_access_iterator =
      bidirectional_iterator<I> &&
      derived_from</* ITER_CONCEPT */(I), random_access_iterator_tag> &&
      totally_ordered<I> &&
      sized_sentinel_for<I, I> &&
      requires(I i, const I j, const iter_difference_t<I> n) {
        { i += n } -> same_as<I&>;
        { j +  n } -> same_as<I>;
        { n +  j } -> same_as<I>;
        { i -= n } -> same_as<I&>;
        { j -  n } -> same_as<I>;
        {  j[n]  } -> same_as<iter_reference_t<I>>;
      };
}

```

#### Concept `contiguous_iterator`

```
namespace std {
  template<class I>
    concept contiguous_iterator =
      random_access_iterator<I> &&
      derived_from</* ITER_CONCEPT */(I), contiguous_iterator_tag> &&
      is_lvalue_reference_v<iter_reference_t<I>> &&
      same_as<iter_value_t<I>, remove_cvref_t<iter_reference_t<I>>> &&
      requires(const I& i) {
        { to_address(i) } -> same_as<add_pointer_t<iter_reference_t<I>>>;
      };
}

```

#### Concept `indirectly_unary_invocable`

```
namespace std {
  template<class F, class I>
    concept indirectly_unary_invocable =
      indirectly_readable<I> &&
      copy_constructible<F> &&
      invocable<F&, iter_value_t<I>&> &&
      invocable<F&, iter_reference_t<I>> &&
      common_reference_with<
        invoke_result_t<F&, iter_value_t<I>&>,
        invoke_result_t<F&, iter_reference_t<I>>>;
}

```

#### Concept `indirectly_regular_unary_invocable`

```
namespace std {
  template<class F, class I>
    concept indirectly_regular_unary_invocable =
      indirectly_readable<I> &&
      copy_constructible<F> &&
      regular_invocable<F&, iter_value_t<I>&> &&
      regular_invocable<F&, iter_reference_t<I>> &&
      common_reference_with<
        invoke_result_t<F&, iter_value_t<I>&>,
        invoke_result_t<F&, iter_reference_t<I>>>;
}

```

#### Concept `indirect_unary_predicate`

```
namespace std {
  template<class F, class I>
    concept indirect_unary_predicate =
      indirectly_readable<I> &&
      copy_constructible<F> &&
      predicate<F&, iter_value_t<I>&> &&
      predicate<F&, iter_reference_t<I>>;
}

```

#### Concept `indirect_binary_predicate`

```
namespace std {
  template<class F, class I1, class I2 = I1>
    concept indirect_binary_predicate =
      indirectly_readable<I1> && indirectly_readable<I2> &&
      copy_constructible<F> &&
      predicate<F&, iter_value_t<I1>&, iter_value_t<I2>&> &&
      predicate<F&, iter_value_t<I1>&, iter_reference_t<I2>> &&
      predicate<F&, iter_reference_t<I1>, iter_value_t<I2>&> &&
      predicate<F&, iter_reference_t<I1>, iter_reference_t<I2>>;
}

```

#### Concept `indirect_equivalence_relation`

```
namespace std {
  template<class F, class I1, class I2 = I1>
    concept indirect_equivalence_relation =
      indirectly_readable<I1> && indirectly_readable<I2> &&
      copy_constructible<F> &&
      equivalence_relation<F&, iter_value_t<I1>&, iter_value_t<I2>&> &&
      equivalence_relation<F&, iter_value_t<I1>&, iter_reference_t<I2>> &&
      equivalence_relation<F&, iter_reference_t<I1>, iter_value_t<I2>&> &&
      equivalence_relation<F&, iter_reference_t<I1>, iter_reference_t<I2>>;
}

```

#### Concept `indirect_strict_weak_order`

```
namespace std {
  template<class F, class I1, class I2 = I1>
    concept indirect_strict_weak_order =
      indirectly_readable<I1> && indirectly_readable<I2> &&
      copy_constructible<F> &&
      strict_weak_order<F&, iter_value_t<I1>&, iter_value_t<I2>&> &&
      strict_weak_order<F&, iter_value_t<I1>&, iter_reference_t<I2>> &&
      strict_weak_order<F&, iter_reference_t<I1>, iter_value_t<I2>&> &&
      strict_weak_order<F&, iter_reference_t<I1>, iter_reference_t<I2>>;
}

```

#### Concept `indirectly_movable`

```
namespace std {
  template<class In, class Out>
    concept indirectly_movable =
      indirectly_readable<In> &&
      indirectly_writable<Out, iter_rvalue_reference_t<In>>;
}

```

#### Concept `indirectly_movable_storable`

```
namespace std {
  template<class In, class Out>
    concept indirectly_movable_storable =
      indirectly_movable<In, Out> &&
      indirectly_writable<Out, iter_value_t<In>> &&
      movable<iter_value_t<In>> &&
      constructible_from<iter_value_t<In>, iter_rvalue_reference_t<In>> &&
      assignable_from<iter_value_t<In>&, iter_rvalue_reference_t<In>>;
}

```

#### Concept `indirectly_copyable`

```
namespace std {
  template<class In, class Out>
    concept indirectly_copyable =
      indirectly_readable<In> &&
      indirectly_writable<Out, iter_reference_t<In>>;
}

```

#### Concept `indirectly_copyable_storable`

```
namespace std {
  template<class In, class Out>
    concept indirectly_copyable_storable =
      indirectly_copyable<In, Out> &&
      indirectly_writable<Out, iter_value_t<In>&> &&
      indirectly_writable<Out, const iter_value_t<In>&> &&
      indirectly_writable<Out, iter_value_t<In>&&> &&
      indirectly_writable<Out, const iter_value_t<In>&&> &&
      copyable<iter_value_t<In>> &&
      constructible_from<iter_value_t<In>, iter_reference_t<In>> &&
      assignable_from<iter_value_t<In>&, iter_reference_t<In>>;
}

```

#### Concept `indirectly_swappable`

```
namespace std {
  template<class I1, class I2 = I1>
    concept indirectly_swappable =
      indirectly_readable<I1> && indirectly_readable<I2> &&
      requires(const I1 i1, const I2 i2) {
        ranges::iter_swap(i1, i1);
        ranges::iter_swap(i2, i2);
        ranges::iter_swap(i1, i2);
        ranges::iter_swap(i2, i1);
      };
}

```

#### Concept `indirectly_comparable`

```
namespace std {
  template<class I1, class I2, class R, class P1 = identity, class P2 = identity>
    concept indirectly_comparable =
      indirect_predicate<R, projected<I1, P1>, projected<I2, P2>>;
}

```

#### Concept `permutable`

```
namespace std {
  template<class I>
    concept permutable =
      forward_iterator<I> &&
      indirectly_movable_storable<I, I> &&
      indirectly_swappable<I, I>;
}

```

#### Concept `mergeable`

```
namespace std {
  template<class I1, class I2, class Out, class R = ranges::less,
           class P1 = identity, class P2 = identity>
    concept mergeable =
      input_iterator<I1> &&
      input_iterator<I2> &&
      weakly_incrementable<Out> &&
      indirectly_copyable<I1, Out> &&
      indirectly_copyable<I2, Out> &&
      indirect_strict_weak_order<R, projected<I1, P1>, projected<I2, P2>>;
}

```

#### Concept `sortable`

```
namespace std {
  template<class I, class R = ranges::less, class P = identity>
    concept sortable =
      permutable<I> &&
      indirect_strict_weak_order<R, projected<I, P>>;
}

```

#### Class template std::incrementable_traits

```
namespace std {
  template<class> struct incrementable_traits { };
 
  template<class T>
    requires is_object_v<T>
  struct incrementable_traits<T*> {
    using difference_type = ptrdiff_t;
  };
 
  template<class I>
  struct incrementable_traits<const I>
    : incrementable_traits<I> { };
 
  template<class T>
    requires requires { typename T::difference_type; }
  struct incrementable_traits<T> {
    using difference_type = typename T::difference_type;
  };
 
  template<class T>
    requires (!requires { typename T::difference_type; } &&
              requires(const T& a, const T& b) { { a - b } -> integral; })
  struct incrementable_traits<T> {
    using difference_type = make_signed_t<decltype(declval<T>() - declval<T>())>;
  };
 
  template<class T>
    using iter_difference_t = /* see description */;
}

```

#### Class template std::indirectly_readable_traits

```
namespace std {
  template<class> struct __cond_value_type { };   // exposition only
  template<class T>
    requires is_object_v<T>
  struct __cond_value_type {
    using value_type = remove_cv_t<T>;
  };
 
  template<class> struct indirectly_readable_traits { };
 
  template<class T>
  struct indirectly_readable_traits<T*>
    : __cond_value_type<T> { };
 
  template<class I>
    requires is_array_v<I>
  struct indirectly_readable_traits<I> {
    using value_type = remove_cv_t<remove_extent_t<I>>;
  };
 
  template<class I>
  struct indirectly_readable_traits<const I>
    : indirectly_readable_traits<I> { };
 
  template<class T>
    requires requires { typename T::value_type; }
  struct indirectly_readable_traits<T>
    : __cond_value_type<typename T::value_type> { };
 
  template<class T>
    requires requires { typename T::element_type; }
  struct indirectly_readable_traits<T>
    : __cond_value_type<typename T::element_type> { };
}

```

#### Class template std::projected

```
namespace std {
  template<indirectly_readable I, indirectly_regular_unary_invocable<I> Proj>
  struct projected {
    using value_type = remove_cvref_t<indirect_result_t<Proj&, I>>;
    indirect_result_t<Proj&, I> operator*() const; // not defined
  };
 
  template<weakly_incrementable I, class Proj>
  struct incrementable_traits<projected<I, Proj>> {
    using difference_type = iter_difference_t<I>;
  };
}

```

#### Class template std::iterator_traits

```
namespace std {
  template<class I>
  struct iterator_traits {
    using iterator_category = /* see description */;
    using value_type        = /* see description */;
    using difference_type   = /* see description */;
    using pointer           = /* see description */;
    using reference         = /* see description */;
  };
 
  template<class T>
    requires is_object_v<T>
  struct iterator_traits<T*> {
    using iterator_concept  = contiguous_iterator_tag;
    using iterator_category = random_access_iterator_tag;
    using value_type        = remove_cv_t<T>;
    using difference_type   = ptrdiff_t;
    using pointer           = T*;
    using reference         = T&;
  };
}

```

#### Iterator tags

```
namespace std {
  struct input_iterator_tag { };
  struct output_iterator_tag { };
  struct forward_iterator_tag: public input_iterator_tag { };
  struct bidirectional_iterator_tag: public forward_iterator_tag { };
  struct random_access_iterator_tag: public bidirectional_iterator_tag { };
  struct contiguous_iterator_tag: public random_access_iterator_tag { };
}

```

#### Class template std::reverse_iterator

```
namespace std {
  template<class Iter>
  class reverse_iterator {
  public:
    using iterator_type     = Iter;
    using iterator_concept  = /* see description */;
    using iterator_category = /* see description */;
    using value_type        = iter_value_t<Iter>;
    using difference_type   = iter_difference_t<Iter>;
    using pointer           = typename iterator_traits<Iter>::pointer;
    using reference         = iter_reference_t<Iter>;
 
    constexpr reverse_iterator();
    constexpr explicit reverse_iterator(Iter x);
    template<class U> constexpr reverse_iterator(const reverse_iterator<U>& u);
    template<class U> constexpr reverse_iterator& operator=(const reverse_iterator<U>& u);
 
    constexpr Iter base() const;
    constexpr reference operator*() const;
    constexpr pointer   operator->() const requires /* see description */;
 
    constexpr reverse_iterator& operator++();
    constexpr reverse_iterator  operator++(int);
    constexpr reverse_iterator& operator--();
    constexpr reverse_iterator  operator--(int);
 
    constexpr reverse_iterator  operator+ (difference_type n) const;
    constexpr reverse_iterator& operator+=(difference_type n);
    constexpr reverse_iterator  operator- (difference_type n) const;
    constexpr reverse_iterator& operator-=(difference_type n);
    constexpr /* unspecified */ operator[](difference_type n) const;
 
    friend constexpr iter_rvalue_reference_t<Iter>
      iter_move(const reverse_iterator& i) noexcept(/* see description */);
    template<indirectly_swappable<Iter> Iter2>
      friend constexpr void
        iter_swap(const reverse_iterator& x,
                  const reverse_iterator<Iter2>& y) noexcept(/* see description */);
 
  protected:
    Iter current;
  };
}

```

#### Class template std::back_insert_iterator

```
namespace std {
  template<class Container>
  class back_insert_iterator {
  protected:
    Container* container = nullptr;
 
  public:
    using iterator_category = output_iterator_tag;
    using value_type        = void;
    using difference_type   = ptrdiff_t;
    using pointer           = void;
    using reference         = void;
    using container_type    = Container;
 
    constexpr back_insert_iterator() noexcept = default;
    constexpr explicit back_insert_iterator(Container& x);
    constexpr back_insert_iterator& operator=(const typename Container::value_type& value);
    constexpr back_insert_iterator& operator=(typename Container::value_type&& value);
 
    constexpr back_insert_iterator& operator*();
    constexpr back_insert_iterator& operator++();
    constexpr back_insert_iterator  operator++(int);
  };
}

```

#### Class template std::front_insert_iterator

```
namespace std {
  template<class Container>
  class front_insert_iterator {
  protected:
    Container* container = nullptr;
 
  public:
    using iterator_category = output_iterator_tag;
    using value_type        = void;
    using difference_type   = ptrdiff_t;
    using pointer           = void;
    using reference         = void;
    using container_type    = Container;
 
    constexpr front_insert_iterator(Container& x) noexcept = default;
    constexpr explicit front_insert_iterator(Container& x);
    constexpr front_insert_iterator&
      operator=(const typename Container::value_type& value);
    constexpr front_insert_iterator& operator=(typename Container::value_type&& value);
 
    constexpr front_insert_iterator& operator*();
    constexpr front_insert_iterator& operator++();
    constexpr front_insert_iterator  operator++(int);
  };
}

```

#### Class template std::insert_iterator

```
namespace std {
  template<class Container>
  class insert_iterator {
  protected:
    Container* container = nullptr;
    ranges::iterator_t<Container> iter = ranges::iterator_t<Container>();
 
  public:
    using iterator_category = output_iterator_tag;
    using value_type        = void;
    using difference_type   = ptrdiff_t;
    using pointer           = void;
    using reference         = void;
    using container_type    = Container;
 
    insert_iterator() = default;
    constexpr insert_iterator(Container& x, ranges::iterator_t<Container> i);
    constexpr insert_iterator& operator=(const typename Container::value_type& value);
    constexpr insert_iterator& operator=(typename Container::value_type&& value);
 
    constexpr insert_iterator& operator*();
    constexpr insert_iterator& operator++();
    constexpr insert_iterator& operator++(int);
  };
}

```

#### Class template std::move_iterator

```
namespace std {
  template<class Iter>
  class move_iterator {
  public:
    using iterator_type     = Iter;
    using iterator_concept  = /* see description */;
    using iterator_category = /* see description */;
    using value_type        = iter_value_t<Iter>;
    using difference_type   = iter_difference_t<Iter>;
    using pointer           = Iter;
    using reference         = iter_rvalue_reference_t<Iter>;
 
    constexpr move_iterator();
    constexpr explicit move_iterator(Iter i);
    template<class U> constexpr move_iterator(const move_iterator<U>& u);
    template<class U> constexpr move_iterator& operator=(const move_iterator<U>& u);
 
    constexpr iterator_type base() const &;
    constexpr iterator_type base() &&;
    constexpr reference operator*() const;
    constexpr pointer operator->() const;
 
    constexpr move_iterator& operator++();
    constexpr auto operator++(int);
    constexpr move_iterator& operator--();
    constexpr move_iterator operator--(int);
 
    constexpr move_iterator operator+(difference_type n) const;
    constexpr move_iterator& operator+=(difference_type n);
    constexpr move_iterator operator-(difference_type n) const;
    constexpr move_iterator& operator-=(difference_type n);
    constexpr reference operator[](difference_type n) const;
 
    template<sentinel_for<Iter> S>
      friend constexpr bool
        operator==(const move_iterator& x, const move_sentinel<S>& y);
    template<sized_sentinel_for<Iter> S>
      friend constexpr iter_difference_t<Iter>
        operator-(const move_sentinel<S>& x, const move_iterator& y);
    template<sized_sentinel_for<Iter> S>
      friend constexpr iter_difference_t<Iter>
        operator-(const move_iterator& x, const move_sentinel<S>& y);
    friend constexpr iter_rvalue_reference_t<Iter>
      iter_move(const move_iterator& i)
        noexcept(noexcept(ranges::iter_move(i.current)));
    template<indirectly_swappable<Iter> Iter2>
      friend constexpr void
        iter_swap(const move_iterator& x, const move_iterator<Iter2>& y)
          noexcept(noexcept(ranges::iter_swap(x.current, y.current)));
 
  private:
    Iter current;     // exposition only
  };
}

```

#### Class template std::move_sentinel

```
namespace std {
  template<semiregular S>
  class move_sentinel {
  public:
    constexpr move_sentinel();
    constexpr explicit move_sentinel(S s);
    template<class S2>
      requires convertible_to<const S2&, S>
        constexpr move_sentinel(const move_sentinel<S2>& s);
    template<class S2>
      requires assignable_from<S&, const S2&>
        constexpr move_sentinel& operator=(const move_sentinel<S2>& s);
 
    constexpr S base() const;
  private:
    S last;     // exposition only
  };
}

```

#### Class template std::common_iterator

```
namespace std {
  template<input_or_output_iterator I, sentinel_for<I> S>
    requires (!same_as<I, S> && copyable<I>)
  class common_iterator {
  public:
    constexpr common_iterator() = default;
    constexpr common_iterator(I i);
    constexpr common_iterator(S s);
    template<class I2, class S2>
      requires convertible_to<const I2&, I> && convertible_to<const S2&, S>
        constexpr common_iterator(const common_iterator<I2, S2>& x);
 
    template<class I2, class S2>
      requires convertible_to<const I2&, I> && convertible_to<const S2&, S> &&
               assignable_from<I&, const I2&> && assignable_from<S&, const S2&>
        common_iterator& operator=(const common_iterator<I2, S2>& x);
 
    decltype(auto) operator*();
    decltype(auto) operator*() const
      requires dereferenceable<const I>;
    decltype(auto) operator->() const
      requires /* see description */;
 
    common_iterator& operator++();
    decltype(auto) operator++(int);
 
    template<class I2, sentinel_for<I> S2>
      requires sentinel_for<S, I2>
    friend bool operator==(
      const common_iterator& x, const common_iterator<I2, S2>& y);
    template<class I2, sentinel_for<I> S2>
      requires sentinel_for<S, I2> && equality_comparable_with<I, I2>
    friend bool operator==(
      const common_iterator& x, const common_iterator<I2, S2>& y);
 
    template<sized_sentinel_for<I> I2, sized_sentinel_for<I> S2>
      requires sized_sentinel_for<S, I2>
    friend iter_difference_t<I2> operator-(
      const common_iterator& x, const common_iterator<I2, S2>& y);
 
    friend constexpr decltype(auto) iter_move(const common_iterator& i)
      noexcept(noexcept(ranges::iter_move(declval<const I&>())))
        requires input_iterator<I>;
    template<indirectly_swappable<I> I2, class S2>
      friend void iter_swap(const common_iterator& x, const common_iterator<I2, S2>& y)
        noexcept(noexcept(ranges::iter_swap(declval<const I&>(), declval<const I2&>())));
 
  private:
    variant<I, S> v_;   // exposition only
  };
 
  template<class I, class S>
  struct incrementable_traits<common_iterator<I, S>> {
    using difference_type = iter_difference_t<I>;
  };
 
  template<input_iterator I, class S>
  struct iterator_traits<common_iterator<I, S>> {
    using iterator_concept = /* see description */;
    using iterator_category = /* see description */;
    using value_type = iter_value_t<I>;
    using difference_type = iter_difference_t<I>;
    using pointer = /* see description */;
    using reference = iter_reference_t<I>;
  };
}

```

#### Class std::default_sentinel_t

```
namespace std {
  struct default_sentinel_t { };
}

```

#### Class template std::counted_iterator

```
namespace std {
  template<input_or_output_iterator I>
  class counted_iterator {
  public:
    using iterator_type = I;
 
    constexpr counted_iterator() = default;
    constexpr counted_iterator(I x, iter_difference_t<I> n);
    template<class I2>
      requires convertible_to<const I2&, I>
        constexpr counted_iterator(const counted_iterator<I2>& x);
 
    template<class I2>
      requires assignable_from<I&, const I2&>
        constexpr counted_iterator& operator=(const counted_iterator<I2>& x);
 
    constexpr I base() const & requires copy_constructible<I>;
    constexpr I base() &&;
    constexpr iter_difference_t<I> count() const noexcept;
    constexpr decltype(auto) operator*();
    constexpr decltype(auto) operator*() const
      requires dereferenceable<const I>;
    constexpr auto operator->() const noexcept
      requires contiguous_iterator<I>;
 
    constexpr counted_iterator& operator++();
    decltype(auto) operator++(int);
    constexpr counted_iterator operator++(int)
      requires forward_iterator<I>;
    constexpr counted_iterator& operator--()
      requires bidirectional_iterator<I>;
    constexpr counted_iterator operator--(int)
      requires bidirectional_iterator<I>;
 
    constexpr counted_iterator operator+(iter_difference_t<I> n) const
      requires random_access_iterator<I>;
    friend constexpr counted_iterator operator+(
      iter_difference_t<I> n, const counted_iterator& x)
        requires random_access_iterator<I>;
    constexpr counted_iterator& operator+=(iter_difference_t<I> n)
      requires random_access_iterator<I>;
 
    constexpr counted_iterator operator-(iter_difference_t<I> n) const
      requires random_access_iterator<I>;
    template<common_with<I> I2>
      friend constexpr iter_difference_t<I2> operator-(
        const counted_iterator& x, const counted_iterator<I2>& y);
    friend constexpr iter_difference_t<I> operator-(
      const counted_iterator& x, default_sentinel_t);
    friend constexpr iter_difference_t<I> operator-(
      default_sentinel_t, const counted_iterator& y);
    constexpr counted_iterator& operator-=(iter_difference_t<I> n)
      requires random_access_iterator<I>;
 
    constexpr decltype(auto) operator[](iter_difference_t<I> n) const
      requires random_access_iterator<I>;
 
    template<common_with<I> I2>
      friend constexpr bool operator==(
        const counted_iterator& x, const counted_iterator<I2>& y);
    friend constexpr bool operator==(
      const counted_iterator& x, default_sentinel_t);
 
    template<common_with<I> I2>
      friend constexpr strong_ordering operator<=>(
        const counted_iterator& x, const counted_iterator<I2>& y);
 
    friend constexpr decltype(auto) iter_move(const counted_iterator& i)
      noexcept(noexcept(ranges::iter_move(i.current)))
        requires input_iterator<I>;
    template<indirectly_swappable<I> I2>
      friend constexpr void iter_swap(const counted_iterator& x,
                                      const counted_iterator<I2>& y)
        noexcept(noexcept(ranges::iter_swap(x.current, y.current)));
 
  private:
    I current = I();                    // exposition only
    iter_difference_t<I> length = 0;    // exposition only
  };
 
  template<input_iterator I>
  struct iterator_traits<counted_iterator<I>> : iterator_traits<I> {
    using pointer = void;
  };
}

```

#### Class std::unreachable_sentinel_t

```
namespace std {
  struct unreachable_sentinel_t {
    template<weakly_incrementable I>
      friend constexpr bool operator==(unreachable_sentinel_t, const I&) noexcept
      { return false; }
  };
}

```

#### Class template std::istream_iterator

```
namespace std {
  template<class T, class CharT = char, class Traits = char_traits<CharT>,
           class Distance = ptrdiff_t>
  class istream_iterator {
  public:
    using iterator_category = input_iterator_tag;
    using value_type        = T;
    using difference_type   = Distance;
    using pointer           = const T*;
    using reference         = const T&;
    using char_type         = CharT;
    using traits_type       = Traits;
    using istream_type      = basic_istream<CharT, Traits>;
 
    constexpr istream_iterator();
    constexpr istream_iterator(default_sentinel_t);
    istream_iterator(istream_type& s);
    istream_iterator(const istream_iterator& x) = default;
    ~istream_iterator() = default;
    istream_iterator& operator=(const istream_iterator&) = default;
 
    const T& operator*() const;
    const T* operator->() const;
    istream_iterator& operator++();
    istream_iterator  operator++(int);
 
    friend bool operator==(const istream_iterator& i, default_sentinel_t);
 
  private:
    basic_istream<CharT, Traits>* in_stream; // exposition only
    T value;                                 // exposition only
  };
}

```

#### Class template std::ostream_iterator

```
namespace std {
  template<class T, class CharT = char, classTraits = char_traits<CharT>>
  class ostream_iterator {
  public:
    using iterator_category = output_iterator_tag;
    using value_type        = void;
    using difference_type   = ptrdiff_t;
    using pointer           = void;
    using reference         = void;
    using char_type         = CharT;
    using traits_type       = Traits;
    using ostream_type      = basic_ostream<CharT, Traits>;
 
    constexpr ostreambuf_iterator() noexcept = default;
    ostream_iterator(ostream_type& s);
    ostream_iterator(ostream_type& s, const CharT* delimiter);
    ostream_iterator(const ostream_iterator& x);
    ~ostream_iterator();
    ostream_iterator& operator=(const ostream_iterator&) = default;
    ostream_iterator& operator=(const T& value);
 
    ostream_iterator& operator*();
    ostream_iterator& operator++();
    ostream_iterator& operator++(int);
 
  private:
    basic_ostream<CharT, Traits>* out_stream = nullptr;          // exposition only
    const CharT* delim = nullptr;                                // exposition only
  };
}

```

#### Class template std::istreambuf_iterator

```
namespace std {
  template<class CharT, class Traits = char_traits<CharT>>
  class istreambuf_iterator {
  public:
    using iterator_category = input_iterator_tag;
    using value_type        = CharT;
    using difference_type   = typename Traits::off_type;
    using pointer           = /* unspecified */;
    using reference         = CharT;
    using char_type         = CharT;
    using traits_type       = Traits;
    using int_type          = typename Traits::int_type;
    using streambuf_type    = basic_streambuf<CharT, Traits>;
    using istream_type      = basic_istream<CharT, Traits>;
 
    class proxy;                          // exposition only
 
    constexpr istreambuf_iterator() noexcept;
    constexpr istreambuf_iterator(default_sentinel_t) noexcept;
    istreambuf_iterator(const istreambuf_iterator&) noexcept = default;
    ~istreambuf_iterator() = default;
    istreambuf_iterator(istream_type& s) noexcept;
    istreambuf_iterator(streambuf_type* s) noexcept;
    istreambuf_iterator(const proxy& p) noexcept;
    istreambuf_iterator& operator=(const istreambuf_iterator&) noexcept = default;
    CharT operator*() const;
    istreambuf_iterator& operator++();
    proxy operator++(int);
    bool equal(const istreambuf_iterator& b) const;
 
    friend bool operator==(const istreambuf_iterator& i, default_sentinel_t s);
 
  private:
    streambuf_type* sbuf_;                // exposition only
  };
 
  template<class CharT, class Traits>
  class istreambuf_iterator<CharT, Traits>::proxy { // exposition only
    CharT keep_;
    basic_streambuf<CharT, Traits>* sbuf_;
    proxy(CharT c, basic_streambuf<CharT, Traits>* sbuf)
      : keep_(c), sbuf_(sbuf) { }
  public:
    CharT operator*() { return keep_; }
  };
}

```

#### Class template std::ostreambuf_iterator

```
namespace std {
  template<class CharT, class Traits = char_traits<CharT>>
  class ostreambuf_iterator {
  public:
    using iterator_category = output_iterator_tag;
    using value_type        = void;
    using difference_type   = ptrdiff_t;
    using pointer           = void;
    using reference         = void;
    using char_type         = CharT;
    using traits_type       = Traits;
    using streambuf_type    = basic_streambuf<CharT, Traits>;
    using ostream_type      = basic_ostream<CharT, Traits>;
 
    constexpr ostreambuf_iterator() noexcept = default;
    ostreambuf_iterator(ostream_type& s) noexcept;
    ostreambuf_iterator(streambuf_type* s) noexcept;
    ostreambuf_iterator& operator=(CharT c);
 
    ostreambuf_iterator& operator*();
    ostreambuf_iterator& operator++();
    ostreambuf_iterator& operator++(int);
    bool failed() const noexcept;
 
  private:
    streambuf_type* sbuf_ = nullptr;    // exposition only
  };
}

```

#### Class template std::iterator

```
namespace std {
  template<class Category, class T, class Distance = ptrdiff_t,
           class Pointer = T*, class Reference = T&>
  struct iterator {
    typedef Category  iterator_category;
    typedef T         value_type;
    typedef Distance  difference_type;
    typedef Pointer   pointer;
    typedef Reference reference;
  };
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 349 | C++98 | the exposition-only member `delim` of std::ostream_iterator had type const char\* | corrected to const CharT\* |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/iterator&oldid=170799>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 April 2024, at 06:05.