# std::experimental::make_ostream_joiner

From cppreference.com
< cpp‎ | experimental‎ | ostream joiner
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

std::experimental::ostream_joiner

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ostream_joiner::ostream_joiner | | | | |
| ostream_joiner::operator= | | | | |
| ostream_joiner::operator\* | | | | |
| ostream_joiner::operator++ostream_joiner::operator++(int) | | | | |
| Non-member functions | | | | |
| ****make_ostream_joiner**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/iterator>` |  |  |
| template< class CharT, class Traits, class DelimT >  std::experimental::ostream_joiner<std::decay_t<DelimT>, CharT, Traits>      make_ostream_joiner( std::basic_ostream<CharT, Traits>& os,                          DelimT&& delimiter ); |  | (library fundamentals TS v2) |
|  |  |  |

Creates an `ostream_joiner` object, deducing the template arguments from the types of the function arguments.

### Parameters

|  |  |  |
| --- | --- | --- |
| os | - | the `basic_ostream` object that the iterator is to be associated to |
| delimiter | - | the delimiter |

### Return value

An `ostream_joiner` object, created as if by std::experimental::ostream_joiner<std::decay_t<DelimT>, CharT, Traits>(os, std::forward<DelimT>(delimiter))

### Example

Run this code

```
#include <experimental/iterator>
#include <iostream>
#include <vector>
 
int main()
{
    std::vector<int> x{1, 2, 3, 4};
    std::copy(x.begin(), x.end(),
              std::experimental::make_ostream_joiner(std::cout, ", "));
}

```

Output:

```
1, 2, 3, 4

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ostream_joiner/make_ostream_joiner&oldid=155051>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 July 2023, at 09:30.