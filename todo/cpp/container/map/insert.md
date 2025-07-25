# std::map<Key,T,Compare,Allocator>::insert

From cppreference.com
< cpp‎ | container‎ | map
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

`std::map`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | map::map | | | | | | map::~map | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | map::operator= | | | | | | map::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | map::at | | | | | | [map::operator[]](operator_at.html "cpp/container/map/operator at") | | | | | | Iterators | | | | | | map::beginmap::cbegin(C++11) | | | | | | map::endmap::cend(C++11) | | | | | | map::rbeginmap::crbegin(C++11) | | | | | | map::rendmap::crend(C++11) | | | | | | Capacity | | | | | | map::size | | | | | | map::max_size | | | | | | map::empty | | | | | | Observers | | | | | | map::key_comp | | | | | | map::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | map::clear | | | | | | ****map::insert**** | | | | | | map::erase | | | | | | map::swap | | | | | | map::extract(C++17) | | | | | | map::merge(C++17) | | | | | | map::insert_range(C++23) | | | | | | map::insert_or_assign(C++17) | | | | | | map::emplace(C++11) | | | | | | map::emplace_hint(C++11) | | | | | | map::try_emplace(C++17) | | | | | | Lookup | | | | | | map::count | | | | | | map::find | | | | | | map::contains(C++20) | | | | | | map::equal_range | | | | | | map::lower_bound | | | | | | map::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::map) | | | | | | erase_if(std::map)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| std::pair<iterator, bool> insert( const value_type& value ); | (1) |  |
| template< class P >  std::pair<iterator, bool> insert( P&& value ); | (2) | (since C++11) |
| std::pair<iterator, bool> insert( value_type&& value ); | (3) | (since C++17) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| iterator insert( iterator pos, const value_type& value ); |  | (until C++11) |
| iterator insert( const_iterator pos, const value_type& value ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| template< class P >  iterator insert( const_iterator pos, P&& value ); | (5) | (since C++11) |
| iterator insert( const_iterator pos, value_type&& value ); | (6) | (since C++17) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (7) |  |
| void insert( std::initializer_list<value_type> ilist ); | (8) | (since C++11) |
| insert_return_type insert( node_type&& nh ); | (9) | (since C++17) |
| iterator insert( const_iterator pos, node_type&& nh ); | (10) | (since C++17) |
|  |  |  |

Inserts element(s) into the container, if the container doesn't already contain an element with an equivalent key.

1-3) Inserts value. Overload (2) is equivalent to emplace(std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.4-6) Inserts value in the position as close as possible to the position just prior to pos. Overload (5) is equivalent to emplace_hint(hint, std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.7) Inserts elements from range ``first`,`last`)`. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending [LWG2844).8) Inserts elements from initializer list ilist. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).9) If nh is an empty node handle, does nothing. Otherwise, inserts the element owned by nh into the container , if the container doesn't already contain an element with a key equivalent to nh.key(). The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().10) If nh is an empty node handle, does nothing and returns the end iterator. Otherwise, inserts the element owned by nh into the container, if the container doesn't already contain an element with a key equivalent to nh.key(), and returns the iterator pointing to the element with key equivalent to nh.key()(regardless of whether the insert succeeded or failed). If the insertion succeeds, nh is moved from, otherwise it retains ownership of the element. The element is inserted as close as possible to the position just prior to pos. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().

No iterators or references are invalidated. If the insertion is successful, pointers and references to the element obtained while it is held in the node handle are invalidated, and pointers and references obtained to that element before it was extracted become valid.(since C++17)

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator to the position before which the new element will be inserted |
| value | - | element value to insert |
| first, last | - | range of elements to insert |
| ilist | - | initializer list to insert the values from |
| nh | - | a compatible node handle |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

1-3) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.4-6) An iterator to the inserted element, or to the element that prevented the insertion.7,8) (none)9) An object of `insert_return_type` with the members initialized as follows:

- If nh is empty, `inserted` is false, `position` is end(), and `node` is empty.
- Otherwise if the insertion took place, `inserted` is true, `position` points to the inserted element, and `node` is empty.
- If the insertion failed, `inserted` is false, `node` has the previous value of nh, and `position` points to an element with a key equivalent to nh.key().
10) End iterator if nh was empty, iterator pointing to the inserted element if insertion took place, and iterator pointing to an element with a key equivalent to nh.key() if it failed.

### Exceptions

1-6) If an exception is thrown by any operation, the insertion has no effect.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: cases 7-10 |

### Complexity

