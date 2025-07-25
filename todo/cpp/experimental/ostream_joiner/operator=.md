# std::experimental::ostream_joiner<DelimT,CharT,Traits>::operator=

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
| ****ostream_joiner::operator=**** | | | | |
| ostream_joiner::operator\* | | | | |
| ostream_joiner::operator++ostream_joiner::operator++(int) | | | | |
| Non-member functions | | | | |
| make_ostream_joiner | | | | |

|  |  |  |
| --- | --- | --- |
| template< class T >  ostream_joiner& operator=( const T& value ); | (1) | (library fundamentals TS v2) |
| ostream_joiner& operator=( const ostream_joiner& other ) = default; | (2) | (library fundamentals TS v2)  (implicitly declared) |
| ostream_joiner& operator=( ostream_joiner&& other ) = default; | (3) | (library fundamentals TS v2)  (implicitly declared) |
|  |  |  |

1) First, if the private "first element" flag is false, insert the delimiter `delim` into the output stream `os` associated with this iterator as if by os << delim;. Then, unconditionally sets the "first element" flag to false, and insert value into the output stream as if by os << value;. Let `out_stream`, `delim`, and `first_element` denote the private stream pointer, delimiter, and "first element" flag members respectively. Then this function is equivalent to

```
if (!first_element)
    *out_stream << delim;
first_element = false;
*out_stream << value;
return *this;

```

2,3) Implicitly declared copy/move assignment operator that copy/move assigns the private stream pointer, delimiter, and "first element" flag members.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | the object to to be written to the stream |
| other | - | the `ostream_joiner` object to be assigned to this object |

### Return value

\*this.

### Example

Run this code

```
#include <experimental/iterator>
#include <iostream>
 
int main()
{
    auto joiner = std::experimental::make_ostream_joiner(std::cout, ", ");
    joiner = "First";
    joiner = "do no harm.";  // prefixes with the delimiter
}

```

Output:

```
First, do no harm.

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/ostream_joiner/operator%3D&oldid=157745>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 23:09.