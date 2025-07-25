# Experimental library header <experimental/filesystem>

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
| ****<experimental/filesystem>**** | | | | |
| Parallelism TS (v1, v2) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/algorithm` | | | | | | `experimental/execution_policy` | | | | | | `experimental/exception_list` | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `experimental/numeric` | | | | | | <experimental/simd> | | | | | | `experimental/task_block` | | | | | |
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

This header is part of the filesystem library.

|  |  |
| --- | --- |
| Defined in namespace `std::experimental::filesystem` | |
| Defined in inline namespace `std::experimental::filesystem::v1` | |
| Classes | |
| path | represents a path   (class) |
| filesystem_error | an exception thrown on file system errors   (class) |
| directory_entry | a directory entry   (class) |
| directory_iterator | an iterator to the contents of the directory   (class) |
| recursive_directory_iterator | an iterator to the contents of a directory and its subdirectories   (class) |
| file_status | represents file type and permissions   (class) |
| space_info | information about free and available space on the filesystem   (class) |
| file_type | the type of a file   (enum) |
| perms | identifies file system permissions   (enum) |
| copy_options | specifies semantics of copy operations   (enum) |
| directory_options | options for iterating directory contents   (enum) |
| file_time_type | represents file time values   (typedef) |
| Functions | |
| swap(std::experimental::filesystem::path) | swaps two paths   (function) |
| hash_value") | calculates a hash value for a path object   (function) |
| operator==operator!=operator<operator<=operator>operator>= | lexicographically compares two paths   (function) |
| operator/ | concatenates two paths with a directory separator   (function) |
| operator<<operator>> | performs stream input and output on a path   (function) |
| u8path | creates a `path` from a UTF-8 encoded source   (function) |
| filesystem::begin(filesystem::directory_iterator)filesystem::end(filesystem::directory_iterator) | range-based for loop support   (function) |
| filesystem::begin(filesystem::recursive_directory_iterator)filesystem::end(filesystem::recursive_directory_iterator) | range-based for loop support   (function) |
| absolutesystem_complete | composes an absolute path converts a path to an absolute path replicating OS-specific behavior   (function) |
| canonical | composes a canonical path   (function) |
| copy | copies files or directories   (function) |
| copy_file | copies file contents   (function) |
| copy_symlink | copies a symbolic link   (function) |
| create_directorycreate_directories | creates new directory   (function) |
| create_hard_link | creates a hard link   (function) |
| create_symlinkcreate_directory_symlink | creates a symbolic link   (function) |
| current_path | return current working directory   (function) |
| exists | checks whether path refers to existing file system object   (function) |
| equivalent | checks whether two paths refer to the same file system object   (function) |
| file_size | returns the size of a file   (function) |
| hard_link_count | returns the number of hard links referring to the specific file   (function) |
| last_write_time | gets or sets the time of the last data modification   (function) |
| permissions | modifies file access permissions   (function) |
| read_symlink | obtains the target of a symbolic link   (function) |
| removeremove_all | removes a file or empty directory removes a file or directory and all its contents, recursively   (function) |
| rename | moves or renames a file or directory   (function) |
| resize_file | changes the size of a regular file by truncation or zero-fill   (function) |
| space | determines available free space on the file system   (function) |
| statussymlink_status | determines file attributes determines file attributes, checking the symlink target   (function) |
| temp_directory_path | returns a directory suitable for temporary files   (function) |
| File types | |
| is_block_file | checks whether the given path refers to block device   (function) |
| is_character_file | checks whether the given path refers to a character device   (function) |
| is_directory | checks whether the given path refers to a directory   (function) |
| is_empty | checks whether the given path refers to an empty file or directory   (function) |
| is_fifo | checks whether the given path refers to a named pipe   (function) |
| is_other | checks whether the argument refers to an **other** file   (function) |
| is_regular_file | checks whether the argument refers to a regular file   (function) |
| is_socket | checks whether the argument refers to a named IPC socket   (function) |
| is_symlink | checks whether the argument refers to a symbolic link   (function) |
| status_known | checks whether file status is known   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/experimental/filesystem&oldid=112227>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 August 2019, at 03:26.