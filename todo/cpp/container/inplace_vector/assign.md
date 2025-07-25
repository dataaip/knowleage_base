# std::inplace_vector<T,N>::assign

From cppreference.com
< cpp‎ | container‎ | inplace vector
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

std::inplace_vector

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | ****inplace_vector::assign**** | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr void assign( size_type count, const T& value ); | (1) | (since C++26) |
| template< class InputIt >  constexpr void assign( InputIt first, InputIt last ); | (2) | (since C++26) |
| constexpr void assign( std::initializer_list<T> ilist ); | (3) | (since C++26) |
|  |  |  |

Replaces the contents of the container.

1) Replaces the contents with count copies of value value.2) Replaces the contents with copies of those in the range ``first`,`last`)`. If either argument is an iterator into \*this, the behavior is undefined.
This overload participates in overload resolution only if `InputIt` satisfies [LegacyInputIterator.3) Replaces the contents with the elements from ilist.

|  |  |
| --- | --- |
|  | This section is incomplete |

### Parameters

|  |  |  |
| --- | --- | --- |
| count | - | the new size of the container |
| value | - | the value to initialize elements of the container with |
| first, last | - | the range to copy the elements from |
| ilist | - | std::initializer_list to copy the values from |

### Complexity

1) Linear in count.2) Linear in distance between first and last.3) Linear in ilist.size().

### Exceptions

1) std::bad_alloc, if count > capacity().2) std::bad_alloc, if std::ranges::distance(first, last) > capacity().3) std::bad_alloc, if ilist.size() > capacity().1-3) Any exception thrown by initialization of inserted elements.

### Example

The following code uses `assign` to add several characters to a std::inplace_vector<char, 5>:

Run this code

```
#include <inplace_vector>
#include <iterator>
#include <new>
#include <print>
 
int main()
{
    std::inplace_vector<char, 5> chars;
 
    chars.assign(4, 'a'); // overload (1)
    std::println("{}", chars);
 
    const char extra[3]{'a', 'b', 'c'};
    chars.assign(std::cbegin(extra), std::cend(extra)); // overload (2)
    std::println("{}", chars);
 
    chars.assign({'C', '+', '+', '2', '6'}); // overload (3)
    std::println("{}", chars);
 
    try
    {
        chars.assign(8, 'x'); // throws: count > chars.capacity()
    }
    catch(const std::bad_alloc&) { std::println("std::bad_alloc #1"); }
 
    try
    {
        const char bad[8]{'?'}; // ranges::distance(bad) > chars.capacity()
        chars.assign(std::cbegin(bad), std::cend(bad)); // throws
    }
    catch(const std::bad_alloc&) { std::println("std::bad_alloc #2"); }
 
    try
    {
        const auto l = {'1', '2', '3', '4', '5', '6'};
        chars.assign(l); // throws: l.size() > chars.capacity()
    }
    catch(const std::bad_alloc&) { std::println("std::bad_alloc #3"); }
}

```

Output:

```
['a', 'a', 'a', 'a']
['a', 'b', 'c']
['C', '+', '+', '2', '6']
std::bad_alloc #1
std::bad_alloc #2
std::bad_alloc #3

```

### See also

|  |  |
| --- | --- |
| assign_range | assigns a range of values to the container   (public member function) |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/assign&oldid=175321>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 August 2024, at 05:54.