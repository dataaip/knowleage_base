# Diagnostics library

From cppreference.com
< cpp
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
| ****Diagnostics library**** | | | | |
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

****Diagnostics library****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

### Exception handling

The header <exception> provides several classes and functions related to exception handling in C++ programs.

|  |  |
| --- | --- |
| Defined in header `<exception>` | |
| exception | base class for exceptions thrown by the standard library components   (class) |
| Capture and storage of exception objects | |
| uncaught_exceptionuncaught_exceptions(removed in C++20\*)(C++17) | checks if exception handling is currently in progress   (function) |
| exception_ptr(C++11) | shared pointer type for handling exception objects   (typedef) |
| make_exception_ptr(C++11) | creates an std::exception_ptr from an exception object   (function template) |
| current_exception(C++11) | captures the current exception in a std::exception_ptr   (function) |
| rethrow_exception(C++11) | throws the exception from an std::exception_ptr   (function) |
| nested_exception(C++11) | a mixin type to capture and store current exceptions   (class) |
| throw_with_nested(C++11) | throws its argument with std::nested_exception mixed in   (function template) |
| rethrow_if_nested(C++11) | throws the exception from a std::nested_exception   (function template) |
| Handling of failures in exception handling | |
| Defined in header `<exception>` | |
| terminate | function called when exception handling fails   (function) |
| terminate_handler | the type of the function called by std::terminate   (typedef) |
| get_terminate(C++11) | obtains the current terminate_handler   (function) |
| set_terminate | changes the function to be called by std::terminate   (function) |
| bad_exception | exception thrown when std::current_exception fails to copy the exception object   (class) |
| Handling of exception specification violations (until C++17) | |
| unexpected(deprecated in C++11)(removed in C++17) | function called when dynamic exception specification is violated   (function) |
| unexpected_handler(deprecated in C++11)(removed in C++17) | the type of the function called by std::unexpected   (typedef) |
| get_unexpected(deprecated in C++11)(removed in C++17) | obtains the current `unexpected_handler`   (function) |
| set_unexpected(deprecated in C++11)(removed in C++17) | changes the function to be called by std::unexpected   (function) |

### Exception categories

Several convenience classes are predefined in the header `<stdexcept>` to report particular error conditions. These classes can be divided into two categories: **logic** errors and **runtime** errors. Logic errors are a consequence of faulty logic within the program and may be preventable. Runtime errors are due to events beyond the scope of the program and cannot easily be predicted.

|  |  |
| --- | --- |
| Defined in header `<stdexcept>` | |
| logic_error | exception class to indicate violations of logical preconditions or class invariants   (class) |
| invalid_argument | exception class to report invalid arguments   (class) |
| domain_error | exception class to report domain errors   (class) |
| length_error | exception class to report attempts to exceed maximum allowed size   (class) |
| out_of_range | exception class to report arguments outside of expected range   (class) |
| runtime_error | exception class to indicate conditions only detectable at run time   (class) |
| range_error | exception class to report range errors in internal computations   (class) |
| overflow_error | exception class to report arithmetic overflows   (class) |
| underflow_error | exception class to report arithmetic underflows   (class) |
| tx_exception(TM TS) | exception class to cancel atomic transactions   (class template) |

### Error numbers

|  |  |
| --- | --- |
| Defined in header `<cerrno>` | |
| errno | macro which expands to POSIX-compatible thread-local error number variable (macro variable) |
| E2BIG, EACCES, ..., EXDEV | macros for standard POSIX-compatible error conditions   (macro constant) |

### System error (since C++11)

The header `<system_error>` defines types and functions used to report error conditions originating from the operating system, streams I/O, std::future, or other low-level APIs.

|  |  |
| --- | --- |
| Defined in header `<system_error>` | |
| error_category(C++11) | base class for error categories   (class) |
| generic_category(C++11) | identifies the generic error category   (function) |
| system_category(C++11) | identifies the operating system error category   (function) |
| error_condition(C++11) | holds a portable error code   (class) |
| errc(C++11) | the std::error_condition enumeration listing all standard <cerrno> macro constants   (class) |
| error_code(C++11) | holds a platform-dependent error code   (class) |
| system_error(C++11) | exception class used to report conditions that have an error_code   (class) |

### Assertions

Assertions help to implement checking of preconditions in programs.

|  |  |
| --- | --- |
| Defined in header `<cassert>` | |
| assert | aborts the program if the user-specified condition is not true. May be disabled for release builds.   (function macro) |

### Stacktrace (since C++23)

|  |  |
| --- | --- |
| Defined in header `<stacktrace>` | |
| stacktrace_entry(C++23) | representation of an evaluation in a stacktrace   (class) |
| basic_stacktrace(C++23) | approximate representation of an invocation sequence consists of stacktrace entries   (class template) |

### Debugging support (since C++26)

|  |  |
| --- | --- |
| Defined in header `<debugging>` | |
| breakpoint(C++26) | pauses the running program when called   (function) |
| breakpoint_if_debugging(C++26) | calls std::breakpoint if std::is_debugger_present returns true   (function) |
| is_debugger_present(C++26) | checks whether a program is running under the control of a debugger   (function) |

### See also

|  |  |
| --- | --- |
| `static_assert` declaration (C++11) | performs compile-time assertion checking |
| C documentation for Error handling | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error&oldid=179907>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 11:35.