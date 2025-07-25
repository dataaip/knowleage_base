# Standard library header <format> (C++20)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | ****<format>**** (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the text processing library.

|  |  |
| --- | --- |
| Concepts | |
| formattable(C++23) | specifies that a type is formattable, that is, it specializes std::formatter and provides member functions `parse` and `format`   (concept) |
| Enumerations | |
| range_format(C++23) | specifies how a range should be formatted   (enum) |
| Classes | |
| formatter(C++20) | defines formatting rules for a given type   (class template) |
| range_formatter(C++23) | class template that helps implementing std::formatter specializations for range types   (class template) |
| basic_format_parse_contextformat_parse_contextwformat_parse_context(C++20)(C++20)(C++20) | formatting string parser state   (class template) |
| basic_format_contextformat_contextwformat_context(C++20)(C++20)(C++20) | formatting state, including all formatting arguments and the output iterator   (class template) |
| basic_format_arg(C++20) | class template that provides access to a formatting argument for user-defined formatters   (class template) |
| basic_format_argsformat_argswformat_args(C++20)(C++20)(C++20) | class that provides access to all formatting arguments   (class template) |
| basic_format_stringformat_stringwformat_string(C++20)(C++20)(C++20) | class template that performs compile-time format string checks at construction time   (class template) |
| format_error(C++20) | exception type thrown on formatting errors   (class) |
| Formatter specializations | |
| std::formatter<**pair-or-tuple**>(C++23) | formatting support for `pair` and `tuple`   (class template specialization) |
| std::formatter<**range**>(C++23) | formatting support for ranges   (class template specialization) |
| Functions | |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |
| format_to(C++20) | writes out formatted representation of its arguments through an output iterator   (function template) |
| format_to_n(C++20) | writes out formatted representation of its arguments through an output iterator, not exceeding specified size   (function template) |
| formatted_size(C++20) | determines the number of characters necessary to store the formatted representation of its arguments   (function template) |
| runtime_format(C++26) | creates runtime format strings directly usable in user-oriented formatting functions   (function) |
| vformat(C++20) | non-template variant of std::format using type-erased argument representation   (function) |
| vformat_to(C++20) | non-template variant of std::format_to using type-erased argument representation   (function template) |
| visit_format_arg(C++20) (deprecated in C++26) | argument visitation interface for user-defined formatters   (function template) |
| make_format_argsmake_wformat_args(C++20)(C++20) | creates a type-erased object referencing all formatting arguments, convertible to `format_args`   (function template) |
| Helpers | |
| format_kind(C++23) | selects a suited std::range_format for a range (variable template) |
| enable_nonlocking_formatter_optimization(C++23) | indicates the argument type can be efficiently printed (variable template) |

### Synopsis

