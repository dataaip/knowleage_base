# std::inplace_vector<T,N>::erase

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | ****inplace_vector::erase**** | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr iterator erase( const_iterator pos ); | (1) | (since C++26) |
| constexpr iterator erase( const_iterator first, const_iterator last ); | (2) | (since C++26) |
|  |  |  |

Erases the specified elements from the container.

1) Removes the element at pos.2) Removes the elements in the range ``first`,`last`)`.

Iterators (including the [`end()` iterator) and references to the elements at or after the point of the erase are invalidated.

The iterator pos must be valid and dereferenceable. Thus the end() iterator (which is valid, but is not dereferenceable) cannot be used as a value for pos.

The iterator first does not need to be dereferenceable if first == last: erasing an empty range is a no-op.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | iterator to the element to remove |
| first, last | - | range of elements to remove |

### Return value

Iterator following the last removed element.

1) If pos refers to the last element, then the end() iterator is returned.2) If last == end() prior to removal, then the updated end() iterator is returned. If ``first`,`last`)` is an empty range, then last is returned.

### Exceptions

Does not throw unless an exception is thrown by the assignment operator of `T`.

### Complexity

Linear: the number of calls to the destructor of `T` is the same as the number of elements erased, the assignment operator of `T` is called the number of times equal to the number of elements in the vector after the erased elements.

### Notes

When container elements need to be erased based on a predicate, rather than iterating the container and calling unary `erase`, the iterator range overload is generally used with [std::remove()/std::remove_if() to minimise the number of moves of the remaining (non-removed) elements, — this is the erase-remove idiom.
`std::erase_if()` replaces the erase-remove idiom.

### Example

Run this code

```
#include <inplace_vector>
#include <print>
 
int main()
{
    std::inplace_vector<int, 10> v{0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
    std::println("{}", v);
 
    v.erase(v.begin());
    std::println("{}", v);
 
    v.erase(v.begin() + 2, v.begin() + 5);
    std::println("{}", v);
 
    // Erase all even numbers
    for (std::inplace_vector<int, 10>::iterator it{v.begin()}; it != v.end();)
        if (*it % 2 == 0)
            it = v.erase(it);
        else
            ++it;
    std::println("{}", v);
}

```

Output:

```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[1, 2, 3, 4, 5, 6, 7, 8, 9]
[1, 2, 6, 7, 8, 9]
[1, 7, 9]

```

### See also

|  |  |
| --- | --- |
| erase(std::inplace_vector)erase_if(std::inplace_vector)(C++26) | erases all elements satisfying specific criteria   (function template) |
| clear | clears the contents   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/erase&oldid=175278>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 August 2024, at 03:18.