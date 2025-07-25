# std::experimental::source_location::function_name

From cppreference.com
< cpp‎ | experimental‎ | source location
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::propagate_const | | | | |
| experimental::not_fn | | | | |
| experimental::observer_ptr | | | | |
| experimental::make_array | | | | |
| experimental::to_array | | | | |
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

std::experimental::source_location

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Creation | | | | |
| source_location::source_location | | | | |
| source_location::current | | | | |
| Field Access | | | | |
| source_location::line | | | | |
| source_location::column | | | | |
| source_location::file_name | | | | |
| ****source_location::function_name**** | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr const char\* function_name() const noexcept; |  | (library fundamentals TS v2) |
|  |  |  |

Returns the name of the function associated with the position represented by this object, if any.

### Parameters

(none)

### Return value

If this object represents a position in a body of a function, returns an implementation-defined null-terminated byte string corresponding to the name of the function.

Otherwise, an empty string is returned.

### Example

The following example shows how it is possible to use the `std::source_location::function_name()` to print a name of a function, constructor, destructor, or overloaded `operator()`.

Run this code

```
#include <experimental/source_location>
#include <iostream>
#include <string_view>
 
inline void function_name(
    const std::string_view signature = "()",
    const std::experimental::source_location& location
        = std::experimental::source_location::current())
{
    std::cout
        << location.function_name() // <- name of the caller!
        << signature
        << '\n';
}
 
void foo() { function_name(); }
 
struct S {
    S() { function_name(); }
    S(int) { function_name("(int)"); }
    S& operator=(S const&) { function_name("(const S&)"); return *this; }
    S& operator=(S&&) { function_name("(S&&)"); return *this; }
    ~S() { function_name(); }
};
 
int main()
{
    foo();
    S p;
    S q{42};
    p = q;
    p = std::move(q);
}

```

Possible output:

```
foo()
S()
S(int)
operator=(const S&)
operator=(S&&)
~S()
~S()

```

### See also

|  |  |
| --- | --- |
| line | return the line number represented by this object   (public member function) |
| column | return the column number represented by this object   (public member function) |
| file_name | return the file name represented by this object   (public member function) |
| C++ documentation for Filename and line information | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/source_location/function_name&oldid=117883>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 April 2020, at 07:43.