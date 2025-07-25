# std::filesystem::status, std::filesystem::symlink_status

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | ****filesystem::status filesystem::symlink_status**** | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| std::filesystem::file_status status( const std::filesystem::path& p ); | (1) | (since C++17) |
| std::filesystem::file_status status( const std::filesystem::path& p,                                       std::error_code& ec ) noexcept; | (2) | (since C++17) |
| std::filesystem::file_status symlink_status( const std::filesystem::path& p ); | (3) | (since C++17) |
| std::filesystem::file_status symlink_status( const std::filesystem::path& p,                                               std::error_code& ec ) noexcept; | (4) | (since C++17) |
|  |  |  |

1,2) Determines the type and attributes of the filesystem object identified by p as if by POSIX `stat` (symlinks are followed to their targets). In the following description, `prms` is the result of (m & perms::mask), where m is obtained as if by taking st_mode from the POSIX struct stat and converting it to the type std::filesystem::perms.

:   - If p is a regular file (as if by POSIX S_ISREG), returns file_status(file_type::regular, prms).
    - If p is a directory (as if by POSIX S_ISDIR), returns file_status(file_type::directory, prms).
    - If p is a block special file (as if by POSIX S_ISBLK), returns file_status(file_type::block, prms).
    - If p is a character special file (as if by POSIX S_ISCHR), returns file_status(file_type::character, prms).
    - If p is a fifo or pipe file (as if by POSIX S_ISFIFO), returns file_status(file_type::fifo, prms).
    - If p is a socket (as if by POSIX S_ISSOCK), returns file_status(file_type::socket, prms).
    - If p has an implementation-defined file type, returns file_status(file_type::A, prms) where `A` is the implementation-defined file_type constant for that type.
    - If p does not exist, returns file_status(file_type::not_found).
    - If p exists but file attributes cannot be determined, e.g. due to lack of permissions, returns file_status(file_type::unknown).
    - If errors prevent even knowing whether p exists, the non-throwing overload sets ec and returns file_status(file_type::none), and the throwing overload throws `filesystem_error`.
    - Otherwise, returns file_status(file_type::unknown, prms).

3,4) Same as (1,2) except that the behavior is as if the POSIX `lstat` is used (symlinks are not followed):

:   - If p is a symlink, returns file_status(file_type::symlink).

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | path to examine |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

The file status (a filesystem::file_status object).

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

1,3) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with p as the first path argument and the OS error code as the error code argument.2,4) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Notes

The information provided by this function is usually also provided as a byproduct of directory iteration, and may be obtained by the member functions of filesystem::directory_entry. During directory iteration, calling `status` again is unnecessary.

### Example

Run this code

```
#include <cstdio>
#include <cstring>
#include <filesystem>
#include <fstream>
#include <iostream>
#include <sys/socket.h>
#include <sys/stat.h>
#include <sys/un.h>
#include <unistd.h>
 
namespace fs = std::filesystem;
 
void demo_status(const fs::path& p, fs::file_status s)
{
    std::cout << p;
    // alternative: switch(s.type()) { case fs::file_type::regular: ...}
    if (fs::is_regular_file(s))
        std::cout << " is a regular file\n";
    if (fs::is_directory(s))
        std::cout << " is a directory\n";
    if (fs::is_block_file(s))
        std::cout << " is a block device\n";
    if (fs::is_character_file(s))
        std::cout << " is a character device\n";
    if (fs::is_fifo(s))
        std::cout << " is a named IPC pipe\n";
    if (fs::is_socket(s))
        std::cout << " is a named IPC socket\n";
    if (fs::is_symlink(s))
        std::cout << " is a symlink\n";
    if (!fs::exists(s))
        std::cout << " does not exist\n";
}
 
int main()
{
    // create files of different kinds
    fs::create_directory("sandbox");
    fs::create_directory("sandbox/dir");
    std::ofstream{"sandbox/file"}; // create regular file
    fs::create_symlink("file", "sandbox/symlink");
 
    mkfifo("sandbox/pipe", 0644);
    sockaddr_un addr;
    addr.sun_family = AF_UNIX;
    std::strcpy(addr.sun_path, "sandbox/sock");
    int fd = socket(PF_UNIX, SOCK_STREAM, 0);
    bind(fd, reinterpret_cast<sockaddr*>(&addr), sizeof addr);
 
    // demo different status accessors
    for (auto it{fs::directory_iterator("sandbox")}; it != fs::directory_iterator(); ++it)
        demo_status(*it, it->symlink_status()); // use cached status from directory entry
    demo_status("/dev/null", fs::status("/dev/null")); // direct calls to status
    demo_status("/dev/sda", fs::status("/dev/sda"));
    demo_status("sandbox/no", fs::status("/sandbox/no"));
 
    // cleanup (prefer std::unique_ptr-based custom deleters)
    close(fd);
    fs::remove_all("sandbox");
}

```

Possible output:

```
"sandbox/file" is a regular file
"sandbox/dir" is a directory
"sandbox/pipe" is a named IPC pipe
"sandbox/sock" is a named IPC socket
"sandbox/symlink" is a symlink
"/dev/null" is a character device
"/dev/sda" is a block device
"sandbox/no" does not exist

```

### See also

|  |  |
| --- | --- |
| file_status(C++17) | represents file type and permissions   (class) |
| status_known(C++17) | checks whether file status is known   (function) |
| is_block_file(C++17) | checks whether the given path refers to block device   (function) |
| is_character_file(C++17) | checks whether the given path refers to a character device   (function) |
| is_directory(C++17) | checks whether the given path refers to a directory   (function) |
| is_fifo(C++17) | checks whether the given path refers to a named pipe   (function) |
| is_other(C++17) | checks whether the argument refers to an **other** file   (function) |
| is_regular_file(C++17) | checks whether the argument refers to a regular file   (function) |
| is_socket(C++17) | checks whether the argument refers to a named IPC socket   (function) |
| is_symlink(C++17) | checks whether the argument refers to a symbolic link   (function) |
| exists(C++17) | checks whether path refers to existing file system object   (function) |
| statussymlink_status | status of the file designated by this directory entry; status of the file/symlink designated by this directory entry   (public member function of `std::filesystem::directory_entry`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/status&oldid=180242>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 February 2025, at 16:48.