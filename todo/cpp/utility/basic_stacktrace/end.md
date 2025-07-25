# std::basic_stacktrace<Allocator>::end, std::basic_stacktrace<Allocator>::cend

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
| ****basic_stacktrace::endbasic_stacktrace::cend**** | | | | |
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
| basic_stacktrace::swap | | | | |
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
| const_iterator end()  const noexcept; | (1) | (since C++23) |
| const_iterator cend() const noexcept; | (2) | (since C++23) |
|  |  |  |

Returns the iterator pointing past the last entry of the `basic_stacktrace`.

This iterator acts as a placeholder; attempting to dereference it results in undefined behavior.

!range-begin-end.svg

### Parameters

(none)

### Return value

The end iterator.

### Complexity

Constant.

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <stacktrace>
 
int main()
{
    auto trace       = std::stacktrace::current();
    auto empty_trace = std::stacktrace{};
 
    // Print stacktrace.
    std::for_each(trace.begin(), trace.end(),
                  [](const auto& f) { std::cout << f << '\n'; });
 
    if (empty_trace.begin() == empty_trace.end())
        std::cout << "stacktrace 'empty_trace' is indeed empty.\n";
}

```

Possible output:

```
0x0000000000402BA8 in ./prog.exe
__libc_start_main in /lib/x86_64-linux-gnu/libc.so.6
0x0000000000402A29 in ./prog.exe
stacktrace 'empty_trace' is indeed empty.

```

### See also

|  |  |
| --- | --- |
| begincbegin | returns an iterator to the beginning   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/basic_stacktrace/end&oldid=129024>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 May 2021, at 04:09.