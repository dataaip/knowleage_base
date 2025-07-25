# std::inplace_vector<T,N>::operator=

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | ****inplace_vector::operator=**** | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr inplace_vector& operator=( const inplace_vector& other ); | (1) | (since C++26) |
| constexpr inplace_vector& operator=( inplace_vector&& other )      noexcept(/\* see below \*/); | (2) | (since C++26) |
| constexpr inplace_vector& operator=( std::initializer_list<T> init ); | (3) | (since C++26) |
|  |  |  |

Replaces the contents of the `inplace_vector`.

1) Copy assignment operator. Also a trivial copy assignment operator, if std::inplace_vector<T, N> has a trivial destructor, and std::is_trivially_copy_constructible_v<T> && std::is_trivially_copy_assignable_v<T> is true. Replaces the contents with a copy of the contents of other.2) Move assignment operator. Also a trivial move assignment operator, if std::inplace_vector<T, N> has a trivial destructor, and std::is_trivially_move_constructible_v<T> && std::is_trivially_move_assignable_v<T> is true. Replaces the contents with those of other using move semantics (i.e., the data in other is moved from other into this container). other is in a valid but unspecified state afterwards.3) Replaces the contents with those identified by initializer list init.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `inplace_vector` to be used as source to initialize the elements of the container with |
| init | - | initializer list to initialize the elements of the container with |

### Complexity

1,2) Linear in the size of \*this and other.3) Linear in the size of \*this and init.

### Exceptions

2)noexcept specification:noexcept(N == 0 ||  

(std::is_nothrow_move_assignable_v<T> &&

std::is_nothrow_move_constructible_v<T>))3) Throws std::bad_alloc if init.size() > N.

### Example

Run this code

```
#include <initializer_list>
#include <inplace_vector>
#include <new>
#include <print>
#include <ranges>
#include <string>
 
int main()
{
    std::inplace_vector<int, 4> x({1, 2, 3}), y;
    std::println("Initially:");
    std::println("x = {}", x);
    std::println("y = {}", y);
 
    std::println("Copy assignment copies data from x to y:");
    y = x; // overload (1)
    std::println("x = {}", x);
    std::println("y = {}", y);
 
    std::inplace_vector<std::string, 3> z, w{"\N{CAT}", "\N{GREEN HEART}"};
    std::println("Initially:");
    std::println("z = {}", z);
    std::println("w = {}", w);
 
    std::println("Move assignment moves data from w to z:");
    z = std::move(w); // overload (2)
    std::println("z = {}", z);
    std::println("w = {}", w); // w is in valid but unspecified state
 
    auto l = {4, 5, 6, 7};
    std::println("Assignment of initializer_list {} to x:", l);
    x = l; // overload (3)
    std::println("x = {}", x);
 
    std::println("Assignment of initializer_list with size bigger than N throws:");
    try
    {
        x = {1, 2, 3, 4, 5}; // throws: (initializer list size == 5) > (capacity N == 4)
    }
    catch(const std::bad_alloc& ex)
    {
        std::println("ex.what(): {}", ex.what());
    }
}

```

Possible output:

```
Initially:
x = [1, 2, 3]
y = []
Copy assignment copies data from x to y:
x = [1, 2, 3]
y = [1, 2, 3]
Initially:
z = []
w = ["🐈", "💚"]
Move assignment moves data from w to z:
z = ["🐈", "💚"]
w = ["", ""]
Assignment of initializer_list [4, 5, 6, 7] to x:
x = [4, 5, 6, 7]
Assignment of initializer_list with size bigger than N throws:
ex.what(): std::bad_alloc

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs the `inplace_vector`   (public member function) |
| assign | assigns values to the container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/operator%3D&oldid=175717>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2024, at 05:19.