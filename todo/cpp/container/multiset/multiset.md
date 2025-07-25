# std::multiset<Key,Compare,Allocator>::multiset

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****multiset::multiset**** | | | | | | multiset::~multiset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::operator= | | | | | | multiset::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multiset::beginmultiset::cbegin(C++11) | | | | | | multiset::endmultiset::cend(C++11) | | | | | | multiset::rbeginmultiset::crbegin(C++11) | | | | | | multiset::rendmultiset::crend(C++11) | | | | | | Capacity | | | | | | multiset::size | | | | | | multiset::max_size | | | | | | multiset::empty | | | | | | Observers | | | | | | multiset::key_comp | | | | | | multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multiset::clear | | | | | | multiset::erase | | | | | | multiset::swap | | | | | | multiset::extract(C++17) | | | | | | multiset::merge(C++17) | | | | | | multiset::insert | | | | | | multiset::insert_range(C++23) | | | | | | multiset::emplace(C++11) | | | | | | multiset::emplace_hint(C++11) | | | | | | Lookup | | | | | | multiset::count | | | | | | multiset::find | | | | | | multiset::contains(C++20) | | | | | | multiset::equal_range | | | | | | multiset::lower_bound | | | | | | multiset::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::multiset) | | | | | | erase_if(std::multiset)(C++20) | | | | | | operator==operator<=>(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| multiset(); |  | (until C++11) |
| multiset()      : multiset(Compare()) {} |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| explicit multiset( const Compare& comp,                     const Allocator& alloc = Allocator() ); | (2) |  |
| explicit multiset( const Allocator& alloc ); | (3) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt >  multiset( InputIt first, InputIt last,            const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (4) |  |
| template< class InputIt >  multiset( InputIt first, InputIt last,            const Allocator& alloc ) : multiset(first, last, Compare(), alloc) {} | (5) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| multiset( const multiset& other ); | (6) |  |
| multiset( const multiset& other, const Allocator& alloc ); | (7) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| multiset( multiset&& other ); | (8) | (since C++11) |
| multiset( multiset&& other, const Allocator& alloc ); | (9) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| multiset( std::initializer_list<value_type> init,  const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (10) | (since C++11) |
| multiset( std::initializer_list<value_type> init,  const Allocator& alloc ) : multiset(init, Compare(), alloc) {} | (11) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| template< container-compatible-range<value_type> R >  multiset( std::from_range_t, R&& rg,            const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (12) | (since C++23) |
| template< container-compatible-range<value_type> R >  multiset( std::from_range_t, R&& rg,            const Allocator& alloc ) : multiset(std::from_range, std::forward<R>(rg), Compare(), alloc) {} | (13) | (since C++23) |
|  |  |  |

Constructs new container from a variety of data sources and optionally using user supplied allocator alloc or comparison function object comp.

1-3) Constructs an empty container.4,5) Constructs the container with the contents of the range ``first`,`last`)`. If `[`first`,`last`)` is not a [valid range, the behavior is undefined.6,7) Copy constructor. Constructs the container with the copy of the contents of other.

|  |  |
| --- | --- |
| If alloc is not provided, allocator is obtained by calling std::allocator_traits<allocator_type>::     select_on_container_copy_construction(other.get_allocator()). | (since C++11) |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

8,9) Move constructor. Constructs the container with the contents of other using move semantics. If alloc is not provided, allocator is obtained by move-construction from the allocator belonging to other.

|  |  |
| --- | --- |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

10,11) Initializer-list constructor. Constructs the container with the contents of the initializer list init.12,13) Constructs the container with the contents of rg.

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | allocator to use for all memory allocations of this container |
| comp | - | comparison function object to use for all comparisons of keys |
| first, last | - | the range to copy the elements from |
| other | - | another container to be used as source to initialize the elements of the container with |
| init | - | initializer list to initialize the elements of the container with |
| rg | - | a container compatible range, that is, an `input_range` whose elements are convertible to `value_type` |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -`Compare` must meet the requirements of Compare. | | |
| -`Allocator` must meet the requirements of Allocator. | | |

### Complexity

1-3) Constant.4,5) \(\scriptsize N \cdot log(N)\)N·log(N) where \(\scriptsize N\)N is std::distance(first, last) in general, linear in \(\scriptsize N\)N if ``first`,`last`)` is already sorted by value_comp().6,7) Linear in size of other.8,9) Constant. If alloc is given and alloc != other.get_allocator(), then linear.10,11) \(\scriptsize N \cdot log(N)\)N·log(N) where \(\scriptsize N\)N is init.size() in general, linear in \(\scriptsize N\)N if init is already sorted by value_comp().12,13) \(\scriptsize N \cdot log(N)\)N·log(N) where \(\scriptsize N\)N is [ranges::distance(rg) in general, linear in \(\scriptsize N\)N if rg is already sorted by value_comp().

### Exceptions

Calls to `Allocator::allocate` may throw.

### Notes

After container move construction (overload (8,9)), references, pointers, and iterators (other than the end iterator) to `other` remain valid, but refer to elements that are now in \*this. The current standard makes this guarantee via the blanket statement in [[container.reqmts]/67](https://eel.is/c++draft/container.reqmts#67), and a more direct guarantee is under consideration via LWG issue 2321.

Although not formally required until C++23, some implementations has already put the template parameter `Allocator` into non-deduced contexts in earlier modes.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_containers_ranges` | `202202L` | (C++23) | Ranges-aware construction and insertion; overloads (12,13) |

### Example

Run this code

```
#include <iostream>
#include <set>
#include <string_view>
 
template <typename T>
void println(const std::string_view name, const std::multiset<T>& ms)
{
    std::cout << name << ": ";
    for (const auto& element : ms)
        std::cout << element << ' ';
    std::cout << '\n';
}
 
int main()
{
    // (1) Default constructor
    std::multiset<int> a;
    a.insert(4);
    a.insert(3);
    a.insert(2);
    a.insert(1);
    println("a", a);
 
    // (4) Range constructor
    std::multiset<int> b(a.begin(), a.find(3));
    println("b", b);
 
    // (6) Copy constructor
    std::multiset<int> c(a);
    println("c", c);
 
    // (8) Move constructor
    std::multiset<int> d(std::move(a));
    println("d", d);
 
    // (10) Initializer list constructor
    std::multiset<int> e{3, 2, 1, 2, 4, 7, 3};
    println("e", e);
 
    // (12) Range constructor
    const auto w = {"α", "β", "γ", "δ", "δ", "γ", "β", "α"};
#if __cpp_lib_containers_ranges
    std::multiset<std::string> f(std::from_range, w); // overload (12)
#else
    std::multiset<std::string> f(w.begin(), w.end()); // fallback to (4)
#endif
    println("f", f);
}

```

Output:

```
a: 1 2 3 4
b: 1 2
c: 1 2 3 4
d: 1 2 3 4
e: 1 2 2 3 3 4 7
f: α α β β γ γ δ δ

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2076 | C++11 | overload (4) conditionally required `Key` to be CopyInsertable into \*this | not required |
| LWG 2193 | C++11 | the default constructor was explicit | made non-explicit |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multiset/multiset&oldid=135716>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2021, at 06:38.