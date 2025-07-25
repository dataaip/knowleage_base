# Standard library header <simd> (C++26)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | ****<simd>**** (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the numeric library.

|  |  |
| --- | --- |
| Classes | |
| basic_simd(C++26) | data-parallel vector type   (class template) |
| simd(C++26) | convenience alias template for `basic_simd` that can specify its width (alias template) |
| basic_simd_mask")(C++26) | data-parallel type with the element type bool   (class template) |
| simd_mask")(C++26) | convenience alias template for `basic_simd_mask` that can specify its width (alias template) |
| simd_flags")(C++26) | load and store flags for data-parallel types   (class template) |
| simd_alignment")(C++26) | obtains an appropriate alignment for `simd_flag_aligned`   (class template) |
| rebind_simd")(C++26) | changes element type of the data-parallel type   (class template) |
| resize_simd")(C++26) | changes the width of the data-parallel type   (class template) |
| Functions | |
| simd_unchecked_loadsimd_partial_load")(C++26) | loads elements from a contiguous range to `basic_simd`   (function template) |
| simd_unchecked_storesimd_partial_store")(C++26) | stores elements from `basic_simd` to a contiguous range   (function template) |
| simd_split")(C++26) | splits single data-parallel object to multiple ones   (function template) |
| simd_cat")(C++26) | concatenates multiple data-parallel objects into a single one   (function template) |
| all_ofany_ofnone_of")(C++26) | reductions of `basic_simd_mask` to bool   (function template) |
| reduce_count")(C++26) | reduction of `basic_simd_mask` to number of true values   (function template) |
| reduce_min_indexreduce_max_index")(C++26) | reductions of `basic_simd_mask` to the index of first or last true value   (function template) |
| reducereduce_minreduce_max")(C++26) | reduces all values in `basic_simd` over a specified binary operation to a single value   (function template) |
| minmaxminmax")(C++26) | element-wise min/max operations for `basic_simd`   (function template) |
| clamp")(C++26) | element-wise clamp operation for `basic_simd`   (function template) |
| simd_select")(C++26) | element-wise selection using conditional operator   (function template) |
| Constants | |
| simd_flag_default")(C++26) | default flag used on load and store operations   (constant) |
| simd_flag_convert")(C++26) | flag enabling conversions that are not value-preserving on load and store operations   (constant) |
| simd_flag_aligned")(C++26) | flag indicating alignment of the load-store address to some specified storage to the value of `simd_alignment`   (constant) |
| simd_flag_overaligned")(C++26) | flag indicating alignment of the load-store address to some specified storage to the specified alignment (variable template) |

### Synopsis

