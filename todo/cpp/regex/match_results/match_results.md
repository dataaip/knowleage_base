# std::match_results<BidirIt,Alloc>::match_results

From cppreference.com
< cpp‎ | regex‎ | match results
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

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

Regular expressions library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_regex(C++11) | | | | |
| sub_match(C++11) | | | | |
| match_results(C++11) | | | | |
| Algorithms | | | | |
| regex_match(C++11) | | | | |
| regex_search(C++11) | | | | |
| regex_replace(C++11) | | | | |
| Iterators | | | | |
| regex_iterator(C++11) | | | | |
| regex_token_iterator(C++11) | | | | |
| Exceptions | | | | |
| regex_error(C++11) | | | | |
| Traits | | | | |
| regex_traits(C++11) | | | | |
| Constants | | | | |
| syntax_option_type(C++11) | | | | |
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

std::match_results

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****match_results::match_results**** | | | | |
| match_results::~match_results | | | | |
| match_results::operator= | | | | |
| match_results::get_allocator | | | | |
| State | | | | |
| match_results::ready | | | | |
| Element access | | | | |
| match_results::size | | | | |
| match_results::max_size | | | | |
| match_results::empty | | | | |
| match_results::length | | | | |
| match_results::position | | | | |
| match_results::str | | | | |
| [match_results::operator[]](operator_at.html "cpp/regex/match results/operator at") | | | | |
| match_results::prefix | | | | |
| match_results::suffix | | | | |
| Iterators | | | | |
| match_results::beginmatch_results::cbegin | | | | |
| match_results::endmatch_results::cend | | | | |
| Format | | | | |
| match_results::format | | | | |
| Modifiers | | | | |
| match_results::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=(until C++20) | | | | |
| swap(std::match_results) | | | | |

|  |  |  |
| --- | --- | --- |
| match_results() : match_results(Allocator()) {} | (1) |  |
| explicit match_results( const Allocator& a ); | (2) |  |
| match_results( const match_results& rhs ); | (3) |  |
| match_results( const match_results& rhs, const Allocator& a ); | (4) |  |
| match_results( match_results&& rhs ) noexcept; | (5) |  |
| match_results( match_results&& rhs, const Allocator& a ); | (6) |  |
|  |  |  |

1,2) Constructs a match result with no established result state.1) The default constructor.2) Constructs the match result using a copy of a as the allocator. When the construction finishes, `ready()` returns false and `size()` returns ​0​.3-6) Constructs a match result from rhs.3) The copy constructor.4) Constructs the match result using a copy of a as the allocator.5) The move constructor. When the construction finishes, rhs is in a valid but unspecified state.6) Constructs the match result using a copy of a as the allocator. When the construction finishes, rhs is in a valid but unspecified state. Given the value of rhs before the construction as m and any integer in ``​0​`,`m.size()`)` as n, when the construction finishes, the following member functions should return the specified values:

| Member function | Value |
| --- | --- |
| [`ready()` | m.ready() |
| `size()` | m.size() |
| `str(n)` | m.str(n) |
| `prefix()` | m.prefix() |
| `suffix()` | m.suffix() |
| `operator[`](operator_at.html "cpp/regex/match results/operator at") | m[n] |
| `length(n)` | m.length(n) |
| `position(n)` | m.position(n) |

### Parameters

|  |  |  |
| --- | --- | --- |
| a | - | allocator to use for all memory allocations of this container |
| rhs | - | another `match_results` to use as source to initialize the `match_results` with |

### Exceptions

1-4) May throw implementation-defined exceptions.6) Throws nothing if a == rhs.get_allocator() is true.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2191 | C++11 | n could be negative in the postconditions of overloads (3-6) | can only be non-negative |
| LWG 2195 | C++11 | the constructors required by AllocatorAwareContainer were missing | added |
| P0935R0 | C++11 | default constructor was explicit | made implicit |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/match_results/match_results&oldid=177533>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 November 2024, at 01:02.