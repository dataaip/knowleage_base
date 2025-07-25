# Standard library header <cinttypes> (C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | ****<cinttypes>**** (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header was originally in the C standard library as <inttypes.h>.

|  |  |
| --- | --- |
| Includes | |
| <cstdint>(C++11) | Fixed-width integer types and limits of other types |
| Types | |
| imaxdiv_t(C++11) | structure type, returned by std::imaxdiv   (typedef) |
| Functions | |
| abs(std::intmax_t)imaxabs(C++11)(C++11) | computes absolute value of an integral value (\(\small{|x|}\)|x|)   (function) |
| div(std::intmax_t)imaxdiv(C++11)(C++11) | computes quotient and remainder of integer division   (function) |
| strtoimaxstrtoumax(C++11)(C++11) | converts a byte string to std::intmax_t or std::uintmax_t   (function) |
| wcstoimaxwcstoumax(C++11)(C++11) | converts a wide string to std::intmax_t or std::uintmax_t   (function) |
| Macros | |
| Format constants for the std::fprintf family of functions | |
| PRId8PRId16PRId32PRId64PRIdLEAST8PRIdLEAST16PRIdLEAST32PRIdLEAST64PRIdFAST8PRIdFAST16PRIdFAST32PRIdFAST64PRIdMAXPRIdPTR(C++11) | format conversion specifier to output a signed decimal integer value of type std::int8_t, std::int16_t, std::int32_t, std::int64_t, std::int_least8_t, std::int_least16_t, std::int_least32_t, std::int_least64_t, std::int_fast8_t, std::int_fast16_t, std::int_fast32_t, std::int_fast64_t, std::intmax_t, std::intptr_t respectively, equivalent to `d` for int   (macro constant) |
| PRIi8PRIi16PRIi32PRIi64PRIiLEAST8PRIiLEAST16PRIiLEAST32PRIiLEAST64PRIiFAST8PRIiFAST16PRIiFAST32PRIiFAST64PRIiMAXPRIiPTR(C++11) | format conversion specifier to output a signed decimal integer value of type std::int8_t, std::int16_t, std::int32_t, std::int64_t, std::int_least8_t, std::int_least16_t, std::int_least32_t, std::int_least64_t, std::int_fast8_t, std::int_fast16_t, std::int_fast32_t, std::int_fast64_t, std::intmax_t, std::intptr_t respectively, equivalent to `i` for int   (macro constant) |
| PRIu8PRIu16PRIu32PRIu64PRIuLEAST8PRIuLEAST16PRIuLEAST32PRIuLEAST64PRIuFAST8PRIuFAST16PRIuFAST32PRIuFAST64PRIuMAXPRIuPTR(C++11) | format conversion specifier to output an unsigned decimal integer value of type std::uint8_t, std::uint16_t, std::uint32_t, std::uint64_t, std::uint_least8_t, std::uint_least16_t, std::uint_least32_t, std::uint_least64_t, std::uint_fast8_t, std::uint_fast16_t, std::uint_fast32_t, std::uint_fast64_t, std::uintmax_t, std::uintptr_t respectively, equivalent to `u` for unsigned int   (macro constant) |
| PRIo8PRIo16PRIo32PRIo64PRIoLEAST8PRIoLEAST16PRIoLEAST32PRIoLEAST64PRIoFAST8PRIoFAST16PRIoFAST32PRIoFAST64PRIoMAXPRIoPTR(C++11) | format conversion specifier to output an unsigned octal integer value of type std::uint8_t, std::uint16_t, std::uint32_t, std::uint64_t, std::uint_least8_t, std::uint_least16_t, std::uint_least32_t, std::uint_least64_t, std::uint_fast8_t, std::uint_fast16_t, std::uint_fast32_t, std::uint_fast64_t, std::uintmax_t, std::uintptr_t respectively, equivalent to `o` for unsigned int   (macro constant) |
| PRIx8PRIx16PRIx32PRIx64PRIxLEAST8PRIxLEAST16PRIxLEAST32PRIxLEAST64PRIxFAST8PRIxFAST16PRIxFAST32PRIxFAST64PRIxMAXPRIxPTR(C++11) | format conversion specifier to output an unsigned lowercase hexadecimal integer value of type std::uint8_t, std::uint16_t, std::uint32_t, std::uint64_t, std::uint_least8_t, std::uint_least16_t, std::uint_least32_t, std::uint_least64_t, std::uint_fast8_t, std::uint_fast16_t, std::uint_fast32_t, std::uint_fast64_t, std::uintmax_t, std::uintptr_t respectively, equivalent to `x` for unsigned int   (macro constant) |
| PRIX8PRIX16PRIX32PRIX64PRIXLEAST8PRIXLEAST16PRIXLEAST32PRIXLEAST64PRIXFAST8PRIXFAST16PRIXFAST32PRIXFAST64PRIXMAXPRIXPTR(C++11) | format conversion specifier to output an unsigned uppercase hexadecimal integer value of type std::uint8_t, std::uint16_t, std::uint32_t, std::uint64_t, std::uint_least8_t, std::uint_least16_t, std::uint_least32_t, std::uint_least64_t, std::uint_fast8_t, std::uint_fast16_t, std::uint_fast32_t, std::uint_fast64_t, std::uintmax_t, std::uintptr_t respectively, equivalent to `X` for unsigned int   (macro constant) |
| Format constants for the std::fscanf family of functions | |
| SCNd8SCNd16SCNd32SCNd64SCNdLEAST8SCNdLEAST16SCNdLEAST32SCNdLEAST64SCNdFAST8SCNdFAST16SCNdFAST32SCNdFAST64SCNdMAXSCNdPTR(C++11) | format conversion specifier to input a signed decimal integer value of type std::int8_t, std::int16_t, std::int32_t, std::int64_t, std::int_least8_t, std::int_least16_t, std::int_least32_t, std::int_least64_t, std::int_fast8_t, std::int_fast16_t, std::int_fast32_t, std::int_fast64_t, std::intmax_t, std::intptr_t respectively, equivalent to `d` for int   (macro constant) |
| SCNi8SCNi16SCNi32SCNi64SCNiLEAST8SCNiLEAST16SCNiLEAST32SCNiLEAST64SCNiFAST8SCNiFAST16SCNiFAST32SCNiFAST64SCNiMAXSCNiPTR(C++11) | format conversion specifier to input a signed decimal/octal/hexadecimal integer value of type std::int8_t, std::int16_t, std::int32_t, std::int64_t, std::int_least8_t, std::int_least16_t, std::int_least32_t, std::int_least64_t, std::int_fast8_t, std::int_fast16_t, std::int_fast32_t, std::int_fast64_t, std::intmax_t, std::intptr_t respectively, equivalent to `i` for int   (macro constant) |
| SCNu8SCNu16SCNu32SCNu64SCNuLEAST8SCNuLEAST16SCNuLEAST32SCNuLEAST64SCNuFAST8SCNuFAST16SCNuFAST32SCNuFAST64SCNuMAXSCNuPTR(C++11) | format conversion specifier to input an unsigned decimal integer value of type std::uint8_t, std::uint16_t, std::uint32_t, std::uint64_t, std::uint_least8_t, std::uint_least16_t, std::uint_least32_t, std::uint_least64_t, std::uint_fast8_t, std::uint_fast16_t, std::uint_fast32_t, std::uint_fast64_t, std::uintmax_t, std::uintptr_t respectively, equivalent to `u` for unsigned int   (macro constant) |
| SCNo8SCNo16SCNo32SCNo64SCNoLEAST8SCNoLEAST16SCNoLEAST32SCNoLEAST64SCNoFAST8SCNoFAST16SCNoFAST32SCNoFAST64SCNoMAXSCNoPTR(C++11) | format conversion specifier to input an unsigned octal integer value of type std::uint8_t, std::uint16_t, std::uint32_t, std::uint64_t, std::uint_least8_t, std::uint_least16_t, std::uint_least32_t, std::uint_least64_t, std::uint_fast8_t, std::uint_fast16_t, std::uint_fast32_t, std::uint_fast64_t, std::uintmax_t, std::uintptr_t respectively, equivalent to `o` for unsigned int   (macro constant) |
| SCNx8SCNx16SCNx32SCNx64SCNxLEAST8SCNxLEAST16SCNxLEAST32SCNxLEAST64SCNxFAST8SCNxFAST16SCNxFAST32SCNxFAST64SCNxMAXSCNxPTR(C++11) | format conversion specifier to input an unsigned hexadecimal integer value of type std::uint8_t, std::uint16_t, std::uint32_t, std::uint64_t, std::uint_least8_t, std::uint_least16_t, std::uint_least32_t, std::uint_least64_t, std::uint_fast8_t, std::uint_fast16_t, std::uint_fast32_t, std::uint_fast64_t, std::uintmax_t, std::uintptr_t respectively, equivalent to `x` for unsigned int   (macro constant) |

