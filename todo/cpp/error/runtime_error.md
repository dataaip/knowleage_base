# std::runtime_error

From cppreference.com
< cpp‎ | error
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | ****runtime_error**** | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdexcept>` |  |  |
| class runtime_error; |  |  |
|  |  |  |

Defines a type of object to be thrown as exception. It reports errors that are due to events beyond the scope of the program and cannot be easily predicted.

!std-runtime error-inheritance.svg

Inheritance diagram

Exceptions of type `std::runtime_error` are thrown by the following standard library components:

- std::locale::locale
- std::locale::combine

|  |  |
| --- | --- |
| - std::chrono::current_zone - std::chrono::get_tzdb_list - std::chrono::get_tzdb - std::chrono::locate_zone - std::chrono::reload_tzdb - std::chrono::remote_version - std::chrono::tzdb::locate_zone | (since C++20) |

In addition, the following standard exception types are derived from `std::runtime_error`:

- std::range_error
- std::overflow_error
- std::underflow_error

|  |  |
| --- | --- |
| - std::ios_base::failure - std::regex_error - std::system_error | (since C++11) |

|  |  |
| --- | --- |
| - std::filesystem::filesystem_error | (since C++17) |

|  |  |
| --- | --- |
| - std::chrono::ambiguous_local_time - std::chrono::nonexistent_local_time - std::format_error | (since C++20) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `runtime_error` object with the given message   (public member function) |
| operator= | replaces the `runtime_error` object   (public member function) |

## std::runtime_error::runtime_error

|  |  |  |
| --- | --- | --- |
| runtime_error( const std::string& what_arg ); | (1) |  |
| runtime_error( const char\* what_arg ); | (2) |  |
| runtime_error( const runtime_error& other ); | (3) | (noexcept since C++11) |
|  |  |  |

1) Constructs the exception object with what_arg as explanatory string. After construction, std::strcmp(what(), what_arg.c_str()) == 0.2) Constructs the exception object with what_arg as explanatory string. After construction, std::strcmp(what(), what_arg) == 0.3) Copy constructor. If \*this and other both have dynamic type `std::runtime_error` then std::strcmp(what(), other.what()) == 0. No exception can be thrown from the copy constructor.

### Parameters

|  |  |  |
| --- | --- | --- |
| what_arg | - | explanatory string |
| other | - | another exception object to copy |

### Exceptions

1,2) May throw std::bad_alloc.

### Notes

Because copying `std::runtime_error` is not permitted to throw exceptions, this message is typically stored internally as a separately-allocated reference-counted string. This is also why there is no constructor taking `std::string&&`: it would have to copy the content anyway.

Before the resolution of LWG issue 254, the non-copy constructor can only accept std::string. It makes dynamic allocation mandatory in order to construct a std::string object.

After the resolution of LWG issue 471, a derived standard exception class must have a publicly accessible copy constructor. It can be implicitly defined as long as the explanatory strings obtained by `what()` are the same for the original object and the copied object.

## std::runtime_error::operator=

|  |  |  |
| --- | --- | --- |
| runtime_error& operator=( const runtime_error& other ); |  | (noexcept since C++11) |
|  |  |  |

Assigns the contents with those of other. If \*this and other both have dynamic type `std::runtime_error` then std::strcmp(what(), other.what()) == 0 after assignment. No exception can be thrown from the copy assignment operator.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another exception object to assign with |

### Return value

\*this

### Notes

After the resolution of LWG issue 471, a derived standard exception class must have a publicly accessible copy assignment operator. It can be implicitly defined as long as the explanatory strings obtained by `what()` are the same for the original object and the copied object.

## Inherited from std::exception

### Member functions

|  |  |
| --- | --- |
| (destructor)[virtual] | destroys the exception object   (virtual public member function of `std::exception`) |
| what[virtual] | returns an explanatory string   (virtual public member function of `std::exception`) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 254 | C++98 | the constructor accepting const char\* was missing | added |
| LWG 471 | C++98 | the explanatory strings of `std::runtime_error`'s copies were implementation-defined | they are the same as that of the original `std::runtime_error` object |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error/runtime_error&oldid=176323>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 September 2024, at 18:10.