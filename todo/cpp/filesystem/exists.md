# std::filesystem::exists

From cppreference.com
< cpp‎ | filesystem
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****filesystem::exists**** | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| bool exists( std::filesystem::file_status s ) noexcept; | (1) | (since C++17) |
| bool exists( const std::filesystem::path& p ); | (2) | (since C++17) |
| bool exists( const std::filesystem::path& p, std::error_code& ec ) noexcept; | (3) | (since C++17) |
|  |  |  |

Checks if the given file status or path corresponds to an existing file or directory.

1) Equivalent to status_known(s) && s.type() != file_type::not_found.2,3) Let s be a std::filesystem::file_status determined as if by status(p) or status(p, ec) (symlinks are followed), respectively. Returns exists(s). The non-throwing overload calls ec.clear() if status_known(s).

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | file status to check |
| p | - | path to examine |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

true if the given path or file status corresponds to an existing file or directory, false otherwise.

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

2) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with p as the first path argument and the OS error code as the error code argument.3) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

No filesystem exception is thrown if object does not exist (use return value).

### Notes

The information provided by this function is usually also provided as a byproduct of directory iteration. During directory iteration, calling exists(\*iterator) is less efficient than exists(iterator->status()).

### Example

Run this code

```
#include <cstdint>
#include <filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::filesystem;
 
void demo_exists(const fs::path& p, fs::file_status s = fs::file_status{})
{
    std::cout << p;
    if (fs::status_known(s) ? fs::exists(s) : fs::exists(p))
        std::cout << " exists\n";
    else
        std::cout << " does not exist\n";
}
 
int main()
{
    const fs::path sandbox{"sandbox"};
    fs::create_directory(sandbox);
    std::ofstream{sandbox/"file"}; // create regular file
    fs::create_symlink("non-existing", sandbox/"symlink");
 
    demo_exists(sandbox);
 
    for (const auto& entry : fs::directory_iterator(sandbox))
        demo_exists(entry, entry.status()); // use cached status from directory entry
 
    fs::remove_all(sandbox);
}

```

Output:

```
"sandbox" exists
"sandbox/symlink" does not exist
"sandbox/file" exists

```

### See also

|  |  |
| --- | --- |
| statussymlink_status(C++17)(C++17) | determines file attributes determines file attributes, checking the symlink target   (function) |
| file_status(C++17) | represents file type and permissions   (class) |
| exists | checks whether directory entry refers to existing file system object   (public member function of `std::filesystem::directory_entry`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/exists&oldid=159790>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 September 2023, at 23:21.