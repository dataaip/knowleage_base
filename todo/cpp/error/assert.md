# assert

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | ****assert**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cassert>` |  |  |
| Disabled assertion |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| #define assert(condition) ((void)0) |  | (until C++26) |
| #define assert(...)       ((void)0) |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
| Enabled assertion |  |  |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| #define assert(condition) /\* unspecified \*/ |  | (until C++26) |
| #define assert(...)       /\* unspecified \*/ |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

The definition of the macro `assert` depends on another macro, NDEBUG, which is not defined by the standard library.

1) If NDEBUG is defined as a macro name at the point in the source code where <cassert> or <assert.h> is included, the assertion is disabled: `assert` does nothing.2) Otherwise, the assertion is enabled:

|  |  |
| --- | --- |
| `assert` checks if its argument (which must have scalar type):   - If the argument compares unequal to zero, there are no further effects. - Otherwise, `assert` creates a diagnostic on the standard error stream and calls std::abort(). | (until C++26) |
| `assert` puts a diagnostic test into programs and expands to an expression of type void. __VA_ARGS__ is evaluated and contextually converted to bool:   - If the evaluation yields true, there are no further effects. - Otherwise, `assert` creates a diagnostic on the standard error stream and calls std::abort(). | (since C++26) |

The diagnostic information has an implementation-defined format, but it always includes the following information:

|  |  |
| --- | --- |
| - the text of condition | (until C++26) |
| - #__VA_ARGS__ | (since C++26) |

- the source file name (i.e., __FILE__)
- the source line number (i.e., __LINE__)
- the name of the enclosing function (i.e., __func__)

|  |  |
| --- | --- |
| The expression assert(E) is guaranteed to be a constant subexpression, if either   - NDEBUG is defined at the point where `assert` is last defined or redefined, or - E, contextually converted to bool, is a constant subexpression that evaluates to true. | (since C++11) |

### Parameters

|  |  |  |
| --- | --- | --- |
| condition | - | expression of scalar type |

### Notes

|  |  |
| --- | --- |
| Because `assert` is a function-like macro, commas anywhere in the argument that are not protected by parentheses are interpreted as macro argument separators. Such commas are often found in template argument lists and list-initialization:   ```text assert(std::is_same_v<int, int>);        // error: assert does not take two arguments assert((std::is_same_v<int, int>));      // OK: one argument static_assert(std::is_same_v<int, int>); // OK: not a macro   std::complex<double> c; assert(c == std::complex<double>{0, 0});   // error assert((c == std::complex<double>{0, 0})); // OK ``` | (until C++26) |

There is no standardized interface to add an additional message to `assert` errors. A portable way to include one is to use a comma operator provided it has not been overloaded, or use `&&` with a string literal:

```
assert(("There are five lights", 2 + 2 == 5));
assert(2 + 2 == 5 && "There are five lights");

```

The implementation of `assert` in Microsoft CRT does not conform to C++11 and later revisions, because its underlying function (`_wassert`) takes neither __func__ nor an equivalent replacement.

Since C++20, the values needed for the diagnostic message can also be obtained from std::source_location::current().

Even though the change of `assert` in C23/C++26 is not formally a defect report, the C committee recommends implementations to backport the change to old modes.

### Example

Run this code

```
#include <iostream>
// uncomment to disable assert()
// #define NDEBUG
#include <cassert>
 
// Use (void) to silence unused warnings.
#define assertm(exp, msg) assert((void(msg), exp))
 
int main()
{
    assert(2 + 2 == 4);
    std::cout << "Checkpoint #1\n";
 
    assert((void("void helps to avoid 'unused value' warning"), 2 * 2 == 4));
    std::cout << "Checkpoint #2\n";
 
    assert((010 + 010 == 16) && "Yet another way to add an assert message");
    std::cout << "Checkpoint #3\n";
 
    assertm((2 + 2) % 3 == 1, "Success");
    std::cout << "Checkpoint #4\n";
 
    assertm(2 + 2 == 5, "Failed"); // assertion fails
    std::cout << "Execution continues past the last assert\n"; // No output
}

```

Possible output:

```
Checkpoint #1
Checkpoint #2
Checkpoint #3
Checkpoint #4
main.cpp:23: int main(): Assertion `((void)"Failed", 2 + 2 == 5)' failed.
Aborted

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2234 | C++11 | `assert` could not be used in constant expression | can be used |

### See also

|  |  |
| --- | --- |
| `static_assert` declaration (C++11) | performs compile-time assertion checking |
| abort | causes abnormal program termination (without cleaning up)   (function) |
| C documentation for assert | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error/assert&oldid=179835>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 January 2025, at 06:54.