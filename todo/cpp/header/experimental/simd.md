# Experimental library header <experimental/simd>

From cppreference.com
< cpp‎ | header‎ | experimental
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

Experimental library headers

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Execution P2300 | | | | |
| <experimental/execution> | | | | |
| Filesystem TS | | | | |
| <experimental/filesystem> | | | | |
| Parallelism TS (v1, v2) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/algorithm` | | | | | | `experimental/execution_policy` | | | | | | `experimental/exception_list` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/numeric` | | | | | | ****<experimental/simd>**** | | | | | | `experimental/task_block` | | | | | |
| Library Fundamentals TS (v1, v2, v3) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/algorithm` | | | | | | <experimental/any> | | | | | | `experimental/array` | | | | | | `experimental/chrono` | | | | | | `experimental/deque` | | | | | | `experimental/forward_list` | | | | | | <experimental/functional> | | | | | | `experimental/future` | | | | | | `experimental/iterator` | | | | | | `experimental/list` | | | | | | `experimental/map` | | | | | | `experimental/memory` | | | | | | <experimental/memory_resource> | | | | | | `experimental/numeric` | | | | | | <experimental/optional> | | | | | | `experimental/propagate_const` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/random` | | | | | | `experimental/ratio` | | | | | | `experimental/regex` | | | | | | `experimental/scope` | | | | | | `experimental/set` | | | | | | `experimental/source_location` | | | | | | `experimental/string` | | | | | | <experimental/string_view> | | | | | | `experimental/system_error` | | | | | | `experimental/tuple` | | | | | | `experimental/type_traits` | | | | | | `experimental/unordered_map` | | | | | | `experimental/unordered_set` | | | | | | `experimental/utility` | | | | | | `experimental/vector` | | | | | |  | | | | | |
| Concurrency TS | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/atomic` | | | | | | `experimental/barrier` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/future` | | | | | | `experimental/latch` | | | | | |
| Ranges TS | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | <experimental/ranges/algorithm> | | | | | | <experimental/ranges/concepts> | | | | | | <experimental/ranges/functional> | | | | | | <experimental/ranges/iterator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | <experimental/ranges/random> | | | | | | <experimental/ranges/tuple> | | | | | | <experimental/ranges/type_traits> | | | | | | <experimental/ranges/utility> | | | | | |
| Coroutines TS | | | | |
| `experimental/coroutine` | | | | |
| Networking TS | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/buffer` | | | | | | `experimental/executor` | | | | | | `experimental/internet` | | | | | | `experimental/io_context` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | <experimental/net> | | | | | | `experimental/netfwd` | | | | | | `experimental/socket` | | | | | | `experimental/timer` | | | | | |
| Reflection TS | | | | |
| <experimental/reflect> | | | | |

The header defines class templates, tag types, trait types, and function templates for
element-wise operations on data-parallel objects.

### Synopsis

```
namespace std::experimental {
inline namespace parallelism_v2 {
namespace simd_abi {
using scalar = /* see below */;
template <int N> using fixed_size = /* see below */;
template <class T>
constexpr int max_fixed_size = /* implementation-defined */;
template <class T> using compatible = /* implementation-defined */;
template <class T> using native = /* implementation-defined */;
template <class T, size_t N, class... Abis> struct deduce {
  using type = /* see below */;
};
template <class T, size_t N, class... Abis>
using deduce_t = typename deduce<T, N, Abis...>::type;
} // namespace simd_abi
struct element_aligned_tag {};
struct vector_aligned_tag {};
template <size_t> struct overaligned_tag {};
inline constexpr element_aligned_tag element_aligned{};
inline constexpr vector_aligned_tag vector_aligned{};
template <size_t N> constexpr overaligned_tag<N> overaligned{};
// 9.4, simd type traits
template <class T> struct is_abi_tag;
template <class T> constexpr bool is_abi_tag_v = is_abi_tag<T>::value;
template <class T> struct is_simd;
template <class T> constexpr bool is_simd_v = is_simd<T>::value;
template <class T> struct is_simd_mask;
template <class T>
constexpr bool is_simd_mask_v = is_simd_mask<T>::value;
template <class T> struct is_simd_flag_type;
template <class T>
constexpr bool is_simd_flag_type_v = is_simd_flag_type<T>::value;
template <class T, class Abi = simd_abi::compatible<T>> struct simd_size;
template <class T, class Abi = simd_abi::compatible<T>>
constexpr size_t simd_size_v = simd_size<T, Abi>::value;
template <class T, class U = typename T::value_type> struct memory_alignment;
template <class T, class U = typename T::value_type>
constexpr size_t memory_alignment_v = memory_alignment<T, U>::value;
template <class T, class V> struct rebind_simd { using type = /* see below */; };
template <class T, class V>
using rebind_simd_t = typename rebind_simd<T, V>::type;
template <int N, class V> struct resize_simd { using type = /* see below */; };
template <int N, class V>
using resize_simd_t = typename resize_simd<N, V>::type;
// 9.6, Class template simd
template <class T, class Abi = simd_abi::compatible<T>> class simd;
template <class T> using native_simd = simd<T, simd_abi::native<T>>;
template <class T, int N>
using fixed_size_simd = simd<T, simd_abi::fixed_size<N>>;
// 9.8, Class template simd_mask
template <class T, class Abi = simd_abi::compatible<T>> class simd_mask;
template <class T> using native_simd_mask = simd_mask<T, simd_abi::native<T>>;
template <class T, int N>
using fixed_size_simd_mask = simd_mask<T, simd_abi::fixed_size<N>>;
// 9.7.5, Casts
template <class T, class U, class Abi>
/* see below */ simd_cast(const simd<U, Abi> &) noexcept;
template <class T, class U, class Abi>
/* see below */ static_simd_cast(const simd<U, Abi> &) noexcept;
template <class T, class Abi>
fixed_size_simd<T, simd_size_v<T, Abi>>
to_fixed_size(const simd<T, Abi> &) noexcept;
template <class T, class Abi>
fixed_size_simd_mask<T, simd_size_v<T, Abi>>
to_fixed_size(const simd_mask<T, Abi> &) noexcept;
template <class T, int N>
native_simd<T> to_native(const fixed_size_simd<T, N> &) noexcept;
template <class T, int N>
native_simd_mask<T> to_native(const fixed_size_simd_mask<T, N> &) noexcept;
template <class T, int N>
simd<T> to_compatible(const fixed_size_simd<T, N> &) noexcept;
template <class T, int N>
simd_mask<T> to_compatible(const fixed_size_simd_mask<T, N> &) noexcept;
template <size_t... Sizes, class T, class Abi>
tuple<simd<T, simd_abi::deduce_t<T, Sizes>>...>
split(const simd<T, Abi> &) noexcept;
template <size_t... Sizes, class T, class Abi>
tuple<simd_mask<T, simd_mask_abi::deduce_t<T, Sizes>>...>
split(const simd_mask<T, Abi> &) noexcept;
template <class V, class Abi>
array<V, simd_size_v<typename V::value_type, Abi> / V::size()>
split(const simd<typename V::value_type, Abi> &) noexcept;
template <class V, class Abi>
array<V, simd_size_v<typename V::simd_type::value_type, Abi> / V::size()>
split(const simd_mask<typename V::simd_type::value_type, Abi> &) noexcept;
template <size_t N, class T, class A>
array<resize_simd<simd_size_v<T, A> / N, simd<T, A>>, N>
split_by(const simd<T, A> &x) noexcept;
template <size_t N, class T, class A>
array<resize_simd<simd_size_v<T, A> / N, simd_mask<T, A>>, N>
split_by(const simd_mask<T, A> &x) noexcept;
template <class T, class... Abis>
simd<T, simd_abi::deduce_t<T, (simd_size_v<T, Abis> + ...)>>
concat(const simd<T, Abis> &...) noexcept;
template <class T, class... Abis>
simd_mask<T, simd_abi::deduce_t<T, (simd_size_v<T, Abis> + ...)>>
concat(const simd_mask<T, Abis> &...) noexcept;
template <class T, class Abi, size_t N>
resize_simd<simd_size_v<T, Abi> * N, simd<T, Abi>>
concat(const array<simd<T, Abi>, N> &arr) noexcept;
template <class T, class Abi, size_t N>
resize_simd<simd_size_v<T, Abi> * N, simd_mask<T, Abi>>
concat(const array<simd_mask<T, Abi>, N> &arr) noexcept;
// 9.9.4, Reductions
template <class T, class Abi> bool all_of(const simd_mask<T, Abi> &) noexcept;
template <class T, class Abi> bool any_of(const simd_mask<T, Abi> &) noexcept;
template <class T, class Abi> bool none_of(const simd_mask<T, Abi> &) noexcept;
template <class T, class Abi> bool some_of(const simd_mask<T, Abi> &) noexcept;
template <class T, class Abi> int popcount(const simd_mask<T, Abi> &) noexcept;
template <class T, class Abi> int find_first_set(const simd_mask<T, Abi> &);
template <class T, class Abi> int find_last_set(const simd_mask<T, Abi> &);
bool all_of(T) noexcept;
bool any_of(T) noexcept;
bool none_of(T) noexcept;
bool some_of(T) noexcept;
int popcount(T) noexcept;
int find_first_set(T);
int find_last_set(T);
// 9.5, Where expression class templates
template <class M, class T> class const_where_expression;
template <class M, class T> class where_expression;
// 9.9.5, Where functions
template <class T, class Abi>
where_expression<simd_mask<T, Abi>, simd<T, Abi>>
where(const typename simd<T, Abi>::mask_type &, simd<T, Abi> &) noexcept;
template <class T, class Abi>
const_where_expression<simd_mask<T, Abi>, simd<T, Abi>>
where(const typename simd<T, Abi>::mask_type &, const simd<T, Abi> &) noexcept;
template <class T, class Abi>
where_expression<simd_mask<T, Abi>, simd_mask<T, Abi>>
where(const type_identity_t<simd_mask<T, Abit>> &,
      simd_mask<T, Abi> &) noexcept;
template <class T, class Abi>
const_where_expression<simd_mask<T, Abi>, simd_mask<T, Abi>>
where(const type_identity_t<simd_mask<T, Abit>> &,
      const simd_mask<T, Abi> &) noexcept;
template <class T> where_expression<bool, T> where(/* see below */ k, T &d) noexcept;
template <class T>
const_where_expression<bool, T> where(/* see below */ k, const T &d) noexcept;
// 9.7.4, Reductions
template <class T, class Abi, class BinaryOperation = plus<>>
T reduce(const simd<T, Abi> &, BinaryOperation = {});
template <class M, class V, class BinaryOperation>
typename V::value_type reduce(const const_where_expression<M, V> &x,
                              typename V::value_type identity_element,
                              BinaryOperation binary_op);
template <class M, class V>
typename V::value_type reduce(const const_where_expression<M, V> &x,
                              plus<> binary_op = {}) noexcept;
template <class M, class V>
typename V::value_type reduce(const const_where_expression<M, V> &x,
                              multiplies<> binary_op) noexcept;
template <class M, class V>
typename V::value_type reduce(const const_where_expression<M, V> &x,
                              bit_and<> binary_op) noexcept;
template <class M, class V>
typename V::value_type reduce(const const_where_expression<M, V> &x,
                              bit_or<> binary_op) noexcept;
template <class M, class V>
typename V::value_type reduce(const const_where_expression<M, V> &x,
                              bit_xor<> binary_op) noexcept;
template <class T, class Abi> T hmin(const simd<T, abi> &) noexcept;
template <class M, class V>
typename V::value_type hmin(const const_where_expression<M, V> &) noexcept;
template <class T, class Abi> T hmax(const simd<T, abi> &) noexcept;
template <class M, class V>
typename V::value_type hmax(const const_where_expression<M, V> &) noexcept;
// 9.7.6, Algorithms
template <class T, class Abi>
simd<T, Abi> min(const simd<T, Abi> &a, const simd<T, Abi> &b) noexcept;
template <class T, class Abi>
simd<T, Abi> max(const simd<T, Abi> &a, const simd<T, Abi> &b) noexcept;
template <class T, class Abi>
pair<simd<T, Abi>, simd<T, Abi>> minmax(const simd<T, Abi> &a,
                                        const simd<T, Abi> &b) noexcept;
template <class T, class Abi>
simd<T, Abi> clamp(const simd<T, Abi> &v, const simd<T, Abi> &lo,
                   const simd<T, Abi> &hi);
} // namespace parallelism_v2
} // namespace std::experimental

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/experimental/simd&oldid=176429>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 September 2024, at 06:13.