# std::filesystem::filesystem_error::path1, std::filesystem::filesystem_error::path2

From cppreference.com
< cpp‎ | filesystem‎ | filesystem error
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | filesystem::perms | | | | | | filesystem::perm_options | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

filesystem_error

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| filesystem_error::filesystem_error | | | | |
| filesystem_error::operator= | | | | |
| ****filesystem_error::path1filesystem_error::path2**** | | | | |
| filesystem_error::what | | | | |
| Inherited from std::system_error | | | | |
| system_error::code | | | | |

|  |  |  |
| --- | --- | --- |
| const std::filesystem::path& path1() const noexcept; |  | (since C++17) |
| const std::filesystem::path& path2() const noexcept; |  | (since C++17) |
|  |  |  |

Returns the paths that were stored in the exception object.

### Parameters

(none)

### Return value

References to the copy of the `path` parameters stored by the constructor.

### Example

Run this code

```
#include <cstdio>
#include <filesystem>
#include <iostream>
 
int main()
{
    const std::filesystem::path old_p{std::tmpnam(nullptr)},
                                new_p{std::tmpnam(nullptr)};
    try {
        std::filesystem::rename(old_p, new_p); // throws since old_p does not exist
    }
    catch(std::filesystem::filesystem_error const& ex) {
        std::cout
            << "what():  " << ex.what() << '\n'
            << "path1(): " << ex.path1() << '\n'
            << "path2(): " << ex.path2() << '\n';
    }
}

```

Possible output:

```
what():  filesystem error: cannot rename: No such file or directory [/tmp/fileIzzRLB] [/tmp/fileiUDWlV]
path1(): "/tmp/fileIzzRLB"
path2(): "/tmp/fileiUDWlV"

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/filesystem_error/path&oldid=128562>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 May 2021, at 16:11.