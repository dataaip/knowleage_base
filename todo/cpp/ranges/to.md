# std::ranges::to

From cppreference.com
< cpp‎ | ranges
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

Ranges library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begin | | | | | | cbegin | | | | | | end | | | | | | cend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rbegin | | | | | | crbegin | | | | | | rend | | | | | | crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | size | | | | | | ssize | | | | | | data | | | | | | cdata | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty | | | | | |  | | | | | |  | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range conversions | | | | | | std::from_range_t std::from_range(C++23)(C++23) | | | | | | ****to****(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Dangling iterator handling | | | | | | dangling | | | | | | borrowed_iterator_t | | | | | | borrowed_subrange_t | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | range_size_trange_difference_trange_value_t | | | | | | elements_of(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator_tconst_iterator_tsentinel_tconst_sentinel_t(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | range_reference_trange_const_reference_trange_rvalue_reference_trange_common_reference_t(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | range | | | | | | borrowed_range | | | | | | sized_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_range | | | | | | view | | | | | | viewable_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_range | | | | | | output_range | | | | | | forward_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bidirectional_range | | | | | | random_access_range | | | | | | contiguous_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constant_range(C++23) | | | | | |  | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Views | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | view_interface | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | subrange | | | | | |  | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range factories | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | single_viewviews::single | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | basic_istream_viewviews::istream | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota_viewviews::iota | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | repeat_viewviews::repeat(C++23)(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< class C, ranges::input_range R, class... Args >      requires (!ranges::view<C>) constexpr C to( R&& r, Args&&... args ); | (1) | (since C++23) |
| template< template< class... > class C,  ranges::input_range R, class... Args > constexpr auto to( R&& r, Args&&... args ); | (2) | (since C++23) |
| template< class C, class... Args >      requires (!ranges::view<C>) constexpr /\*range adaptor closure\*/ to( Args&&... args ); | (3) | (since C++23) |
| template< template< class... > class C, class... Args >  constexpr /\*range adaptor closure\*/ to( Args&&... args ); | (4) | (since C++23) |
| Helper templates |  |  |
| template< class Container >  constexpr bool /\*reservable-container\*/ =      ranges::sized_range<Container> &&      requires (Container& c, ranges::range_size_t<Container> n)      {          c.reserve(n);          { c.capacity() } -> std::same_as<decltype(n)>;          { c.max_size() } -> std::same_as<decltype(n)>; }; | (5) | (exposition only\*) |
| template< class Container, class Reference >  constexpr bool /\*container-appendable\*/ =      requires (Container& c, Reference&& ref)      {          requires          (              requires { c.emplace_back(std::forward<Reference>(ref)); }     ||              requires { c.push_back(std::forward<Reference>(ref)); }        ||              requires { c.emplace(c.end(), std::forward<Reference>(ref)); } ||              requires { c.insert(c.end(), std::forward<Reference>(ref)); }          ); }; | (6) | (exposition only\*) |
| template< class Reference, class C >  constexpr auto /\*container-appender\*/( C& c ); | (7) | (exposition only\*) |
| template< class R, class T >  concept /\*container-compatible-range\*/ =      ranges::input_range<R> && std::convertible_to<ranges::range_reference_t<R>, T>; | (8) | (exposition only\*) |
|  |  |  |

The overloads of the range conversion function construct a new non-view object from a source range as its first argument by calling a constructor taking a range, a `std::from_range_t` tagged ranged constructor, a constructor taking an iterator-sentinel pair, or by back inserting each element of the source range into the arguments-constructed object.

1) Constructs an object of type `C` from the elements of r in the following:a) If `C` does not satisfy `input_range` or std::convertible_to<ranges::range_reference_t<R>, ranges::range_value_t<C>> is true:1) Constructing a non-view object as if direct-initializing (but not direct-list-initializing) an object of type `C` from the source range std::forward<R>(r) and the rest of the functional arguments std::forward<Args>(args)... if std::constructible_from<C, R, Args...> is true.2) Otherwise, constructing a non-view object as if direct-initializing (but not direct-list-initializing) an object of type `C` from additional disambiguation tag std::from_range, the source range std::forward<R>(r) and the rest of the functional arguments std::forward<Args>(args)... if std::constructible_from<C, std::from_range_t, R, Args...> is true.3) Otherwise, constructing a non-view object as if direct-initializing (but not direct-list-initializing) an object of type `C` from the iterator-sentinel pair (ranges::begin(r) as an iterator and ranges::end(r) as sentinel, where iterator and sentinel have the same type. In other words, the source range must be a common range), and the rest of function arguments std::forward<Args>(args)... if all of the conditions below are true:

