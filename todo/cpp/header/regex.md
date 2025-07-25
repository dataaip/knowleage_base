# Standard library header <regex> (C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | ****<regex>**** (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the text processing library.

|  |  |
| --- | --- |
| Includes | |
| <compare>(C++20) | Three-way comparison operator support |
| <initializer_list>(C++11) | std::initializer_list class template |
| Classes | |
| basic_regex(C++11) | regular expression object   (class template) |
| std::regex | std::basic_regex<char> (typedef) |
| std::wregex | std::basic_regex<wchar_t> (typedef) |
| sub_match(C++11) | identifies the sequence of characters matched by a sub-expression   (class template) |
| std::csub_match | std::sub_match<const char\*> (typedef) |
| std::wcsub_match | std::sub_match<const wchar_t\*> (typedef) |
| std::ssub_match | std::sub_match<std::string::const_iterator> (typedef) |
| std::wssub_match | std::sub_match<std::wstring::const_iterator> (typedef) |
| match_results(C++11) | identifies one regular expression match, including all sub-expression matches   (class template) |
| std::cmatch | std::match_results<const char\*> (typedef) |
| std::wcmatch | std::match_results<const wchar_t\*> (typedef) |
| std::smatch | std::match_results<std::string::const_iterator> (typedef) |
| std::wsmatch | std::match_results<std::wstring::const_iterator> (typedef) |
| regex_iterator(C++11) | iterates through all regex matches within a character sequence   (class template) |
| std::cregex_iterator | std::regex_iterator<const char\*> (typedef) |
| std::wcregex_iterator | std::regex_iterator<const wchar_t\*> (typedef) |
| std::sregex_iterator | std::regex_iterator<std::string::const_iterator> (typedef) |
| std::wsregex_iterator | std::regex_iterator<std::wstring::const_iterator> (typedef) |
| regex_token_iterator(C++11) | iterates through the specified sub-expressions within all regex matches in a given string or through unmatched substrings   (class template) |
| std::cregex_token_iterator | std::regex_token_iterator<const char\*> (typedef) |
| std::wcregex_token_iterator | std::regex_token_iterator<const wchar_t\*> (typedef) |
| std::sregex_token_iterator | std::regex_token_iterator<std::string::const_iterator> (typedef) |
| std::wsregex_token_iterator | std::regex_token_iterator<std::wstring::const_iterator> (typedef) |
| regex_error(C++11) | reports errors generated by the regular expressions library   (class) |
| regex_traits(C++11) | provides metainformation about a character type, required by the regex library   (class template) |
| regex constant types | |
| Defined in namespace `std::regex_constants` | |
| syntax_option_type(C++11) | general options controlling regex behavior   (typedef) |
| match_flag_type(C++11) | options specific to matching   (typedef) |
| error_type(C++11) | describes different types of matching errors   (typedef) |
| Functions | |
| Algorithm | |
| regex_match(C++11) | attempts to match a regular expression to an entire character sequence   (function template) |
| regex_search(C++11) | attempts to match a regular expression to any part of a character sequence   (function template) |
| regex_replace(C++11) | replaces occurrences of a regular expression with formatted replacement text   (function template) |
| Non-member operations | |
| std::swap(std::basic_regex)(C++11) | specializes the std::swap algorithm   (function template) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | compares a `sub_match` with another `sub_match`, a string, or a character   (function template) |
| operator<< | outputs the matched character subsequence   (function template) |
| operator==operator!=(removed in C++20) | lexicographically compares the values in the two match result   (function template) |
| std::swap(std::match_results)(C++11) | specializes the std::swap algorithm   (function template) |
| Range access | |
| begincbegin(C++11)(C++14) | returns an iterator to the beginning of a container or array   (function template) |
| endcend(C++11)(C++14) | returns an iterator to the end of a container or array   (function template) |
| rbegincrbegin(C++14) | returns a reverse iterator to the beginning of a container or array   (function template) |
| rendcrend(C++14) | returns a reverse end iterator for a container or array   (function template) |
| sizessize(C++17)(C++20) | returns the size of a container or array   (function template) |
| empty(C++17) | checks whether the container is empty   (function template) |
| data(C++17) | obtains the pointer to the underlying array   (function template) |

### Synopsis

