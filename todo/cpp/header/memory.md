# Standard library header <memory>

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | ****<memory>**** | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the dynamic memory management library.

|  |  |
| --- | --- |
| Includes | |
| <compare>(C++20) | Three-way comparison operator support |
| Classes | |
| Pointer traits | |
| pointer_traits(C++11) | provides information about pointer-like types   (class template) |
| Garbage collector support | |
| pointer_safety(C++11)(removed in C++23) | lists pointer safety models   (enum) |
| Allocators | |
| allocator | the default allocator   (class template) |
| allocator_traits(C++11) | provides information about allocator types   (class template) |
| allocation_result(C++23) | records the address and the actual size of storage allocated by `allocate_at_least`   (class template) |
| uses_allocator(C++11) | checks if the specified type supports uses-allocator construction   (class template) |
| Uninitialized storage | |
| raw_storage_iterator(deprecated in C++17)(removed in C++20) | an iterator that allows standard algorithms to store results in uninitialized memory   (class template) |
| Smart pointers | |
| unique_ptr(C++11) | smart pointer with unique object ownership semantics   (class template) |
| shared_ptr(C++11) | smart pointer with shared object ownership semantics   (class template) |
| weak_ptr(C++11) | weak reference to an object managed by std::shared_ptr   (class template) |
| auto_ptr(deprecated in C++11)(removed in C++17) | smart pointer with strict object ownership semantics   (class template) |
| Helper classes | |
| std::atomic<std::shared_ptr>(C++20) | atomic shared pointer   (class template specialization) |
| std::atomic<std::weak_ptr>(C++20) | atomic weak pointer   (class template specialization) |
| owner_less(C++11) | provides mixed-type owner-based ordering of shared and weak pointers   (class template) |
| owner_hash(C++26) | provides owner-based hashing for shared and weak pointers   (class) |
| owner_equal(C++26) | provides mixed-type owner-based equal comparisons of shared and weak pointers   (class) |
| enable_shared_from_this(C++11) | allows an object to create a `shared_ptr` referring to itself   (class template) |
| bad_weak_ptr(C++11) | exception thrown when accessing a `weak_ptr` which refers to already destroyed object   (class) |
| default_delete(C++11) | default deleter for unique_ptr   (class template) |
| std::hash<std::unique_ptr>(C++11) | hash support for std::unique_ptr   (class template specialization) |
| std::hash<std::shared_ptr>(C++11) | hash support for std::shared_ptr   (class template specialization) |
| Smart pointer adaptors | |
| out_ptr_t(C++23) | interoperates with foreign pointer setters and resets a smart pointer on destruction   (class template) |
| inout_ptr_t(C++23) | interoperates with foreign pointer setters, obtains the initial pointer value from a smart pointer, and resets it on destruction   (class template) |
| Forward declarations | |
| Defined in header `<functional>` | |
| hash(C++11) | hash function object   (class template) |
| Defined in header `<atomic>` | |
| atomic(C++11) | atomic class template and specializations for bool, integral, floating-point,(since C++20) and pointer types   (class template) |
| Tags | |
| allocator_argallocator_arg_t(C++11) | a tag used to select allocator-aware constructors (tag) |
| Functions | |
| Uses-allocator construction | |
| uses_allocator_construction_args(C++20) | prepares the argument list matching the flavor of uses-allocator construction required by the given type   (function template) |
| make_obj_using_allocator(C++20) | creates an object of the given type by means of uses-allocator construction   (function template) |
| uninitialized_construct_using_allocator(C++20) | creates an object of the given type at specified memory location by means of uses-allocator construction   (function template) |
| Miscellaneous | |
| to_address(C++20) | obtains a raw pointer from a pointer-like type   (function template) |
| addressof(C++11) | obtains actual address of an object, even if the `&` operator is overloaded   (function template) |
| align(C++11) | aligns a pointer in a buffer   (function) |
| assume_aligned(C++20) | informs the compiler that a pointer is aligned   (function template) |
| is_sufficiently_aligned(C++26) | checks whether the pointer points to an object whose alignment has at least the given value   (function template) |
| Explicit lifetime management | |
| start_lifetime_asstart_lifetime_as_array(C++23) | implicitly creates objects in given storage with the object representation reused   (function template) |
| Garbage collector support | |
| declare_reachable(C++11)(removed in C++23) | declares that an object can not be recycled   (function) |
| undeclare_reachable(C++11)(removed in C++23) | declares that an object can be recycled   (function template) |
| declare_no_pointers(C++11)(removed in C++23) | declares that a memory area does not contain traceable pointers   (function) |
| undeclare_no_pointers(C++11)(removed in C++23) | cancels the effect of std::declare_no_pointers   (function) |
| get_pointer_safety(C++11)(removed in C++23) | returns the current pointer safety model   (function) |
| Uninitialized storage | |
| uninitialized_copy | copies a range of objects to an uninitialized area of memory   (function template) |
| uninitialized_copy_n(C++11) | copies a number of objects to an uninitialized area of memory   (function template) |
| uninitialized_fill | copies an object to an uninitialized area of memory, defined by a range   (function template) |
| uninitialized_fill_n | copies an object to an uninitialized area of memory, defined by a start and a count   (function template) |
| uninitialized_move(C++17) | moves a range of objects to an uninitialized area of memory   (function template) |
| uninitialized_move_n(C++17) | moves a number of objects to an uninitialized area of memory   (function template) |
| uninitialized_default_construct(C++17) | constructs objects by default-initialization in an uninitialized area of memory, defined by a range   (function template) |
| uninitialized_default_construct_n(C++17) | constructs objects by default-initialization in an uninitialized area of memory, defined by a start and a count   (function template) |
| uninitialized_value_construct(C++17) | constructs objects by value-initialization in an uninitialized area of memory, defined by a range   (function template) |
| uninitialized_value_construct_n(C++17) | constructs objects by value-initialization in an uninitialized area of memory, defined by a start and a count   (function template) |
| construct_at(C++20) | creates an object at a given address   (function template) |
| destroy_at(C++17) | destroys an object at a given address   (function template) |
| destroy(C++17) | destroys a range of objects   (function template) |
| destroy_n(C++17) | destroys a number of objects in a range   (function template) |
| get_temporary_buffer(deprecated in C++17)(removed in C++20) | obtains uninitialized storage   (function template) |
| return_temporary_buffer(deprecated in C++17)(removed in C++20) | frees uninitialized storage   (function template) |
| Smart pointer non-member operations | |
| make_uniquemake_unique_for_overwrite(C++14)(C++20) | creates a unique pointer that manages a new object   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(C++20) | compares to another `unique_ptr` or with nullptr   (function template) |
| make_sharedmake_shared_for_overwrite(C++20) | creates a shared pointer that manages a new object   (function template) |
| allocate_sharedallocate_shared_for_overwrite(C++20) | creates a shared pointer that manages a new object allocated using an allocator   (function template) |
| static_pointer_castdynamic_pointer_castconst_pointer_castreinterpret_pointer_cast(C++17) | applies static_cast, dynamic_cast, const_cast, or reinterpret_cast to the stored pointer   (function template) |
| get_deleter | returns the deleter of specified type, if owned   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | compares with another `shared_ptr` or with nullptr   (function template) |
| operator<<(std::shared_ptr) | outputs the value of the stored pointer to an output stream   (function template) |
| operator<<(std::unique_ptr)(C++20) | outputs the value of the managed pointer to an output stream   (function template) |
| std::swap(std::unique_ptr)(C++11) | specializes the std::swap algorithm   (function template) |
| std::swap(std::shared_ptr)(C++11) | specializes the std::swap algorithm   (function template) |
| std::swap(std::weak_ptr)(C++11) | specializes the std::swap algorithm   (function template) |
| Smart pointer adaptor creation | |
| out_ptr(C++23) | creates an `out_ptr_t` with an associated smart pointer and resetting arguments   (function template) |
| inout_ptr(C++23) | creates an `inout_ptr_t` with an associated smart pointer and resetting arguments   (function template) |

