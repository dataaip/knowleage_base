# std::experimental::filesystem::begin(recursive_directory_iterator), std::experimental::filesystem::end(recursive_directory_iterator)

From cppreference.com
< cpp‎ | experimental‎ | fs‎ | recursive directory iterator
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
| Library fundamentals (library fundamentals TS) | | | | |
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

Filesystem library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

recursive_directory_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| recursive_directory_iterator::recursive_directory_iterator | | | | |
| recursive_directory_iterator::operator\*recursive_directory_iterator::operator-> | | | | |
| recursive_directory_iterator::options | | | | |
| recursive_directory_iterator::depth | | | | |
| recursive_directory_iterator::recursion_pending | | | | |
| recursive_directory_iterator::operator= | | | | |
| recursive_directory_iterator::incrementrecursive_directory_iterator::operator++ | | | | |
| recursive_directory_iterator::pop | | | | |
| recursive_directory_iterator::disable_recursion_pending | | | | |
| Non-member functions | | | | |
| ****begin(recursive_directory_iterator)end(recursive_directory_iterator)**** | | | | |

|  |  |  |
| --- | --- | --- |
| recursive_directory_iterator begin( recursive_directory_iterator iter ); | (1) | (filesystem TS) |
| recursive_directory_iterator end( const recursive_directory_iterator& ); | (2) | (filesystem TS) |
|  |  |  |

1) Returns iter unchanged.2) Returns a default-constructed recursive_directory_iterator, which serves as the end iterator. The argument is ignored.

These non-member functions enable the use of `recursive_directory_iterator`s with range-based for loops.

### Parameters

|  |  |  |
| --- | --- | --- |
| iter | - | a recursive_directory_iterator |

### Return value

1) iter unchanged.2) End iterator (default-constructed `recursive_directory_iterator`).

### Exceptions

noexcept specification:noexcept

### Example

Run this code

```
#include <experimental/filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::experimental::filesystem;
 
int main()
{
    fs::create_directories("sandbox/a/b");
    std::ofstream("sandbox/file1.txt");
    fs::create_symlink("a", "sandbox/syma");
    for (auto& p : fs::recursive_directory_iterator("sandbox"))
        std::cout << p << '\n';
    fs::remove_all("sandbox");
}

```

Possible output:

```
"sandbox/a"
"sandbox/a/b"
"sandbox/file1.txt"
"sandbox/syma"

```

### See also

|  |  |
| --- | --- |
| filesystem::begin(filesystem::directory_iterator)filesystem::end(filesystem::directory_iterator) | range-based for loop support   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/recursive_directory_iterator/begin&oldid=154917>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 July 2023, at 06:07.