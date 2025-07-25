# Standard library header <functional>

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | ****<functional>**** | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the function objects library and provides the standard hash function.

|  |  |
| --- | --- |
| Namespaces | |
| placeholders (C++11) | Provides placeholders for the unbound arguments in a std::bind expression |
| Classes | |
| Wrappers | |
| function(C++11) | copyable wrapper of any copy constructible callable object   (class template) |
| move_only_function(C++23) | move-only wrapper of any callable object that supports qualifiers in a given call signature   (class template) |
| copyable_function(C++26) | copyable wrapper of any copy constructible callable object that supports qualifiers in a given call signature   (class template) |
| function_ref(C++26) | non-owning wrapper of any callable object   (class template) |
| mem_fn(C++11) | creates a function object out of a pointer to a member   (function template) |
| reference_wrapper(C++11) | CopyConstructible and CopyAssignable reference wrapper   (class template) |
| unwrap_referenceunwrap_ref_decay(C++20)(C++20) | get the reference type wrapped in std::reference_wrapper   (class template) |
| Helper classes | |
| bad_function_call(C++11) | the exception thrown when invoking an empty std::function   (class) |
| is_bind_expression(C++11) | indicates that an object is `std::bind` expression or can be used as one   (class template) |
| is_placeholder(C++11) | indicates that an object is a standard placeholder or can be used as one   (class template) |
| Arithmetic operations | |
| plus | function object implementing x + y   (class template) |
| minus | function object implementing x - y   (class template) |
| multiplies | function object implementing x \* y   (class template) |
| divides | function object implementing x / y   (class template) |
| modulus | function object implementing x % y   (class template) |
| negate | function object implementing -x   (class template) |
| Comparisons | |
| equal_to | function object implementing x == y   (class template) |
| not_equal_to | function object implementing x != y   (class template) |
| greater | function object implementing x > y   (class template) |
| less | function object implementing x < y   (class template) |
| greater_equal | function object implementing x >= y   (class template) |
| less_equal | function object implementing x <= y   (class template) |
| Concept-constrained comparisons | |
| ranges::equal_to(C++20) | constrained function object implementing x == y   (class) |
| ranges::not_equal_to(C++20) | constrained function object implementing x != y   (class) |
| ranges::greater(C++20) | constrained function object implementing x > y   (class) |
| ranges::less(C++20) | constrained function object implementing x < y   (class) |
| ranges::greater_equal(C++20) | constrained function object implementing x >= y   (class) |
| ranges::less_equal(C++20) | constrained function object implementing x <= y   (class) |
| compare_three_way(C++20) | constrained function object implementing x <=> y   (class) |
| Logical operations | |
| logical_and | function object implementing x && y   (class template) |
| logical_or | function object implementing x || y   (class template) |
| logical_not | function object implementing !x   (class template) |
| Bitwise operations | |
| bit_and | function object implementing x & y   (class template) |
| bit_or | function object implementing x | y   (class template) |
| bit_xor | function object implementing x ^ y   (class template) |
| bit_not(C++14) | function object implementing ~x   (class template) |
| Negators | |
| not_fn(C++17) | creates a function object that returns the complement of the result of the function object it holds   (function template) |
| Identities | |
| identity(C++20) | function object that returns its argument unchanged   (class) |
| Searchers | |
| default_searcher(C++17) | standard C++ library search algorithm implementation   (class template) |
| boyer_moore_searcher(C++17) | Boyer-Moore search algorithm implementation   (class template) |
| boyer_moore_horspool_searcher(C++17) | Boyer-Moore-Horspool search algorithm implementation   (class template) |
| Hashing | |
| hash(C++11) | hash function object   (class template) |
| std::hash<**Arithmetic**>std::hash<**Enumeration**>std::hash<std::nullptr_t>std::hash<T\*>(C++11) | std::hash specializations for fundamental, enumeration, and pointer types   (class template specialization) |
| Constants | |
| Defined in namespace `std::placeholders` | |
| _1, _2, _3, _4, ...(C++11) | placeholders for the unbound arguments in a `std::bind` expression   (constant) |
| Functions | |
| bind_frontbind_back(C++20)(C++23) | bind a variable number of arguments, in order, to a function object   (function template) |
| bind(C++11) | binds one or more arguments to a function object   (function template) |
| refcref(C++11)(C++11) | creates a std::reference_wrapper with a type deduced from its argument   (function template) |
| invokeinvoke_r(C++17)(C++23) | invokes any Callable object with given arguments and possibility to specify return type(since C++23)   (function template) |