```
#include <compare>
#include <initializer_list>
 
namespace std {
  // regex constants
  namespace regex_constants {
    using syntax_option_type = /*T1*/;
    using match_flag_type = /*T2*/;
    using error_type = /*T3*/;
  }
 
  // class regex_error
  class regex_error;
 
  // class template regex_traits
  template<class CharT> struct regex_traits;
 
  // class template basic_regex
  template<class CharT, class Traits = regex_traits<CharT>> class basic_regex;
 
  using regex  = basic_regex<char>;
  using wregex = basic_regex<wchar_t>;
 
  // basic_regex swap
  template<class CharT, class Traits>
    void swap(basic_regex<CharT, Traits>& e1, basic_regex<CharT, Traits>& e2);
 
  // class template sub_match
  template<class BiIt>
    class sub_match;
 
  using csub_match  = sub_match<const char*>;
  using wcsub_match = sub_match<const wchar_t*>;
  using ssub_match  = sub_match<string::const_iterator>;
  using wssub_match = sub_match<wstring::const_iterator>;
 
  // sub_match non-member operators
  template<class BiIt>
    bool operator==(const sub_match<BiIt>& lhs, const sub_match<BiIt>& rhs);
  template<class BiIt>
    auto operator<=>(const sub_match<BiIt>& lhs, const sub_match<BiIt>& rhs);
 
  template<class BiIt, class ST, class SA>
    bool operator==(
      const sub_match<BiIt>& lhs,
      const basic_string<typename iterator_traits<BiIt>::value_type, ST, SA>& rhs);
  template<class BiIt, class ST, class SA>
    auto operator<=>(
      const sub_match<BiIt>& lhs,
      const basic_string<typename iterator_traits<BiIt>::value_type, ST, SA>& rhs);
 
  template<class BiIt>
    bool operator==(const sub_match<BiIt>& lhs,
                    const typename iterator_traits<BiIt>::value_type* rhs);
  template<class BiIt>
    auto operator<=>(const sub_match<BiIt>& lhs,
                     const typename iterator_traits<BiIt>::value_type* rhs);
 
  template<class BiIt>
    bool operator==(const sub_match<BiIt>& lhs,
                    const typename iterator_traits<BiIt>::value_type& rhs);
  template<class BiIt>
    auto operator<=>(const sub_match<BiIt>& lhs,
                     const typename iterator_traits<BiIt>::value_type& rhs);
 
  template<class CharT, class ST, class BiIt>
    basic_ostream<CharT, ST>&
      operator<<(basic_ostream<CharT, ST>& os, const sub_match<BiIt>& m);
 
  // class template match_results
  template<class BiIt,
           class Allocator = allocator<sub_match<BiIt>>>
    class match_results;
 
  using cmatch  = match_results<const char*>;
  using wcmatch = match_results<const wchar_t*>;
  using smatch  = match_results<string::const_iterator>;
  using wsmatch = match_results<wstring::const_iterator>;
 
  // match_results comparisons
  template<class BiIt, class Allocator>
    bool operator==(const match_results<BiIt, Allocator>& m1,
                    const match_results<BiIt, Allocator>& m2);
 
  // match_results swap
  template<class BiIt, class Allocator>
    void swap(match_results<BiIt, Allocator>& m1, match_results<BiIt, Allocator>& m2);
 
  // function template regex_match
  template<class BiIt, class Allocator, class CharT, class Traits>
    bool regex_match(BiIt first, BiIt last,
                     match_results<BiIt, Allocator>& m,
                     const basic_regex<CharT, Traits>& e,
                     regex_constants::match_flag_type flags =
                       regex_constants::match_default);
  template<class BiIt, class CharT, class Traits>
    bool regex_match(BiIt first, BiIt last,
                     const basic_regex<CharT, Traits>& e,
                     regex_constants::match_flag_type flags =
                       regex_constants::match_default);
  template<class CharT, class Allocator, class Traits>
    bool regex_match(const CharT* str, match_results<const CharT*, Allocator>& m,
                     const basic_regex<CharT, Traits>& e,
                     regex_constants::match_flag_type flags =
                       regex_constants::match_default);
  template<class ST, class SA, class Allocator, class CharT, class Traits>
    bool regex_match(const basic_string<CharT, ST, SA>& s,
                     match_results<typename basic_string<CharT, ST, SA>::const_iterator,
                                   Allocator>& m,
                     const basic_regex<CharT, Traits>& e,
                     regex_constants::match_flag_type flags =
                       regex_constants::match_default);
  template<class ST, class SA, class Allocator, class CharT, class Traits>
    bool regex_match(const basic_string<CharT, ST, SA>&&,
                     match_results<typename basic_string<CharT, ST, SA>::const_iterator,
                                   Allocator>&,
                     const basic_regex<CharT, Traits>&,
                     regex_constants::match_flag_type =
                       regex_constants::match_default) = delete;
  template<class CharT, class Traits>
    bool regex_match(const CharT* str,
                     const basic_regex<CharT, Traits>& e,
                     regex_constants::match_flag_type flags =
                       regex_constants::match_default);
  template<class ST, class SA, class CharT, class Traits>
    bool regex_match(const basic_string<CharT, ST, SA>& s,
                     const basic_regex<CharT, Traits>& e,
                     regex_constants::match_flag_type flags =
                       regex_constants::match_default);
 
  // function template regex_search
  template<class BiIt, class Allocator, class CharT, class Traits>
    bool regex_search(BiIt first, BiIt last,
                      match_results<BiIt, Allocator>& m,
                      const basic_regex<CharT, Traits>& e,
                      regex_constants::match_flag_type flags =
                        regex_constants::match_default);
  template<class BiIt, class CharT, class Traits>
    bool regex_search(BiItfirst, BiIt last,
                      const basic_regex<CharT, Traits>& e,
                      regex_constants::match_flag_type flags =
                        regex_constants::match_default);
  template<class CharT, class Allocator, class Traits>
    bool regex_search(const CharT* str,
                      match_results<const CharT*, Allocator>& m,
                      const basic_regex<CharT, Traits>& e,
                      regex_constants::match_flag_type flags =
                        regex_constants::match_default);
  template<class CharT, class Traits>
    bool regex_search(const CharT* str,
                      const basic_regex<CharT, Traits>& e,
                      regex_constants::match_flag_type flags =
                        regex_constants::match_default);
  template<class ST, class SA, class CharT, class Traits>
    bool regex_search(const basic_string<CharT, ST, SA>& s,
                      const basic_regex<CharT, Traits>& e,
                      regex_constants::match_flag_type flags =
                        regex_constants::match_default);
  template<class ST, class SA, class Allocator, class CharT, class Traits>
    bool regex_search(const basic_string<CharT, ST, SA>& s,
                      match_results<typename basic_string<CharT, ST, SA>::const_iterator,
                                    Allocator>& m,
                      const basic_regex<CharT, Traits>& e,
                      regex_constants::match_flag_type flags =
                        regex_constants::match_default);
  template<class ST, class SA, class Allocator, class CharT, class Traits>
    bool regex_search(const basic_string<CharT, ST, SA>&&,
                      match_results<typename basic_string<CharT, ST, SA>::const_iterator,
                                    Allocator>&,
                      const basic_regex<CharT, Traits>&,
                      regex_constants::match_flag_type
                        = regex_constants::match_default) = delete;
 
  // function template regex_replace
  template<class OutputIt, class BiIt,
            class Traits, class CharT, class ST, class SA>
    OutputIt
      regex_replace(OutputIt out,
                    BiIt first, BiIt last,
                    const basic_regex<CharT, Traits>& e,
                    const basic_string<CharT, ST, SA>& fmt,
                    regex_constants::match_flag_type flags =
                      regex_constants::match_default);
  template<class OutputIt, class BiIt, class Traits, class CharT>
    OutputIt
      regex_replace(OutputIt out,
                    BiIt first, BiIt last,
                    const basic_regex<CharT, Traits>& e,
                    const CharT* fmt,
                    regex_constants::match_flag_type flags =
                      regex_constants::match_default);
  template<class Traits, class CharT, class ST, class SA, class FST, class FSA>
    basic_string<CharT, ST, SA>
      regex_replace(const basic_string<CharT, ST, SA>& s,
                    const basic_regex<CharT, Traits>& e,
                    const basic_string<CharT, FST, FSA>& fmt,
                    regex_constants::match_flag_type flags =
                      regex_constants::match_default);
  template<class Traits, class CharT, class ST, class SA>
    basic_string<CharT, ST, SA>
      regex_replace(const basic_string<CharT, ST, SA>& s,
                    const basic_regex<CharT, Traits>& e,
                    const CharT* fmt,
                    regex_constants::match_flag_type flags =
                      regex_constants::match_default);
  template<class Traits, class CharT, class ST, class SA>
    basic_string<CharT>
      regex_replace(const CharT* s,
                    const basic_regex<CharT, Traits>& e,
                    const basic_string<CharT, ST, SA>& fmt,
                    regex_constants::match_flag_type flags =
                      regex_constants::match_default);
  template<class Traits, class CharT>
    basic_string<CharT>
      regex_replace(const CharT* s,
                    const basic_regex<CharT, Traits>& e,
                    const CharT* fmt,
                    regex_constants::match_flag_type flags =
                      regex_constants::match_default);
 
  // class template regex_iterator
  template<class BiIt,
            class CharT = typename iterator_traits<BiIt>::value_type,
            class Traits = regex_traits<CharT>>
    class regex_iterator;
 
  using cregex_iterator  = regex_iterator<const char*>;
  using wcregex_iterator = regex_iterator<const wchar_t*>;
  using sregex_iterator  = regex_iterator<string::const_iterator>;
  using wsregex_iterator = regex_iterator<wstring::const_iterator>;
 
  // class template regex_token_iterator
  template<class BiIt,
            class CharT = typename iterator_traits<BiIt>::value_type,
            class Traits = regex_traits<CharT>>
    class regex_token_iterator;
 
  using cregex_token_iterator  = regex_token_iterator<const char*>;
  using wcregex_token_iterator = regex_token_iterator<const wchar_t*>;
  using sregex_token_iterator  = regex_token_iterator<string::const_iterator>;
  using wsregex_token_iterator = regex_token_iterator<wstring::const_iterator>;
 
  namespace pmr {
    template<class BiIt>
      using match_results =
        std::match_results<BiIt, polymorphic_allocator<sub_match<BiIt>>>;
 
    using cmatch  = match_results<const char*>;
    using wcmatch = match_results<const wchar_t*>;
    using smatch  = match_results<string::const_iterator>;
    using wsmatch = match_results<wstring::const_iterator>;
  }
}

```