|  |  |
| --- | --- |
| std::atomic_is_lock_free(std::shared_ptr)std::atomic_load(std::shared_ptr)std::atomic_load_explicit(std::shared_ptr)std::atomic_store(std::shared_ptr)std::atomic_store_explicit(std::shared_ptr)std::atomic_exchange(std::shared_ptr)std::atomic_exchange_explicit(std::shared_ptr)std::atomic_compare_exchange_weak(std::shared_ptr)std::atomic_compare_exchange_strong(std::shared_ptr)std::atomic_compare_exchange_weak_explicit(std::shared_ptr)std::atomic_compare_exchange_strong_explicit(std::shared_ptr)(deprecated in C++20)(removed in C++26) | specializes atomic operations for `std::shared_ptr`   (function template) |

|  |  |
| --- | --- |
| Function-like entities | |
| Defined in namespace `std::ranges` | |
| Uninitialized storage | |
| ranges::uninitialized_copy(C++20) | copies a range of objects to an uninitialized area of memory (algorithm function object) |
| ranges::uninitialized_copy_n(C++20) | copies a number of objects to an uninitialized area of memory (algorithm function object) |
| ranges::uninitialized_fill(C++20) | copies an object to an uninitialized area of memory, defined by a range (algorithm function object) |
| ranges::uninitialized_fill_n(C++20) | copies an object to an uninitialized area of memory, defined by a start and a count (algorithm function object) |
| ranges::uninitialized_move(C++20) | moves a range of objects to an uninitialized area of memory (algorithm function object) |
| ranges::uninitialized_move_n(C++20) | moves a number of objects to an uninitialized area of memory (algorithm function object) |
| ranges::uninitialized_default_construct(C++20) | constructs objects by default-initialization in an uninitialized area of memory, defined by a range (algorithm function object) |
| ranges::uninitialized_default_construct_n(C++20) | constructs objects by default-initialization in an uninitialized area of memory, defined by a start and count (algorithm function object) |
| ranges::uninitialized_value_construct(C++20) | constructs objects by value-initialization in an uninitialized area of memory, defined by a range (algorithm function object) |
| ranges::uninitialized_value_construct_n(C++20) | constructs objects by value-initialization in an uninitialized area of memory, defined by a start and a count (algorithm function object) |
| ranges::construct_at(C++20) | creates an object at a given address (algorithm function object) |
| ranges::destroy_at(C++20) | destroys an object at a given address (algorithm function object) |
| ranges::destroy(C++20) | destroys a range of objects (algorithm function object) |
| ranges::destroy_n(C++20) | destroys a number of objects in a range (algorithm function object) |

### Synopsis

