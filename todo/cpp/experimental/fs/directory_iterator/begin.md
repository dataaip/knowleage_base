# std::experimental::filesystem::begin(directory_iterator), std::experimental::filesystem::end(directory_iterator)

From cppreference.com
< cpp‎ | experimental‎ | fs‎ | directory iterator
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

Filesystem library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

directory_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| directory_iterator::directory_iterator | | | | |
| directory_iterator::operator\*directory_iterator::operator-> | | | | |
| directory_iterator::operator= | | | | |
| directory_iterator::incrementdirectory_iterator::operator++ | | | | |
| Non-member functions | | | | |
| ****begin(directory_iterator)end(directory_iterator)**** | | | | |

|  |  |  |
| --- | --- | --- |
| directory_iterator begin( directory_iterator iter ); | (1) | (filesystem TS) |
| directory_iterator end( const directory_iterator& ); | (2) | (filesystem TS) |
|  |  |  |

1) Returns iter unchanged.2) Returns a default-constructed directory_iterator, which serves as the end iterator. The argument is ignored.

These non-member functions enable the use of `directory_iterator`s with range-based for loops.

### Parameters

|  |  |  |
| --- | --- | --- |
| iter | - | a directory_iterator |

### Return value

1) iter unchanged.2) End iterator (default-constructed `directory_iterator`).

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
    std::ofstream("sandbox/file2.txt");
    for (auto& p : fs::directory_iterator("sandbox"))
        std::cout << p << '\n';
    fs::remove_all("sandbox");
}

```

Possible output:

```
"sandbox/a"
"sandbox/file1.txt"
"sandbox/file2.txt"

```

### See also

|  |  |
| --- | --- |
| filesystem::begin(filesystem::recursive_directory_iterator)filesystem::end(filesystem::recursive_directory_iterator) | range-based for loop support   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/directory_iterator/begin&oldid=154837>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 July 2023, at 00:51.