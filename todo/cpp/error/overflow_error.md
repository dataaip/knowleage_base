# std::overflow_error

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | Error codes | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | ****overflow_error**** | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdexcept>` |  |  |
| class overflow_error; |  |  |
|  |  |  |

Defines a type of object to be thrown as exception. It can be used to report arithmetic overflow errors (that is, situations where a result of a computation is too large for the destination type).

|  |  |
| --- | --- |
| The only standard library component that throws this exception is std::bitset::to_ulong. | (until C++11) |
| The only standard library components that throw this exception are std::bitset::to_ulong and std::bitset::to_ullong. | (since C++11) |

The mathematical functions of the standard library components do not throw this exception (mathematical functions report overflow errors as specified in math_errhandling). Third-party libraries, however, use this. For example,
boost.math throws `std::overflow_error` if `boost::math::policies::throw_on_error` is enabled (the default setting).

!std-overflow error-inheritance.svg

Inheritance diagram

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `overflow_error` object with the given message   (public member function) |
| operator= | replaces the `overflow_error` object   (public member function) |

## std::overflow_error::overflow_error

|  |  |  |
| --- | --- | --- |
| overflow_error( const std::string& what_arg ); | (1) |  |
| overflow_error( const char\* what_arg ); | (2) |  |
| overflow_error( const overflow_error& other ); | (3) | (noexcept since C++11) |
|  |  |  |

1) Constructs the exception object with what_arg as explanatory string. After construction, std::strcmp(what(), what_arg.c_str()) == 0.2) Constructs the exception object with what_arg as explanatory string. After construction, std::strcmp(what(), what_arg) == 0.3) Copy constructor. If \*this and other both have dynamic type `std::overflow_error` then std::strcmp(what(), other.what()) == 0. No exception can be thrown from the copy constructor.

### Parameters

|  |  |  |
| --- | --- | --- |
| what_arg | - | explanatory string |
| other | - | another exception object to copy |

### Exceptions

1,2) May throw std::bad_alloc.

### Notes

Because copying `std::overflow_error` is not permitted to throw exceptions, this message is typically stored internally as a separately-allocated reference-counted string. This is also why there is no constructor taking `std::string&&`: it would have to copy the content anyway.

Before the resolution of LWG issue 254, the non-copy constructor can only accept std::string. It makes dynamic allocation mandatory in order to construct a std::string object.

After the resolution of LWG issue 471, a derived standard exception class must have a publicly accessible copy constructor. It can be implicitly defined as long as the explanatory strings obtained by `what()` are the same for the original object and the copied object.

## std::overflow_error::operator=

|  |  |  |
| --- | --- | --- |
| overflow_error& operator=( const overflow_error& other ); |  | (noexcept since C++11) |
|  |  |  |

Assigns the contents with those of other. If \*this and other both have dynamic type `std::overflow_error` then std::strcmp(what(), other.what()) == 0 after assignment. No exception can be thrown from the copy assignment operator.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another exception object to assign with |

### Return value

\*this

### Notes

After the resolution of LWG issue 471, a derived standard exception class must have a publicly accessible copy assignment operator. It can be implicitly defined as long as the explanatory strings obtained by `what()` are the same for the original object and the copied object.

## Inherited from std::runtime_error

## Inherited from std::exception

### Member functions

|  |  |
| --- | --- |
| (destructor)[virtual] | destroys the exception object   (virtual public member function of `std::exception`) |
| what[virtual] | returns an explanatory string   (virtual public member function of `std::exception`) |

### Example

Run this code

```
#include <iostream>
#include <limits>
#include <stdexcept>
#include <utility>
 
template<typename T, int N>
    requires (N > 0) /*...*/
class Stack
{
    int top_{-1};
    T data_[N];
 
public:
    [[nodiscard]] bool empty() const { return top_ == -1; }
 
    void push(T x)
    {
        if (top_ == N - 1)
            throw std::overflow_error("Stack overflow!");
        data_[++top_] = std::move(x);
    }
 
    void pop()
    {
        if (empty())
            throw std::underflow_error("Stack underflow!");
        --top_;
    }
 
    T const& top() const
    {
        if (empty())
            throw std::overflow_error("Stack is empty!");
        return data_[top_];
    }
};
 
int main()
{
    Stack<int, 4> st;
 
    try
    {
        [[maybe_unused]] auto x = st.top();
    }
    catch (std::overflow_error const& ex)
    {
        std::cout << "1) Exception: " << ex.what() << '\n';
    }
 
    st.push(1337);
    while (!st.empty())
    	st.pop();
 
    try
    {
        st.pop();
    }
    catch (std::underflow_error const& ex)
    {
        std::cout << "2) Exception: " << ex.what() << '\n';
    }
 
    try
    {
        for (int i{}; i != 13; ++i)
            st.push(i);
    }
    catch (std::overflow_error const& ex)
    {
        std::cout << "3) Exception: " << ex.what() << '\n';
    }
}

```

Output:

```
1) Exception: Stack is empty!
2) Exception: Stack underflow!
3) Exception: Stack overflow!

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 254 | C++98 | the constructor accepting const char\* was missing | added |
| LWG 471 | C++98 | the explanatory strings of `std::overflow_error`'s copies were implementation-defined | they are the same as that of the original `std::overflow_error` object |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error/overflow_error&oldid=160614>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 October 2023, at 12:42.