### Deprecated in C++11 and removed in C++17

|  |  |
| --- | --- |
| Base | |
| unary_function(deprecated in C++11)(removed in C++17) | adaptor-compatible unary function base class   (class template) |
| binary_function(deprecated in C++11)(removed in C++17) | adaptor-compatible binary function base class   (class template) |
| Binders | |
| binder1stbinder2nd(deprecated in C++11)(removed in C++17) | function object holding a binary function and one of its arguments   (class template) |
| bind1stbind2nd(deprecated in C++11)(removed in C++17) | binds one argument to a binary function   (function template) |
| Function adaptors | |
| pointer_to_unary_function(deprecated in C++11)(removed in C++17) | adaptor-compatible wrapper for a pointer to unary function   (class template) |
| pointer_to_binary_function(deprecated in C++11)(removed in C++17) | adaptor-compatible wrapper for a pointer to binary function   (class template) |
| ptr_fun(deprecated in C++11)(removed in C++17) | creates an adaptor-compatible function object wrapper from a pointer to function   (function template) |
| mem_fun_tmem_fun1_tconst_mem_fun_tconst_mem_fun1_t(deprecated in C++11)(removed in C++17) | wrapper for a pointer to nullary or unary member function, callable with a pointer to object   (class template) |
| mem_fun(deprecated in C++11)(removed in C++17) | creates a wrapper from a pointer to member function, callable with a pointer to object   (function template) |
| mem_fun_ref_tmem_fun1_ref_tconst_mem_fun_ref_tconst_mem_fun1_ref_t(deprecated in C++11)(removed in C++17) | wrapper for a pointer to nullary or unary member function, callable with a reference to object   (class template) |
| mem_fun_ref(deprecated in C++11)(removed in C++17) | creates a wrapper from a pointer to member function, callable with a reference to object   (function template) |

### Deprecated in C++17 and removed in C++20

|  |  |
| --- | --- |
| Negators | |
| unary_negate(deprecated in C++17)(removed in C++20) | wrapper function object returning the complement of the unary predicate it holds   (class template) |
| binary_negate(deprecated in C++17)(removed in C++20) | wrapper function object returning the complement of the binary predicate it holds   (class template) |
| not1(deprecated in C++17)(removed in C++20) | constructs custom std::unary_negate object   (function template) |
| not2(deprecated in C++17)(removed in C++20) | constructs custom std::binary_negate object   (function template) |

### Synopsis

