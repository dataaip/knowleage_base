# std::inplace_vector<T,N>::inplace_vector

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****inplace_vector::inplace_vector**** | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr inplace_vector() noexcept; | (1) | (since C++26) |
| constexpr explicit inplace_vector( size_type count ); | (2) | (since C++26) |
| constexpr inplace_vector( size_type count, const T& value ); | (3) | (since C++26) |
| template< class InputIt >  constexpr inplace_vector( InputIt first, InputIt last ); | (4) | (since C++26) |
| template< /\*container-compatible-range\*/<T> R >  constexpr inplace_vector( std::from_range_t, R&& rg ); | (5) | (since C++26) |
| constexpr inplace_vector( const inplace_vector& other ); | (6) | (since C++26) |
| constexpr inplace_vector( inplace_vector&& other )      noexcept(N == 0 || std::is_nothrow_move_constructible_v<T>); | (7) | (since C++26) |
| constexpr inplace_vector( std::initializer_list<T> init ); | (8) | (since C++26) |
|  |  |  |

Constructs a new `inplace_vector` from a variety of data sources.

1) Constructs an empty `inplace_vector` whose data() == nullptr and size() == 0.2) Constructs an `inplace_vector` with count default-inserted elements.3) Constructs an `inplace_vector` with count copies of elements with value value.4) Constructs an `inplace_vector` with the contents of the range ``first`,`last`)`.5) Constructs an `inplace_vector` with the contents of the range rg. For the definition of /\*container-compatible-range\*/, see [ranges::to.6) A copy constructor. Constructs an `inplace_vector` with the copy of the contents of other. The constructor is a trivial copy constructor if N > 0 and std::is_trivially_copy_constructible_v<T> are both true.7) A move constructor. Constructs an `inplace_vector` with the contents of other using move semantics. The constructor is a trivial move constructor if N > 0 and std::is_trivially_move_constructible_v<T> are both true.8) Constructs an `inplace_vector` with the contents of the initializer list init.

### Parameters

|  |  |  |
| --- | --- | --- |
| count | - | the size of the container |
| value | - | the value to initialize elements of the container with |
| first, last | - | the range ``first`,`last`)` to copy the elements from |
| rg | - | the range of values to initialize elements of the container with |
| other | - | another `inplace_vector` to be used as source to initialize the elements of the container with |
| init | - | initializer list to initialize the elements of the container with |
| Type requirements | | |
| -`T` must meet the requirements of [DefaultInsertable in order to use overloads (2,3). | | |

### Complexity

1) Constant.2,3) Linear in count.4) Linear in std::distance(first, last).5) Linear in std::ranges::distance(rg).6,7) Linear in size of other.8) Linear in size of init.

### Exceptions

2,3) Throws std::bad_alloc if count > N.5) Throws std::bad_alloc if std::ranges::size(rg) > N.8) Throws std::bad_alloc if init.size() > N.

### Example

Run this code

```
#include <cassert>
#include <initializer_list>
#include <inplace_vector>
#include <new>
#include <print>
#include <ranges>
 
int main()
{
    std::inplace_vector<int, 4> v1; // overload (1)
    assert(v1.size() == 0 && v1.capacity() == 4);
 
    std::inplace_vector<int, 0> v2; // overload (1), N == 0 is allowed
    assert(v2.size() == 0 && v2.capacity() == 0);
 
    std::inplace_vector<int, 5> v3(3); // overload (2)
    assert(v3.size() == 3 && v3.capacity() == 5);
    std::println("v3 = {}", v3);
 
    try
    {
        std::inplace_vector<int, 3> v(4); // overload (2), throws: count > N
    }
    catch(const std::bad_alloc& ex1)
    {
        std::println("ex1.what(): {}", ex1.what());
    }
 
    std::inplace_vector<int, 5> v4(3, 8); // overload (3)
    assert(v4.size() == 3 && v4.capacity() == 5);
    std::println("v4 = {}", v4);
 
    try
    {
        std::inplace_vector<int, 3> v(4, 2); // overload (3), throws: count > N
    }
    catch(const std::bad_alloc& ex2)
    {
        std::println("ex2.what(): {}", ex2.what());
    }
 
    const auto init = {1, 2, 3};
 
    std::inplace_vector<int, 4> v5(init.begin(), init.end()); // overload (4)
    assert(v5.size() == 3 && v5.capacity() == 4);
    std::println("v5 = {}", v5);
 
    std::inplace_vector<int, 4> v6(std::from_range, init); // overload (5)
    assert(v6.size() == 3 && v6.capacity() == 4);
    std::println("v6 = {}", v6);
 
    std::inplace_vector<int, 4> v7(v6); // overload (6)
    assert(v7.size() == 3 && v7.capacity() == 4);
    std::println("v7 = {}", v7);
    assert(v6.size() == 3);
 
    std::inplace_vector<int, 4> v8(std::move(v6)); // overload (7)
    // Note that after the move v6 is left in valid but indeterminate state.
    assert(v8.size() == 3 && v8.capacity() == 4);
    std::println("v8 = {}", v8);
 
    std::inplace_vector<int, 4> v9(init); // overload (8)
    assert(v9.size() == 3 && v9.capacity() == 4);
    std::println("v9 = {}", v9);
 
    try
    {
        std::inplace_vector<int, 2> v(init); // overload (8), throws: init.size() > N
    }
    catch(const std::bad_alloc& ex3)
    {
        std::println("ex3.what(): {}", ex3.what());
    }
}

```

Possible output:

```
v3 = [0, 0, 0]
ex1.what(): std::bad_alloc
v4 = [42, 42, 42]
ex2.what(): std::bad_alloc
v5 = [1, 2, 3]
v6 = [1, 2, 3]
v7 = [1, 2, 3]
v8 = [1, 2, 3]
v9 = [1, 2, 3]
ex3.what(): std::bad_alloc

```

### See also

|  |  |
| --- | --- |
| operator= | assigns values to the container   (public member function) |
| capacity[static] | returns the number of elements that can be held in currently allocated storage   (public static member function) |
| data | direct access to the underlying contiguous storage   (public member function) |
| size | returns the number of elements   (public member function) |
| sizessize(C++17)(C++20) | returns the size of a container or array   (function template) |
| data(C++17) | obtains the pointer to the underlying array   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/inplace_vector&oldid=177323>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 October 2024, at 17:58.