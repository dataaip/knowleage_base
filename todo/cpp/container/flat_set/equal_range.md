# std::flat_set<Key,Compare,KeyContainer>::equal_range

From cppreference.com
< cpp‎ | container‎ | flat set
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

std::flat_set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_set::flat_set | | | | | | flat_set::operator= | | | | | | Iterators | | | | | | flat_set::beginflat_set::cbegin | | | | | | flat_set::endflat_set::cend | | | | | | flat_set::rbeginflat_set::crbegin | | | | | | flat_set::rendflat_set::crend | | | | | | Capacity | | | | | | flat_set::size | | | | | | flat_set::max_size | | | | | | flat_set::empty | | | | | | Observers | | | | | | flat_set::key_comp | | | | | | flat_set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_set::clear | | | | | | flat_set::insert | | | | | | flat_set::insert_range | | | | | | flat_set::emplace | | | | | | flat_set::emplace_hint | | | | | | flat_set::erase | | | | | | flat_set::swap | | | | | | flat_set::extract | | | | | | flat_set::replace | | | | | | Lookup | | | | | | flat_set::count | | | | | | flat_set::find | | | | | | flat_set::contains | | | | | | ****flat_set::equal_range**** | | | | | | flat_set::lower_bound | | | | | | flat_set::upper_bound | | | | | | | Non-member functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_set) | | | | | | erase_if(std::flat_set) | | | | | | |
| Helper classes | | | | |
| uses_allocator<std::flat_set> | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| std::pair<iterator, iterator> equal_range( const Key& key ); | (1) | (since C++23) |
| std::pair<const_iterator, const_iterator> equal_range( const Key& key ) const; | (2) | (since C++23) |
| template< class K >  std::pair<iterator, iterator> equal_range( const K& x ); | (3) | (since C++23) |
| template< class K >  std::pair<const_iterator, const_iterator> equal_range( const K& x ) const; | (4) | (since C++23) |
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

### Example

Run this code

```
#include <flat_set>
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
| contains | checks if the container contains element with specific key   (public member function) |
| count | returns the number of elements matching specific key   (public member function) |
| upper_bound | returns an iterator to the first element **greater** than the given key   (public member function) |
| lower_bound | returns an iterator to the first element **not less** than the given key   (public member function) |
| equal_range | returns range of elements matching a specific key   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_set/equal_range&oldid=169458>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 January 2024, at 08:02.