```
namespace std {
  // invoke
  template<class F, class... Args>
    constexpr invoke_result_t<F, Args...> invoke(F&& f, Args&&... args)
      noexcept(is_nothrow_invocable_v<F, Args...>);
  template<class R, class F, class... Args>
    constexpr R invoke_r(F&& f, Args&&... args)
      noexcept(is_nothrow_invocable_r_v<R, F, Args...>);
 
  // reference_wrapper
  template<class T> class reference_wrapper;
 
  template<class T> constexpr reference_wrapper<T> ref(T&) noexcept;
  template<class T> constexpr reference_wrapper<const T> cref(const T&) noexcept;
  template<class T> void ref(const T&&) = delete;
  template<class T> void cref(const T&&) = delete;
 
  template<class T>
    constexpr reference_wrapper<T> ref(reference_wrapper<T>) noexcept;
  template<class T>
    constexpr reference_wrapper<const T> cref(reference_wrapper<T>) noexcept;
 
  template<class T> struct unwrap_reference;
  template<class T> using unwrap_reference_t = typename unwrap_reference<T>::type;
  template<class T> struct unwrap_ref_decay;
  template<class T> using unwrap_ref_decay_t = typename unwrap_ref_decay<T>::type;
 
  // common_reference related specializations
  template<class R, class T, template<class> class RQual, template<class> class TQual>
    requires /* see below */
  struct basic_common_reference<R, T, RQual, TQual>;
 
  template<class T, class R, template<class> class TQual, template<class> class RQual>
    requires /* see below */
  struct basic_common_reference<T, R, TQual, RQual>;
 
  // arithmetic operations
  template<class T = void> struct plus;
  template<class T = void> struct minus;
  template<class T = void> struct multiplies;
  template<class T = void> struct divides;
  template<class T = void> struct modulus;
  template<class T = void> struct negate;
  template<> struct plus<void>;
  template<> struct minus<void>;
  template<> struct multiplies<void>;
  template<> struct divides<void>;
  template<> struct modulus<void>;
  template<> struct negate<void>;
 
  // comparisons
  template<class T = void> struct equal_to;
  template<class T = void> struct not_equal_to;
  template<class T = void> struct greater;
  template<class T = void> struct less;
  template<class T = void> struct greater_equal;
  template<class T = void> struct less_equal;
  template<> struct equal_to<void>;
  template<> struct not_equal_to<void>;
  template<> struct greater<void>;
  template<> struct less<void>;
  template<> struct greater_equal<void>;
  template<> struct less_equal<void>;
 
  // logical operations
  template<class T = void> struct logical_and;
  template<class T = void> struct logical_or;
  template<class T = void> struct logical_not;
  template<> struct logical_and<void>;
  template<> struct logical_or<void>;
  template<> struct logical_not<void>;
 
  // bitwise operations
  template<class T = void> struct bit_and;
  template<class T = void> struct bit_or;
  template<class T = void> struct bit_xor;
  template<class T = void> struct bit_not;
  template<> struct bit_and<void>;
  template<> struct bit_or<void>;
  template<> struct bit_xor<void>;
  template<> struct bit_not<void>;
 
  // identity
  struct identity;
 
  // function template not_fn
  template<class F> constexpr /* unspecified */ not_fn(F&& f);
 
  // function templates bind_front and bind_back
  template<class F, class... Args> constexpr /* unspecified */ bind_front(F&&, Args&&...);
  template<class F, class... Args> constexpr /* unspecified */ bind_back(F&&, Args&&...);
 
  // bind
  template<class T> struct is_bind_expression;
  template<class T>
    inline constexpr bool is_bind_expression_v = is_bind_expression<T>::value;
 
  template<class T> struct is_placeholder;
  template<class T>
    inline constexpr int is_placeholder_v = is_placeholder<T>::value;
 
  template<class F, class... BoundArgs>
    constexpr /* unspecified */ bind(F&&, BoundArgs&&...);
  template<class R, class F, class... BoundArgs>
    constexpr /* unspecified */ bind(F&&, BoundArgs&&...);
 
  namespace placeholders {
    // M is the implementation-defined number of placeholders
    /* see description */ _1;
    /* see description */ _2;
               .
               .
               .
    /* see description */ _M;
  }
 
  // member function adaptors
  template<class R, class T>
    constexpr /* unspecified */ mem_fn(R T::*) noexcept;
 
  // polymorphic function wrappers
  class bad_function_call;
 
  template<class> class function; // not defined
  template<class R, class... ArgTypes> class function<R(ArgTypes...)>;
 
  template<class R, class... ArgTypes>
    void swap(function<R(ArgTypes...)>&, function<R(ArgTypes...)>&) noexcept;
 
  template<class R, class... ArgTypes>
    bool operator==(const function<R(ArgTypes...)>&, nullptr_t) noexcept;
 
  // move-only wrapper
  template<class...> class move_only_function; // not defined
 
  template<class R, class... ArgTypes>
    class move_only_function<R(ArgTypes...) /*cv ref*/ noexcept(/*noex*/)>;
 
  // copyable wrapper
  template<class...> class copyable_function; // not defined
 
  template<class R, class... ArgTypes>
    class copyable_function<R(ArgTypes...) /*cv ref*/ noexcept(/*noex*/)>;
 
  // non-owning wrapper
  template<class...> class function_ref; // not defined
 
  template<class R, class... ArgTypes>
    class function_ref<R(ArgTypes...) /*cv*/ noexcept(/*noex*/)>;
 
  // searchers
  template<class ForwardIter, class BinaryPredicate = equal_to<>>
    class default_searcher;
 
  template<class RandomAccessIter,
           class Hash = hash<typename iterator_traits<RandomAccessIter>::value_type>,
           class BinaryPredicate = equal_to<>>
    class boyer_moore_searcher;
 
  template<class RandomAccessIter,
           class Hash = hash<typename iterator_traits<RandomAccessIter>::value_type>,
           class BinaryPredicate = equal_to<>>
    class boyer_moore_horspool_searcher;
 
  // hash function primary template
  template<class T>
    struct hash;
 
  // concept-constrained comparisons
  struct compare_three_way;
  namespace ranges {
    struct equal_to;
    struct not_equal_to;
    struct greater;
    struct less;
    struct greater_equal;
    struct less_equal;
  }
 
  // exposition only
  template<class Fn, class... Args>
    concept /*callable*/ =
      requires (Fn&& fn, Args&&... args) {
        std::forward<Fn>(fn)(std::forward<Args>(args)...);
      };
 
  // exposition only
  template<class Fn, class... Args>
    concept /*nothrow-callable*/ =
      /*callable*/<Fn, Args...> &&
      requires (Fn&& fn, Args&&... args) {
        { std::forward<Fn>(fn)(std::forward<Args>(args)...) } noexcept;
      };
 
  // exposition only
  template<class Fn, class... Args>
    using /*call-result-t*/ = decltype(std::declval<Fn>()(std::declval<Args>()...));
 
  // exposition only
  template<const auto& T>
    using /*decayed-typeof*/ = decltype(auto(T));
}

```

