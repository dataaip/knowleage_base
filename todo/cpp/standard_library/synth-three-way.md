# **synth-three-way**, **synth-three-way-result**

From cppreference.com
< cpp‎ | standard library
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

Standard library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Customization point object (C++20) | | | | |
| Exposition-only entities | | | | |
| **decay-copy**(C++11) | | | | |
| ******synth-three-way****synth-three-way-result******(C++20)(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr auto synth-three-way = /\* see below \*/; | (1) | (since C++20)  (exposition only\*) |
| template< class T, class U = T >  using synth-three-way-result =     decltype(synth-three-way(std::declval<T&>(), std::declval<U&>())); | (2) | (since C++20)  (exposition only\*) |
|  |  |  |

1) A function object whose operator() behaves as the synthesized three-way comparison function. Equivalent to:

```
constexpr auto synth-three-way =
    []<class T, class U>(const T& t, const U& u)
        requires requires
        {
            { t < u } -> boolean-testable;
            { u < t } -> boolean-testable;
        }
    {
        if constexpr (std::three_way_comparable_with<T, U>)
            return t <=> u;
        else
        {
            if (t < u)
                return std::weak_ordering::less;
            if (u < t)
                return std::weak_ordering::greater;
            return std::weak_ordering::equivalent;
        }
    };

```

2) The return type of the operator() of (1) (`synth-three-way`).

### Parameters

|  |  |  |
| --- | --- | --- |
| t, u | - | the values to be compared |

### Return value

The compare result.

### See also

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values in the `pair`   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values in the tuple   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++20) | lexicographically compares the values of two `array`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `deque`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++11)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++11)(removed in C++20)(C++20) | lexicographically compares the values of two `forward_list`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `list`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `vector`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `map`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `multimap`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `set`s   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | lexicographically compares the values of two `multiset`s   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/standard_library/synth-three-way&oldid=156904>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 August 2023, at 23:44.