#### Bitmask type std::regex_constants::syntax_option_type

```
namespace std::regex_constants {
  using syntax_option_type = /*T1*/;
  inline constexpr syntax_option_type icase = /* unspecified */;
  inline constexpr syntax_option_type nosubs = /* unspecified */;
  inline constexpr syntax_option_type optimize = /* unspecified */;
  inline constexpr syntax_option_type collate = /* unspecified */;
  inline constexpr syntax_option_type ECMAScript = /* unspecified */;
  inline constexpr syntax_option_type basic = /* unspecified */;
  inline constexpr syntax_option_type extended = /* unspecified */;
  inline constexpr syntax_option_type awk = /* unspecified */;
  inline constexpr syntax_option_type grep = /* unspecified */;
  inline constexpr syntax_option_type egrep = /* unspecified */;
  inline constexpr syntax_option_type multiline = /* unspecified */;
}

```

#### Bitmask type std::regex_constants::match_flag_type

```
namespace std::regex_constants {
  using match_flag_type = /*T2*/;
  inline constexpr match_flag_type match_default = {};
  inline constexpr match_flag_type match_not_bol = /* unspecified */;
  inline constexpr match_flag_type match_not_eol = /* unspecified */;
  inline constexpr match_flag_type match_not_bow = /* unspecified */;
  inline constexpr match_flag_type match_not_eow = /* unspecified */;
  inline constexpr match_flag_type match_any = /* unspecified */;
  inline constexpr match_flag_type match_not_null = /* unspecified */;
  inline constexpr match_flag_type match_continuous = /* unspecified */;
  inline constexpr match_flag_type match_prev_avail = /* unspecified */;
  inline constexpr match_flag_type format_default = {};
  inline constexpr match_flag_type format_sed = /* unspecified */;
  inline constexpr match_flag_type format_no_copy = /* unspecified */;
  inline constexpr match_flag_type format_first_only = /* unspecified */;
}

```