#### Class template std::reference_wrapper

```
namespace std {
  template<class T> class reference_wrapper {
  public:
    // types
    using type = T;
 
    // construct/copy/destroy
    template<class U>
      constexpr reference_wrapper(U&&) noexcept(/* see below */);
    constexpr reference_wrapper(const reference_wrapper& x) noexcept;
 
    // assignment
    constexpr reference_wrapper& operator=(const reference_wrapper& x) noexcept;
 
    // access
    constexpr operator T& () const noexcept;
    constexpr T& get() const noexcept;
 
    // invocation
    template<class... ArgTypes>
      constexpr invoke_result_t<T&, ArgTypes...> operator()(ArgTypes&&...) const
        noexcept(is_nothrow_invocable_v<T&, ArgTypes...>);
 
    // comparison
    friend constexpr bool operator==(reference_wrapper, reference_wrapper);
    friend constexpr bool operator==(reference_wrapper, const T&);
    friend constexpr bool operator==(reference_wrapper, reference_wrapper<const T>);
 
    friend constexpr auto operator<=>(reference_wrapper, reference_wrapper);
    friend constexpr auto operator<=>(reference_wrapper, const T&);
    friend constexpr auto operator<=>(reference_wrapper, reference_wrapper<const T>);
  };
  // deduction guides
  template<class T>
    reference_wrapper(T&) -> reference_wrapper<T>;
}

```

#### Class template std::unwrap_reference

```
namespace std {
  template<class T>
    struct unwrap_reference;
}

```

#### Class template std::unwrap_ref_decay

```
namespace std {
  template<class T>
    struct unwrap_ref_decay;
}

```

#### Class template std::plus

```
namespace std {
  template<class T = void> struct plus {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct plus<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) + std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::minus

```
namespace std {
  template<class T = void> struct minus {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct minus<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) - std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::multiplies

```
namespace std {
  template<class T = void> struct multiplies {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct multiplies<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) * std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::divides

```
namespace std {
  template<class T = void> struct divides {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct divides<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) / std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::modulus

```
namespace std {
  template<class T = void> struct modulus {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct modulus<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) % std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::negate

```
namespace std {
  template<class T = void> struct negate {
    constexpr T operator()(const T& x) const;
  };
 