```
#include <compare>
 
namespace std {
  // pointer traits
  template<class Ptr> struct pointer_traits;
  template<class T> struct pointer_traits<T*>;
 
  // pointer conversion
  template<class T>
    constexpr T* to_address(T* p) noexcept;
  template<class Ptr>
    constexpr auto to_address(const Ptr& p) noexcept;
 
  // pointer alignment
  void* align(size_t alignment, size_t size, void*& ptr, size_t& space);
  template<size_t N, class T>
    constexpr T* assume_aligned(T* ptr);
 
  // explicit lifetime management
  template<class T>
    T* start_lifetime_as(void* p) noexcept;                                   // freestanding
  template<class T>
    const T* start_lifetime_as(const void* p) noexcept;                       // freestanding
  template<class T>
    volatile T* start_lifetime_as(volatile void* p) noexcept;                 // freestanding
  template<class T>
    const volatile T* start_lifetime_as(const volatile void* p) noexcept;     // freestanding
  template<class T>
    T* start_lifetime_as_array(void* p, size_t n) noexcept;                   // freestanding
  template<class T>
    const T* start_lifetime_as_array(const void* p, size_t n) noexcept;       // freestanding
  template<class T>
    volatile T* start_lifetime_as_array(volatile void* p, size_t n) noexcept; // freestanding
  template<class T>
    const volatile T* start_lifetime_as_array(const volatile void* p,         // freestanding
                                              size_t n) noexcept;
 
  // allocator argument tag
  struct allocator_arg_t { explicit allocator_arg_t() = default; };
  inline constexpr allocator_arg_t allocator_arg{};
 
  // uses_allocator
  template<class T, class Alloc> struct uses_allocator;
 
  // uses_allocator
  template<class T, class Alloc>
    inline constexpr bool uses_allocator_v = uses_allocator<T, Alloc>::value;
 
  // uses-allocator construction
  template<class T, class Alloc, class... Args>
    constexpr auto uses_allocator_construction_args(const Alloc& alloc,
                                                    Args&&... args) noexcept;
  template<class T, class Alloc, class Tuple1, class Tuple2>
    constexpr auto uses_allocator_construction_args(const Alloc& alloc, piecewise_construct_t,
                                                    Tuple1&& x, Tuple2&& y) noexcept;
  template<class T, class Alloc>
    constexpr auto uses_allocator_construction_args(const Alloc& alloc) noexcept;
  template<class T, class Alloc, class U, class V>
    constexpr auto uses_allocator_construction_args(const Alloc& alloc,
                                                    U&& u, V&& v) noexcept;
  template<class T, class Alloc, class U, class V>
    constexpr auto uses_allocator_construction_args(const Alloc& alloc,
                                                    const pair<U, V>& pr) noexcept;
  template<class T, class Alloc, class U, class V>
    constexpr auto uses_allocator_construction_args(const Alloc& alloc,
                                                    pair<U, V>&& pr) noexcept;
  template<class T, class Alloc, class... Args>
    constexpr T make_obj_using_allocator(const Alloc& alloc, Args&&... args);
  template<class T, class Alloc, class... Args>
    constexpr T* uninitialized_construct_using_allocator(T* p, const Alloc& alloc,
                                                         Args&&... args);
 
  // allocator traits
  template<class Alloc> struct allocator_traits;
 
  template<class Pointer, class SizeType = size_t>
  struct allocation_result {
    Pointer ptr;
    SizeType count;
  };
 
  // the default allocator
  template<class T> class allocator;
  template<class T, class U>
    constexpr bool operator==(const allocator<T>&, const allocator<U>&) noexcept;
 
  // addressof
  template<class T>
    constexpr T* addressof(T& r) noexcept;
  template<class T>
    const T* addressof(const T&&) = delete;
 
  // specialized algorithms
  // special memory concepts
  template<class I>
    concept no-throw-input-iterator = /* see description */;    // exposition only
  template<class I>
    concept no-throw-forward-iterator = /* see description */;  // exposition only
  template<class S, class I>
    concept no-throw-sentinel-for = /* see description */;      // exposition only
  template<class R>
    concept no-throw-input-range = /* see description */;       // exposition only
  template<class R>
    concept no-throw-forward-range = /* see description */;     // exposition only
 
  template<class NoThrowForwardIt>
    void uninitialized_default_construct(NoThrowForwardIt first,
                                         NoThrowForwardIt last);
  template<class ExecutionPolicy, class NoThrowForwardIt>
    void uninitialized_default_construct(ExecutionPolicy&& exec,
                                         NoThrowForwardIt first,
                                         NoThrowForwardIt last);
  template<class NoThrowForwardIt, class Size>
    NoThrowForwardIt
      uninitialized_default_construct_n(NoThrowForwardIt first, Size n);
  template<class ExecutionPolicy, class NoThrowForwardIt, class Size>
    NoThrowForwardIt
      uninitialized_default_construct_n(ExecutionPolicy&& exec,
                                        NoThrowForwardIt first, Size n);
 
  namespace ranges {
    template<no-throw-forward-iterator I, no-throw-sentinel-for<I> S>
      requires default_initializable<iter_value_t<I>>
        I uninitialized_default_construct(I first, S last);
    template<no-throw-forward-range R>
      requires default_initializable<range_value_t<R>>
        borrowed_iterator_t<R> uninitialized_default_construct(R&& r);
 
    template<no-throw-forward-iterator I>
      requires default_initializable<iter_value_t<I>>
        I uninitialized_default_construct_n(I first, iter_difference_t<I> n);
  }
 
  template<class NoThrowForwardIterator>
    void uninitialized_value_construct(NoThrowForwardIterator first,
                                       NoThrowForwardIterator last);
  template<class ExecutionPolicy, class NoThrowForwardIt>
    void uninitialized_value_construct(ExecutionPolicy&& exec,
                                       NoThrowForwardIt first,
                                       NoThrowForwardIt last);
  template<class NoThrowForwardIt, class Size>
    NoThrowForwardIt
      uninitialized_value_construct_n(NoThrowForwardIt first, Size n);
  template<class ExecutionPolicy, class NoThrowForwardIt, class Size>
    NoThrowForwardIt
      uninitialized_value_construct_n(ExecutionPolicy&& exec,
                                      NoThrowForwardIt first, Size n);
 
  namespace ranges {
    template<no-throw-forward-iterator I, no-throw-sentinel-for<I> S>
      requires default_initializable<iter_value_t<I>>
        I uninitialized_value_construct(I first, S last);
    template<no-throw-forward-range R>
      requires default_initializable<range_value_t<R>>
        borrowed_iterator_t<R> uninitialized_value_construct(R&& r);
 
    template<no-throw-forward-iterator I>
      requires default_initializable<iter_value_t<I>>
        I uninitialized_value_construct_n(I first, iter_difference_t<I> n);
  }
 
  template<class InputIt, class NoThrowForwardIt>
    NoThrowForwardIt uninitialized_copy(InputIt first, InputIt last,
                                        NoThrowForwardIt result);
  template<class ExecutionPolicy, class ForwardIt, class NoThrowForwardIt>
    NoThrowForwardIt uninitialized_copy(ExecutionPolicy&& exec,
                                        ForwardIt first, ForwardIt last,
                                        NoThrowForwardIt result);
  template<class InputIt, class Size, class NoThrowForwardIt>
    NoThrowForwardIt uninitialized_copy_n(InputIt first, Size n,
                                          NoThrowForwardIt result);
  template<class ExecutionPolicy, class ForwardIt, class Size,
           class NoThrowForwardIt>
    NoThrowForwardIt uninitialized_copy_n(ExecutionPolicy&& exec,
                                          ForwardIt first, Size n,
                                          NoThrowForwardIt result);
 
  namespace ranges {
    template<class I, class O>
      using uninitialized_copy_result = in_out_result<I, O>;
    template<input_iterator I, sentinel_for<I> S1,
             no-throw-forward-iterator O, no-throw-sentinel-for<O> S2>
      requires constructible_from<iter_value_t<O>, iter_reference_t<I>>
        uninitialized_copy_result<I, O>
          uninitialized_copy(I ifirst, S1 ilast, O ofirst, S2 olast);
    template<input_range IR, no-throw-forward-range OR>
      requires constructible_from<range_value_t<OR>, range_reference_t<IR>>
        uninitialized_copy_result<borrowed_iterator_t<IR>, borrowed_iterator_t<OR>>
          uninitialized_copy(IR&& in_range, OR&& out_range);
 
    template<class I, class O>
      using uninitialized_copy_n_result = in_out_result<I, O>;
    template<input_iterator I, no-throw-forward-iterator O, no-throw-sentinel-for<O> S>
      requires constructible_from<iter_value_t<O>, iter_reference_t<I>>
        uninitialized_copy_n_result<I, O>
          uninitialized_copy_n(I ifirst, iter_difference_t<I> n, O ofirst, S olast);
  }
 
  template<class InputIt, class NoThrowForwardIt>
    NoThrowForwardIt uninitialized_move(InputIt first, InputIt last,
                                        NoThrowForwardIt result);
  template<class ExecutionPolicy, class ForwardIt, class NoThrowForwardIt>
    NoThrowForwardIt uninitialized_move(ExecutionPolicy&& exec,
                                        ForwardIt first, ForwardIt last,
                                        NoThrowForwardIt result);
  template<class InputIt, class Size, class NoThrowForwardIt>
    pair<InputIt, NoThrowForwardIt>
      uninitialized_move_n(InputIt first, Size n, NoThrowForwardIt result);
  template<class ExecutionPolicy, class ForwardIt, class Size,
           class NoThrowForwardIt>
    pair<ForwardIt, NoThrowForwardIt>
      uninitialized_move_n(ExecutionPolicy&& exec,
                           ForwardIt first, Size n, NoThrowForwardIt result);
 
  namespace ranges {
    template<class I, class O>
      using uninitialized_move_result = in_out_result<I, O>;
    template<input_iterator I, sentinel_for<I> S1,
             no-throw-forward-iterator O, no-throw-sentinel-for<O> S2>
      requires constructible_from<iter_value_t<O>, iter_rvalue_reference_t<I>>
        uninitialized_move_result<I, O>
          uninitialized_move(I ifirst, S1 ilast, O ofirst, S2 olast);
    template<input_range IR, no-throw-forward-range OR>
      requires constructible_from<range_value_t<OR>, range_rvalue_reference_t<IR>>
        uninitialized_move_result<borrowed_iterator_t<IR>, borrowed_iterator_t<OR>>
          uninitialized_move(IR&& in_range, OR&& out_range);
 
    template<class I, class O>
      using uninitialized_move_n_result = in_out_result<I, O>;
    template<input_iterator I,
             no-throw-forward-iterator O, no-throw-sentinel-for<O> S>
      requires constructible_from<iter_value_t<O>, iter_rvalue_reference_t<I>>
        uninitialized_move_n_result<I, O>
          uninitialized_move_n(I ifirst, iter_difference_t<I> n, O ofirst, S olast);
  }
 
  template<class NoThrowForwardIt, class T>
    void uninitialized_fill(NoThrowForwardIt first, NoThrowForwardIt last,
                            const T& x);
  template<class ExecutionPolicy, class NoThrowForwardIt, class T>
    void uninitialized_fill(ExecutionPolicy&& exec,
                            NoThrowForwardIt first, NoThrowForwardIt last,
                            const T& x);
  template<class NoThrowForwardIt, class Size, class T>
    NoThrowForwardIt
      uninitialized_fill_n(NoThrowForwardIt first, Size n, const T& x);
  template<class ExecutionPolicy, class NoThrowForwardIt, class Size, class T>
    NoThrowForwardIt
      uninitialized_fill_n(ExecutionPolicy&& exec,
                           NoThrowForwardIt first, Size n, const T& x);
 
  namespace ranges {
    template<no-throw-forward-iterator I, no-throw-sentinel-for<I> S, class T>
      requires constructible_from<iter_value_t<I>, const T&>
        I uninitialized_fill(I first, S last, const T& x);
    template<no-throw-forward-range R, class T>
      requires constructible_from<range_value_t<R>, const T&>
        borrowed_iterator_t<R> uninitialized_fill(R&& r, const T& x);
 
    template<no-throw-forward-iterator I, class T>
      requires constructible_from<iter_value_t<I>, const T&>
        I uninitialized_fill_n(I first, iter_difference_t<I> n, const T& x);
  }
 
  // construct_at
  template<class T, class... Args>
    constexpr T* construct_at(T* location, Args&&... args);
 
  namespace ranges {
    template<class T, class... Args>
      constexpr T* construct_at(T* location, Args&&... args);
  }
 
  // destroy
  template<class T>
    constexpr void destroy_at(T* location);
  template<class NoThrowForwardIt>
    constexpr void destroy(NoThrowForwardIt first, NoThrowForwardIt last);
  template<class ExecutionPolicy, class NoThrowForwardIt>
    void destroy(ExecutionPolicy&& exec,
                 NoThrowForwardIt first, NoThrowForwardIt last);
  template<class NoThrowForwardIt, class Size>
    constexpr NoThrowForwardIt destroy_n(NoThrowForwardIt first, Size n);
  template<class ExecutionPolicy, class NoThrowForwardIt, class Size>
    NoThrowForwardIt destroy_n(ExecutionPolicy&& exec,
                               NoThrowForwardIt first, Size n);
 
  namespace ranges {
    template<destructible T>
      constexpr void destroy_at(T* location) noexcept;
 
    template<no-throw-input-iterator I, no-throw-sentinel-for<I> S>
      requires destructible<iter_value_t<I>>
        constexpr I destroy(I first, S last) noexcept;
    template<no-throw-input-range R>
      requires destructible<range_value_t<R>>
        constexpr borrowed_iterator_t<R> destroy(R&& r) noexcept;
 
    template<no-throw-input-iterator I>
      requires destructible<iter_value_t<I>>
        constexpr I destroy_n(I first, iter_difference_t<I> n) noexcept;
  }
 
  // class template unique_ptr
  template<class T> struct default_delete;
  template<class T> struct default_delete<T[]>;
  template<class T, class D = default_delete<T>> class unique_ptr;
  template<class T, class D> class unique_ptr<T[], D>;
 
  template<class T, class... Args>
    unique_ptr<T> make_unique(Args&&... args);                                  // T is not array
  template<class T>
    unique_ptr<T> make_unique(size_t n);                                        // T is U[]
  template<class T, class... Args>
    /* unspecified */ make_unique(Args&&...) = delete;                          // T is U[N]
 
  template<class T>
    unique_ptr<T> make_unique_for_overwrite();                                  // T is not array
  template<class T>
    unique_ptr<T> make_unique_for_overwrite(size_t n);                          // T is U[]
  template<class T, class... Args>
    /* unspecified */ make_unique_for_overwrite(Args&&...) = delete;            // T is U[N]
 
  template<class T, class D>
    void swap(unique_ptr<T, D>& x, unique_ptr<T, D>& y) noexcept;
 
  template<class T1, class D1, class T2, class D2>
    bool operator==(const unique_ptr<T1, D1>& x, const unique_ptr<T2, D2>& y);
  template<class T1, class D1, class T2, class D2>
    bool operator<(const unique_ptr<T1, D1>& x, const unique_ptr<T2, D2>& y);
  template<class T1, class D1, class T2, class D2>
    bool operator>(const unique_ptr<T1, D1>& x, const unique_ptr<T2, D2>& y);
  template<class T1, class D1, class T2, class D2>
    bool operator<=(const unique_ptr<T1, D1>& x, const unique_ptr<T2, D2>& y);
  template<class T1, class D1, class T2, class D2>
    bool operator>=(const unique_ptr<T1, D1>& x, const unique_ptr<T2, D2>& y);
  template<class T1, class D1, class T2, class D2>
    requires three_way_comparable_with<typename unique_ptr<T1, D1>::pointer,
                                       typename unique_ptr<T2, D2>::pointer>
    compare_three_way_result_t<typename unique_ptr<T1, D1>::pointer,
                               typename unique_ptr<T2, D2>::pointer>
      operator<=>(const unique_ptr<T1, D1>& x, const unique_ptr<T2, D2>& y);
 
  template<class T, class D>
    bool operator==(const unique_ptr<T, D>& x, nullptr_t) noexcept;
  template<class T, class D>
    bool operator<(const unique_ptr<T, D>& x, nullptr_t);
  template<class T, class D>
    bool operator<(nullptr_t, const unique_ptr<T, D>& y);
  template<class T, class D>
    bool operator>(const unique_ptr<T, D>& x, nullptr_t);
  template<class T, class D>
    bool operator>(nullptr_t, const unique_ptr<T, D>& y);
  template<class T, class D>
    bool operator<=(const unique_ptr<T, D>& x, nullptr_t);
  template<class T, class D>
    bool operator<=(nullptr_t, const unique_ptr<T, D>& y);
  template<class T, class D>
    bool operator>=(const unique_ptr<T, D>& x, nullptr_t);
  template<class T, class D>
    bool operator>=(nullptr_t, const unique_ptr<T, D>& y);
  template<class T, class D>
    requires three_way_comparable<typename unique_ptr<T, D>::pointer>
    compare_three_way_result_t<typename unique_ptr<T, D>::pointer>
      operator<=>(const unique_ptr<T, D>& x, nullptr_t);
 
  template<class E, class T, class Y, class D>
    basic_ostream<E, T>& operator<<(basic_ostream<E, T>& os, const unique_ptr<Y, D>& p);
 
  // class bad_weak_ptr
  class bad_weak_ptr;
 
  // class template shared_ptr
  template<class T> class shared_ptr;
 
  // shared_ptr creation
  template<class T, class... Args>
    shared_ptr<T> make_shared(Args&&... args);                                  // T is not array
  template<class T, class A, class... Args>
    shared_ptr<T> allocate_shared(const A& a, Args&&... args);                  // T is not array
 
  template<class T>
    shared_ptr<T> make_shared(size_t N);                                        // T is U[]
  template<class T, class A>
    shared_ptr<T> allocate_shared(const A& a, size_t N);                        // T is U[]
 
  template<class T>
    shared_ptr<T> make_shared();                                                // T is U[N]
  template<class T, class A>
    shared_ptr<T> allocate_shared(const A& a);                                  // T is U[N]
 
  template<class T>
    shared_ptr<T> make_shared(size_t N, const remove_extent_t<T>& u);           // T is U[]
  template<class T, class A>
    shared_ptr<T> allocate_shared(const A& a, size_t N,
                                  const remove_extent_t<T>& u);                 // T is U[]
 
  template<class T>
    shared_ptr<T> make_shared(const remove_extent_t<T>& u);                     // T is U[N]
  template<class T, class A>
    shared_ptr<T> allocate_shared(const A& a, const remove_extent_t<T>& u);     // T is U[N]
 
  template<class T>
    shared_ptr<T> make_shared_for_overwrite();                                  // T is not U[]
  template<class T, class A>
    shared_ptr<T> allocate_shared_for_overwrite(const A& a);                    // T is not U[]
 
  template<class T>
    shared_ptr<T> make_shared_for_overwrite(size_t N);                          // T is U[]
  template<class T, class A>
    shared_ptr<T> allocate_shared_for_overwrite(const A& a, size_t N);          // T is U[]
 
  // shared_ptr comparisons
  template<class T, class U>
    bool operator==(const shared_ptr<T>& a, const shared_ptr<U>& b) noexcept;
  template<class T, class U>
    strong_ordering operator<=>(const shared_ptr<T>& a, const shared_ptr<U>& b) noexcept;
 
  template<class T>
    bool operator==(const shared_ptr<T>& x, nullptr_t) noexcept;
  template<class T>
    strong_ordering operator<=>(const shared_ptr<T>& x, nullptr_t) noexcept;
 
  // shared_ptr specialized algorithms
  template<class T>
    void swap(shared_ptr<T>& a, shared_ptr<T>& b) noexcept;
 
  // shared_ptr casts
  template<class T, class U>
    shared_ptr<T> static_pointer_cast(const shared_ptr<U>& r) noexcept;
  template<class T, class U>
    shared_ptr<T> static_pointer_cast(shared_ptr<U>&& r) noexcept;
  template<class T, class U>
    shared_ptr<T> dynamic_pointer_cast(const shared_ptr<U>& r) noexcept;
  template<class T, class U>
    shared_ptr<T> dynamic_pointer_cast(shared_ptr<U>&& r) noexcept;
  template<class T, class U>
    shared_ptr<T> const_pointer_cast(const shared_ptr<U>& r) noexcept;
  template<class T, class U>
    shared_ptr<T> const_pointer_cast(shared_ptr<U>&& r) noexcept;
  template<class T, class U>
    shared_ptr<T> reinterpret_pointer_cast(const shared_ptr<U>& r) noexcept;
  template<class T, class U>
    shared_ptr<T> reinterpret_pointer_cast(shared_ptr<U>&& r) noexcept;
 
  // shared_ptr get_deleter
  template<class D, class T>
    D* get_deleter(const shared_ptr<T>& p) noexcept;
 
  // shared_ptr I/O
  template<class E, class T, class Y>
    basic_ostream<E, T>& operator<<(basic_ostream<E, T>& os, const shared_ptr<Y>& p);
 
  // class template weak_ptr
  template<class T> class weak_ptr;
 
  // weak_ptr specialized algorithms
  template<class T> void swap(weak_ptr<T>& a, weak_ptr<T>& b) noexcept;
 
  // class template owner_less
  template<class T = void> struct owner_less;
 
  // class template enable_shared_from_this
  template<class T> class enable_shared_from_this;
 
  // hash support
  template<class T> struct hash;
  template<class T, class D> struct hash<unique_ptr<T, D>>;
  template<class T> struct hash<shared_ptr<T>>;
 
  // atomic smart pointers
  template<class T> struct atomic;
  template<class T> struct atomic<shared_ptr<T>>;
  template<class T> struct atomic<weak_ptr<T>>;
 
  // class template out_ptr_t
  template<class Smart, class Pointer, class... Args>
    class out_ptr_t;
 
  // function template out_ptr
  template<class Pointer = void, class Smart, class... Args>
    auto out_ptr(Smart& s, Args&&... args);
 
  // class template inout_ptr_t
  template<class Smart, class Pointer, class... Args>
    class inout_ptr_t;
 
  // function template inout_ptr
  template<class Pointer = void, class Smart, class... Args>
    auto inout_ptr(Smart& s, Args&&... args);
}
 
// deprecated
namespace std {
  template<class T>
    bool atomic_is_lock_free(const shared_ptr<T>* p);
 
  template<class T>
    shared_ptr<T> atomic_load(const shared_ptr<T>* p);
  template<class T>
    shared_ptr<T> atomic_load_explicit(const shared_ptr<T>* p, memory_order mo);
 
  template<class T>
    void atomic_store(shared_ptr<T>* p, shared_ptr<T> r);
  template<class T>
    void atomic_store_explicit(shared_ptr<T>* p, shared_ptr<T> r, memory_order mo);
 
  template<class T>
    shared_ptr<T> atomic_exchange(shared_ptr<T>* p, shared_ptr<T> r);
  template<class T>
    shared_ptr<T> atomic_exchange_explicit(shared_ptr<T>* p, shared_ptr<T> r, memory_order mo);
 
  template<class T>
    bool atomic_compare_exchange_weak(shared_ptr<T>* p, shared_ptr<T>* v, shared_ptr<T> w);
  template<class T>
    bool atomic_compare_exchange_strong(shared_ptr<T>* p, shared_ptr<T>* v, shared_ptr<T> w);
  template<class T>
    bool atomic_compare_exchange_weak_explicit(
      shared_ptr<T>* p, shared_ptr<T>* v, shared_ptr<T> w,
      memory_order success, memory_order failure);
  template<class T>
    bool atomic_compare_exchange_strong_explicit(
      shared_ptr<T>* p, shared_ptr<T>* v, shared_ptr<T> w,
      memory_order success, memory_order failure);
}

```