```
namespace std {
  // class template basic_format_context
  template<class Out, class CharT> class basic_format_context;
  using format_context = basic_format_context</* unspecified */, char>;
  using wformat_context = basic_format_context</* unspecified */, wchar_t>;
 
  // class template basic_format_args
  template<class Context> class basic_format_args;
  using format_args = basic_format_args<format_context>;
  using wformat_args = basic_format_args<wformat_context>;
 
  // class template basic_format_string
  template<class CharT, class... Args>
    struct basic_format_string;
 
  template<class... Args>
    using format_string = basic_format_string<char, type_identity_t<Args>...>;
  template<class... Args>
    using wformat_string = basic_format_string<wchar_t, type_identity_t<Args>...>;
 
  // formatting functions
  template<class... Args>
    string format(format_string<Args...> fmt, Args&&... args);
  template<class... Args>
    wstring format(wformat_string<Args...> fmt, Args&&... args);
  template<class... Args>
    string format(const locale& loc, format_string<Args...> fmt, Args&&... args);
  template<class... Args>
    wstring format(const locale& loc, wformat_string<Args...> fmt, Args&&... args);
 
  string vformat(string_view fmt, format_args args);
  wstring vformat(wstring_view fmt, wformat_args args);
  string vformat(const locale& loc, string_view fmt, format_args args);
  wstring vformat(const locale& loc, wstring_view fmt, wformat_args args);
 
  template<class Out, class... Args>
    Out format_to(Out out, format_string<Args...> fmt, Args&&... args);
  template<class Out, class... Args>
    Out format_to(Out out, wformat_string<Args...> fmt, Args&&... args);
  template<class Out, class... Args>
    Out format_to(Out out, const locale& loc, format_string<Args...> fmt, Args&&... args);
  template<class Out, class... Args>
    Out format_to(Out out, const locale& loc, wformat_string<Args...> fmt, Args&&... args);
 
  template<class Out>
    Out vformat_to(Out out, string_view fmt, format_args args);
  template<class Out>
    Out vformat_to(Out out, wstring_view fmt, wformat_args args);
  template<class Out>
    Out vformat_to(Out out, const locale& loc, string_view fmt, format_args args);
  template<class Out>
    Out vformat_to(Out out, const locale& loc, wstring_view fmt, wformat_args args);
 
  template<class Out> struct format_to_n_result {
    Out out;
    iter_difference_t<Out> size;
  };
  template<class Out, class... Args>
    format_to_n_result<Out> format_to_n(Out out, iter_difference_t<Out> n,
                                        format_string<Args...> fmt, Args&&... args);
  template<class Out, class... Args>
    format_to_n_result<Out> format_to_n(Out out, iter_difference_t<Out> n,
                                        wformat_string<Args...> fmt, Args&&... args);
  template<class Out, class... Args>
    format_to_n_result<Out> format_to_n(Out out, iter_difference_t<Out> n,
                                        const locale& loc, format_string<Args...> fmt,
                                        Args&&... args);
  template<class Out, class... Args>
    format_to_n_result<Out> format_to_n(Out out, iter_difference_t<Out> n,
                                        const locale& loc, wformat_string<Args...> fmt,
                                        Args&&... args);
 
  template<class... Args>
    size_t formatted_size(format_string<Args...> fmt, Args&&... args);
  template<class... Args>
    size_t formatted_size(wformat_string<Args...> fmt, Args&&... args);
  template<class... Args>
    size_t formatted_size(const locale& loc, format_string<Args...> fmt, Args&&... args);
  template<class... Args>
    size_t formatted_size(const locale& loc, wformat_string<Args...> fmt, Args&&... args);
 
  // formatter
  template<class T, class CharT = char>
    struct formatter;
 
  // variable template enable_nonlocking_formatter_optimization
  template<class T>
    constexpr bool enable_nonlocking_formatter_optimization = false;
 
  // concept formattable
  template<class T, class CharT>
    concept formattable = /* see description */;
 
  template<class R, class CharT>
    concept __const_formattable_range =                               // exposition only
      ranges::input_range<const R> &&
      formattable<ranges::range_reference_t<const R>, CharT>;
 
  template<class R, class CharT>
    using __fmt_maybe_const =                                         // exposition only
      conditional_t<__const_formattable_range<R, CharT>, const R, R>;
 
  // class template basic_format_parse_context
  template<class CharT> class basic_format_parse_context;
  using format_parse_context = basic_format_parse_context<char>;
  using wformat_parse_context = basic_format_parse_context<wchar_t>;
 
  // formatting of ranges
  // variable template format_kind
  enum class range_format {
    disabled,
    map,
    set,
    sequence,
    string,
    debug_string
  };
 
  template<class R>
    constexpr /* unspecified */ format_kind = /* unspecified */;
 
  template<ranges::input_range R>
      requires same_as<R, remove_cvref_t<R>>
    constexpr range_format format_kind<R> = /* see description */;
 
  // class template range_formatter
  template<class T, class CharT = char>
    requires same_as<remove_cvref_t<T>, T> && formattable<T, CharT>
  class range_formatter;
 
  // class template range-default-formatter
  template<range_format K, ranges::input_range R, class CharT>
    struct __range_default_formatter;                                 // exposition only
 
  // specializations for maps, sets, and strings
  template<ranges::input_range R, class CharT>
    requires (format_kind<R> != range_format::disabled) &&
             formattable<ranges::range_reference_t<R>, CharT>
  struct formatter<R, CharT> : __range_default_formatter<format_kind<R>, R, CharT> { };
 
  // arguments
  // class template basic_format_arg
  template<class Context> class basic_format_arg;
 
  template<class Visitor, class Context>
    decltype(auto) visit_format_arg(Visitor&& vis, basic_format_arg<Context> arg);
 
  // class template format-arg-store
  template<class Context, class... Args> class __format_arg_store;    // exposition only
 
  template<class Context = format_context, class... Args>
    __format_arg_store<Context, Args...>
      make_format_args(Args&&... fmt_args);
  template<class... Args>
    __format_arg_store<wformat_context, Args...>
      make_wformat_args(Args&&... args);
 
  // class format_error
  class format_error;
}

```

