# std::inplace_vector<T,N>::try_emplace_back

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | ****inplace_vector::try_emplace_back**** | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| template< class... Args >  constexpr pointer try_emplace_back( Args&&... args ); |  | (since C++26) |
|  |  |  |

Conditionally appends an object of type `T` to the end of the container.

If size() == capacity() is true, there are no effects. Otherwise, appends direct-non-list-initialized with std::forward<Args>(args)... object of type `T`.

No iterators or references are invalidated, except `end()`, which is invalidated if the insertion occurs.

### Parameters

|  |  |  |
| --- | --- | --- |
| args | - | arguments to forward to the constructor of the element |
| Type requirements | | |
| -`T` must be EmplaceConstructible into `inplace_vector` from std::forward<Args>(args).... | | |

### Return value

std::addressof(back()) if size() < capacity(), nullptr otherwise.

### Complexity

Constant.

### Exceptions

Any exception thrown by initialization of inserted element. If an exception is thrown for any reason, this function has no effect (strong exception safety guarantee).

### Notes

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Explain the purpose of this API. |

### Example

Run this code

```
#include <cassert>
#include <complex>
#include <inplace_vector>
 
int main()
{
    using namespace std::complex_literals;
    using C = std::complex<double>;
    using I = std::inplace_vector<C, 3>;
    auto v = I{1.0 + 2.0i, 3.0 + 4.0i};
 
    C* c = v.try_emplace_back(5.0, 6.0);
    assert(*c == 5.0 + 6.0i);
    assert((v == I{1.0 + 2.0i, 3.0 + 4.0i, 5.0 + 6.0i}));
 
    c = v.try_emplace_back(7.0, 8.0); // no space => no insertion
    assert(c == nullptr);
    assert((v == I{1.0 + 2.0i, 3.0 + 4.0i, 5.0 + 6.0i}));
}

```

### See also

|  |  |
| --- | --- |
| emplace_back | constructs an element in-place at the end   (public member function) |
| push_back | adds an element to the end   (public member function) |
| append_range | adds a range of elements to the end   (public member function) |
| try_append_range | tries to add a range of elements to the end   (public member function) |
| unchecked_emplace_back | unconditionally constructs an element in-place at the end   (public member function) |
| unchecked_push_back | unconditionally adds an element to the end   (public member function) |
| pop_back | removes the last element   (public member function) |
| back_inserter | creates a std::back_insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/try_emplace_back&oldid=175521>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 August 2024, at 03:11.