#### Helper concepts

Note: These names are only for exposition, they are not part of the interface.

```
template<class I>
concept no-throw-input-iterator = // exposition only
  input_iterator<I> &&
  is_lvalue_reference_v<iter_reference_t<I>> &&
  same_as<remove_cvref_t<iter_reference_t<I>>, iter_value_t<I>>;
 
template<class S, class I>
concept no-throw-sentinel-for = sentinel_for<S, I>; // exposition only
 
template<class R>
concept no-throw-input-range = // exposition only
  ranges::range<R> &&
  no-throw-input-iterator<ranges::iterator_t<R>> &&
  no-throw-sentinel-for<ranges::sentinel_t<R>, ranges::iterator_t<R>>;
 
template<class I>
concept no-throw-forward-iterator = // exposition only
  no-throw-input-iterator<I> &&
  forward_iterator<I> &&
  no-throw-sentinel-for<I, I>;
 
template<class R>
concept no-throw-forward-range = // exposition only
  no-throw-input-range<R> &&
  no-throw-forward-iterator<ranges::iterator_t<R>>;

```

#### Class template std::pointer_traits

```
namespace std {
  template<class Ptr> struct pointer_traits {
    using pointer         = Ptr;
    using element_type    = /* see description */;
    using difference_type = /* see description */;
 
    template<class U> using rebind = /* see description */;
 
    static pointer pointer_to(/* see description */ r);
  };
 
  template<class T> struct pointer_traits<T*> {
    using pointer         = T*;
    using element_type    = T;
    using difference_type = ptrdiff_t;
 
    template<class U> using rebind = U*;
 
    static constexpr pointer pointer_to(/* see description */ r) noexcept;
  };
}

```

