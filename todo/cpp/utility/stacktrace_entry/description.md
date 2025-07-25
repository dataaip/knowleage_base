# std::stacktrace_entry::description

From cppreference.com
< cpp‎ | utility‎ | stacktrace entry
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

std::stacktrace_entry

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| stacktrace_entry::stacktrace_entry | | | | |
| stacktrace_entry::operator= | | | | |
| Observers | | | | |
| stacktrace_entry::native_handle | | | | |
| stacktrace_entry::operator bool | | | | |
| Query | | | | |
| ****stacktrace_entry::description**** | | | | |
| stacktrace_entry::source_file | | | | |
| stacktrace_entry::source_line | | | | |
| Non-member functions | | | | |
| operator== operator<=> | | | | |
| to_string(std::stacktrace_entry) | | | | |
| operator<< | | | | |
| Helper classes | | | | |
| hash<std::stacktrace_entry> | | | | |
| formatter<std::stacktrace_entry> | | | | |

|  |  |  |
| --- | --- | --- |
| std::string description() const; |  | (since C++23) |
|  |  |  |

Returns a description of the evaluation represented by \*this on success, or an empty string on failure other than allocation failure, e.g. when \*this is empty.

### Parameters

(none)

### Return value

A description of the represented evaluation on success, an empty string on failure other than allocation failure.

### Exceptions

Throws std::bad_alloc if memory for the internal data structures or the resulting string cannot be allocated.

### Notes

Custom allocators support for this function is not provided, because the implementations usually require platform specific allocations, system calls and a lot of CPU intensive work, while a custom allocator does not provide benefits for this function as the platform specific operations take an order of magnitude more time than the allocation.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/stacktrace_entry/description&oldid=126238>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 January 2021, at 08:38.