# std::flat_map<Key,T,Compare,KeyContainer,MappedContainer>::clear

From cppreference.com
< cpp‎ | container‎ | flat map
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

std::flat_map

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_map::flat_map | | | | | | flat_map::operator= | | | | | | Element access | | | | | | flat_map::at | | | | | | [flat_map::operator[]](operator_at.html "cpp/container/flat map/operator at") | | | | | | Iterators | | | | | | flat_map::beginflat_map::cbegin | | | | | | flat_map::endflat_map::cend | | | | | | flat_map::rbeginflat_map::crbegin | | | | | | flat_map::rendflat_map::crend | | | | | | Lookup | | | | | | flat_map::count | | | | | | flat_map::find | | | | | | flat_map::contains | | | | | | flat_map::equal_range | | | | | | flat_map::lower_bound | | | | | | flat_map::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | flat_map::size | | | | | | flat_map::max_size | | | | | | flat_map::empty | | | | | | Modifiers | | | | | | ****flat_map::clear**** | | | | | | flat_map::erase | | | | | | flat_map::swap | | | | | | flat_map::emplace | | | | | | flat_map::extract | | | | | | flat_map::replace | | | | | | flat_map::insert | | | | | | flat_map::insert_range | | | | | | flat_map::insert_or_assign | | | | | | flat_map::emplace_hint | | | | | | flat_map::try_emplace | | | | | | Observers | | | | | | flat_map::key_comp | | | | | | flat_map::keys | | | | | | flat_map::value_comp | | | | | | flat_map::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_map) | | | | | | erase_if(std::flat_map) | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_map> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| void clear() noexcept; |  | (since C++23) |
|  |  |  |

Erases all elements from the container adaptor. After this call, size() returns zero.

Invalidates any references, pointers, and iterators referring to contained elements.

### Parameters

(none)

### Return value

(none)

### Complexity

Linear in the size of the container adaptor, i.e., the number of elements.

### Example

Run this code

```
#include <iostream>
#include <string_view>
#include <flat_map>
 
void print_info(std::string_view rem, const std::flat_map<int, char>& v)
{
    std::cout << rem << "{ ";
    for (const auto& [key, value] : v)
        std::cout << '[' << key << "]:" << value << ' ';
    std::cout << "}\n";
    std::cout << "Size=" << v.size() << '\n';
}
 
int main()
{
    std::flat_map<int, char> container{{1, 'x'}, {2, 'y'}, {3, 'z'}};
    print_info("Before clear: ", container);
    container.clear();
    print_info("After clear: ", container);
}

```

Output:

```
Before clear: { [1]:x [2]:y [3]:z }
Size=3
After clear: { }
Size=0

```

### See also

|  |  |
| --- | --- |
| erase | erases elements   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_map/clear&oldid=168968>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 January 2024, at 05:14.