#### Class std::allocator_arg_t

```
namespace std {
  struct allocator_arg_t { explicit allocator_arg_t() = default; };
  inline constexpr allocator_arg_t allocator_arg{};
}

```

#### Class template std::allocator_traits

```
namespace std {
  template<class Alloc> struct allocator_traits {
    using allocator_type     = Alloc;
 
    using value_type         = typename Alloc::value_type;
 
    using pointer            = /* see description */;
    using const_pointer      = /* see description */;
    using void_pointer       = /* see description */;
    using const_void_pointer = /* see description */;
 
    using difference_type    = /* see description */;
    using size_type          = /* see description */;
 
    using propagate_on_container_copy_assignment = /* see description */;
    using propagate_on_container_move_assignment = /* see description */;
    using propagate_on_container_swap            = /* see description */;
    using is_always_equal                        = /* see description */;
 
    template<class T> using rebind_alloc = /* see description */;
    template<class T> using rebind_traits = allocator_traits<rebind_alloc<T>>;
 
    static pointer allocate(Alloc& a, size_type n);
    static pointer allocate(Alloc& a, size_type n,
                            const_void_pointer hint);
 
    static constexpr allocation_result<pointer, size_type>
          allocate_at_least(Alloc& a, size_type n);
 
    static void deallocate(Alloc& a, pointer p, size_type n);
 
    template<class T, class... Args>
      static void construct(Alloc& a, T* p, Args&&... args);
 
    template<class T>
      static void destroy(Alloc& a, T* p);
 
    static size_type max_size(const Alloc& a) noexcept;
 
    static Alloc select_on_container_copy_construction(const Alloc& rhs);
  };
}

```