### Synopsis

```
#include <cstdint>
 
namespace std
{
    using imaxdiv_t = /* see description */;
 
    constexpr intmax_t imaxabs(intmax_t j);
    constexpr imaxdiv_t imaxdiv(intmax_t numer, intmax_t denom);
    intmax_t strtoimax(const char* nptr, char** endptr, int base);
    uintmax_t strtoumax(const char* nptr, char** endptr, int base);
    intmax_t wcstoimax(const wchar_t* nptr, wchar_t** endptr, int base);
    uintmax_t wcstoumax(const wchar_t* nptr, wchar_t** endptr, int base);
 
    constexpr intmax_t abs(intmax_t);            // optional, see description
    constexpr imaxdiv_t div(intmax_t, intmax_t); // optional, see description
}
 
#define PRIdN /* see description */
#define PRIiN /* see description */
#define PRIoN /* see description */
#define PRIuN /* see description */
#define PRIxN /* see description */
#define PRIXN /* see description */
#define SCNdN /* see description */
#define SCNiN /* see description */
#define SCNoN /* see description */
#define SCNuN /* see description */
#define SCNxN /* see description */
#define PRIdLEASTN /* see description */
#define PRIiLEASTN /* see description */
#define PRIoLEASTN /* see description */
#define PRIuLEASTN /* see description */
#define PRIxLEASTN /* see description */
#define PRIXLEASTN /* see description */
#define SCNdLEASTN /* see description */
#define SCNiLEASTN /* see description */
#define SCNoLEASTN /* see description */
#define SCNuLEASTN /* see description */
#define SCNxLEASTN /* see description */
#define PRIdFASTN /* see description */
#define PRIiFASTN /* see description */
#define PRIoFASTN /* see description */
#define PRIuFASTN /* see description */
#define PRIxFASTN /* see description */
#define PRIXFASTN /* see description */
#define SCNdFASTN /* see description */
#define SCNiFASTN /* see description */
#define SCNoFASTN /* see description */
#define SCNuFASTN /* see description */
#define SCNxFASTN /* see description */
#define PRIdMAX /* see description */
#define PRIiMAX /* see description */
#define PRIoMAX /* see description */
#define PRIuMAX /* see description */
#define PRIxMAX /* see description */
#define PRIXMAX /* see description */
#define SCNdMAX /* see description */
#define SCNiMAX /* see description */
#define SCNoMAX /* see description */
#define SCNuMAX /* see description */
#define SCNxMAX /* see description */
#define PRIdPTR /* see description */
#define PRIiPTR /* see description */
#define PRIoPTR /* see description */
#define PRIuPTR /* see description */
#define PRIxPTR /* see description */
#define PRIXPTR /* see description */
#define SCNdPTR /* see description */
#define SCNiPTR /* see description */
#define SCNoPTR /* see description */
#define SCNuPTR /* see description */
#define SCNxPTR /* see description */

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/cinttypes&oldid=156553>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 August 2023, at 13:37.