1-3) Logarithmic in the size of the container, `O(log(size()))`.4-6) Amortized constant if the insertion happens in the position just **after**(until C++11)**before**(since C++11) pos, logarithmic in the size of the container otherwise.7,8) `O(N·log(size() + N))`, where `N` is the number of elements to insert.9) Logarithmic in the size of the container, `O(log(size()))`.10) Amortized constant if the insertion happens in the position just **before** pos, logarithmic in the size of the container otherwise.

### Notes

The hinted insert (4-6) does not return a boolean in order to be signature-compatible with positional insert on sequential containers, such as std::vector::insert. This makes it possible to create generic inserters such as std::inserter. One way to check success of a hinted insert is to compare `size()` before and after.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <map>
#include <string>
using namespace std::literals;
 
template<typename It>
void print_insertion_status(It it, bool success)
{
    std::cout << "Insertion of " << it->first
              << (success ? " succeeded\n" : " failed\n");
}
 
int main()
{
    std::map<std::string, float> heights;
 
    // Overload 3: insert from rvalue reference
    const auto [it_hinata, success] = heights.insert({"Hinata"s, 162.8});
    print_insertion_status(it_hinata, success);
 
    {
        // Overload 1: insert from lvalue reference
        const auto [it, success2] = heights.insert(*it_hinata);
        print_insertion_status(it, success2);
    }
    {
        // Overload 2: insert via forwarding to emplace
        const auto [it, success] = heights.insert(std::pair{"Kageyama", 180.6});
        print_insertion_status(it, success);
    }
    {
        // Overload 6: insert from rvalue reference with positional hint
        const std::size_t n = std::size(heights);
        const auto it = heights.insert(it_hinata, {"Azumane"s, 184.7});
        print_insertion_status(it, std::size(heights) != n);
    }
    {
        // Overload 4: insert from lvalue reference with positional hint
        const std::size_t n = std::size(heights);
        const auto it = heights.insert(it_hinata, *it_hinata);
        print_insertion_status(it, std::size(heights) != n);
    }
    {
        // Overload 5: insert via forwarding to emplace with positional hint
        const std::size_t n = std::size(heights);
        const auto it = heights.insert(it_hinata, std::pair{"Tsukishima", 188.3});
        print_insertion_status(it, std::size(heights) != n);
    }
 
    auto node_hinata = heights.extract(it_hinata);
    std::map<std::string, float> heights2;
 
    // Overload 7: insert from iterator range
    heights2.insert(std::begin(heights), std::end(heights));
 
    // Overload 8: insert from initializer_list
    heights2.insert({{"Kozume"s, 169.2}, {"Kuroo", 187.7}});
 
    // Overload 9: insert node
    const auto status = heights2.insert(std::move(node_hinata));
    print_insertion_status(status.position, status.inserted);
 
    node_hinata = heights2.extract(status.position);
    {
        // Overload 10: insert node with positional hint
        const std::size_t n = std::size(heights2);
        const auto it = heights2.insert(std::begin(heights2), std::move(node_hinata));
        print_insertion_status(it, std::size(heights2) != n);
    }
 
    // Print resulting map
    std::cout << std::left << '\n';
    for (const auto& [name, height] : heights2)
        std::cout << std::setw(10) << name << " | " << height << "cm\n";
}

```

Output:

```
Insertion of Hinata succeeded
Insertion of Hinata failed
Insertion of Kageyama succeeded
Insertion of Azumane succeeded
Insertion of Hinata failed
Insertion of Tsukishima succeeded
Insertion of Hinata succeeded
Insertion of Hinata succeeded
 
Azumane    | 184.7cm
Hinata     | 162.8cm
Kageyama   | 180.6cm
Kozume     | 169.2cm
Kuroo      | 187.7cm
Tsukishima | 188.3cm

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 233 | C++98 | pos was just a hint, it could be totally ignored | the insertion is required to be as close as possible to the position just prior to pos |
| LWG 264 | C++98 | the complexity of overload (7) was required to be linear if the range ``first`,`last`)` is sorted according to `Compare` | removed the linear requirement in this special case |
| [LWG 316 | C++98 | in the return value of overload (1), it was not specified which bool value indicates a successful insertion | success is indicated by true |
| LWG 2005 | C++11 | overloads (2,5) were poorly described | improved the description |

### See also

|  |  |
| --- | --- |
| emplace(C++11) | constructs element in-place   (public member function) |
| emplace_hint(C++11) | constructs elements in-place using a hint   (public member function) |
| insert_or_assign(C++17) | inserts an element or assigns to the current element if the key already exists   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/map/insert&oldid=170188>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 March 2024, at 10:35.