#### Class template std::allocator

```
namespace std {
  template<class T> class allocator {
   public:
    using value_type                             = T;
    using size_type                              = size_t;
    using difference_type                        = ptrdiff_t;
    using propagate_on_container_move_assignment = true_type;
 
    constexpr allocator() noexcept;
    constexpr allocator(const allocator&) noexcept;
    template<class U> constexpr allocator(const allocator<U>&) noexcept;
    constexpr ~allocator();
    constexpr allocator& operator=(const allocator&) = default;
 
    constexpr T* allocate(size_t n);
    constexpr allocation_result<T*> allocate_at_least(size_t n);
    constexpr void deallocate(T* p, size_t n);
 
    // deprecated
    using is_always_equal = true_type;
  };
}

```

#### Class template std::default_delete

```
namespace std {
  template<class T> struct default_delete {
    constexpr default_delete() noexcept = default;
    template<class U> default_delete(const default_delete<U>&) noexcept;
    void operator()(T*) const;
  };
 
  template<class T> struct default_delete<T[]> {
    constexpr default_delete() noexcept = default;
    template<class U> default_delete(const default_delete<U[]>&) noexcept;
    template<class U> void operator()(U* ptr) const;
  };
}

```

#### Class template std::unique_ptr

```
namespace std {
  template<class T, class D = default_delete<T>> class unique_ptr {
  public:
    using pointer      = /* see description */;
    using element_type = T;
    using deleter_type = D;
 
    // constructors
    constexpr unique_ptr() noexcept;
    explicit unique_ptr(pointer p) noexcept;
    unique_ptr(pointer p, /* see description */ d1) noexcept;
    unique_ptr(pointer p, /* see description */ d2) noexcept;
    unique_ptr(unique_ptr&& u) noexcept;
    constexpr unique_ptr(nullptr_t) noexcept;
    template<class U, class E>
      unique_ptr(unique_ptr<U, E>&& u) noexcept;
 
    // destructor
    ~unique_ptr();
 
    // assignment
    unique_ptr& operator=(unique_ptr&& u) noexcept;
    template<class U, class E>
      unique_ptr& operator=(unique_ptr<U, E>&& u) noexcept;
    unique_ptr& operator=(nullptr_t) noexcept;
 
    // observers
    add_lvalue_reference_t<T> operator*() const noexcept(/* see description */);
    pointer operator->() const noexcept;
    pointer get() const noexcept;
    deleter_type& get_deleter() noexcept;
    const deleter_type& get_deleter() const noexcept;
    explicit operator bool() const noexcept;
 
    // modifiers
    pointer release() noexcept;
    void reset(pointer p = pointer()) noexcept;
    void swap(unique_ptr& u) noexcept;
 
    // disable copy from lvalue
    unique_ptr(const unique_ptr&) = delete;
    unique_ptr& operator=(const unique_ptr&) = delete;
  };
 
  template<class T, class D> class unique_ptr<T[], D> {
  public:
    using pointer      = /* see description */;
    using element_type = T;
    using deleter_type = D;
 
    // constructors
    constexpr unique_ptr() noexcept;
    template<class U> explicit unique_ptr(U p) noexcept;
    template<class U> unique_ptr(U p, /* see description */ d) noexcept;
    template<class U> unique_ptr(U p, /* see description */ d) noexcept;
    unique_ptr(unique_ptr&& u) noexcept;
    template<class U, class E>
      unique_ptr(unique_ptr<U, E>&& u) noexcept;
    constexpr unique_ptr(nullptr_t) noexcept;
 
    // destructor
    ~unique_ptr();
 
    // assignment
    unique_ptr& operator=(unique_ptr&& u) noexcept;
    template<class U, class E>
      unique_ptr& operator=(unique_ptr<U, E>&& u) noexcept;
    unique_ptr& operator=(nullptr_t) noexcept;
 
    // observers
    T& operator[](size_t i) const;
    pointer get() const noexcept;
    deleter_type& get_deleter() noexcept;
    const deleter_type& get_deleter() const noexcept;
    explicit operator bool() const noexcept;
 
    // modifiers
    pointer release() noexcept;
    template<class U> void reset(U p) noexcept;
    void reset(nullptr_t = nullptr) noexcept;
    void swap(unique_ptr& u) noexcept;
 
    // disable copy from lvalue
    unique_ptr(const unique_ptr&) = delete;
    unique_ptr& operator=(const unique_ptr&) = delete;
  };
}

```