#### Class template std::basic_format_string

```
namespace std {
  template<class CharT, class... Args>
  struct basic_format_string {
  private:
    basic_string_view<CharT> str;         // exposition only
 
  public:
    template<class T> consteval basic_format_string(const T& s);
 
    constexpr basic_string_view<CharT> get() const noexcept { return str; }
  };
}

```

#### Concept `std::formattable`

```
template<class T, class CharT>
  concept formattable =
    semiregular<formatter<remove_cvref_t<T>, CharT>> &&
    requires(formatter<remove_cvref_t<T>, CharT> f,
             const formatter<remove_cvref_t<T>, CharT> cf,
             T t,
             basic_format_context<__fmt_iter_for<CharT>, CharT> fc,
             basic_format_parse_context<CharT> pc) {
        { f.parse(pc) } -> same_as<basic_format_parse_context<CharT>::iterator>;
        { cf.format(t, fc) } -> same_as<__fmt_iter_for<CharT>>;
    };

```

#### Class template std::basic_format_parse_context

```
namespace std {
  template<class CharT>
  class basic_format_parse_context {
  public:
    using char_type = CharT;
    using const_iterator = typename basic_string_view<CharT>::const_iterator;
    using iterator = const_iterator;
 
  private:
    iterator begin_;                                    // exposition only
    iterator end_;                                      // exposition only
    enum indexing { unknown, manual, automatic };       // exposition only
    indexing indexing_;                                 // exposition only
    size_t next_arg_id_;                                // exposition only
    size_t num_args_;                                   // exposition only
 
  public:
    constexpr explicit basic_format_parse_context(basic_string_view<CharT> fmt,
                                                  size_t num_args = 0) noexcept;
    basic_format_parse_context(const basic_format_parse_context&) = delete;
    basic_format_parse_context& operator=(const basic_format_parse_context&) = delete;
 
    constexpr const_iterator begin() const noexcept;
    constexpr const_iterator end() const noexcept;
    constexpr void advance_to(const_iterator it);
 
    constexpr size_t next_arg_id();
    constexpr void check_arg_id(size_t id);
 
    template<class... Ts>
    constexpr void check_dynamic_spec(size_t id) noexcept;
    constexpr void check_dynamic_spec_integral(size_t id) noexcept;
    constexpr void check_dynamic_spec_string(size_t id) noexcept;
  };
}

```

#### Class template std::basic_format_context

```
namespace std {
  template<class Out, class CharT>
  class basic_format_context {
    basic_format_args<basic_format_context> args_;      // exposition only
    Out out_;                                           // exposition only
 
    basic_format_context(const basic_format_context&) = delete;
    basic_format_context& operator=(const basic_format_context&) = delete;
 
  public:
    using iterator = Out;
    using char_type = CharT;
    template<class T> using formatter_type = formatter<T, CharT>;
 
    basic_format_arg<basic_format_context> arg(size_t id) const noexcept;
    std::locale locale();
 
    iterator out();
    void advance_to(iterator it);
  };
}

```

#### Variable template std::format_kind

```
template<ranges::input_range R>
    requires same_as<R, remove_cvref_t<R>>
  constexpr range_format format_kind<R> = /* see description */;

```

#### Class template std::range_formatter

