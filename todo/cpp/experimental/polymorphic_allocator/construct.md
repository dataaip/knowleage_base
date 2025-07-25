# std::experimental::pmr::polymorphic_allocator<T>::construct

From cppreference.com
< cpp‎ | experimental‎ | polymorphic allocator
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

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

Polymorphic allocator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| polymorphic_allocator | | | | |
| Convenience aliases for containers using `polymorphic_allocator` | | | | |
| Memory resource classes | | | | |
| memory_resource | | | | |
| synchronized_pool_resource | | | | |
| unsynchronized_pool_resource | | | | |
| monotonic_buffer_resource | | | | |
| resource_adaptor | | | | |
| Global memory resources | | | | |
| new_delete_resource | | | | |
| null_memory_resource | | | | |
| get_default_resource | | | | |
| set_default_resource | | | | |
| Type-erased allocator support for existing classes | | | | |
| function | | | | |
| packaged_task | | | | |
| promise | | | | |

std::experimental::pmr::polymorphic_allocator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| polymorphic_allocator::polymorphic_allocator | | | | |
| polymorphic_allocator::operator= | | | | |
| polymorphic_allocator::allocate | | | | |
| polymorphic_allocator::deallocate | | | | |
| ****polymorphic_allocator::construct**** | | | | |
| polymorphic_allocator::destroy | | | | |
| polymorphic_allocator::select_on_container_copy_construction | | | | |
| polymorphic_allocator::resource | | | | |
| Non-member functions | | | | |
| operator==operator!= | | | | |

|  |  |  |
| --- | --- | --- |
| template< class U, class... Args >  void construct( U\* p, Args&&... args ); | (1) | (library fundamentals TS) |
| template< class T1, class T2, class... Args1, class... Args2 >  void construct( std::pair<T1, T2>\* p,                  std::piecewise_construct_t,                  std::tuple<Args1...> x, std::tuple<Args2...> y ); | (2) | (library fundamentals TS) |
| template< class T1, class T2 >  void construct( std::pair<T1, T2>\* p ); | (3) | (library fundamentals TS) |
| template< class T1, class T2, class U, class V >  void construct( std::pair<T1, T2>\* p, U&& x, V&& y ); | (4) | (library fundamentals TS) |
| template< class T1, class T2, class U, class V >  void construct( std::pair<T1, T2>\* p, const std::pair<U, V>& xy ); | (5) | (library fundamentals TS) |
| template< class T1, class T2, class U, class V >  void construct( std::pair<T1, T2>\* p, std::pair<U, V>&& xy ); | (6) | (library fundamentals TS) |
|  |  |  |

Constructs an object in allocated, but not initialized storage pointed to by p the provided constructor arguments. If the object is of type that itself uses allocators, or if it is std::pair, passes `this->resource()` down to the constructed object.

1) If std::uses_allocator<U, memory_resource\*>::value == false (the type `U` does not use allocators) and std::is_constructible<U, Args...>::value == true, then constructs the object as if by ::new((void \*) p) U(std::forward<Args>(args)...);.

Otherwise, if std::uses_allocator<U, memory_resource\*>::value == true (the type `U` uses allocators, e.g. it is a container) and std::is_constructible<U, std::allocator_arg_t, memory_resource\*, Args...>::value == true, then constructs the object as if by ::new((void \*) p) U(std::allocator_arg, this->resource(), std::forward<Args>(args)...);.

Otherwise, if std::uses_allocator<U, memory_resource\*>::value == true (the type `U` uses allocators, e.g. it is a container) and std::is_constructible<U, Args..., memory_resource\*>::value == true, then constructs the object as if by ::new((void \*) p) U(std::forward<Args>(args)..., this->resource());.

Otherwise, the program is ill-formed.

2) First, if either `T1` or `T2` is allocator-aware, modifies the tuples x and y to include `this->resource()`, resulting in the two new tuples `xprime` and `yprime`, according to the following three rules:

2a) if `T1` is not allocator-aware (std::uses_allocator<T1, memory_resource\*>::value == false) and std::is_constructible<T1, Args1...>::value == true, then `xprime` is x, unmodified.

2b) if `T1` is allocator-aware (std::uses_allocator<T1, memory_resource\*>::value == true), and its constructor takes an allocator tag (std::is_constructible<T1, std::allocator_arg_t, memory_resource\*, Args1...>::value == true, then `xprime` is
std::tuple_cat(std::make_tuple(std::allocator_arg, this->resource()), std::move(x)).

2c) if `T1` is allocator-aware (std::uses_allocator<T1, memory_resource\*>::value == true), and its constructor takes the allocator as the last argument (std::is_constructible<T1, Args1..., memory_resource\*>::value == true), then `xprime` is std::tuple_cat(std::move(x), std::make_tuple(this->resource())).

2d) Otherwise, the program is ill-formed.

Same rules apply to `T2` and the replacement of y with `yprime`.

Once `xprime` and `yprime` are constructed, constructs the pair p in allocated storage as if by ::new((void \*) p) pair<T1, T2>(std::piecewise_construct, std::move(xprime), std::move(yprime));.

3) Equivalent to construct(p, std::piecewise_construct, std::tuple<>(), std::tuple<>()), that is, passes the memory resource on to the pair's member types if they accept them.

4) Equivalent to

construct(p, std::piecewise_construct, std::forward_as_tuple(std::forward<U>(x)),  
                                       std::forward_as_tuple(std::forward<V>(y)))

5) Equivalent to

construct(p, std::piecewise_construct, std::forward_as_tuple(xy.first),  
                                       std::forward_as_tuple(xy.second))

6) Equivalent to

construct(p, std::piecewise_construct, std::forward_as_tuple(std::forward<U>(xy.first)),  
                                       std::forward_as_tuple(std::forward<V>(xy.second)))

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | pointer to allocated, but not initialized storage |
| args... | - | the constructor arguments to pass to the constructor of `T` |
| x | - | the constructor arguments to pass to the constructor of `T1` |
| y | - | the constructor arguments to pass to the constructor of `T2` |
| xy | - | the pair whose two members are the constructor arguments for `T1` and `T2` |

### Return value

(none)

### Notes

This function is called (through std::allocator_traits) by any allocator-aware object, such as std::vector, that was given a std::polymorphic_allocator as the allocator to use. Since `memory_resource*` implicitly converts to `polymorphic_allocator`, the memory resource pointer will propagate to any allocator-aware subobjects using polymorphic allocators.

### See also

|  |  |
| --- | --- |
| construct[static] | constructs an object in the allocated storage   (function template) |
| construct(until C++20) | constructs an object in allocated storage   (public member function of `std::allocator<T>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/polymorphic_allocator/construct&oldid=155152>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 July 2023, at 22:35.