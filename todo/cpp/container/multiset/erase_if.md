# std::erase_if (std::multiset)

From cppreference.com
< cpp‎ | container‎ | multiset
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

std::multiset

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::multiset | | | | | | multiset::~multiset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::operator= | | | | | | multiset::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multiset::beginmultiset::cbegin(C++11) | | | | | | multiset::endmultiset::cend(C++11) | | | | | | multiset::rbeginmultiset::crbegin(C++11) | | | | | | multiset::rendmultiset::crend(C++11) | | | | | | Capacity | | | | | | multiset::size | | | | | | multiset::max_size | | | | | | multiset::empty | | | | | | Observers | | | | | | multiset::key_comp | | | | | | multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multiset::clear | | | | | | multiset::erase | | | | | | multiset::swap | | | | | | multiset::extract(C++17) | | | | | | multiset::merge(C++17) | | | | | | multiset::insert | | | | | | multiset::insert_range(C++23) | | | | | | multiset::emplace(C++11) | | | | | | multiset::emplace_hint(C++11) | | | | | | Lookup | | | | | | multiset::count | | | | | | multiset::find | | | | | | multiset::contains(C++20) | | | | | | multiset::equal_range | | | | | | multiset::lower_bound | | | | | | multiset::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::multiset) | | | | | | ****erase_if(std::multiset)****(C++20) | | | | | | operator==operator<=>(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<set>` |  |  |
| template< class Key, class Compare, class Alloc,  class Pred >  std::multiset<Key, Compare, Alloc>::size_type      erase_if( std::multiset<Key, Compare, Alloc>& c,               Pred pred ); |  | (since C++20) |
|  |  |  |

Erases all elements that satisfy the predicate pred from c.

Equivalent to

```
auto old_size = c.size();
for (auto first = c.begin(), last = c.end(); first != last;)
{
    if (pred(*first))
        first = c.erase(first);
    else
        ++first;
}
return old_size - c.size();

```

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | container from which to erase |
| pred | - | predicate that returns true if the element should be erased |

### Return value

The number of erased elements.

### Complexity

Linear.

### Example

Run this code

```
#include <iostream>
#include <set>
 
void println(auto rem, auto const& container)
{
    std::cout << rem << '{';
    for (char sep[]{0, ' ', 0}; const auto& item : container)
        std::cout << sep << item, *sep = ',';
    std::cout << "}\n";
}
 
int main()
{
    std::multiset data{3, 3, 4, 5, 5, 6, 6, 7, 2, 1, 0};
    println("Original:\n", data);
 
    auto divisible_by_3 = [](auto const& x) { return (x % 3) == 0; };
 
    const auto count = std::erase_if(data, divisible_by_3);
 
    println("Erase all items divisible by 3:\n", data);
    std::cout << count << " items erased.\n";
}

```

Output:

```
Original:
{0, 1, 2, 3, 3, 4, 5, 5, 6, 6, 7}
Erase all items divisible by 3:
{1, 2, 4, 5, 5, 7}
5 items erased.

```

### See also

|  |  |
| --- | --- |
| removeremove_if | removes elements satisfying specific criteria   (function template) |
| ranges::removeranges::remove_if(C++20)(C++20) | removes elements satisfying specific criteria (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multiset/erase_if&oldid=135725>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2021, at 06:59.