```
namespace std {
  template<class T, class CharT = char>
    requires same_as<remove_cvref_t<T>, T> && formattable<T, CharT>
  class range_formatter {
    formatter<T, CharT> underlying_;                        // exposition only
    basic_string_view<CharT> separator_ =                   // exposition only
      __STATICALLY_WIDEN<CharT>(", ");
    basic_string_view<CharT> __opening_bracket_ =           // exposition only
      __STATICALLY_WIDEN<CharT>("[");
    basic_string_view<CharT> __closing_bracket_ =           // exposition only
      __STATICALLY_WIDEN<CharT>("]");
 
  public:
    constexpr void set_separator(basic_string_view<CharT> sep);
    constexpr void set_brackets(basic_string_view<CharT> opening,
                                basic_string_view<CharT> closing);
    constexpr formatter<T, CharT>& underlying() { return underlying_; }
    constexpr const formatter<T, CharT>& underlying() const { return underlying_; }
 
    template<class ParseContext>
      constexpr typename ParseContext::iterator
        parse(ParseContext& ctx);
 
    template<ranges::input_range R, class FormatContext>
        requires formattable<ranges::range_reference_t<R>, CharT> &&
                 same_as<remove_cvref_t<ranges::range_reference_t<R>>, T>
      typename FormatContext::iterator
        format(R&& r, FormatContext& ctx) const;
  };
}

```

#### Class template **__range_default_formatter**

```
namespace std {
  template<ranges::input_range R, class CharT>
  struct __range_default_formatter<range_format::sequence, R, CharT> {
  private:
    using __maybe_const_r = __fmt_maybe_const<R, CharT>;
    range_formatter<remove_cvref_t<ranges::range_reference_t<__maybe_const_r>>,
                    CharT> underlying_;       // exposition only
 
  public:
    constexpr void set_separator(basic_string_view<CharT> sep);
    constexpr void set_brackets(basic_string_view<CharT> opening,
                                basic_string_view<CharT> closing);
 
    template<class ParseContext>
      constexpr typename ParseContext::iterator
        parse(ParseContext& ctx);
 
    template<class FormatContext>
      typename FormatContext::iterator
        format(__maybe_const_r& elems, FormatContext& ctx) const;
  };
}

```

#### Specialization of **__range_default_formatter** for maps

```
namespace std {
  template<ranges::input_range R, class CharT>
  struct __range_default_formatter<range_format::map, R, CharT> {
  private:
    using __maybe_const_map = __fmt_maybe_const<R, CharT>;          // exposition only
    using __element_type =                                          // exposition only
      remove_cvref_t<ranges::range_reference_t<__maybe_const_map>>;
    range_formatter<__element_type, CharT> underlying_;             // exposition only
  public:
    constexpr __range_default_formatter();
 
    template<class ParseContext>
      constexpr typename ParseContext::iterator
        parse(ParseContext& ctx);
 
    template<class FormatContext>
      typename FormatContext::iterator
        format(__maybe_const_map& r, FormatContext& ctx) const;
  };
}

```

#### Specialization of **__range_default_formatter** for sets

```
namespace std {
  template<ranges::input_range R, class CharT>
  struct __range_default_formatter<range_format::set, R, CharT> {
  private:
    using __maybe_const_set = __fmt_maybe_const<R, CharT>;          // exposition only
    range_formatter<remove_cvref_t<ranges::range_reference_t<__maybe_const_set>>,
                    CharT> underlying_;                             // exposition only
  public:
    constexpr __range_default_formatter();
 
    template<class ParseContext>
      constexpr typename ParseContext::iterator
        parse(ParseContext& ctx);
 
    template<class FormatContext>
      typename FormatContext::iterator
        format(__maybe_const_set& r, FormatContext& ctx) const;
  };
}

```

#### Specialization of **__range_default_formatter** for strings

```
namespace std {
  template<range_format K, ranges::input_range R, class CharT>
    requires (K == range_format::string || K == range_format::debug_string)
  struct __range_default_formatter<K, R, CharT> {
  private:
    formatter<basic_string<CharT>, CharT> underlying_;              // exposition only
 
  public:
    template<class ParseContext>
      constexpr typename ParseContext::iterator
        parse(ParseContext& ctx);
 
    template<class FormatContext>
      typename FormatContext::iterator
        format(/* see description */& str, FormatContext& ctx) const;
  };
}

```