```
namespace std {
  // SIMD type traits
  template<class T, class U = typename T::value_type>
    struct simd_alignment;
  template<class T, class U = typename T::value_type>
    constexpr size_t simd_alignment_v = simd_alignment<T, U>::value;
 
  template<class T, class V>
    struct rebind_simd { using type = /* see description */; };
  template<class T, class V>
    using rebind_simd_t = typename rebind_simd<T, V>::type;
  template</*simd-size-type*/ N, class V>
    struct resize_simd { using type = /* see description */; };
  template</*simd-size-type*/ N, class V>
    using resize_simd_t = typename resize_simd<N, V>::type;
 
  // load and store flags
  template<class... Flags>
    struct simd_flags;
  inline constexpr simd_flags<> simd_flag_default{};
  inline constexpr simd_flags</*convert-flag*/> simd_flag_convert{};
  inline constexpr simd_flags</*aligned-flag*/> simd_flag_aligned{};
  template<size_t N>
      requires (has_single_bit(N))
    constexpr simd_flags</*overaligned-flag*/<N>> simd_flag_overaligned{};
 
  // class template basic_simd
  template<class T, class Abi = /*native-abi*/<T>>
    class basic_simd;
  template<class T, /*simd-size-type*/ N = /*simd-size-v*/<T, /*native-abi*/<T>>>
    using simd = basic_simd<T, /*deduce-abi-t*/<T, N>>;
 
  // class template basic_simd_mask
  template<size_t Bytes, class Abi = /*native-abi*/</*integer-from*/<Bytes>>>
    class basic_simd_mask;
  template<class T, /*simd-size-type*/ N = /*simd-size-v*/<T, /*native-abi*/<T>>>
    using simd_mask = basic_simd_mask<sizeof(T), /*deduce-abi-t*/<T, N>>;
 
  // basic_simd load and store functions
  template<class V = /* see below */, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R>
    constexpr V simd_unchecked_load(R&& r, simd_flags<Flags...> f = {});
  template<class V = /* see below */, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R>
    constexpr V simd_unchecked_load(R&& r, const typename V::mask_type& k,
                                    simd_flags<Flags...> f = {});
 
  template<class V = /* see below */, contiguous_iterator I, class... Flags>
    constexpr V simd_unchecked_load(I first, iter_difference_t<I> n, 
                                    simd_flags<Flags...> f = {});
  template<class V = /* see below */, contiguous_iterator I, class... Flags>
    constexpr V simd_unchecked_load(I first, iter_difference_t<I> n,
                                    const typename V::mask_type& k
                                    simd_flags<Flags...> f = {});
 
  template<class V = /* see below */, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
    constexpr V simd_unchecked_load(I first, S last, simd_flags<Flags...> f = {});
  template<class V = /* see below */, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
    constexpr V simd_unchecked_load(I first, S last, 
                                    const typename V::mask_type& k,
                                    simd_flags<Flags...> f = {});
 
  template<class V = /* see below */, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R>
    constexpr V simd_partial_load(R&& r, simd_flags<Flags...> f = {});
  template<class V = /* see below */, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R>
    constexpr V simd_partial_load(R&& r, const typename V::mask_type& k,
                                  simd_flags<Flags...> f = {});
 
  template<class V = /* see below */, contiguous_iterator I, class... Flags>
    constexpr V simd_partial_load(I first, iter_difference_t<I> n, 
                                  simd_flags<Flags...> f = {});
  template<class V = /* see below */, contiguous_iterator I, class... Flags>
    constexpr V simd_partial_load(I first, iter_difference_t<I> n,
                                  const typename V::mask_type& k
                                  simd_flags<Flags...> f = {});
 
  template<class V = /* see below */, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
    constexpr V simd_partial_load(I first, S last, simd_flags<Flags...> f = {});
  template<class V = /* see below */, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
    constexpr V simd_partial_load(I first, S last, 
                                  const typename V::mask_type& k,
                                  simd_flags<Flags...> f = {});
 
  template<class T, class Abi, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R> && indirectly_writable<ranges::iterator_t<R>, T>
    constexpr void simd_unchecked_store(const basic_simd<T, Abi>& v, R&& r, 
                                        simd_flags<Flags...> f = {});
  template<class T, class Abi, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R> && indirectly_writable<ranges::iterator_t<R>, T>
    constexpr void simd_unchecked_store(const basic_simd<T, Abi>& v, R&& r, 
                                        const typename basic_simd<T, Abi>::mask_type& k,
                                        simd_flags<Flags...> f = {});
 
  template<class T, class Abi, contiguous_iterator I, class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_unchecked_store(const basic_simd<T, Abi>& v,
                                        I first, iter_difference_t<I> n,
                                        simd_flags<Flags...> f = {});
  template<class T, class Abi, contiguous_iterator I, class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_unchecked_store(const basic_simd<T, Abi>& v,
                                        I first, iter_difference_t<I> n,
                                        const typename basic_simd<T, Abi>::mask_type& k,
                                        simd_flags<Flags...> f = {});
 
  template<class T, class Abi, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_unchecked_store(const basic_simd<T, Abi>& v,
                                        I first, S last,
                                        simd_flags<Flags...> f = {});
  template<class T, class Abi, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_unchecked_store(const basic_simd<T, Abi>& v,
                                        I first, S last,
                                        const typename basic_simd<T, Abi>::mask_type& k,
                                        simd_flags<Flags...> f = {});
 
  template<class T, class Abi, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R> && indirectly_writable<ranges::iterator_t<R>, T>
    constexpr void simd_partial_store(const basic_simd<T, Abi>& v, R&& r, 
                                      simd_flags<Flags...> f = {});
  template<class T, class Abi, ranges::contiguous_range R, class... Flags>
      requires ranges::sized_range<R> && indirectly_writable<ranges::iterator_t<R>, T>
    constexpr void simd_partial_store(const basic_simd<T, Abi>& v, R&& r, 
                                      const typename basic_simd<T, Abi>::mask_type& k,
                                      simd_flags<Flags...> f = {});
 
  template<class T, class Abi, contiguous_iterator I, class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_partial_store(const basic_simd<T, Abi>& v,
                                      I first, iter_difference_t<I> n,
                                      simd_flags<Flags...> f = {});
  template<class T, class Abi, contiguous_iterator I, class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_partial_store(const basic_simd<T, Abi>& v,
                                      I first, iter_difference_t<I> n,
                                      const typename basic_simd<T, Abi>::mask_type& k,
                                      simd_flags<Flags...> f = {});
 
  template<class T, class Abi, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_partial_store(const basic_simd<T, Abi>& v,
                                      I first, S last,
                                      simd_flags<Flags...> f = {});
  template<class T, class Abi, contiguous_iterator I, sized_sentinel_for<I> S,
           class... Flags>
      requires indirectly_writable<I, T>
    constexpr void simd_partial_store(const basic_simd<T, Abi>& v,
                                      I first, S last,
                                      const typename basic_simd<T, Abi>::mask_type& k,
                                      simd_flags<Flags...> f = {});
 
  // basic_simd and basic_simd_mask creation
  template<class T, class Abi>
    constexpr auto simd_split(
      const basic_simd<typename T::value_type, Abi>& x) noexcept;
  template<class T, class Abi>
    constexpr auto simd_split(
      const basic_simd_mask</*mask-element-size*/<T>, Abi>& x) noexcept;
 
  template<class T, class... Abis>
    constexpr basic_simd<T, /*deduce-abi-t*/<T, (basic_simd<T, Abis>::size() + ...)>>
    simd_cat(const basic_simd<T, Abis>&...) noexcept;
  template<size_t Bytes,, class... Abis>
    constexpr basic_simd<Bytes, /*deduce-abi-t*/</*integer-from*/<Bytes>, 
                        (basic_simd_mask<Bytes, Abis>::size() + ...)>>
    simd_cat(const basic_simd<Bytes, Abis>&...) noexcept;
 
  // basic_simd_mask reductions
  template<size_t Bytes, class Abi>
    constexpr bool all_of(const basic_simd_mask<Bytes, Abi>&) noexcept;
  template<size_t Bytes, class Abi>
    constexpr bool any_of(const basic_simd_mask<Bytes, Abi>&) noexcept;
  template<size_t Bytes, class Abi>
    constexpr bool none_of(const basic_simd_mask<Bytes, Abi>&) noexcept;
  template<size_t Bytes, class Abi>
    constexpr /*simd-size-type*/ reduce_count(const basic_simd_mask<Bytes, Abi>&) noexcept;
  template<size_t Bytes, class Abi>
    constexpr /*simd-size-type*/ reduce_min_index(const basic_simd_mask<Bytes, Abi>&);
  template<size_t Bytes, class Abi>
    constexpr /*simd-size-type*/ reduce_max_index(const basic_simd_mask<Bytes, Abi>&);
 
  constexpr bool all_of(same_as<bool> auto) noexcept;
  constexpr bool any_of(same_as<bool> auto) noexcept;
  constexpr bool none_of(same_as<bool> auto) noexcept;
  constexpr /*simd-size-type*/ reduce_count(same_as<bool> auto) noexcept;
  constexpr /*simd-size-type*/ reduce_min_index(same_as<bool> auto);
  constexpr /*simd-size-type*/ reduce_max_index(same_as<bool> auto);
 
  // basic_simd reductions
  template<class T, class Abi, class BinaryOperation = plus<>>
    constexpr T reduce(const basic_simd<T, Abi>&, BinaryOperation = {});
  template<class T, class Abi, class BinaryOperation = plus<>>
    constexpr T reduce(const basic_simd<T, Abi>& x, 
                       const typename basic_simd<T, Abi>::mask_type& mask,
                       BinaryOperation binary_op = {}, 
                       type_identity_t<T> identity_element = /* see description */ );
  template<class T, class Abi>
    constexpr T reduce_min(const basic_simd<T, Abi>&) noexcept;
  template<class T, class Abi>
    constexpr T reduce_min(const basic_simd<T, Abi>&,
                           const typename basic_simd<T, Abi>::mask_type&) noexcept;
  template<class T, class Abi>
    constexpr T reduce_max(const basic_simd<T, Abi>&) noexcept;
  template<class T, class Abi>
    constexpr T reduce_max(const basic_simd<T, Abi>&,
                           const typename basic_simd<T, Abi>::mask_type&) noexcept;
 
  // algorithms
  template<class T, class Abi>
    constexpr basic_simd<T, Abi>
    min(const basic_simd<T, Abi>& a, const basic_simd<T, Abi>& b) noexcept;
  template<class T, class Abi>
    constexpr basic_simd<T, Abi>
    max(const basic_simd<T, Abi>& a, const basic_simd<T, Abi>& b) noexcept;
  template<class T, class Abi>
    constexpr pair<basic_simd<T, Abi>, basic_simd<T, Abi>>
    minmax(const basic_simd<T, Abi>& a, const basic_simd<T, Abi>& b) noexcept;
  template<class T, class Abi>
    constexpr basic_simd<T, Abi>
    clamp(const basic_simd<T, Abi>& v, const basic_simd<T, Abi>& lo,
          const basic_simd<T, Abi>& hi);
 
  template<class T, class U>
    constexpr auto simd_select(bool c, const T& a, const U& b)
      -> remove_cvref_t<decltype(c ? a : b)>;
  template<size_t Bytes, class Abi, class T, class U>
    constexpr auto simd_select(const basic_simd_mask<Bytes, Abi>& c, 
                               const T& a, const U& b) noexcept 
      -> decltype(/*simd-select-impl*/(c, a, b));
 
  // mathematical functions
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> acos(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> asin(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> atan(const V& x);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> atan2(const V0& y, const V1& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> cos(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> sin(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> tan(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> acosh(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> asinh(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> atanh(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> cosh(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> sinh(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> tanh(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> exp(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> exp2(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> expm1(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V>
    frexp(const V& value, rebind_simd_t<int, /*deduced-simd-t*/<V>>* exp);
  template</*math-floating-point*/ V>
    constexpr rebind_simd_t<int, /*deduced-simd-t*/<V>> ilogb(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> ldexp(const V& x,
                                          const rebind_simd_t<int, 
                                            /*deduced-simd-t*/<V>>& exp);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> log(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> log10(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> log1p(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> log2(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> logb(const V& x);
  template<class T, class Abi>
    constexpr basic_simd<T, Abi> modf(const type_identity_t<basic_simd<T, Abi>>& value,
                                      basic_simd<T, Abi>* iptr);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> scalbn(const V& x,
                                           const rebind_simd_t<int, 
                                             /*deduced-simd-t*/<V>>& n);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> scalbln(const V& x,
                                            const rebind_simd_t<long int, 
                                              /*deduced-simd-t*/<V>>& n);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> cbrt(const V& x);
  template<signed_integral T, class Abi>
    constexpr basic_simd<T, Abi> abs(const basic_simd<T, Abi>& j);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> abs(const V& j);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> fabs(const V& x);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> hypot(const V0& x, const V1& y);
  template<class V0, class V1, class V2>
    constexpr /*math-common-simd-t*/<V0, V1, V2> hypot(const V0& x, const V1& y, 
                                                       const V2& z);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> pow(const V0& x, const V1& y);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> sqrt(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> erf(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> erfc(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> lgamma(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> tgamma(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> ceil(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> floor(const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> nearbyint(const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> rint(const V& x);
  template</*math-floating-point*/ V>
    rebind_simd_t<long int, /*deduced-simd-t*/<V>> lrint(const V& x);
  template</*math-floating-point*/ V>
    rebind_simd_t<long long int, V> llrint(const /*deduced-simd-t*/<V>& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> round(const V& x);
  template</*math-floating-point*/ V>
    constexpr rebind_simd_t<long int, /*deduced-simd-t*/<V>> lround(const V& x);
  template</*math-floating-point*/ V>
    constexpr rebind_simd_t<long long int, /*deduced-simd-t*/<V>> llround(const V& x);
  template</*math-floating-point*/ V>
    constexpr /*deduced-simd-t*/<V> trunc(const V& x);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> fmod(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> remainder(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1>
    remquo(const V0& x, const V1& y, 
           rebind_simd_t<int, /*math-common-simd-t*/<V0, V1>>* quo);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> copysign(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> nextafter(const V0& x, const V1& y);
 
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> fdim(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> fmax(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr /*math-common-simd-t*/<V0, V1> fmin(const V0& x, const V1& y);
  template<class V0, class V1, class V2>
    constexpr /*math-common-simd-t*/<V0, V1, V2> fma(const V0& x, const V1& y, 
                                                     const V2& z);
  template<class V0, class V1, class V2>
    constexpr /*math-common-simd-t*/<V0, V1, V2> lerp(const V0& a, const V1& b, 
                                                      const V2& t) noexcept;
  template</*math-floating-point*/ V>
    constexpr rebind_simd_t<int, /*deduced-simd-t*/<V>> fpclassify(const V& x);
  template</*math-floating-point*/ V>
    constexpr typename /*deduced-simd-t*/<V>::mask_type isfinite(const V& x);
  template</*math-floating-point*/ V>
    constexpr typename /*deduced-simd-t*/<V>::mask_type isinf(const V& x);
  template</*math-floating-point*/ V>
    constexpr typename /*deduced-simd-t*/<V>::mask_type isnan(const V& x);
  template</*math-floating-point*/ V>
    constexpr typename /*deduced-simd-t*/<V>::mask_type isnormal(const V& x);
  template</*math-floating-point*/ V>
    constexpr typename /*deduced-simd-t*/<V>::mask_type signbit(const V& x);
  template<class V0, class V1>
    constexpr typename /*math-common-simd-t*/<V0, V1>::mask_type
    isgreater(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr typename /*math-common-simd-t*/<V0, V1>::mask_type
    isgreaterequal(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr typename /*math-common-simd-t*/<V0, V1>::mask_type
    isless(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr typename /*math-common-simd-t*/<V0, V1>::mask_type
    islessequal(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr typename /*math-common-simd-t*/<V0, V1>::mask_type
    islessgreater(const V0& x, const V1& y);
  template<class V0, class V1>
    constexpr typename /*math-common-simd-t*/<V0, V1>::mask_type
    isunordered(const V0& x, const V1& y);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> assoc_laguerre(const rebind_simd_t<unsigned, 
                                           /*deduced-simd-t*/<V>>& n,
                                         const rebind_simd_t<unsigned, 
                                           /*deduced-simd-t*/<V>>& m,
                                         const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> assoc_legendre(const rebind_simd_t<unsigned, 
                                           /*deduced-simd-t*/<V>>& l,
                                         const rebind_simd_t<unsigned, 
                                           /*deduced-simd-t*/<V>>& m,
                                         const V& x);
 
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> beta(const V0& x, const V1& y);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> comp_ellint_1(const V& k);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> comp_ellint_2(const V& k);
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> comp_ellint_3(const V0& k, const V1& nu);
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> cyl_bessel_i(const V0& nu, const V1& x);
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> cyl_bessel_j(const V0& nu, const V1& x);
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> cyl_bessel_k(const V0& nu, const V1& x);
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> cyl_neumann(const V0& nu, const V1& x);
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> ellint_1(const V0& k, const V1& phi);
  template<class V0, class V1>
    /*math-common-simd-t*/<V0, V1> ellint_2(const V0& k, const V1& phi);
  template<class V0, class V1, class V2>
    /*math-common-simd-t*/<V0, V1, V2> ellint_3(const V0& k, const V1& nu, const V2& phi);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> expint(const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> hermite(const rebind_simd_t<unsigned, 
                                    /*deduced-simd-t*/<V>>& n,
                                  const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> laguerre(const rebind_simd_t<unsigned, 
                                     /*deduced-simd-t*/<V>>& n,
                                   const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> legendre(const rebind_simd_t<unsigned, 
                                     /*deduced-simd-t*/<V>>& l,
                                   const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> riemann_zeta(const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> sph_bessel(const rebind_simd_t<unsigned, 
                                       /*deduced-simd-t*/<V>>& n,
                                     const V& x);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> sph_legendre(const rebind_simd_t<unsigned, 
                                         /*deduced-simd-t*/<V>>& l,
                                       const rebind_simd_t<unsigned, 
                                         /*deduced-simd-t*/<V>>& m,
                                       const V& theta);
  template</*math-floating-point*/ V>
    /*deduced-simd-t*/<V> sph_neumann(const rebind_simd_t<unsigned, 
                                        /*deduced-simd-t*/<V>>& n,
                                      const V& x);
}

```