#### Enumerated type std::regex_constants::error_type

```
namespace std::regex_constants {
  using error_type = /*T3*/;
  inline constexpr error_type error_collate = /* unspecified */;
  inline constexpr error_type error_ctype = /* unspecified */;
  inline constexpr error_type error_escape = /* unspecified */;
  inline constexpr error_type error_backref = /* unspecified */;
  inline constexpr error_type error_brack = /* unspecified */;
  inline constexpr error_type error_paren = /* unspecified */;
  inline constexpr error_type error_brace = /* unspecified */;
  inline constexpr error_type error_badbrace = /* unspecified */;
  inline constexpr error_type error_range = /* unspecified */;
  inline constexpr error_type error_space = /* unspecified */;
  inline constexpr error_type error_badrepeat = /* unspecified */;
  inline constexpr error_type error_complexity = /* unspecified */;
  inline constexpr error_type error_stack = /* unspecified */;
}

```

#### Class std::regex_error

```
namespace std {
  class regex_error : public runtime_error {
  public:
    explicit regex_error(regex_constants::error_type ecode);
    regex_constants::error_type code() const;
  };
}

```

#### Class template std::regex_traits

```
namespace std {
  template<class CharT>
    struct regex_traits {
      using char_type       = CharT;
      using string_type     = basic_string<char_type>;
      using locale_type     = locale;
      using char_class_type = /* bitmask-type */;
 
      regex_traits();
      static size_t length(const char_type* p);
      CharT translate(CharT c) const;
      CharT translate_nocase(CharT c) const;
      template<class ForwardIt>
        string_type transform(ForwardIt first, ForwardIt last) const;
      template<class ForwardIt>
        string_type transform_primary(ForwardIt first, ForwardIt last) const;
      template<class ForwardIt>
        string_type lookup_collatename(ForwardIt first, ForwardIt last) const;
      template<class ForwardIt>
        char_class_type lookup_classname(ForwardIt first, ForwardIt last,
                                         bool icase = false) const;
      bool isctype(CharT c, char_class_type f) const;
      int value(CharT ch, int radix) const;
      locale_type imbue(locale_type l);
      locale_type getloc() const;
    };
}

```

