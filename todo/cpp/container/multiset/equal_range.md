# std::multiset<Key,Compare,Allocator>::equal_range

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multiset::beginmultiset::cbegin(C++11) | | | | | | multiset::endmultiset::cend(C++11) | | | | | | multiset::rbeginmultiset::crbegin(C++11) | | | | | | multiset::rendmultiset::crend(C++11) | | | | | | Capacity | | | | | | multiset::size | | | | | | multiset::max_size | | | | | | multiset::empty | | | | | | Observers | | | | | | multiset::key_comp | | | | | | multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multiset::clear | | | | | | multiset::erase | | | | | | multiset::swap | | | | | | multiset::extract(C++17) | | | | | | multiset::merge(C++17) | | | | | | multiset::insert | | | | | | multiset::insert_range(C++23) | | | | | | multiset::emplace(C++11) | | | | | | multiset::emplace_hint(C++11) | | | | | | Lookup | | | | | | multiset::count | | | | | | multiset::find | | | | | | multiset::contains(C++20) | | | | | | ****multiset::equal_range**** | | | | | | multiset::lower_bound | | | | | | multiset::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::multiset) | | | | | | erase_if(std::multiset)(C++20) | | | | | | operator==operator<=>(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
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

|  |  |
| --- | --- |
| Since `emplace` and unhinted `insert` always insert at the upper bound, the order of equivalent elements in the equal range is the order of insertion unless hinted `insert` or `emplace_hint` was used to insert an element at a different position. | (since C++11) |

### Complexity

Logarithmic in the size of the container.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_generic_associative_lookup` | `201304L` | (C++14) | Heterogeneous comparison lookup in associative containers, for overloads (3,4) |

### Example

Run this code

```
#include <iostream>
#include <set>
 
template<typename I>
void print_equal_range(I first, I lb, I ub, I last)
{
    for (I i{first}; i != lb; ++i)
        std::cout << *i << ' ';
    std::cout << "[ ";
 
    for (I i{lb}; i != ub; ++i)
        std::cout << *i << ' ';
    std::cout << ") ";
 
    for (I i{ub}; i != last; ++i)
        std::cout << *i << ' ';
    std::cout << '\n';
}
 
int main()
{
    std::multiset<int> c{4, 3, 2, 1, 3, 3};
    std::cout << "c = ";
    print_equal_range(begin(c), begin(c), end(c), end(c));
    for (int key{}; key != 6; ++key)
    {
        std::cout << "key = " << key << "; equal range = ";
        const auto [lb, ub] = c.equal_range(key);
        print_equal_range(begin(c), lb, ub, end(c));
    }
}

```

Output:

```
c =  1 2 3 3 3 4 )
key = 0; equal range = [ ) 1 2 3 3 3 4
key = 1; equal range = [ 1 ) 2 3 3 3 4
key = 2; equal range = 1 [ 2 ) 3 3 3 4
key = 3; equal range = 1 2 [ 3 3 3 ) 4
key = 4; equal range = 1 2 3 3 3 [ 4 )
key = 5; equal range = 1 2 3 3 3 4 [ )

```

### See also

|  |  |
| --- | --- |
| [find | finds element with specific key   (public member function) |
| contains(C++20) | checks if the container contains element with specific key   (public member function) |
| count | returns the number of elements matching specific key   (public member function) |
| upper_bound | returns an iterator to the first element **greater** than the given key   (public member function) |
| lower_bound | returns an iterator to the first element **not less** than the given key   (public member function) |
| equal_range | returns range of elements matching a specific key   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multiset/equal_range&oldid=135916>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 18:10.