  template<> struct negate<void> {
    template<class T> constexpr auto operator()(T&& t) const
      -> decltype(-std::forward<T>(t));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::equal_to

```
namespace std {
  template<class T = void> struct equal_to {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct equal_to<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) == std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::not_equal_to

```
namespace std {
  template<class T = void> struct not_equal_to {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct not_equal_to<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) != std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::greater

```
namespace std {
  template<class T = void> struct greater {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct greater<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) > std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::less

```
namespace std {
  template<class T = void> struct less {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct less<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) < std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::greater_equal

```
namespace std {
  template<class T = void> struct greater_equal {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct greater_equal<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) >= std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::less_equal

```
namespace std {
  template<class T = void> struct less_equal {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct less_equal<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) <= std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class std::compare_three_way

```
namespace std {
  struct compare_three_way {
    template<class T, class U>
    constexpr auto operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class std::ranges::equal_to

```
namespace std::ranges {
  struct equal_to {
    template<class T, class U>
    constexpr bool operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class std::ranges::not_equal_to

```
namespace std::ranges {
  struct not_equal_to {
    template<class T, class U>
    constexpr bool operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class std::ranges::greater

```
namespace std::ranges {
  struct greater {
    template<class T, class U>
    constexpr bool operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class std::ranges::less

```
namespace std::ranges {
  struct less {
    template<class T, class U>
    constexpr bool operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class std::ranges::greater_equal

```
namespace std::ranges {
  struct greater_equal {
    template<class T, class U>
    constexpr bool operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class std::ranges::less_equal

```
namespace std::ranges {
  struct less_equal {
    template<class T, class U>
    constexpr bool operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::logical_and

```
namespace std {
  template<class T = void> struct logical_and {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct logical_and<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) && std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::logical_or

```
namespace std {
  template<class T = void> struct logical_or {
    constexpr bool operator()(const T& x, const T& y) const;
  };
 
  template<> struct logical_or<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) || std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::logical_not

```
namespace std {
  template<class T = void> struct logical_not {
    constexpr bool operator()(const T& x) const;
  };
 
  template<> struct logical_not<void> {
    template<class T> constexpr auto operator()(T&& t) const
      -> decltype(!std::forward<T>(t));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::bit_and

```
namespace std {
  template<class T = void> struct bit_and {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct bit_and<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) & std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::bit_or

```
namespace std {
  template<class T = void> struct bit_or {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct bit_or<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) | std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::bit_xor

```
namespace std {
  template<class T = void> struct bit_xor {
    constexpr T operator()(const T& x, const T& y) const;
  };
 
  template<> struct bit_xor<void> {
    template<class T, class U> constexpr auto operator()(T&& t, U&& u) const
      -> decltype(std::forward<T>(t) ^ std::forward<U>(u));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::bit_not

```
namespace std {
  template<class T = void> struct bit_not {
    constexpr T operator()(const T& x) const;
  };
 
  template<> struct bit_not<void> {
    template<class T> constexpr auto operator()(T&& t) const
      -> decltype(~std::forward<T>(t));
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::identity

```
namespace std {
  struct identity {
    template<class T>
      constexpr T&& operator()(T&& t) const noexcept;
 
    using is_transparent = /* unspecified */;
  };
}

```

#### Class template std::is_bind_expression

```
namespace std {
  template<class T> struct is_bind_expression;
}

```

#### Class template std::is_placeholder

```
namespace std {
  template<class T> struct is_placeholder;
}

```

#### Class std::bad_function_call

```
namespace std {
  class bad_function_call : public exception {
  public:
    // see [exception] for the specification of the special member functions
    const char* what() const noexcept override;
  };
}

```

#### Class template std::function

```
namespace std {
  template<class> class function; // not defined
 
  template<class R, class... ArgTypes>
  class function<R(ArgTypes...)> {
  public:
    using result_type = R;
 
    // construct/copy/destroy
    function() noexcept;
    function(nullptr_t) noexcept;
    function(const function&);
    function(function&&) noexcept;
    template<class F> function(F);
 
    function& operator=(const function&);
    function& operator=(function&&);
    function& operator=(nullptr_t) noexcept;
    template<class F> function& operator=(F&&);
    template<class F> function& operator=(reference_wrapper<F>) noexcept;
 
    ~function();
 
    // function modifiers
    void swap(function&) noexcept;
 
    // function capacity
    explicit operator bool() const noexcept;
 
    // function invocation
    R operator()(ArgTypes...) const;
 
    // function target access
    const type_info& target_type() const noexcept;
    template<class T>       T* target() noexcept;
    template<class T> const T* target() const noexcept;
  };
 
  template<class R, class... ArgTypes>
    function(R(*)(ArgTypes...)) -> function<R(ArgTypes...)>;
 
  template<class F> function(F) -> function</* see description */>;
 
  // null pointer comparison functions
  template<class R, class... ArgTypes>
    bool operator==(const function<R(ArgTypes...)>&, nullptr_t) noexcept;
 
  // specialized algorithms
  template<class R, class... ArgTypes>
    void swap(function<R(ArgTypes...)>&, function<R(ArgTypes...)>&) noexcept;
}

```

#### Class template std::move_only_function

```
namespace std {
  template<class... S> class move_only_function; // not defined
 
  template<class R, class... ArgTypes>
  class move_only_function<R(ArgTypes...) /*cv-ref*/ noexcept(/*noex*/)> {
  public:
    using result_type = R;
 
    // construct/move/destroy
    move_only_function() noexcept;
    move_only_function(nullptr_t) noexcept;
    move_only_function(move_only_function&&) noexcept;
    template<class F> move_only_function(F&&);
 
    template<class T, class... Args>
      explicit move_only_function(in_place_type_t<T>, Args&&...);
    template<class T, class U, class... Args>
      explicit move_only_function(in_place_type_t<T>, initializer_list<U>, Args&&...);
 
    move_only_function& operator=(move_only_function&&);
    move_only_function& operator=(nullptr_t) noexcept;
    template<class F> move_only_function& operator=(F&&);
 
    ~move_only_function();
 
    // invocation
    explicit operator bool() const noexcept;
 
    R operator()(ArgTypes...) /*cv-ref*/ noexcept(/*noex*/);
 
    // utility
    void swap(move_only_function&) noexcept;
 
    friend void swap(move_only_function&, move_only_function&) noexcept;
 
    friend bool operator==(const move_only_function&, nullptr_t) noexcept;
 
  private:
    // exposition-only
    template<class VT>
      static constexpr bool /*is-callable-from*/ = /* see description */; 
  };
}

```

#### Class template std::copyable_function

```
namespace std {
  template<class... S> class copyable_function; // not defined
 
  template<class R, class... ArgTypes>
  class copyable_function<R(ArgTypes...) /*cv-ref*/ noexcept(/*noex*/)> {
  public:
    using result_type = R;
 
    // construct/move/destroy
    copyable_function() noexcept;
    copyable_function(nullptr_t) noexcept;
    copyable_function(const copyable_function&);
    copyable_function(copyable_function&&) noexcept;
    template<class F> copyable_function(F&&);
 
    template<class T, class... Args>
      explicit copyable_function(in_place_type_t<T>, Args&&...);
    template<class T, class U, class... Args>
      explicit copyable_function(in_place_type_t<T>, initializer_list<U>, Args&&...);
 
    copyable_function& operator=(const copyable_function&);
    copyable_function& operator=(copyable_function&&);
    copyable_function& operator=(nullptr_t) noexcept;
    template<class F> copyable_function& operator=(F&&);
 
    ~copyable_function();
 
    // invocation
    explicit operator bool() const noexcept;
 
    R operator()(ArgTypes...) /*cv-ref*/ noexcept(/*noex*/);
 
    // utility
    void swap(copyable_function&) noexcept;
 
    friend void swap(copyable_function&, copyable_function&) noexcept;
 
    friend bool operator==(const copyable_function&, nullptr_t) noexcept;
 
  private:
    // exposition-only
    template<class VT>
      static constexpr bool /*is-callable-from*/ = /* see description */; 
  };
}

```

#### Class template std::function_ref

```
namespace std {
  template<class... S> class function_ref; // not defined
 
  template<class R, class... ArgTypes>
  class function_ref<R(ArgTypes...) /*cv*/ noexcept(/*noex*/)> {
  public:
    // constructors and assignment operators
    template<class F> function_ref(F*) noexcept;
    template<class F> constexpr function_ref(F&&) noexcept;
    template<auto f> constexpr function_ref(nontype_t<f>) noexcept;
    template<auto f, class U>
      constexpr function_ref(nontype_t<f>, U&&) noexcept;
    template<auto f, class T>
      constexpr function_ref(nontype_t<f>, /*cv*/ T*) noexcept;
 
    constexpr function_ref(const function_ref&) noexcept = default;
    constexpr function_ref& operator=(const function_ref&) noexcept = default;
    template<class T> function_ref& operator=(T) = delete;
 
    // invocation
    R operator()(ArgTypes...) /*cv*/ noexcept(/*noex*/);
 
  private:
    // exposition-only
    template<class... T>
      static constexpr bool /*is-invocable-using*/ = /* see description */;
 
    R (*thunk-ptr)(BoundEntityType, ArgTypes&&...) noexcept(/*noex*/); // exposition-only
    BoundEntityType bound-entity; // exposition-only
  };
  // deduction guides
  template<class F>
    function_ref(F*) -> function_ref<F>;
  template<auto f>
    function_ref(nontype_t<f>) -> function_ref</* see description */>;
  template<auto f, class T>
    function_ref(nontype_t<f>, T&&) -> function_ref</* see description */>;
}

```

#### Class template std::default_searcher

```
namespace std {
  template<class ForwardIter1, class BinaryPredicate = equal_to<>>
    class default_searcher {
    public:
      constexpr default_searcher(ForwardIter1 pat_first, ForwardIter1 pat_last,
                                 BinaryPredicate pred = BinaryPredicate());
 
      template<class ForwardIter2>
        constexpr pair<ForwardIter2, ForwardIter2>
          operator()(ForwardIter2 first, ForwardIter2 last) const;
 
    private:
      ForwardIter1 pat_first_;            // exposition only
      ForwardIter1 pat_last_;             // exposition only
      BinaryPredicate pred_;              // exposition only
  };
}

```

#### Class template std::boyer_moore_searcher

```
namespace std {
  template<class RandomAccessIter1,
           class Hash = hash<typename iterator_traits<RandomAccessIter1>::value_type>,
           class BinaryPredicate = equal_to<>>
    class boyer_moore_searcher {
    public:
      boyer_moore_searcher(RandomAccessIter1 pat_first,
                           RandomAccessIter1 pat_last,
                           Hash hf = Hash(),
                           BinaryPredicate pred = BinaryPredicate());
 
      template<class RandomAccessIter2>
        pair<RandomAccessIter2, RandomAccessIter2>
          operator()(RandomAccessIter2 first, RandomAccessIter2 last) const;
 
    private:
      RandomAccessIter1 pat_first_;       // exposition only
      RandomAccessIter1 pat_last_;        // exposition only
      Hash hash_;                         // exposition only
      BinaryPredicate pred_;              // exposition only
    };
}

```

#### Class template std::boyer_moore_horspool_searcher

```
namespace std {
  template<class RandomAccessIter1,
           class Hash = hash<typename iterator_traits<RandomAccessIter1>::value_type>,
           class BinaryPredicate = equal_to<>>
    class boyer_moore_horspool_searcher {
    public:
      boyer_moore_horspool_searcher(RandomAccessIter1 pat_first,
                                    RandomAccessIter1 pat_last,
                                    Hash hf = Hash(),
                                    BinaryPredicate pred = BinaryPredicate());
 
      template<class RandomAccessIter2>
        pair<RandomAccessIter2, RandomAccessIter2>
          operator()(RandomAccessIter2 first, RandomAccessIter2 last) const;
 
    private:
      RandomAccessIter1 pat_first_;       // exposition only
      RandomAccessIter1 pat_last_;        // exposition only
      Hash hash_;                         // exposition only
      BinaryPredicate pred_;              // exposition only
  };
}

```

### See also

|  |  |
| --- | --- |
| std::hash specializations for library types | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/functional&oldid=173900>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 July 2024, at 07:29.