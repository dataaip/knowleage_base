# std::deque<T,Allocator>::assign

From cppreference.com
< cpp‎ | container‎ | deque
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

std::deque

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | deque::deque | | | | | | deque::~deque | | | | | | deque::operator= | | | | | | ****deque::assign**** | | | | | | deque::assign_range(C++23) | | | | | | deque::get_allocator | | | | | | Element access | | | | | | deque::at | | | | | | [deque::operator[]](operator_at.html "cpp/container/deque/operator at") | | | | | | deque::front | | | | | | deque::back | | | | | | Iterators | | | | | | deque::begindeque::cbegin(C++11) | | | | | | deque::enddeque::cend(C++11) | | | | | | deque::rbegindeque::crbegin(C++11) | | | | | | deque::renddeque::crend(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | deque::empty | | | | | | deque::size | | | | | | deque::max_size | | | | | | deque::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | deque::clear | | | | | | deque::insert | | | | | | deque::insert_range(C++23) | | | | | | deque::emplace | | | | | | deque::erase | | | | | | deque::push_front | | | | | | deque::emplace_front(C++11) | | | | | | deque::prepend_range(C++23) | | | | | | deque::pop_front | | | | | | deque::push_back | | | | | | deque::emplace_back(C++11) | | | | | | deque::append_range(C++23) | | | | | | deque::pop_back | | | | | | deque::resize | | | | | | deque::swap | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::deque) | | | | | | erase(std::deque)erase_if(std::deque)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void assign( size_type count, const T& value ); | (1) |  |
| template< class InputIt >  void assign( InputIt first, InputIt last ); | (2) |  |
| void assign( std::initializer_list<T> ilist ); | (3) | (since C++11) |
|  |  |  |

Replaces the contents of the container.

1) Replaces the contents with count copies of value value.2) Replaces the contents with copies of those in the range ``first`,`last`)`. If either argument is an iterator into \*this, the behavior is undefined.

|  |  |
| --- | --- |
| This overload has the same effect as overload (1) if `InputIt` is an integral type. | (until C++11) |
| This overload participates in overload resolution only if `InputIt` satisfies [LegacyInputIterator. | (since C++11) |

3) Replaces the contents with the elements from ilist.

All iterators (including the `end()` iterator) and all references to the elements are invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| count | - | the new size of the container |
| value | - | the value to initialize elements of the container with |
| first, last | - | the range to copy the elements from |
| ilist | - | std::initializer_list to copy the values from |

### Complexity

1) Linear in count.2) Linear in distance between first and last.3) Linear in ilist.size().

### Example

The following code uses `assign` to add several characters to a std::deque<char>:

Run this code

```
#include <deque>
#include <iostream>
#include <string>
 
int main()
{
    std::deque<char> characters;
 
    auto print_deque = [&]()
    {
        for (char c : characters)
            std::cout << c << ' ';
        std::cout << '\n';
    };
 
    characters.assign(5, 'a');
    print_deque();
 
    const std::string extra(6, 'b');
    characters.assign(extra.begin(), extra.end());
    print_deque();
 
    characters.assign({'C', '+', '+', '1', '1'});
    print_deque();
}

```

Output:

```
a a a a a
b b b b b b
C + + 1 1

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2209 | C++98 | the replacement operation was required to be implemented as erasing all existing elements followed by inserting the given elements | removed the requirement |

### See also

|  |  |
| --- | --- |
| assign_range(C++23) | assigns a range of values to the container   (public member function) |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/deque/assign&oldid=135168>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 November 2021, at 17:50.