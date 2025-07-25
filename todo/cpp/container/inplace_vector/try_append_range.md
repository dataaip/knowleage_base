# std::inplace_vector<T,N>::try_append_range

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | ****inplace_vector::try_append_range**** | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| template< container-compatible-range<T> R >  constexpr std::ranges::borrowed_iterator_t<R> try_append_range( R&& rg ); |  | (since C++26) |
|  |  |  |

Appends copies of initial elements in rg before `end()`, until all elements are inserted or the internal storage is exhausted (i.e. size() == capacity() is true).

All iterators and references remain valid. The `end()` iterator is invalidated.

Each iterator in rg is dereferenced at most once.

### Parameters

|  |  |  |
| --- | --- | --- |
| rg | - | a container compatible range, that is, an `input_range` whose elements are convertible to `T` |
| Type requirements | | |
| -`T` must be EmplaceConstructible into `inplace_vector` from \*ranges::begin(rg). Otherwise, the behavior is undefined. | | |

### Return value

An iterator pointing to the first element of rg that was not inserted into \*this, or ranges::end(rg) if no such element exists.

### Complexity

Linear in the number of elements inserted.

### Exceptions

Any exception thrown by initialization of inserted element.

`inplace_vector` provides the **basic exception safety guarantee**, i.e., all elements of the container before the call are preserved, and all already inserted elements (before the exception, if any) are also preserved.

### Notes

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Explain the purpose of this API. |

### Example

Run this code

```
#include <cassert>
#include <initializer_list>
#include <inplace_vector>
 
int main()
{
    using I = std::inplace_vector<int, 8>;
    auto nums = I{1, 2, 3};
    const auto rg = {-1, -2, -3};
 
    auto it = nums.try_append_range(rg);
    assert(nums.size() == 6);
    assert((nums == I{1, 2, 3, -1, -2, -3}));
    assert(it == rg.end());
 
    it = nums.try_append_range(rg);
    assert(nums.size() == 8);
    assert((nums == I{1, 2, 3, -1, -2, -3, -1, -2}));
    assert(it == rg.begin() + 2);
}

```

### See also

|  |  |
| --- | --- |
| append_range | adds a range of elements to the end   (public member function) |
| push_back | adds an element to the end   (public member function) |
| try_push_back | tries to add an element to the end   (public member function) |
| unchecked_push_back | unconditionally adds an element to the end   (public member function) |
| emplace_back | constructs an element in-place at the end   (public member function) |
| try_emplace_back | tries to construct an element in-place at the end   (public member function) |
| unchecked_emplace_back | unconditionally constructs an element in-place at the end   (public member function) |
| pop_back | removes the last element   (public member function) |
| back_inserter | creates a std::back_insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/try_append_range&oldid=175514>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 August 2024, at 10:37.