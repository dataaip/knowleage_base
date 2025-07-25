# std::set<Key,Compare,Allocator>::equal_range

From cppreference.com
< cpp‎ | container‎ | set
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

std::set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set::set | | | | | | set::~set | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set::operator= | | | | | | set::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | set::beginset::cbegin(C++11) | | | | | | set::endset::cend(C++11) | | | | | | set::rbeginset::crbegin(C++11) | | | | | | set::rendset::crend(C++11) | | | | | | Capacity | | | | | | set::size | | | | | | set::max_size | | | | | | set::empty | | | | | | Observers | | | | | | set::key_comp | | | | | | set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | set::clear | | | | | | set::erase | | | | | | set::swap | | | | | | set::extract(C++17) | | | | | | set::merge(C++17) | | | | | | set::insert | | | | | | set::insert_range(C++23) | | | | | | set::emplace(C++11) | | | | | | set::emplace_hint(C++11) | | | | | | Lookup | | | | | | set::count | | | | | | set::find | | | | | | set::contains(C++20) | | | | | | ****set::equal_range**** | | | | | | set::lower_bound | | | | | | set::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::set) | | | | | | erase_if(std::set)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| std::pair<iterator, iterator> equal_range( const Key& key ); | (1) |  |
| std::pair<const_iterator, const_iterator> equal_range( const Key& key ) const; | (2) |  |
| template< class K >  std::pair<iterator, iterator> equal_range( const K& x ); | (3) | (since C++14) |
| template< class K >  std::pair<const_iterator, const_iterator> equal_range( const K& x ) const; | (4) | (since C++14) |
|  |  |  |

Returns a range containing all elements with the given key in the container. The range is defined by two iterators, one pointing to the first element that is **not less** than key and another pointing to the first element **greater** than key. Alternatively, the first iterator may be obtained with lower_bound(), and the second with upper_bound().

1,2) Compares the keys to key.3,4) Compares the keys to the value x. This overload participates in overload resolution only if the qualified-id Compare::is_transparent is valid and denotes a type. It allows calling this function without constructing an instance of `Key`.

### Parameters

|  |  |  |
| --- | --- | --- |
| key | - | key value to compare the elements to |
| x | - | alternative value that can be compared to `Key` |

### Return value

std::pair containing a pair of iterators defining the wanted range: the first pointing to the first element that is not **less** than key and the second pointing to the first element **greater** than key.

If there are no elements **not less** than key, past-the-end (see end()) iterator is returned as the first element. Similarly if there are no elements **greater** than key, past-the-end iterator is returned as the second element.

### Complexity

Logarithmic in the size of the container.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_generic_associative_lookup` | `201304L` | (C++14) | Heterogeneous comparison lookup in associative containers, for overloads (3,4) |

### Example

Run this code

```
#include <set>
#include <functional>
#include <print>
#include <ranges>
#include <string>
#include <string_view>
#include <tuple>
 
struct Names
{
    std::string forename, surname;
    friend auto operator<(const Names& lhs, const Names& rhs)
    {
        return std::tie(lhs.surname, lhs.forename) < std::tie(rhs.surname, rhs.forename);
    }
};
 
struct SurnameCompare
{
    std::string_view surname;
 
    friend bool operator<(const Names& lhs, const SurnameCompare& rhs)
    {
        return lhs.surname < rhs.surname;
    }
 
    friend bool operator<(const SurnameCompare& lhs, const Names& rhs)
    {
        return lhs.surname < rhs.surname;
    }
}; 
 
std::set<Names, std::less<>> characters
{
    {"Homer", "Simpson"},
    {"Marge", "Simpson"},
    {"Lisa", "Simpson"},
    {"Ned", "Flanders"},
    {"Joe", "Quimby"}
};
 
void print_unique(const Names& names)
{
    auto [begin, end] = characters.equal_range(names);
    std::print(
        "Found {} characters with name \"{} {}\"\n", 
        std::distance(begin, end), 
        names.forename, names.surname
    );
}
 
void print_by_surname(std::string_view surname)
{
    auto [begin, end] = characters.equal_range(SurnameCompare{surname});
    std::print("Found {} characters with surname \"{}\":\n", std::distance(begin, end), surname);
    for (const Names& names : std::ranges::subrange(begin, end))
        std::print("    {} {}\n", names.forename, names.surname);
}
 
int main()
{
    print_unique({"Maude", "Flanders"});
    print_unique({"Lisa", "Simpson"});
    print_by_surname("Simpson");
}

```

Output:

```
Found 0 characters with name "Maude Flanders"
Found 1 characters with name "Lisa Simpson"
Found 3 characters with surname "Simpson":
    Homer Simpson
    Lisa Simpson
    Marge Simpson

```

### See also

|  |  |
| --- | --- |
| find | finds element with specific key   (public member function) |
| contains(C++20) | checks if the container contains element with specific key   (public member function) |
| count | returns the number of elements matching specific key   (public member function) |
| upper_bound | returns an iterator to the first element **greater** than the given key   (public member function) |
| lower_bound | returns an iterator to the first element **not less** than the given key   (public member function) |
| equal_range | returns range of elements matching a specific key   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/set/equal_range&oldid=135454>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2021, at 18:41.