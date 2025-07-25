# std::filesystem::rename

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | ****filesystem::rename**** | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| void rename( const std::filesystem::path& old_p,               const std::filesystem::path& new_p ); | (1) | (since C++17) |
| void rename( const std::filesystem::path& old_p,  const std::filesystem::path& new_p, std::error_code& ec ) noexcept; | (2) | (since C++17) |
|  |  |  |

Moves or renames the filesystem object identified by old_p to new_p as if by the POSIX `rename`:

- If old_p is a non-directory file, then new_p must be one of:

:   - the same file as old_p or a hardlink to it: nothing is done in this case.
    - existing non-directory file: new_p is first deleted, then, without allowing other processes to observe new_p as deleted, the pathname new_p is linked to the file and old_p is unlinked from the file. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.
    - non-existing file in an existing directory: The pathname new_p is linked to the file and old_p is unlinked from the file. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.

- If old_p is a directory, then new_p must be one of:

:   - the same directory as old_p or a hardlink to it: nothing is done in this case.
    - existing directory: new_p is deleted if empty on POSIX systems, but this may be an error on other systems. If not an error, then new_p is first deleted, then, without allowing other processes to observe new_p as deleted, the pathname new_p is linked to the directory and old_p is unlinked from the directory. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.
    - non-existing directory, not ending with a directory separator, and whose parent directory exists: The pathname new_p is linked to the directory and old_p is unlinked from the directory. Write permissions are required to both the directory that contains old_p and the directory that contains new_p.

- Symlinks are not followed: if old_p is a symlink, it is itself renamed, not its target. If new_p is an existing symlink, it is itself erased, not its target.

Rename fails if

- new_p ends with dot or with dot-dot.
- new_p names a non-existing directory ending with a directory separator.
- old_p is a directory which is an ancestor of new_p.

### Parameters

|  |  |  |
| --- | --- | --- |
| old_p | - | path to move or rename |
| new_p | - | target path for the move/rename operation |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

(none)

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

1) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with old_p as the first path argument, new_p as the second path argument, and the OS error code as the error code argument.2) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Example

Run this code

```
#include <filesystem>
#include <fstream>
namespace fs = std::filesystem;
 
int main()
{
    std::filesystem::path p = std::filesystem::current_path() / "sandbox";
    std::filesystem::create_directories(p / "from");
    std::ofstream{ p / "from/file1.txt" }.put('a');
    std::filesystem::create_directory(p / "to");
 
//  fs::rename(p / "from/file1.txt", p / "to/"); // error: "to" is a directory
    fs::rename(p / "from/file1.txt", p / "to/file2.txt"); // OK
//  fs::rename(p / "from", p / "to"); // error: "to" is not empty
    fs::rename(p / "from", p / "to/subdir"); // OK
 
    std::filesystem::remove_all(p);
}

```

### See also

|  |  |
| --- | --- |
| rename | renames a file   (function) |
| removeremove_all(C++17)(C++17) | removes a file or empty directory removes a file or directory and all its contents, recursively   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/rename&oldid=158974>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2023, at 09:34.