#### Class template std::simd_flags

```
namespace std {
  template<class... Flags>
  struct simd_flags {
    // simd_flags operators
    template<class... Other>
      friend consteval auto operator|(simd_flags, simd_flags<Other...>);
  };
}

```

#### Class template std::basic_simd

```
namespace std {
  template<class T, class Abi>
  class basic_simd {
  public:
    using value_type = T;
    using mask_type  = basic_simd_mask<sizeof(T), Abi>;
    using abi_type   = Abi;
 
    static constexpr integral_constant<
      /*simd-size-type*/, /*simd-size-v*/<T, Abi>> size {};
 
    // basic_simd constructors
    constexpr basic_simd() noexcept = default;
    template<class U> 
      constexpr basic_simd(U&& value) noexcept;
    template<class U, class UAbi>
      constexpr explicit(/* see description */) 
      basic_simd(const basic_simd<U, UAbi>&) noexcept;
    template<class G> 
      constexpr explicit basic_simd(G&& gen) noexcept;
    template<class R, class... Flags>
      constexpr basic_simd(R&& range, simd_flags<Flags...> = {});
    template<class R, class... Flags>
      constexpr basic_simd(R&& range, const mask_type& mask, 
                           simd_flags<Flags...> = {});
 
    // basic_simd subscript operator
    constexpr value_type operator[](/*simd-size-type*/) const;
 
    // basic_simd unary operators
    constexpr basic_simd& operator++() noexcept;
    constexpr basic_simd operator++(int) noexcept;
    constexpr basic_simd& operator--() noexcept;
    constexpr basic_simd operator--(int) noexcept;
    constexpr mask_type operator!() const noexcept;
    constexpr basic_simd operator~() const noexcept;
    constexpr basic_simd operator+() const noexcept;
    constexpr basic_simd operator-() const noexcept;
 
    // basic_simd binary operators
    friend constexpr basic_simd operator+(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator-(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator*(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator/(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator%(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator&(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator|(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator^(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator<<(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator>>(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd operator<<(const basic_simd&, /*simd-size-type*/) noexcept;
    friend constexpr basic_simd operator>>(const basic_simd&, /*simd-size-type*/) noexcept;
 
    // basic_simd compound assignment
    friend constexpr basic_simd& operator+=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator-=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator*=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator/=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator%=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator&=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator|=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator^=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator<<=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator>>=(basic_simd&, const basic_simd&) noexcept;
    friend constexpr basic_simd& operator<<=(basic_simd&, /*simd-size-type*/) noexcept;
    friend constexpr basic_simd& operator>>=(basic_simd&, /*simd-size-type*/) noexcept;
 
    // basic_simd comparison operators
    friend constexpr mask_type operator==(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr mask_type operator!=(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr mask_type operator>=(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr mask_type operator<=(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr mask_type operator>(const basic_simd&, const basic_simd&) noexcept;
    friend constexpr mask_type operator<(const basic_simd&, const basic_simd&) noexcept;
 
    // basic_simd exposition only conditional operators
    // exposition only
    friend constexpr basic_simd /*simd-select-impl*/(
      const mask_type&, const basic_simd&, const basic_simd&) noexcept;
  };
 
  template<class R, class... Ts>
    basic_simd(R&& r, Ts...) -> /* see description */;
}

```