#### Class template std::basic_regex

```
namespace std {
  template<class CharT, class Traits = regex_traits<CharT>>
    class basic_regex {
    public:
      // types
      using value_type  =          CharT;
      using Traits_type =          Traits;
      using string_type = typename Traits::string_type;
      using flag_type   =          regex_constants::syntax_option_type;
      using locale_type = typename Traits::locale_type;
 
      // constants
      static constexpr flag_type icase = regex_constants::icase;
      static constexpr flag_type nosubs = regex_constants::nosubs;
      static constexpr flag_type optimize = regex_constants::optimize;
      static constexpr flag_type collate = regex_constants::collate;
      static constexpr flag_type ECMAScript = regex_constants::ECMAScript;
      static constexpr flag_type basic = regex_constants::basic;
      static constexpr flag_type extended = regex_constants::extended;
      static constexpr flag_type awk = regex_constants::awk;
      static constexpr flag_type grep = regex_constants::grep;
      static constexpr flag_type egrep = regex_constants::egrep;
      static constexpr flag_type multiline = regex_constants::multiline;
 
      // construct/copy/destroy
      basic_regex();
      explicit basic_regex(const CharT* p, flag_type f = regex_constants::ECMAScript);
      basic_regex(const CharT* p, size_t len, flag_type f = regex_constants::ECMAScript);
      basic_regex(const basic_regex&);
      basic_regex(basic_regex&&) noexcept;
      template<class ST, class SA>
        explicit basic_regex(const basic_string<CharT, ST, SA>& s,
                             flag_type f = regex_constants::ECMAScript);
      template<class ForwardIt>
        basic_regex(ForwardIt first, ForwardIt last,
                    flag_type f = regex_constants::ECMAScript);
      basic_regex(initializer_list<CharT> il, flag_type f = regex_constants::ECMAScript);
 
      ~basic_regex();
 
      // assign
      basic_regex& operator=(const basic_regex& e);
      basic_regex& operator=(basic_regex&& e) noexcept;
      basic_regex& operator=(const CharT* p);
      basic_regex& operator=(initializer_list<CharT> il);
      template<class ST, class SA>
        basic_regex& operator=(const basic_string<CharT, ST, SA>& s);
 
      basic_regex& assign(const basic_regex& e);
      basic_regex& assign(basic_regex&& e) noexcept;
      basic_regex& assign(const CharT* p, flag_type f = regex_constants::ECMAScript);
      basic_regex& assign(const CharT* p, size_t len,
                          flag_type f = regex_constants::ECMAScript);
      template<class ST, class SA>
        basic_regex& assign(const basic_string<CharT, ST, SA>& s,
                            flag_type f = regex_constants::ECMAScript);
      template<class InputIt>
        basic_regex& assign(InputIt first, InputIt last,
                            flag_type f = regex_constants::ECMAScript);
      basic_regex& assign(initializer_list<CharT>,
                          flag_type f = regex_constants::ECMAScript);
 
      // const operations
      unsigned mark_count() const;
      flag_type flags() const;
 
      // locale
      locale_type imbue(locale_type loc);
      locale_type getloc() const;
 
      // swap
      void swap(basic_regex&);
    };
 
  template<class ForwardIt>
    basic_regex(ForwardIt, ForwardIt,
                regex_constants::syntax_option_type = regex_constants::ECMAScript)
      -> basic_regex<typename iterator_traits<ForwardIt>::value_type>;
}

```