#### Class std::bad_weak_ptr

```
namespace std {
  class bad_weak_ptr : public exception {
  public:
    bad_weak_ptr() noexcept;
  };
}

```

#### Class template std::shared_ptr

```
namespace std {
  template<class T> class shared_ptr {
  public:
    using element_type = remove_extent_t<T>;
    using weak_type    = weak_ptr<T>;
 
    // constructors
    constexpr shared_ptr() noexcept;
    constexpr shared_ptr(nullptr_t) noexcept : shared_ptr() { }
    template<class Y>
      explicit shared_ptr(Y* p);
    template<class Y, class D>
      shared_ptr(Y* p, D d);
    template<class Y, class D, class A>
      shared_ptr(Y* p, D d, A a);
    template<class D>
      shared_ptr(nullptr_t p, D d);
    template<class D, class A>
      shared_ptr(nullptr_t p, D d, A a);
    template<class Y>
      shared_ptr(const shared_ptr<Y>& r, element_type* p) noexcept;
    template<class Y>
      shared_ptr(shared_ptr<Y>&& r, element_type* p) noexcept;
    shared_ptr(const shared_ptr& r) noexcept;
    template<class Y>
      shared_ptr(const shared_ptr<Y>& r) noexcept;
    shared_ptr(shared_ptr&& r) noexcept;
    template<class Y>
      shared_ptr(shared_ptr<Y>&& r) noexcept;
    template<class Y>
      explicit shared_ptr(const weak_ptr<Y>& r);
    template<class Y, class D>
      shared_ptr(unique_ptr<Y, D>&& r);
 
    // destructor
    ~shared_ptr();
 
    // assignment
    shared_ptr& operator=(const shared_ptr& r) noexcept;
    template<class Y>
      shared_ptr& operator=(const shared_ptr<Y>& r) noexcept;
    shared_ptr& operator=(shared_ptr&& r) noexcept;
    template<class Y>
      shared_ptr& operator=(shared_ptr<Y>&& r) noexcept;
    template<class Y, class D>
      shared_ptr& operator=(unique_ptr<Y, D>&& r);
 
    // modifiers
    void swap(shared_ptr& r) noexcept;
    void reset() noexcept;
    template<class Y>
      void reset(Y* p);
    template<class Y, class D>
      void reset(Y* p, D d);
    template<class Y, class D, class A>
      void reset(Y* p, D d, A a);
 
    // observers
    element_type* get() const noexcept;
    T& operator*() const noexcept;
    T* operator->() const noexcept;
    element_type& operator[](ptrdiff_t i) const;
    long use_count() const noexcept;
    explicit operator bool() const noexcept;
    template<class U>
      bool owner_before(const shared_ptr<U>& b) const noexcept;
    template<class U>
      bool owner_before(const weak_ptr<U>& b) const noexcept;
  };
 
  template<class T>
    shared_ptr(weak_ptr<T>) -> shared_ptr<T>;
  template<class T, class D>
    shared_ptr(unique_ptr<T, D>) -> shared_ptr<T>;
}

```

#### Class template std::weak_ptr

```
namespace std {
  template<class T> class weak_ptr {
  public:
    using element_type = remove_extent_t<T>;
 
    // constructors
    constexpr weak_ptr() noexcept;
    template<class Y>
      weak_ptr(const shared_ptr<Y>& r) noexcept;
    weak_ptr(const weak_ptr& r) noexcept;
    template<class Y>
      weak_ptr(const weak_ptr<Y>& r) noexcept;
    weak_ptr(weak_ptr&& r) noexcept;
    template<class Y>
      weak_ptr(weak_ptr<Y>&& r) noexcept;
 
    // destructor
    ~weak_ptr();
 
    // assignment
    weak_ptr& operator=(const weak_ptr& r) noexcept;
    template<class Y>
      weak_ptr& operator=(const weak_ptr<Y>& r) noexcept;
    template<class Y>
      weak_ptr& operator=(const shared_ptr<Y>& r) noexcept;
    weak_ptr& operator=(weak_ptr&& r) noexcept;
    template<class Y>
      weak_ptr& operator=(weak_ptr<Y>&& r) noexcept;
 
    // modifiers
    void swap(weak_ptr& r) noexcept;
    void reset() noexcept;
 
    // observers
    long use_count() const noexcept;
    bool expired() const noexcept;
    shared_ptr<T> lock() const noexcept;
    template<class U>
      bool owner_before(const shared_ptr<U>& b) const noexcept;
    template<class U>
      bool owner_before(const weak_ptr<U>& b) const noexcept;
  };
 
  template<class T>
    weak_ptr(shared_ptr<T>) -> weak_ptr<T>;
}

```