- ranges::common_range<R>
- If std::iterator_traits<ranges::iterator_t<R>>::iterator_category is valid and denotes a type that satisfies std::derived_from<std::input_iterator_tag>
- std::constructible_from<C, ranges::iterator_t<R>, ranges::sentinel_t<R>, Args...>
4) Otherwise, constructing a non-view range object as if direct-initializing (but not direct-list-initializing) an object of type `C` from the rest of the function arguments std::forward<Args>(args)... with the following equivalent call below after the construction:

if constexpr (ranges::sized_range<R> && /\*reservable-container\*/<C>)  
    c.reserve(static_cast<ranges::range_size_t<C>>(ranges::size(r)));  
ranges::for_each(r, /\*container-appender\*/(c));  
If the `R` satisfies `sized_range` and `C` satisfies `reservable-container`, the constructed object c of type `C` is able to reserve storage with the initial storage size ranges::size(r) to prevent additional allocations during inserting new elements. Each element of r is appended to c.
The operations above are valid if both of the conditions below are true:

- std::constructible_from<C, Args...>
- `container-appendable`<C, ranges::range_reference_t<R>>
b) Otherwise, the return expression is equivalent to:

to<C>(ranges::ref_view(r) | views::transform([](auto&& elem)  
{  
    return to<ranges::range_value_t<C>>(std::forward<decltype(elem)>(elem));  
}), std::forward<Args>(args)...)  
Which allows nested range constructions within the range if ranges::input_range<ranges::range_reference_t<C>> is true.

Otherwise, the program is ill-formed.2) Constructs an object of deduced type from the elements of r.

Let /\*input-iterator\*/ be an exposition only type that satisfies LegacyInputIterator:

|  |  |  |
| --- | --- | --- |
| struct /\*input-iterator\*/  {      using iterator_category = std::input_iterator_tag;      using value_type = ranges::range_value_t<R>;      using difference_type = std::ptrdiff_t;      using pointer = std::add_pointer_t<ranges::range_reference_t<R>>;      using reference = ranges::range_reference_t<R>;      reference operator\*() const;                      // not defined      pointer operator->() const;                       // not defined      /\*input-iterator\*/& operator++();                 // not defined      /\*input-iterator\*/ operator++(int);               // not defined      bool operator==(const /\*input-iterator\*/&) const; // not defined }; |  | (exposition only\*) |
|  |  |  |

Let /\*DEDUCE-EXPR\*/ be defined as follows:

- C(std::declval<R>(), std::declval<Args>()...), if that expression is valid.
- Otherwise, C(std::from_range, std::declval<R>(),  
    std::declval<Args>()...), if that expression is valid.
- Otherwise, C(std::declval</\*input-iterator\*/>(),  
    std::declval</\*input-iterator\*/>(),  
    std::declval<Args>()...), if that expression is valid.
- Otherwise, the program is ill-formed.

The call is equivalent to to<decltype(/\*DEDUCE-EXPR\*/)>  
    (std::forward<R>(r), std::forward<Args>(args)...).3,4) Returns a perfect forwarding call wrapper that is also a RangeAdaptorClosureObject.5) Is true if it satisfies ranges::sized_range and is eligible to be reservable.6) Is true if one element of type `Reference` can be appended to `Container` through a member function call `emplace_back`, `push_back`, `emplace` or `insert`.7) Returns a function object where a call to the returned function object is expression-equivalent to appending one element to a container. The return expression is equivalent to:

return [&c]<class Reference>(Reference&& ref)  
{  
    if constexpr (requires { c.emplace_back(std::declval<Reference>()); })  
        c.emplace_back(std::forward<Reference>(ref));  
    else if constexpr (requires { c.push_back(std::declval<Reference>()); })  
        c.push_back(std::forward<Reference>(ref));  
    else if constexpr (requires { c.emplace(c.end(),  
                                            std::declval<Reference>()); })  
        c.emplace(c.end(), std::forward<Reference>(ref));  
    else  
        c.insert(c.end(), std::forward<Reference>(ref));  
};

8) Is used in the definition of containers in constructing an input range `R` whose range reference type must be convertible to `T`.

### Parameters

|  |  |  |
| --- | --- | --- |
| r | - | a source range object |
| args | - | list of the arguments to (1,2) construct a range or (3,4) bind to the last parameters of range adaptor closure object |
| Type requirements | | |
| -`C` must be cv-unqualified class type (1,3) | | |

### Return value

1,2) A constructed non-view object.3,4) A range adaptor closure object of unspecified type, with the following properties:

## ranges::to return type

#### Member objects

The returned object behaves as if it has no target object, and an std::tuple object tup constructed with std::tuple<std::decay_t<Args>...>(std::forward<Args>(args)...), except that the returned object's assignment behavior is unspecified and the names are for exposition only.

#### Constructors

The return type of `ranges::to` (3,4) behaves as if its copy/move constructors perform a memberwise copy/move. It is CopyConstructible if all of its member objects (specified above) are CopyConstructible, and is MoveConstructible otherwise.

#### Member function `operator()`

Given an object `G` obtained from an earlier call to range::to</\* see below \*/>(args...), when a glvalue g designating `G` is invoked in a function call expression g(r), an invocation of the stored object takes place, as if by

- ranges::to</\* see below \*/>(r, std::get<Ns>(g.tup)...), where

:   - r is a source range object that must satisfy `input_range`.
    - Ns is an integer pack 0, 1, ..., (sizeof...(Args) - 1).
    - g is an lvalue in the call expression if it is an lvalue in the call expression, and is an rvalue otherwise. Thus std::move(g)(r) can move the bound arguments into the call, where g(r) would copy.
    - The specified template argument is (3) `C` or (4) the deduced type from a class template `C` that must not satisfy `view`.

The program is ill-formed if g has volatile-qualified type.

### Exceptions

Only throws if construction of a non-view object throws.

### Notes

The insertion of elements into the container may involve copy which can be less efficient than move because lvalue references are produced during the indirection call. Users can opt-in to use views::as_rvalue to adapt the range in order for their elements to always produce an rvalue reference during the indirection call which implies move.

The parentheses are mandatory when using the pipe syntax.

```
auto vec = r | std::ranges::to<std::vector>;   // Error
auto vec = r | std::ranges::to<std::vector>(); // OK

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_to_container` | `202202L` | (C++23) | `std::ranges::to` |

### Example

A preview link: Compiler Explorer

Run this code

```
#include <boost/container/devector.hpp>
#include <concepts>
#include <list>
#include <initializer_list>
#include <iostream>
#include <print>
#include <ranges>
#include <regex>
#include <string>
#include <vector>
 
int main()
{
    auto vec = std::views::iota(1, 5)
             | std::views::transform([](int v){ return v * 2; })
             | std::ranges::to<std::vector>();
 
    static_assert(std::same_as<decltype(vec), std::vector<int>>);
    std::println("{}", vec);
 
    auto list = vec | std::views::take(3) | std::ranges::to<std::list<double>>();
    std::println("{}", list);
}
 
void ctor_demos()
{
    // 1.a.1) Direct init
    {
        char array[]{'a', 'b', '\0', 'c'};
 
        // Argument type is convertible to result value type:
        auto str_to = std::ranges::to<std::string>(array);
        // Equivalent to
        std::string str(array);
 
        // Result type is not an input range:
        auto re_to = std::ranges::to<std::regex>(array);
        // Equivalent to
        std::regex re(array);
    }
 
    // 1.a.2) from_range ctor
    {
        auto list = {'a', 'b', '\0', 'c'};
 
        // Argument type is convertible to result value type:
        auto str_to = std::ranges::to<std::string>(list);
        // Equivalent to
        std::string str(std::from_range, list);
 
        // Result type is not an input range:
        auto pair_to = std::ranges::to<std::pair<std::from_range_t, bool>>(true);
        // Equivalent to
        std::pair<std::from_range_t, bool> pair(std::from_range, true);
    }
 
    // 1.a.3) iterator pair ctor
    {
        auto list = {'a', 'b', '\0', 'c'};
 
        // Argument type is convertible to result value type:
        auto devector_to = std::ranges::to<boost::container::devector<char>>(list);
        // Equivalent to
        boost::container::devector<char> devector(std::ranges::begin(list), 
                                                  std::ranges::end(list));
 
        // Result type is not an input range:
        std::regex re;
        auto it_to = std::ranges::to<std::cregex_iterator>(list, re);
        // Equivalent to
        std::cregex_iterator it(std::ranges::begin(list), std::ranges::end(list), re);
    }
}

```

Output:

```
[2, 4, 6, 8]
[2, 4, 6]

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3984 | C++23 | the nested construction branch of `ranges::to` resulted to program ill-formed if `R&` does not model `viewable_range` | made well-formed |
| LWG 4016 | C++23 | the container insertion branch of `ranges::to` involved use of insert iterators | replaced with direct appending of elements to container |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 26.5.7 Range conversions [range.utility.conv]

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/to&oldid=178446>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 December 2024, at 04:12.