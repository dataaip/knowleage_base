# std::inplace_vector<T,N>::resize

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | ****inplace_vector::resize**** | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr void resize( size_type count ); | (1) | (since C++26) |
| constexpr void resize( size_type count, const value_type& value ); | (2) | (since C++26) |
|  |  |  |

Resizes the container to contain count elements, does nothing if count == size().

If the current size is greater than count, the container is reduced to its first count elements.

If the current size is less than count, then:

1) Additional default-inserted elements are appended.2) Additional copies of value are appended.

### Parameters

|  |  |  |
| --- | --- | --- |
| count | - | new size of the container |
| value | - | the value to initialize the new elements with |
| Type requirements | | |
| -`T` must meet the requirements of DefaultInsertable in order to use overload (1). | | |
| -`T` must meet the requirements of CopyInsertable in order to use overload (2). | | |

### Complexity

Linear in the difference between the current size and count.

### Exceptions

1,2) Throws std::bad_alloc if count > N.

If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).

### Example

Run this code

```
#include <inplace_vector>
#include <print>
 
int main()
{
    std::inplace_vector<int, 6> v(6, 9);
    std::println("Initially, v = {}", v);
 
    v.resize(2);
    std::println("After resize(2), v = {}", v);
 
    v.resize(4);
    std::println("After resize(4), v = {}", v);
 
    v.resize(6, -1);
    std::println("After resize(6, -1), v = {}", v);
 
    try
    {
        std::print("Trying resize(13): ");
        v.resize(13); // throws, because count > N; v is left unchanged
    }
    catch(const std::bad_alloc& ex)
    {
        std::println("ex.what(): {}", ex.what());
    }
    std::println("After exception, v = {}", v);
}

```

Possible output:

```
Initially, v = [9, 9, 9, 9, 9, 9]
After resize(2), v = [9, 9]
After resize(4), v = [9, 9, 0, 0]
After resize(6, -1), v = [9, 9, 0, 0, -1, -1]
Trying resize(13): ex.what(): std::bad_alloc
After exception, v = [9, 9, 0, 0, -1, -1]

```

### See also

|  |  |
| --- | --- |
| max_size[static] | returns the maximum possible number of elements   (public static member function) |
| size | returns the number of elements   (public member function) |
| capacity[static] | returns the number of elements that can be held in currently allocated storage   (public static member function) |
| empty | checks whether the container is empty   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/resize&oldid=175137>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 August 2024, at 10:15.