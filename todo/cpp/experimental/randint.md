# std::experimental::randint

From cppreference.com
< cpp‎ | experimental
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
| ****experimental::randint**** | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/random>` |  |  |
| template< class IntType >  IntType randint( IntType a, IntType b ); |  | (library fundamentals TS v2) |
|  |  |  |

Generates a random integer in the closed interval `[a, b]`.

### Parameters

|  |  |  |
| --- | --- | --- |
| a, b | - | integer values specifying the range |

### Return value

A random integer i in the closed interval `[a, b]`, produced using a thread-local instance of std::uniform_int_distribution<IntType> invoked with the per-thread random number engine.

### Remarks

If `IntType` is not one of short, int, long, long long, unsigned short, unsigned int, unsigned long, or unsigned long long, the program is ill-formed.

The behavior is undefined if a > b.

### Example

Run this code

```
#include <experimental/random>
#include <iostream>
 
int main()
{
    int random_number = std::experimental::randint(100, 999);
    std::cout << "random 3-digit number: " << random_number << '\n';
}

```

Possible output:

```
random 3-digit number: 273

```

### See also

|  |  |
| --- | --- |
| reseed | reseeds the per-thread random engine   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/randint&oldid=155222>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 July 2023, at 10:14.