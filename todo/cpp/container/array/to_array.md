# std::to_array

From cppreference.com
< cpp‎ | container‎ | array
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

std::array

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | array::at | | | | | | [array::operator[]](operator_at.html "cpp/container/array/operator at") | | | | | | array::front | | | | | | array::back | | | | | | array::data | | | | | | Operations | | | | | | array::fill | | | | | | array::swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | array::beginarray::cbegin | | | | | | array::endarray::cend | | | | | | array::rbeginarray::crbegin | | | | | | array::rendarray::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | array::empty | | | | | | array::size | | | | | | array::max_size | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | get(std::array) | | | | | | swap(std::array) | | | | | | ****to_array****(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator|=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| tuple_size<std::array> | | | | |
| tuple_element<std::array> | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<array>` |  |  |
| template< class T, std::size_t N >  constexpr std::array<std::remove_cv_t<T>, N> to_array( T (&a)[N] ); | (1) | (since C++20) |
| template< class T, std::size_t N >  constexpr std::array<std::remove_cv_t<T>, N> to_array( T (&&a)[N] ); | (2) | (since C++20) |
|  |  |  |

Creates a std::array from the one dimensional built-in array `a`. Copying or moving multidimensional built-in array is not supported.

1) For every `i` in `0, ..., N - 1`, copy-initializes result's correspond element with a[i]. This overload is ill-formed when std::is_constructible_v<T, T&> is false.2) For every `i` in `0, ..., N - 1`, move-initializes result's correspond element with std::move(a[i]). This overload is ill-formed when std::is_move_constructible_v<T> is false.

Both overloads are ill-formed when std::is_array_v<T> is true.

### Parameters

|  |  |  |
| --- | --- | --- |
| a | - | the built-in array to be converted the std::array |
| Type requirements | | |
| -`T` must meet the requirements of CopyConstructible in order to use overload (1). | | |
| -`T` must meet the requirements of MoveConstructible in order to use overload (2). | | |

### Return value

1) std::array<std::remove_cv_t<T>, N>{ a[0], ..., a[N - 1] }2) std::array<std::remove_cv_t<T>, N>{ std::move(a[0]), ..., std::move(a[N - 1]) }

### Notes

There are some occasions where class template argument deduction of std::array cannot be used while `to_array` is available:

- `to_array` can be used when the element type of the `std::array` is manually specified and the length is deduced, which is preferable when implicit conversion is wanted.
- `to_array` can copy a string literal, while class template argument deduction constructs a `std::array` of a single pointer to its first character.

```
std::to_array<long>({3, 4}); // OK: implicit conversion
// std::array<long>{3, 4};   // error: too few template arguments
std::to_array("foo");        // creates std::array<char, 4>{'f', 'o', 'o', '\0'}
std::array{"foo"};           // creates std::array<const char*, 1>{"foo"}

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_to_array` | `201907L` | (C++20) | `std::to_array` |

### Possible implementation

| to_array (1) |
| --- |
| ```text namespace detail {     template<class T, std::size_t N, std::size_t... I>     constexpr std::array<std::remove_cv_t<T>, N>         to_array_impl(T (&a)[N], std::index_sequence<I...>)     {         return {{a[I]...}};     } }   template<class T, std::size_t N> constexpr std::array<std::remove_cv_t<T>, N> to_array(T (&a)[N]) {     return detail::to_array_impl(a, std::make_index_sequence<N>{}); } ``` |
| to_array (2) |
| ```text namespace detail {     template<class T, std::size_t N, std::size_t... I>     constexpr std::array<std::remove_cv_t<T>, N>         to_array_impl(T (&&a)[N], std::index_sequence<I...>)     {         return {{std::move(a[I])...}};     } }   template<class T, std::size_t N> constexpr std::array<std::remove_cv_t<T>, N> to_array(T (&&a)[N]) {     return detail::to_array_impl(std::move(a), std::make_index_sequence<N>{}); } ``` |

### Example

Run this code

```
#include <array>
#include <memory>
#include <string_view>
#include <type_traits>
#include <utility>
 
// creates a constexpr array of string_view's    
constexpr auto w1n = std::to_array<std::string_view>({
    "Mary", "Patricia", "Linda", "Barbara", "Elizabeth", "Jennifer"
});
static_assert(std::is_same_v<decltype(w1n), const std::array<std::string_view, 6>>);
static_assert(w1n.size() == 6 and w1n[5] == "Jennifer");
 
int main()
{
    // copies a string literal
    auto a1 = std::to_array("foo");
    static_assert(a1.size() == 4);
 
    // deduces both element type and length
    auto a2 = std::to_array({0, 2, 1, 3});
    static_assert(std::is_same_v<decltype(a2), std::array<int, 4>>);
 
    // deduces length with element type specified
    // implicit conversion happens
    auto a3 = std::to_array<long>({0, 1, 3});
    static_assert(std::is_same_v<decltype(a3), std::array<long, 3>>);
 
    auto a4 = std::to_array<std::pair<int, float>>(
        {{3, 0.0f}, {4, 0.1f}, {4, 0.1e23f}});
    static_assert(a4.size() == 3);
 
    // creates a non-copyable std::array
    auto a5 = std::to_array({std::make_unique<int>(3)});
    static_assert(a5.size() == 1);
 
    // error: copying multidimensional arrays is not supported
    // char s[2][6] = {"nice", "thing"};
    // auto a6 = std::to_array(s);
}

```

### See also

|  |  |
| --- | --- |
| make_array(library fundamentals TS v2) | creates a std::array object whose size and optionally element type are deduced from the arguments   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/array/to_array&oldid=155015>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 July 2023, at 12:40.