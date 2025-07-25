# std::basic_stacktrace<Allocator>::swap

From cppreference.com
< cpp‎ | utility‎ | basic stacktrace
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

Diagnostics library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

std::basic_stacktrace

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_stacktrace::basic_stacktrace | | | | |
| basic_stacktrace::~basic_stacktrace | | | | |
| basic_stacktrace::operator= | | | | |
| basic_stacktrace::current | | | | |
| basic_stacktrace::get_allocator | | | | |
| Iterators | | | | |
| basic_stacktrace::beginbasic_stacktrace::cbegin | | | | |
| basic_stacktrace::endbasic_stacktrace::cend | | | | |
| basic_stacktrace::rbeginbasic_stacktrace::crbegin | | | | |
| basic_stacktrace::rendbasic_stacktrace::crend | | | | |
| Capacity | | | | |
| basic_stacktrace::empty | | | | |
| basic_stacktrace::size | | | | |
| basic_stacktrace::max_size | | | | |
| Element access | | | | |
| [basic_stacktrace::operator[]](operator_at.html "cpp/utility/basic stacktrace/operator at") | | | | |
| basic_stacktrace::at | | | | |
| Modifiers | | | | |
| ****basic_stacktrace::swap**** | | | | |
| Non-member functions | | | | |
| operator== operator<=> | | | | |
| swap(std::basic_stacktrace) | | | | |
| to_string(std::basic_stacktrace) | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| hash<std::basic_stacktrace> | | | | |
| formatter<std::basic_stacktrace> | | | | |

|  |  |  |
| --- | --- | --- |
| void swap( basic_stacktrace& other ) noexcept(/\* see below \*/); |  | (since C++23) |
|  |  |  |

Exchanges the contents of the container with those of `other`. Does not invoke any move, copy, or swap operations on individual `stacktrace_entry` objects.

All iterators and references remain valid. The `end()` iterator is invalidated.

If std::allocator_traits<allocator_type>::propagate_on_container_swap::value is true, then the allocators are exchanged using an unqualified call to non-member `swap`. Otherwise, they are not swapped (and if get_allocator() != other.get_allocator(), the behavior is undefined).

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | `basic_stacktrace` to exchange the contents with |

### Return value

(none)

### Exceptions

noexcept specification:noexcept(std::allocator_traits<Allocator>::propagate_on_container_swap::value  
|| std::allocator_traits<Allocator>::is_always_equal::value)

### Complexity

Constant.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| std::swap(std::basic_stacktrace)(C++23) | specializes the std::swap algorithm   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/basic_stacktrace/swap&oldid=126288>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 January 2021, at 16:20.