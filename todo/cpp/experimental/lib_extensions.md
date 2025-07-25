# C++ standard libraries extensions

From cppreference.com
< cpp‎ | experimental
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| ****Library fundamentals**** (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

****Library fundamentals****

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

Version 1 of the C++ Extensions for Library Fundamentals, ISO/IEC TS 19568:2015 defines the following new components for the C++ standard library:

## Not selected for inclusion in C++17

The following components of ISO/IEC TS 19568:2015 were not selected for inclusion in C++17.

#### Modified versions of existing classes to support type-erased allocators

|  |  |
| --- | --- |
| Defined in header `<experimental/functional>` | |
| function | a modified version of std::function with support for type-erased allocators   (class template) |
| Defined in header `<experimental/future>` | |
| promise | a modified version of std::promise with support for type-erased allocators   (class template) |
| packaged_task | a modified version of std::packaged_task with support for type-erased allocators   (class template) |

#### Memory resource adaptors

|  |  |
| --- | --- |
| resource_adaptor | adapts an allocator into a memory_resource (alias template) |

### General utilities

|  |  |
| --- | --- |
| Defined in header `<experimental/utility>` | |
| erased_type | placeholder type for type erasure, such as in allocators   (class) |
| Defined in header `<experimental/type_traits>` | |
| invocation_typeraw_invocation_type | deduce the implied function type of the callable object when called with the given argument types   (class template) |

### Feature test macros

|  |  |
| --- | --- |
| Defined in header `<experimental/optional>` | |
| __cpp_lib_experimental_optional | a value of at least 201411 indicates that the optional type is supported   (macro constant) |
| Defined in header `<experimental/any>` | |
| __cpp_lib_experimental_any | a value of at least 201411 indicates that the any type is supported   (macro constant) |
| Defined in header `<experimental/string_view>` | |
| __cpp_lib_experimental_string_view | a value of at least 201411 indicates that basic_string_view template is supported   (macro constant) |
| Defined in header `<experimental/tuple>` | |
| __cpp_lib_experimental_apply | a value of at least 201402 indicates that the tuple apply() function is supported   (macro constant) |
| Defined in header `<experimental/type_traits>` | |
| __cpp_lib_experimental_type_trait_variable_templates | a value of at least 201402 indicates that variable template type traits are supported   (macro constant) |
| __cpp_lib_experimental_invocation_type | a value of at least 201406 indicates that invocation type traits are supported   (macro constant) |
| Defined in header `<experimental/functional>` | |
| __cpp_lib_experimental_boyer_moore_searching | a value of at least 201411 indicates that additional searching algorithms are supported   (macro constant) |
| __cpp_lib_experimental_function_erased_allocator | a value of at least 201406 indicates that type-erased allocator for std::function is supported   (macro constant) |
| Defined in header `<experimental/future>` | |
| __cpp_lib_experimental_promise_erased_allocator | a value of at least 201406 indicates that type-erased allocator for std::promise is supported   (macro constant) |
| __cpp_lib_experimental_packaged_task_erased_allocator | a value of at least 201406 indicates that type-erased allocator for std::packaged_task is supported   (macro constant) |
| Defined in header `<experimental/memory>` | |
| __cpp_lib_experimental_shared_ptr_arrays | a value of at least 201406 indicates that shared_ptr arrays are supported   (macro constant) |
| Defined in header `<experimental/memory_resource>` | |
| __cpp_lib_experimental_memory_resources | a value of at least 201402 indicates that polymorphic memory resources are supported   (macro constant) |
| Defined in header `<experimental/algorithm>` | |
| __cpp_lib_experimental_sample | a value of 201402 indicates that the sample algorithm is supported   (macro constant) |

## Merged into C++17

The following components of ISO/IEC TS 19568:2015 were included into C++17.

### optional objects

|  |  |
| --- | --- |
| Defined in header `<experimental/optional>` | |
| optional | a class template representing **optional objects**   (class template) |

### class `any`

|  |  |
| --- | --- |
| Defined in header `<experimental/any>` | |
| any | a type-safe container for single values of any type   (class) |

### `string_view`

|  |  |
| --- | --- |
| Defined in header `<experimental/string_view>` | |
| basic_string_view | a non-owning reference to a string   (class template) |

### Type-erased and polymorphic allocators

#### Polymorphic allocators and memory resources

The entities in this section are declared in the std::experimental::pmr namespace.

|  |  |
| --- | --- |
| Defined in header `<experimental/memory_resource>` | |
| memory_resource | an abstract interface for classes that encapsulate memory resources   (class) |
| synchronized_pool_resource | a thread-safe memory_resource for managing allocations in pools of different block sizes   (class) |
| unsynchronized_pool_resource | a thread-unsafe memory_resource for managing allocations in pools of different block sizes   (class) |
| monotonic_buffer_resource | a special-purpose memory_resource that releases the allocated memory only when the resource is destroyed   (class) |
| polymorphic_allocator | an allocator that supports run-time polymorphism based on the memory_resource it is constructed with   (class template) |
| new_delete_resource | returns a static program-wide `memory_resource` that uses the global operator new and operator delete to allocate and deallocate memory   (function) |
| null_memory_resource | returns a static `memory_resource` that performs no allocation   (function) |
| get_default_resource | gets the default `memory_resource`   (function) |
| set_default_resource | sets the default `memory_resource`   (function) |

#### Convenience aliases for containers using polymorphic allocators

Convenience aliases and alias templates for containers using polymorphic allocators are provided in the `std::experimental::pmr` namespace for the following class templates in the standard library:

| List of container templates for which convenience aliases are provided |
| --- |
| - std::vector - std::deque - std::forward_list - std::list - std::basic_string - std::map - std::multimap - std::set - std::multiset - std::match_results - std::unordered_map - std::unordered_multimap - std::unordered_set - std::unordered_multiset |

### Array support for `shared_ptr`

|  |  |
| --- | --- |
| Defined in header `<experimental/memory>` | |
| Class | Description |
| shared_ptr | a modified version of std::shared_ptr that supports arrays   (class template) |
| weak_ptr | a modified version of std::weak_ptr that supports arrays   (class template) |

### Sampling and searching algorithms

|  |  |
| --- | --- |
| Defined in header `<experimental/algorithm>` | |
| sample | selects n random elements from a sequence   (function template) |
| search | applies a Searcher to a sequence   (function template) |
| Defined in header `<experimental/functional>` | |
| default_searcher | standard C++ library search algorithm implementation   (class template) |
| make_default_searcher | helper function to create a default_searcher   (function template) |
| boyer_moore_searcher | Boyer-Moore search algorithm implementation   (class template) |
| make_boyer_moore_searcher | helper function to create a boyer_moore_searcher   (function template) |
| boyer_moore_horspool_searcher | Boyer-Moore-Horspool search algorithm implementation   (class template) |
| make_boyer_moore_horspool_searcher | helper function to create a boyer_moore_horspool_searcher   (function template) |

### General utilities

|  |  |
| --- | --- |
| Defined in header `<experimental/tuple>` | |
| apply | calls a function to a tuple of arguments   (function template) |

In addition, the TS provides numerous `constexpr` variable templates for the following type traits and other class templates in the standard library:

| List of type traits and other class templates for which variable templates are provided |
| --- |
| - std::is_void - std::is_null_pointer - std::is_integral - std::is_floating_point - std::is_array - std::is_pointer - std::is_lvalue_reference - std::is_rvalue_reference - std::is_member_object_pointer - std::is_member_function_pointer - std::is_enum - std::is_union - std::is_class - std::is_function - std::is_reference - std::is_arithmetic - std::is_fundamental - std::is_object - std::is_scalar - std::is_compound - std::is_member_pointer - std::is_const - std::is_volatile - std::is_trivial - std::is_trivially_copyable - std::is_standard_layout - std::is_pod - std::is_literal_type - std::is_empty - std::is_polymorphic - std::is_abstract - std::is_final - std::is_signed - std::is_unsigned - std::is_constructible - std::is_trivially_constructible - std::is_nothrow_constructible - std::is_default_constructible - std::is_trivially_default_constructible - std::is_nothrow_default_constructible - std::is_copy_constructible - std::is_trivially_copy_constructible - std::is_nothrow_copy_constructible - std::is_move_constructible - std::is_trivially_move_constructible - std::is_nothrow_move_constructible - std::is_assignable - std::is_trivially_assignable - std::is_nothrow_assignable - std::is_copy_assignable - std::is_trivially_copy_assignable - std::is_nothrow_copy_assignable - std::is_move_assignable - std::is_trivially_move_assignable - std::is_nothrow_move_assignable - std::is_destructible - std::is_trivially_destructible - std::is_nothrow_destructible - std::has_virtual_destructor - std::alignment_of - std::rank - std::extent - std::is_same - std::is_base_of - std::is_convertible - std::ratio_equal - std::ratio_not_equal - std::ratio_less - std::ratio_less_equal - std::ratio_greater - std::ratio_greater_equal - std::tuple_size - std::chrono::treat_as_floating_point - std::is_error_code_enum - std::is_error_condition_enum - std::is_bind_expression - std::is_placeholder - std::uses_allocator |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/lib_extensions&oldid=164146>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 November 2023, at 00:10.