# std::map<Key,T,Compare,Allocator>::map

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****map::map**** | | | | | | map::~map | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | map::operator= | | | | | | map::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | map::at | | | | | | [map::operator[]](operator_at.html "cpp/container/map/operator at") | | | | | | Iterators | | | | | | map::beginmap::cbegin(C++11) | | | | | | map::endmap::cend(C++11) | | | | | | map::rbeginmap::crbegin(C++11) | | | | | | map::rendmap::crend(C++11) | | | | | | Capacity | | | | | | map::size | | | | | | map::max_size | | | | | | map::empty | | | | | | Observers | | | | | | map::key_comp | | | | | | map::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | map::clear | | | | | | map::insert | | | | | | map::erase | | | | | | map::swap | | | | | | map::extract(C++17) | | | | | | map::merge(C++17) | | | | | | map::insert_range(C++23) | | | | | | map::insert_or_assign(C++17) | | | | | | map::emplace(C++11) | | | | | | map::emplace_hint(C++11) | | | | | | map::try_emplace(C++17) | | | | | | Lookup | | | | | | map::count | | | | | | map::find | | | | | | map::contains(C++20) | | | | | | map::equal_range | | | | | | map::lower_bound | | | | | | map::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::map) | | | | | | erase_if(std::map)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| map(); |  | (until C++11) |
| map()      : map(Compare()) {} |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| explicit map( const Compare& comp,                const Allocator& alloc = Allocator() ); | (2) |  |
| explicit map( const Allocator& alloc ); | (3) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| template< class InputIt >  map( InputIt first, InputIt last,       const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (4) |  |
| template< class InputIt >  map( InputIt first, InputIt last,       const Allocator& alloc ) : map(first, last, Compare(), alloc) {} | (5) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| map( const map& other ); | (6) |  |
| map( const map& other, const Allocator& alloc ); | (7) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| map( map&& other ); | (8) | (since C++11) |
| map( map&& other, const Allocator& alloc ); | (9) | (since C++11) |
|  |  |  |
| --- | --- | --- |
| map( std::initializer_list<value_type> init,  const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (10) | (since C++11) |
| map( std::initializer_list<value_type> init,  const Allocator& alloc ) : map(init, Compare(), alloc) {} | (11) | (since C++14) |
|  |  |  |
| --- | --- | --- |
| template< container-compatible-range<value_type> R >  map( std::from_range_t, R&& rg,       const Compare& comp = Compare(), const Allocator& alloc = Allocator() ); | (12) | (since C++23) |
| template< container-compatible-range<value_type> R >  map( std::from_range_t, R&& rg,       const Allocator& alloc ) : map(std::from_range, std::forward<R>(rg), Compare(), alloc) {} | (13) | (since C++23) |
|  |  |  |

Constructs new container from a variety of data sources and optionally using user supplied allocator alloc or comparison function object comp.

1-3) Constructs an empty container.4,5) Constructs the container with the contents of the range ``first`,`last`)`. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending [LWG2844). If ``first`,`last`)` is not a [valid range, the behavior is undefined.6,7) Copy constructor. Constructs the container with the copy of the contents of other.

|  |  |
| --- | --- |
| If alloc is not provided, allocator is obtained by calling std::allocator_traits<allocator_type>::     select_on_container_copy_construction(other.get_allocator()). | (since C++11) |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

8,9) Move constructor. Constructs the container with the contents of other using move semantics. If alloc is not provided, allocator is obtained by move-construction from the allocator belonging to other.

|  |  |
| --- | --- |
| During class template argument deduction, only the first argument contributes to the deduction of the container's `Allocator` template parameter. | (since C++23) |

10,11) Initializer-list constructor. Constructs the container with the contents of the initializer list init.If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).12,13) Constructs the container with the contents of rg. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).

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
#include <iomanip>
#include <iostream>
#include <map>
#include <string>
 
template<typename Key, typename Value, typename Cmp>
std::ostream& operator<<(std::ostream& os, std::map<Key, Value, Cmp> const& map)
{
    os << "{ ";
    for (auto comma{map.size()}; auto const& p : map)
        os << '\'' << p.first << "' is " << p.second << (--comma ? ", " : " ");
    return os << "}\n";
}
 
struct Point
{
    double x, y;
 
