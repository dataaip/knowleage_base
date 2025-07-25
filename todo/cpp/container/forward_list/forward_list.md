# std::forward_list<T,Allocator>::forward_list

From cppreference.com
< cpp‎ | container‎ | forward list
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

std::forward_list

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****forward_list::forward_list**** | | | | | | forward_list::~forward_list | | | | | | forward_list::operator= | | | | | | forward_list::assign | | | | | | forward_list::assign_range(C++23) | | | | | | forward_list::get_allocator | | | | | | Element access | | | | | | forward_list::front | | | | | | Iterators | | | | | | forward_list::before_beginforward_list::cbefore_begin | | | | | | forward_list::beginforward_list::cbegin | | | | | | forward_list::endforward_list::cend | | | | | | Capacity | | | | | | forward_list::empty | | | | | | forward_list::max_size | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | forward_list::clear | | | | | | forward_list::emplace_front | | | | | | forward_list::push_front | | | | | | forward_list::insert_after | | | | | | forward_list::emplace_after | | | | | | forward_list::erase_after | | | | | | forward_list::insert_range_after(C++23) | | | | | | forward_list::prepend_range(C++23) | | | | | | forward_list::pop_front | | | | | | forward_list::resize | | | | | | forward_list::swap | | | | | | Operations | | | | | | forward_list::merge | | | | | | forward_list::splice_after | | | | | | forward_list::removeforward_list::remove_if | | | | | | forward_list::reverse | | | | | | forward_list::unique | | | | | | forward_list::sort | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::forward_list) | | | | | | erase(std::forward_list)erase_if(std::forward_list)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| forward_list() : forward_list(Allocator()) {} | (1) |  |
| explicit forward_list( const Allocator& alloc ); | (2) |  |
| explicit forward_list( size_type count,                         const Allocator& alloc = Allocator() ); | (3) |  |
| forward_list( size_type count, const T& value,         const Allocator& alloc = Allocator() ); | (4) |  |
| template< class InputIt >  forward_list( InputIt first, InputIt last, const Allocator& alloc = Allocator() ); | (5) |  |
| template< container-compatible-range<T> R >  forward_list( std::from_range_t, R&& rg, const Allocator& alloc = Allocator() ); | (6) | (since C++23) |
| forward_list( const forward_list& other ); | (7) |  |
| forward_list( forward_list&& other ); | (8) |  |
|  |  |  |
| --- | --- | --- |
|  | (9) |  |
| forward_list( const forward_list& other, const Allocator& alloc ); |  | (until C++23) |
| forward_list( const forward_list& other,                const std::type_identity_t<Allocator>& alloc ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
|  | (10) |  |
| forward_list( forward_list&& other, const Allocator& alloc ); |  | (until C++23) |
| forward_list( forward_list&& other,                const std::type_identity_t<Allocator>& alloc ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| forward_list( std::initializer_list<T> init,                const Allocator& alloc = Allocator() ); | (11) |  |
|  |  |  |

Constructs a new `forward_list` from a variety of data sources, optionally using a user supplied allocator alloc.

1) The default constructor. Constructs an empty `forward_list` with a default-constructed allocator. If `Allocator` is not DefaultConstructible, the behavior is undefined.2) Constructs an empty `forward_list` with the given allocator alloc.3) Constructs a `forward_list` with count default-inserted objects of `T`. No copies are made. If `T` is not DefaultInsertable into std::forward_list<T>, the behavior is undefined.4) Constructs a `forward_list` with count copies of elements with value value. If `T` is not CopyInsertable into std::forward_list<T>, the behavior is undefined.5) Constructs a `forward_list` with the contents of the range ``first`,`last`)`. Each iterator in `[`first`,`last`)` is dereferenced exactly once. This overload participates in overload resolution only if `InputIt` satisfies the requirements of [LegacyInputIterator. If `T` is not EmplaceConstructible into std::forward_list<T> from \*first, the behavior is undefined.6) Constructs a `forward_list` with the contents of the range rg. Each iterator in rg is dereferenced exactly once. If `T` is not EmplaceConstructible into std::forward_list<T> from \*ranges::begin(rg), the behavior is undefined.7-10) Constructs a `forward_list` with the contents of other.7) The copy constructor. The allocator is obtained as if by calling std::allocator_traits<Allocator>::  
    select_on_container_copy_construction  
        (other.get_allocator()).8) The move constructor. The allocator is obtained by move construction from other.get_allocator().9) Same as the copy constructor, except that alloc is used as the allocator. If `T` is not CopyInsertable into std::forward_list<T>, the behavior is undefined.10) Same as the move constructor, except that alloc is used as the allocator. If `T` is not MoveInsertable into std::forward_list<T>, the behavior is undefined.11) Equivalent to forward_list(il.begin(), il.end(), alloc).

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use for all memory allocations of this container |
| count | - | the size of the container |
| value | - | the value to initialize elements of the container with |
| first, last | - | the range to copy the elements from |
| other | - | another container to be used as source to initialize the elements of the container with |
| init | - | initializer list to initialize the elements of the container with |
| rg | - | a container compatible range |

