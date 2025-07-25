# std::flat_multimap<Key,T,Compare,KeyContainer,MappedContainer>::rbegin, std::flat_multimap<Key,T,Compare,KeyContainer,MappedContainer>::crbegin

From cppreference.com
< cpp‎ | container‎ | flat multimap
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

std::flat_multimap

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_multimap::flat_multimap | | | | | | flat_multimap::operator= | | | | | | Modifiers | | | | | | flat_multimap::clear | | | | | | flat_multimap::erase | | | | | | flat_multimap::swap | | | | | | flat_multimap::extract | | | | | | flat_multimap::replace | | | | | | flat_multimap::insert | | | | | | flat_multimap::insert_range | | | | | | flat_multimap::emplace | | | | | | flat_multimap::emplace_hint | | | | | | Lookup | | | | | | flat_multimap::count | | | | | | flat_multimap::find | | | | | | flat_multimap::contains | | | | | | flat_multimap::equal_range | | | | | | flat_multimap::lower_bound | | | | | | flat_multimap::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | flat_multimap::beginflat_multimap::cbegin | | | | | | flat_multimap::endflat_multimap::cend | | | | | | ****flat_multimap::rbeginflat_multimap::crbegin**** | | | | | | flat_multimap::rendflat_multimap::crend | | | | | | Capacity | | | | | | flat_multimap::size | | | | | | flat_multimap::max_size | | | | | | flat_multimap::empty | | | | | | Observers | | | | | | flat_multimap::key_comp | | | | | | flat_multimap::keys | | | | | | flat_multimap::value_comp | | | | | | flat_multimap::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_multimap) | | | | | | erase_if(std::flat_multimap) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_multimap> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| reverse_iterator rbegin() noexcept; | (1) | (since C++23) |
| const_reverse_iterator rbegin() const noexcept; | (2) | (since C++23) |
| const_reverse_iterator crbegin() const noexcept; | (3) | (since C++23) |
|  |  |  |

Returns a reverse iterator to the first element of the reversed `flat_multimap`. It corresponds to the last element of the non-reversed `flat_multimap`. If the `flat_multimap` is empty, the returned iterator is equal to rend().

!range-rbegin-rend.svg

### Parameters

(none)

### Return value

Reverse iterator to the first element.

### Complexity

Constant.

### Notes

The underlying iterator of the returned reverse iterator is the end iterator. Hence the returned iterator is invalidated if and when the end iterator is invalidated.

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <string>
#include <flat_map>
 
int main()
{
    std::flat_multimap<std::string, int> map
    {
        {"█", 1},
        {"▒", 5},
        {"░", 3},
        {"▓", 7},
        {"▓", 8},
        {"░", 4},
        {"▒", 6},
        {"█", 2}
    };
 
    std::cout << "Print out in reverse order using const reverse iterators:\n";
    std::for_each(map.crbegin(), map.crend(),
        [](std::pair<const std::string, int> const& e)
        {
            std::cout << "{ \"" << e.first << "\", " << e.second << " };\n";
        });
 
    map.rbegin()->second = 42; // OK: non-const value is modifiable
//  map.crbegin()->second = 42; // Error: cannot modify the const value
}

```

Possible output:

```
Print out in reverse order using const reverse iterators:
{ "▓", 8 };
{ "▓", 7 };
{ "▒", 6 };
{ "▒", 5 };
{ "░", 4 };
{ "░", 3 };
{ "█", 2 };
{ "█", 1 };

```

### See also

|  |  |
| --- | --- |
| rendcrend | returns a reverse iterator to the end   (public member function) |
| rbegincrbegin(C++14) | returns a reverse iterator to the beginning of a container or array   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_multimap/rbegin&oldid=168835>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 January 2024, at 13:58.