# std::experimental::erase_if (std::map)

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
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/map>` |  |  |
| template< class Key, class T, class Compare, class Alloc, class Pred >  void erase_if( std::map<Key, T, Compare, Alloc>& c, Pred pred ); |  | (library fundamentals TS v2) |
|  |  |  |

Erases all elements that satisfy the predicate pred from the container. Equivalent to

```
for (auto i = c.begin(), last = c.end(); i != last;)
{
    if (pred(*i))
        i = c.erase(i);
    else
        ++i;
}

```

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | container from which to erase |
| pred | - | predicate that determines which elements should be erased |

### Complexity

Linear.

### Example

Run this code

```
#include <experimental/map>
#include <iostream>
 
template<typename Os, typename Container>
inline Os& operator<<(Os& os, Container const& cont)
{
    os << '{';
    for (const auto& item : cont)
        os << '{' << item.first << ", " << item.second << '}';
    return os << '}';
}
 
int main()
{
    std::map<int, char> data{{1, 'a'},{2, 'b'},{3, 'c'},{4, 'd'},
                             {5, 'e'},{4, 'f'},{5, 'g'},{5, 'g'}};
    std::cout << "Original:\n" << data << '\n';
    std::experimental::erase_if(data, [](const auto& item)
    {
        return (item.first & 1) == 1;
    });
    std::cout << "Erase items with odd keys:\n" << data << '\n';
}

```

Output:

```
Original:
{{1, a}{2, b}{3, c}{4, d}{5, e}}
Erase items with odd keys:
{{2, b}{4, d}}

```

### See also

|  |  |
| --- | --- |
| removeremove_if | removes elements satisfying specific criteria   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/map/erase_if&oldid=98559>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2018, at 20:27.