    friend std::ostream& operator<<(std::ostream& os, Point pt)
    {
        return os << '(' << pt.x << ", " << pt.y << ')';
    }
};
 
struct PointCmp
{
    bool operator()(const Point& lhs, const Point& rhs) const
    {
        return lhs.x < rhs.x; // NB: y is intentionally ignored
    }
};
 
int main()
{
    // (1) Default constructor
    std::map<std::string, int> map1;
    map1["something"] = 69;
    map1["anything"] = 199;
    map1["that thing"] = 50;
    std::cout << "map1 = " << map1;
 
    // (4) Range constructor
    std::map<std::string, int> iter(map1.find("anything"), map1.end());
    std::cout << "\niter = " << iter;
    std::cout << "map1 = " << map1;
 
    // (6) Copy constructor
    std::map<std::string, int> copied(map1);
    std::cout << "\ncopied = " << copied;
    std::cout << "map1 = " << map1;
 
    // (8) Move constructor
    std::map<std::string, int> moved{std::move(map1)};
    std::cout << "\nmoved = " << moved;
    std::cout << "map1 = " << map1;
 
    // (10) Initializer list constructor
    const std::map<std::string, int> init
    {
        {"this", 100},
        {"can", 100},
        {"be", 100},
        {"const", 100}
    };
    std::cout << "\ninit = " << init;
 
    std::cout << "\nCustom Key class option 1:\n";
    // Use a comparison struct
    std::map<Point, double, PointCmp> mag =
    {
        {{5, -12}, 13},
        {{3, 4}, 5},
        {{-8, -15}, 17}
    };
    std::cout << "mag = " << mag << '\n';
 
    std::cout << "Custom Key class option 2:\n";
    // Use a comparison lambda
    // This lambda sorts points according to their magnitudes, where
    // these magnitudes are taken from the local variable mag.
    auto cmpLambda = &mag
    {
        return mag[lhs] < mag[rhs];
    };
 
    // You could also use a lambda that is not dependent on local variables, like this:
    // auto cmpLambda = [](const Point& lhs, const Point& rhs){ return lhs.y < rhs.y; };
    std::map<Point, double, decltype(cmpLambda)> magy(cmpLambda);
 
    // Various ways of inserting elements:
    magy.insert(std::pair<Point, double>({5, -12}, 13));
    magy.insert({{3, 4}, 5});
    magy.insert({Point{-8.0, -15.0}, 17});    
    std::cout << "magy = " << magy << '\n';
 
    std::cout << "Construction from a range:\n";
    using PS = std::pair<const std::string, int>;
    const auto rg = {PS{"one", 1}, {"one", 101}, {"two", 2}, {"three", 3}};
#if __cpp_lib_containers_ranges
    std::map<std::string, int> nums(std::from_range, rg); // overload (12)
#else
    std::map<std::string, int> nums(rg.begin(), rg.end()); // fallback to (4)
#endif
    std::cout << "nums = " << nums << '\n';
}

```

Output:

```
map1 = { 'anything' is 199, 'something' is 69, 'that thing' is 50 }
 
iter = { 'anything' is 199, 'something' is 69, 'that thing' is 50 }
map1 = { 'anything' is 199, 'something' is 69, 'that thing' is 50 }
 
copied = { 'anything' is 199, 'something' is 69, 'that thing' is 50 }
map1 = { 'anything' is 199, 'something' is 69, 'that thing' is 50 }
 
moved = { 'anything' is 199, 'something' is 69, 'that thing' is 50 }
map1 = { }
 
init = { 'be' is 100, 'can' is 100, 'const' is 100, 'this' is 100 }
 
Custom Key class option 1:
mag = { '(-8, -15)' is 17, '(3, 4)' is 5, '(5, -12)' is 13 }
 
Custom Key class option 2:
magy = { '(3, 4)' is 5, '(5, -12)' is 13, '(-8, -15)' is 17 }
 
Construction from a range:
nums = { 'one' is 1, 'three' is 3, 'two' is 2 }

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2076 | C++11 | overload (4) conditionally required `Key`and `T` to be CopyInsertable into \*this | not required |
| LWG 2193 | C++11 | the default constructor was explicit | made non-explicit |

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/map/map&oldid=135939>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 18:53.