# std::experimental::filesystem::perms

From cppreference.com
< cpp‎ | experimental‎ | fs
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | ****filesystem::perms**** | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute filesystem::system_complete | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/filesystem>` |  |  |
| enum class perms; |  | (filesystem TS) |
|  |  |  |

This type represents file access permissions. `perms` satisfies the requirements of BitmaskType (which means the bitwise operators operator&, operator|, operator^, operator~, operator&=, operator|=, and operator^= are defined for this type).

Access permissions model POSIX permission bits, and any individual file permissions (as reported by status) are a combination of some of the following bits:

### Member constants

| Member constant | Value (octal) | POSIX equivalent | Meaning |
| --- | --- | --- | --- |
| `none` | ​0​ |  | No permission bits are set |
| `owner_read` | 0400 | S_IRUSR | File owner has read permission |
| `owner_write` | 0200 | S_IWUSR | File owner has write permission |
| `owner_exec` | 0100 | S_IXUSR | File owner has execute/search permission |
| `owner_all` | 0700 | S_IRWXU | File owner has read, write, and execute/search permissions Equivalent to owner_read | owner_write | owner_exec |
| `group_read` | 040 | S_IRGRP | The file's user group has read permission |
| `group_write` | 020 | S_IWGRP | The file's user group has write permission |
| `group_exec` | 010 | S_IXGRP | The file's user group has execute/search permission |
| `group_all` | 070 | S_IRWXG | The file's user group has read, write, and execute/search permissions Equivalent to group_read | group_write | group_exec |
| `others_read` | 04 | S_IROTH | Other users have read permission |
| `others_write` | 02 | S_IWOTH | Other users have write permission |
| `others_exec` | 01 | S_IXOTH | Other users have execute/search permission |
| `others_all` | 07 | S_IRWXO | Other users have read, write, and execute/search permissions Equivalent to others_read | others_write | others_exec |
| `all` | 0777 |  | All users have read, write, and execute/search permissions Equivalent to owner_all | group_all | others_all |
| `set_uid` | 04000 | S_ISUID | Set user ID to file owner user ID on execution |
| `set_gid` | 02000 | S_ISGID | Set group ID to file's user group ID on execution |
| `sticky_bit` | 01000 | S_ISVTX | Implementation-defined meaning, but POSIX XSI specifies that when set on a directory, only file owners may delete files even if the directory is writeable to others (used with /tmp) |
| `mask` | 07777 |  | All valid permission bits Equivalent to all | set_uid | set_gid | sticky_bit |

Additionally, the following constants of this type are defined, which do not represent permissions:

| Member constant | Value (hex) | Meaning |
| --- | --- | --- |
| `unknown` | 0xFFFF | Unknown permissions (e.g. when file_status is created without permissions) |
| `add_perms` | 0x10000 | Control bit that instructs permissions to add, but not clear permission bits |
| `remove_perms` | 0x20000 | Control bit that instructs permissions to clear, but not add permission bits |
| `resolve_symlinks` | 0x40000 | Control bit that instructs permissions to resolve symlinks |

### Notes

Permissions may not necessarily be implemented as bits, but they are treated that way conceptually.

Some permission bits may be ignored on some systems, and changing some bits may automatically change others (e.g. on platforms without owner/group/all distinction, setting any of the three write bits set all three).

### Example

Run this code

```
#include <bitset>
#include <experimental/filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::experimental::filesystem;
 
void demo_perms(fs::perms p)
{
     std::cout << ((p & fs::perms::owner_read) != fs::perms::none ? "r" : "-")
               << ((p & fs::perms::owner_write) != fs::perms::none ? "w" : "-")
               << ((p & fs::perms::owner_exec) != fs::perms::none ? "x" : "-")
               << ((p & fs::perms::group_read) != fs::perms::none ? "r" : "-")
               << ((p & fs::perms::group_write) != fs::perms::none ? "w" : "-")
               << ((p & fs::perms::group_exec) != fs::perms::none ? "x" : "-")
               << ((p & fs::perms::others_read) != fs::perms::none ? "r" : "-")
               << ((p & fs::perms::others_write) != fs::perms::none ? "w" : "-")
               << ((p & fs::perms::others_exec) != fs::perms::none ? "x" : "-")
               << '\n';
}
 
int main()
{
    std::ofstream("test.txt"); // create file
 
    std::cout << "Created file with permissions: ";
    demo_perms(fs::status("test.txt").permissions());
 
    fs::permissions("test.txt", fs::perms::add_perms |
                                fs::perms::owner_all | fs::perms::group_all);
 
    std::cout << "After adding o+rwx and g+rwx:  ";
    demo_perms(fs::status("test.txt").permissions());
 
    fs::remove("test.txt");
}

```

Possible output:

```
Created file with permissions: rw-r--r--
After adding o+rwx and g+rwx:  rwxrwxr--

```

### See also

|  |  |
| --- | --- |
| statussymlink_status | determines file attributes determines file attributes, checking the symlink target   (function) |
| permissions | modifies file access permissions   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/perms&oldid=158868>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2023, at 01:52.