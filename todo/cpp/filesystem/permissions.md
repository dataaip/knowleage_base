# std::filesystem::permissions

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | ****filesystem::permissions**** | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| void permissions( const std::filesystem::path& p,  std::filesystem::perms prms, std::filesystem::perm_options opts = perm_options::replace ); | (1) | (since C++17) |
| void permissions( const std::filesystem::path& p,  std::filesystem::perms prms, std::error_code& ec ) noexcept; | (2) | (since C++17) |
| void permissions( const std::filesystem::path& p,  std::filesystem::perms prms,                    std::filesystem::perm_options opts, std::error_code& ec ); | (3) | (since C++17) |
|  |  |  |

Changes access permissions of the file to which p resolves, as if by POSIX `fchmodat`. Symlinks are followed unless `perm_options::nofollow` is set in opts.

The second signature behaves as if called with opts set to perm_options::replace.

The effects depend on prms and opts as follows:

- If opts is perm_options::replace, file permissions are set to exactly prms & std::filesystem::perms::mask (meaning, every valid bit of prms is applied).
- If opts is perm_options::add, the file permissions are set to exactly status(p).permissions() | (prms & perms::mask) (meaning, any valid bit that is set in prms, but not in the file's current permissions is added to the file's permissions).
- If opts is perm_options::remove, the file permissions are set to exactly status(p).permissions() & ~(prms & perms::mask) (meaning, any valid bit that is clear in prms, but set in the file's current permissions is cleared in the file's permissions).

opts is required to have only one of `replace`, `add`, or `remove` to be set.

The non-throwing overload has no special action on error.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | path to examine |
| prms | - | permissions to set, add, or remove |
| opts | - | options controlling the action taken by this function |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

(none)

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

1) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with p as the first path argument and the OS error code as the error code argument.2,3) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Notes

Permissions may not necessarily be implemented as bits, but they are treated that way conceptually.

Some permission bits may be ignored on some systems, and changing some bits may automatically change others (e.g. on platforms without owner/group/all distinction, setting any of the three write bits set all three).

### Example

Run this code

```
#include <filesystem>
#include <fstream>
#include <iostream>
 
void demo_perms(std::filesystem::perms p)
{
    using std::filesystem::perms;
    auto show = =
    {
        std::cout << (perms::none == (perm & p) ? '-' : op);
    };
    show('r', perms::owner_read);
    show('w', perms::owner_write);
    show('x', perms::owner_exec);
    show('r', perms::group_read);
    show('w', perms::group_write);
    show('x', perms::group_exec);
    show('r', perms::others_read);
    show('w', perms::others_write);
    show('x', perms::others_exec);
    std::cout << '\n';
}
 
int main()
{
    std::ofstream("test.txt"); // create file
 
    std::cout << "Created file with permissions: ";
    demo_perms(std::filesystem::status("test.txt").permissions());
 
    std::filesystem::permissions(
        "test.txt",
        std::filesystem::perms::owner_all | std::filesystem::perms::group_all,
        std::filesystem::perm_options::add
    );
 
    std::cout << "After adding u+rwx and g+rwx:  ";
    demo_perms(std::filesystem::status("test.txt").permissions());
 
    std::filesystem::remove("test.txt");
}

```

Possible output:

```
Created file with permissions: rw-r--r--
After adding u+rwx and g+wrx:  rwxrwxr--

```

### See also

|  |  |
| --- | --- |
| perms(C++17) | identifies file system permissions   (enum) |
| statussymlink_status(C++17)(C++17) | determines file attributes determines file attributes, checking the symlink target   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/permissions&oldid=157969>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2023, at 13:07.