#### Class template std::basic_simd_mask

```
namespace std {
  template<size_t Bytes, class Abi>
  class basic_simd_mask {
  public:
    using value_type = bool;
    using abi_type   = Abi;
 
    static constexpr integral_constant<
      /*simd-size-type*/, /*simd-size-v*/</*integer-from*/<Bytes>, Abi>> size {};
 
    // basic_simd_mask constructors
    constexpr basic_simd_mask() noexcept = default;
    constexpr explicit basic_simd_mask(value_type) noexcept;
    template<size_t UBytes, class UAbi>
      constexpr explicit basic_simd_mask(const basic_simd_mask<UBytes, UAbi>&) noexcept;
    template<class G> 
      constexpr explicit basic_simd_mask(G&& gen) noexcept;
 
    // basic_simd_mask subscript operator
    constexpr value_type operator[](/*simd-size-type*/) const;
 
    // basic_simd_mask unary operators
    constexpr basic_simd_mask operator!() const noexcept;
    constexpr basic_simd</*integer-from*/<Bytes>, Abi> operator+() const noexcept;
    constexpr basic_simd</*integer-from*/<Bytes>, Abi> operator-() const noexcept;
    constexpr basic_simd</*integer-from*/<Bytes>, Abi> operator~() const noexcept;
 
    // basic_simd_mask conversion operators
    template<class U, class A>
      constexpr explicit(sizeof(U) != Bytes) 
      operator basic_simd<U, A>() const noexcept;
 
    // basic_simd_mask binary operators
    friend constexpr basic_simd_mask
      operator&&(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator||(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator&(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator|(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator^(const basic_simd_mask&, const basic_simd_mask&) noexcept;
 
    // basic_simd_mask compound assignment
    friend constexpr basic_simd_mask&
      operator&=(basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask&
      operator|=(basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask&
      operator^=(basic_simd_mask&, const basic_simd_mask&) noexcept;
 
    // basic_simd_mask comparisons
    friend constexpr basic_simd_mask
      operator==(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator!=(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator>=(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator<=(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator>(const basic_simd_mask&, const basic_simd_mask&) noexcept;
    friend constexpr basic_simd_mask
      operator<(const basic_simd_mask&, const basic_simd_mask&) noexcept;
 
    // basic_simd_mask exposition only conditional operators
    // exposition only
    friend constexpr basic_simd_mask /*simd-select-impl*/(
      const basic_simd_mask&, const basic_simd_mask&, const basic_simd_mask&) noexcept;
    // exposition only
    friend constexpr basic_simd_mask /*simd-select-impl*/(
      const basic_simd_mask&, same_as<bool> auto, same_as<bool> auto) noexcept;
    // exposition only
    template<class T0, class T1>
      friend constexpr simd<see below , size()>
      /*simd-select-impl*/(const basic_simd_mask&, const T0&, const T1&) noexcept;
  };
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/simd&oldid=178390>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 December 2024, at 18:13.