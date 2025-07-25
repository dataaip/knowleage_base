# std::inplace_vector<T,N>::push_back

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | ****inplace_vector::push_back**** | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr reference push_back( const T& value ); | (1) | (since C++26) |
| constexpr reference push_back( T&& value ); | (2) | (since C++26) |
|  |  |  |

Appends the given element value to the end of the container.

1) The new element is initialized as a copy of value.2) value is moved into the new element.

No iterators or references are invalidated, except `end()`, which is invalidated if the insertion occurs.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | the value of the element to append |
| Type requirements | | |
| -`T` must meet the requirements of CopyInsertable in order to use overload (1). | | |
| -`T` must meet the requirements of MoveInsertable in order to use overload (2). | | |

### Return value

`back()`, i.e. a reference to the inserted element.

### Complexity

Constant.

### Exceptions

- std::bad_alloc if size() == capacity() before invocation.
- Any exception thrown by initialization of inserted element.

If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).

### Example

Run this code

```
#include <inplace_vector>
#include <new>
#include <print>
#include <string>
 
int main()
{
    std::inplace_vector<std::string, 2> fauna;
    std::string dog{"\N{DOG}"};
 
    fauna.push_back("\N{CAT}"); // overload (1)
    fauna.push_back(std::move(dog)); // overload (2)
    std::println("fauna = {}", fauna);
 
    try
    {
        fauna.push_back("\N{BUG}"); // throws: there is no space
    }
    catch(const std::bad_alloc& ex)
    {
        std::println("{}", ex.what());
    }
    std::println("fauna = {}", fauna);
}

```

Possible output:

```
fauna = ["🐈", "🐕"]
std::bad_alloc
fauna = ["🐈", "🐕"]

```

### See also

|  |  |
| --- | --- |
| emplace_back | constructs an element in-place at the end   (public member function) |
| append_range | adds a range of elements to the end   (public member function) |
| try_push_back | tries to add an element to the end   (public member function) |
| try_emplace_back | tries to construct an element in-place at the end   (public member function) |
| try_append_range | tries to add a range of elements to the end   (public member function) |
| unchecked_push_back | unconditionally adds an element to the end   (public member function) |
| unchecked_emplace_back | unconditionally constructs an element in-place at the end   (public member function) |
| pop_back | removes the last element   (public member function) |
| back_inserter | creates a std::back_insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/push_back&oldid=176284>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2024, at 05:19.