### Complexity

1,2) Constant.3,4) Linear in count.5) Linear in std::distance(first, last).6) Linear in ranges::distance(rg).7) Linear in other.size().8) Constant.9) Linear in other.size().10) Linear in other.size() if alloc != other.get_allocator(), otherwise constant.11) Linear in init.size().

### Exceptions

Calls to Allocator::allocate may throw.

### Notes

After container move construction (overload (8)), references, pointers, and iterators (other than the end iterator) to `other` remain valid, but refer to elements that are now in \*this. The current standard makes this guarantee via the blanket statement in [[container.reqmts]/67](https://eel.is/c++draft/container.reqmts#67), and a more direct guarantee is under consideration via LWG issue 2321.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overload (6) |

### Example

Run this code

```
#include <forward_list>
#include <iostream>
#include <string>
 
template<typename T>
std::ostream& operator<<(std::ostream& s, const std::forward_list<T>& v)
{
    s.put('{');
    for (char comma[]{'\0', ' ', '\0'}; const auto& e : v)
        s << comma << e, comma[0] = ',';
    return s << "}\n";
}
 
int main()
{
    // C++11 initializer list syntax:
    std::forward_list<std::string> words1{"the", "frogurt", "is", "also", "cursed"};
    std::cout << "1: " << words1;
 
    // words2 == words1
    std::forward_list<std::string> words2(words1.begin(), words1.end());
    std::cout << "2: " << words2;
 
    // words3 == words1
    std::forward_list<std::string> words3(words1);
    std::cout << "3: " << words3;
 
    // words4 is {"Mo", "Mo", "Mo", "Mo", "Mo"}
    std::forward_list<std::string> words4(5, "Mo");
    std::cout << "4: " << words4;
 
    const auto rg = {"cat", "cow", "crow"};
#ifdef __cpp_lib_containers_ranges
    std::forward_list<std::string> words5(std::from_range, rg); // overload (6)
#else
    std::forward_list<std::string> words5(rg.begin(), rg.end()); // overload (5)
#endif
    std::cout << "5: " << words5;
}

```

Output:

```
1: {the, frogurt, is, also, cursed}
2: {the, frogurt, is, also, cursed}
3: {the, frogurt, is, also, cursed}
4: {Mo, Mo, Mo, Mo, Mo}
5: {cat, cow, crow}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2193 | C++11 | the default constructor was explicit | made non-explicit |
| LWG 2210 | C++11 | overload (3) did not have an allocator parameter | added the parameter |
| N3346 | C++11 | for overload (3), the elements in the container were value-initialized | they are default-inserted |

### See also

|  |  |
| --- | --- |
| assign | assigns values to the container   (public member function) |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/forward_list/forward_list&oldid=177597>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 November 2024, at 19:33.