#### Class template std::owner_less

```
namespace std {
  template<class T = void> struct owner_less;
 
  template<class T> struct owner_less<shared_ptr<T>> {
    bool operator()(const shared_ptr<T>&, const shared_ptr<T>&) const noexcept;
    bool operator()(const shared_ptr<T>&, const weak_ptr<T>&) const noexcept;
    bool operator()(const weak_ptr<T>&, const shared_ptr<T>&) const noexcept;
  };
 
  template<class T> struct owner_less<weak_ptr<T>> {
    bool operator()(const weak_ptr<T>&, const weak_ptr<T>&) const noexcept;
    bool operator()(const shared_ptr<T>&, const weak_ptr<T>&) const noexcept;
    bool operator()(const weak_ptr<T>&, const shared_ptr<T>&) const noexcept;
  };
 
  template<> struct owner_less<void> {
    template<class T, class U>
      bool operator()(const shared_ptr<T>&, const shared_ptr<U>&) const noexcept;
    template<class T, class U>
      bool operator()(const shared_ptr<T>&, const weak_ptr<U>&) const noexcept;
    template<class T, class U>
      bool operator()(const weak_ptr<T>&, const shared_ptr<U>&) const noexcept;
    template<class T, class U>
      bool operator()(const weak_ptr<T>&, const weak_ptr<U>&) const noexcept;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::enable_shared_from_this

```
namespace std {
  template<class T> class enable_shared_from_this {
  protected:
    constexpr enable_shared_from_this() noexcept;
    enable_shared_from_this(const enable_shared_from_this&) noexcept;
    enable_shared_from_this& operator=(const enable_shared_from_this&) noexcept;
    ~enable_shared_from_this();
 
  public:
    shared_ptr<T> shared_from_this();
    shared_ptr<T const> shared_from_this() const;
    weak_ptr<T> weak_from_this() noexcept;
    weak_ptr<T const> weak_from_this() const noexcept;
 
  private:
    mutable weak_ptr<T> weak_this;  // exposition only
  };
}

```

#### Class template std::atomic's specialization for std::shared_ptr

```
namespace std {
  template<class T> struct atomic<shared_ptr<T>> {
    using value_type = shared_ptr<T>;
    static constexpr bool is_always_lock_free = /* implementation-defined */;
 
    bool is_lock_free() const noexcept;
    void store(shared_ptr<T> desired, memory_order order = memory_order::seq_cst) noexcept;
    shared_ptr<T> load(memory_order order = memory_order::seq_cst) const noexcept;
    operator shared_ptr<T>() const noexcept;
 
    shared_ptr<T> exchange(shared_ptr<T> desired,
                           memory_order order = memory_order::seq_cst) noexcept;
 
    bool compare_exchange_weak(shared_ptr<T>& expected, shared_ptr<T> desired,
                               memory_order success, memory_order failure) noexcept;
    bool compare_exchange_strong(shared_ptr<T>& expected, shared_ptr<T> desired,
                                 memory_order success, memory_order failure) noexcept;
 
    bool compare_exchange_weak(shared_ptr<T>& expected, shared_ptr<T> desired,
                               memory_order order = memory_order::seq_cst) noexcept;
    bool compare_exchange_strong(shared_ptr<T>& expected, shared_ptr<T> desired,
                                 memory_order order = memory_order::seq_cst) noexcept;
 
    constexpr atomic() noexcept = default;
    atomic(shared_ptr<T> desired) noexcept;
    atomic(const atomic&) = delete;
    void operator=(const atomic&) = delete;
    void operator=(shared_ptr<T> desired) noexcept;
 
  private:
    shared_ptr<T> p;            // exposition only
  };
}

```

#### Class template std::atomic's specialization for std::weak_ptr

```
namespace std {
  template<class T> struct atomic<weak_ptr<T>> {
    using value_type = weak_ptr<T>;
    static constexpr bool is_always_lock_free = /* implementation-defined */;
 
    bool is_lock_free() const noexcept;
    void store(weak_ptr<T> desired, memory_order order = memory_order::seq_cst) noexcept;
    weak_ptr<T> load(memory_order order = memory_order::seq_cst) const noexcept;
    operator weak_ptr<T>() const noexcept;
 
    weak_ptr<T> exchange(weak_ptr<T> desired,
                         memory_order order = memory_order::seq_cst) noexcept;
 
    bool compare_exchange_weak(weak_ptr<T>& expected, weak_ptr<T> desired,
                               memory_order success, memory_order failure) noexcept;
    bool compare_exchange_strong(weak_ptr<T>& expected, weak_ptr<T> desired,
                                 memory_order success, memory_order failure) noexcept;
 
    bool compare_exchange_weak(weak_ptr<T>& expected, weak_ptr<T> desired,
                               memory_order order = memory_order::seq_cst) noexcept;
    bool compare_exchange_strong(weak_ptr<T>& expected, weak_ptr<T> desired,
                                 memory_order order = memory_order::seq_cst) noexcept;
 
    constexpr atomic() noexcept = default;
    atomic(weak_ptr<T> desired) noexcept;
    atomic(const atomic&) = delete;
    void operator=(const atomic&) = delete;
    void operator=(weak_ptr<T> desired) noexcept;
 
  private:
    weak_ptr<T> p;              // exposition only
  };
}

```

#### Class template std::out_ptr_t

```
namespace std {
  template<class Smart, class Pointer, class... Args>
  class out_ptr_t {
  public:
    explicit out_ptr_t(Smart&, Args...);
    out_ptr_t(const out_ptr_t&) = delete;
 
    ~out_ptr_t();
 
    operator Pointer*() const noexcept;
    operator void**() const noexcept;
 
  private:
    Smart& s;                   // exposition only
    tuple<Args...> a;           // exposition only
    Pointer p;                  // exposition only
  };
}

```

#### Class template std::inout_ptr_t

```
namespace std {
  template<class Smart, class Pointer, class... Args>
  class inout_ptr_t {
  public:
    explicit inout_ptr_t(Smart&, Args...);
    inout_ptr_t(const inout_ptr_t&) = delete;
 
    ~inout_ptr_t();
 
    operator Pointer*() const noexcept;
    operator void**() const noexcept;
 
  private:
    Smart& s;                   // exposition only
    tuple<Args...> a;           // exposition only
    Pointer p;                  // exposition only
  };
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/memory&oldid=178230>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 December 2024, at 02:54.