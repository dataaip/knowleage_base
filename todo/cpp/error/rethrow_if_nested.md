# std::rethrow_if_nested

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | ****rethrow_if_nested****(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<exception>` |  |  |
| template< class E >  void rethrow_if_nested( const E& e ); |  | (since C++11)  (constexpr since C++26) |
|  |  |  |

If `E` is not a polymorphic class type, or if std::nested_exception is an inaccessible or ambiguous base class of `E`, there is no effect.

Otherwise, performs

```
if (auto p = dynamic_cast<const std::nested_exception*>(std::addressof(e)))
    p->rethrow_nested();

```

### Parameters

|  |  |  |
| --- | --- | --- |
| e | - | the exception object to rethrow |

### Notes

Unlike many related functions, this function is **not** intended to be called with a std::exception_ptr but rather an actual exception reference.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_constexpr_exceptions` | `202411L` | (C++26) | constexpr for exception types |

### Possible implementation

|  |
| --- |
| ```text namespace details {     template<class E>     struct can_dynamic_cast         : std::integral_constant<bool,               std::is_polymorphic<E>::value &&               (!std::is_base_of<std::nested_exception, E>::value ||                  std::is_convertible<E*, std::nested_exception*>::value)           > {};       template<class T>     void rethrow_if_nested_impl(const T& e, std::true_type)     {         if (auto nep = dynamic_cast<const std::nested_exception*>(std::addressof(e)))             nep->rethrow_nested();     }       template<class T>     void rethrow_if_nested_impl(const T&, std::false_type) {} }   template<class T> void rethrow_if_nested(const T& t) {     details::rethrow_if_nested_impl(t, details::can_dynamic_cast<T>()); } ``` |

### Example

Demonstrates construction and recursion through a nested exception object.

Run this code

```
#include <exception>
#include <fstream>
#include <iostream>
#include <stdexcept>
#include <string>
 
// prints the explanatory string of an exception. If the exception is nested,
// recurses to print the explanatory string of the exception it holds
void print_exception(const std::exception& e, int level =  0)
{
    std::cerr << std::string(level, ' ') << "exception: " << e.what() << '\n';
    try
    {
        std::rethrow_if_nested(e);
    }
    catch (const std::exception& nestedException)
    {
        print_exception(nestedException, level + 1);
    }
    catch (...) {}
}
 
// sample function that catches an exception and wraps it in a nested exception
void open_file(const std::string& s)
{
    try
    {
        std::ifstream file(s);
        file.exceptions(std::ios_base::failbit);
    }
    catch (...)
    {
        std::throw_with_nested(std::runtime_error("Couldn't open " + s));
    }
}
 
// sample function that catches an exception and wraps it in a nested exception
void run()
{
    try
    {
        open_file("nonexistent.file");
    }
    catch (...)
    {
        std::throw_with_nested(std::runtime_error("run() failed"));
    }
}
 
// runs the sample function above and prints the caught exception
int main()
{
    try
    {
        run();
    }
    catch (const std::exception& e)
    {
        print_exception(e);
    }
}

```

Possible output:

```
exception: run() failed
 exception: Couldn't open nonexistent.file
  exception: basic_ios::clear

```

### See also

|  |  |
| --- | --- |
| nested_exception(C++11) | a mixin type to capture and store current exceptions   (class) |
| throw_with_nested(C++11) | throws its argument with std::nested_exception mixed in   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error/rethrow_if_nested&oldid=177873>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 12:33.