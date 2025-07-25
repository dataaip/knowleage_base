# std::set_terminate

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | ****set_terminate**** | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<exception>` |  |  |
|  |  |  |
| --- | --- | --- |
| std::terminate_handler set_terminate( std::terminate_handler f ) throw(); |  | (until C++11) |
| std::terminate_handler set_terminate( std::terminate_handler f ) noexcept; |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Makes f the new global terminate handler function and returns the previously installed std::terminate_handler. f shall terminate execution of the program without returning to its caller, otherwise the behavior is undefined.

|  |  |
| --- | --- |
| This function is thread-safe. Every call to `std::set_terminate` **synchronizes-with** (see std::memory_order) subsequent calls to `std::set_terminate` and std::get_terminate. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| f | - | pointer to function of type std::terminate_handler, or null pointer |

### Return value

The previously-installed terminate handler, or a null pointer value if none was installed.

### Example

Run this code

```
#include <cstdlib>
#include <exception>
#include <iostream>
 
int main()
{
    std::set_terminate([]()
    {
        std::cout << "Unhandled exception\n" << std::flush;
        std::abort();
    });
    throw 1;
}

```

Possible output:

```
Unhandled exception
bash: line 7:  7743 Aborted                 (core dumped) ./a.out

```

The terminate handler will also work for launched threads, so it can be used as an alternative to wrapping the thread function with a try/catch block. In the following example, since the exception is unhandled, std::terminate will be called.

Run this code

```
#include <iostream>
#include <thread>
 
void run()
{
    throw std::runtime_error("Thread failure");
}
 
int main()
{
    try
    {
        std::thread t{run};
        t.join();
        return EXIT_SUCCESS;
    }
    catch (const std::exception& ex)
    {
        std::cerr << "Exception: " << ex.what() << '\n';
    }
    catch (...)
    {
        std::cerr << "Unknown exception caught\n";
    }
    return EXIT_FAILURE;
}

```

Possible output:

```
terminate called after throwing an instance of 'std::runtime_error'
  what():  Thread failure
Aborted (core dumped)

```

With the introduction of the terminate handler, the exception thrown from the non-main thread can be analyzed, and exit can be gracefully performed.

Run this code

```
#include <iostream>
#include <thread>
 
class foo
{
public:
    foo() { std::cerr << "foo::foo()\n"; }
    ~foo() { std::cerr << "foo::~foo()\n"; }
};
 
// Static object, expecting destructor on exit
foo f;
 
void run()
{
    throw std::runtime_error("Thread failure");
}
 
int main()
{
    std::set_terminate([]()
    {
        try
        {
            std::exception_ptr eptr{std::current_exception()};
            if (eptr)
            {
                std::rethrow_exception(eptr);
            }
            else
            {
                std::cerr << "Exiting without exception\n";
            }
        }
        catch (const std::exception& ex)
        {
            std::cerr << "Exception: " << ex.what() << '\n';
        }
        catch (...)
        {
            std::cerr << "Unknown exception caught\n";
        }
        std::exit(EXIT_FAILURE);
    });
 
    std::thread t{run};
    t.join();
}

```

Output:

```
foo::foo()
Exception: Thread failure
foo::~foo()

```

### See also

|  |  |
| --- | --- |
| terminate | function called when exception handling fails   (function) |
| get_terminate(C++11) | obtains the current terminate_handler   (function) |
| terminate_handler | the type of the function called by std::terminate   (typedef) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error/set_terminate&oldid=173429>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 July 2024, at 10:28.