#### Class template std::basic_format_arg

```
namespace std {
  template<class Context>
  class basic_format_arg {
  public:
    class handle;
 
  private:
    using char_type = typename Context::char_type;                     // exposition only
 
    variant<monostate, bool, char_type,
            int, unsigned int, long long int, unsigned long long int,
            float, double, long double,
            const char_type*, basic_string_view<char_type>,
            const void*, handle> value;                                // exposition only
 
    template<class T> explicit basic_format_arg(T&& v) noexcept;       // exposition only
    explicit basic_format_arg(float n) noexcept;                       // exposition only
    explicit basic_format_arg(double n) noexcept;                      // exposition only
    explicit basic_format_arg(long double n) noexcept;                 // exposition only
    explicit basic_format_arg(const char_type* s);                     // exposition only
 
    template<class traits>
      explicit basic_format_arg(
        basic_string_view<char_type, traits> s) noexcept;              // exposition only
 
    template<class traits, class Allocator>
      explicit basic_format_arg(
        const basic_string<char_type, traits, Allocator>& s) noexcept; // exposition only
 
    explicit basic_format_arg(nullptr_t) noexcept;                     // exposition only
 
    template<class T>
      explicit basic_format_arg(T* p) noexcept;                        // exposition only
 
  public:
    basic_format_arg() noexcept;
 
    explicit operator bool() const noexcept;
 
    template<class Visitor>
      decltype(auto) visit(this basic_format_arg arg, Visitor&& vis);
    template<class R, class Visitor>
      R visit(this basic_format_arg arg, Visitor&& vis);
  };
}

```

#### Class std::basic_format_arg::handle

```
namespace std {
  template<class Context>
  class basic_format_arg<Context>::handle {
    const void* ptr_;                                           // exposition only
    void (*format_)(basic_format_parse_context<char_type>&,
                    Context&, const void*);                     // exposition only
 
    template<class T> explicit handle(T&& val) noexcept;        // exposition only
 
    friend class basic_format_arg<Context>;                     // exposition only
 
  public:
    void format(basic_format_parse_context<char_type>&, Context& ctx) const;
  };
}

```

#### Class template **__format_arg_store**

```
namespace std {
  template<class Context, class... Args>
  class __format_arg_store {                                    // exposition only
    array<basic_format_arg<Context>, sizeof...(Args)> args;     // exposition only
  };
}

```

#### Class template std::basic_format_args

```
namespace std {
  template<class Context>
  class basic_format_args {
    size_t size_;                               // exposition only
    const basic_format_arg<Context>* data_;     // exposition only
 
  public:
    template<class... Args>
      basic_format_args(const __format_arg_store<Context, Args...>& store) noexcept;
 
    basic_format_arg<Context> get(size_t i) const noexcept;
  };
}

```

#### Tuple formatter

```
namespace std {
  template<class CharT, formattable<CharT>... Ts>
  struct formatter<__pair_or_tuple<Ts...>, CharT> {
  private:
    tuple<formatter<remove_cvref_t<Ts>, CharT>...> underlying_;     // exposition only
    basic_string_view<CharT> separator_ =                           // exposition only
      __STATICALLY_WIDEN<CharT>(", ");
    basic_string_view<CharT> opening_bracket_ =                     // exposition only
      __STATICALLY_WIDEN<CharT>("(");
    basic_string_view<CharT> closing_bracket_ =                     // exposition only
      __STATICALLY_WIDEN<CharT>(")");
 
  public:
    constexpr void set_separator(basic_string_view<CharT> sep);
    constexpr void set_brackets(basic_string_view<CharT> opening,
                                basic_string_view<CharT> closing);
 
    template<class ParseContext>
      constexpr typename ParseContext::iterator
        parse(ParseContext& ctx);
 
    template<class FormatContext>
      typename FormatContext::iterator
        format(/* see description */& elems, FormatContext& ctx) const;
  };
}

```

#### Class std::format_error

```
namespace std {
  class format_error : public runtime_error {
  public:
    explicit format_error(const string& what_arg);
    explicit format_error(const char* what_arg);
  };
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/format&oldid=179094>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 21:00.