#### Class template std::sub_match

```
namespace std {
  template<class BiIt>
    class sub_match : public pair<BiIt, BiIt> {
    public:
      using value_type      = typename iterator_traits<BiIt>::value_type;
      using difference_type = typename iterator_traits<BiIt>::difference_type;
      using iterator        = BiIt;
      using string_type     = basic_string<value_type>;
 
      bool matched;
 
      constexpr sub_match();
 
      difference_type length() const;
      operator string_type() const;
      string_type str() const;
 
      int compare(const sub_match& s) const;
      int compare(const string_type& s) const;
      int compare(const value_type* s) const;
 
      void swap(sub_match& s) noexcept(/* see description */);
    };
}

```

#### Class template std::match_results

```
namespace std {
  template<class BiIt,
           class Allocator = allocator<sub_match<BiIt>>>
    class match_results {
    public:
      using value_type      = sub_match<BiIt>;
      using const_reference = const value_type&;
      using reference       = value_type&;
      using const_iterator  = /* implementation-defined */;
      using iterator        = const_iterator;
      using difference_type = typename iterator_traits<BiIt>::difference_type;
      using size_type       = typename allocator_traits<Allocator>::size_type;
      using allocator_type  = Allocator;
      using char_type       = typename iterator_traits<BiIt>::value_type;
      using string_type     = basic_string<char_type>;
 
      // construct/copy/destroy
      match_results() : match_results(Allocator()) {}
      explicit match_results(const Allocator& a);
      match_results(const match_results& m);
      match_results(const match_results& m, const Allocator& a);
      match_results(match_results&& m) noexcept;
      match_results(match_results&& m, const Allocator& a);
      match_results& operator=(const match_results& m);
      match_results& operator=(match_results&& m);
      ~match_results();
 
      // state
      bool ready() const;
 
      // size
      size_type size() const;
      size_type max_size() const;
      bool empty() const;
 
      // element access
      difference_type length(size_type sub = 0) const;
      difference_type position(size_type sub = 0) const;
      string_type str(size_type sub = 0) const;
      const_reference operator[](size_type n) const;
 
      const_reference prefix() const;
      const_reference suffix() const;
      const_iterator begin() const;
      const_iterator end() const;
      const_iterator cbegin() const;
      const_iterator cend() const;
 
      // format
      template<class OutputIt>
        OutputIt
          format(OutputIt out,
                 const char_type* fmt_first, const char_type* fmt_last,
                 regex_constants::match_flag_type flags =
                   regex_constants::format_default) const;
      template<class OutputIt, class ST, class SA>
        OutputIt
          format(OutputIt out,
                 const basic_string<char_type, ST, SA>& fmt,
                 regex_constants::match_flag_type flags =
                   regex_constants::format_default) const;
      template<class ST, class SA>
        basic_string<char_type, ST, SA>
          format(const basic_string<char_type, ST, SA>& fmt,
                 regex_constants::match_flag_type flags =
                   regex_constants::format_default) const;
      string_type
        format(const char_type* fmt,
               regex_constants::match_flag_type flags =
                 regex_constants::format_default) const;
 
      // allocator
      allocator_type get_allocator() const;
 
      // swap
      void swap(match_results& that);
    };
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/regex&oldid=179092>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 20:59.