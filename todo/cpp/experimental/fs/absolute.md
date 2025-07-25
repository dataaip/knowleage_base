# std::experimental::filesystem::absolute, std::experimental::filesystem::system_complete

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::space_info | | | | | | filesystem::file_type | | | | | | filesystem::perms | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | | filesystem::file_time_type | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****filesystem::absolute filesystem::system_complete**** | | | | | | filesystem::canonical | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | | filesystem::temp_directory_path | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/filesystem>` |  |  |
| path absolute( const path& p, const path& base = current_path() ); | (1) | (filesystem TS) |
| path system_complete( const path& p );  path system_complete( const path& p, error_code& ec ); | (2) | (filesystem TS) |
|  |  |  |

1) Returns absolute path of p relative to base according to the following rules:

:   - If p has both root name and root directory (e.g. "C:\users", then the path is returned, unmodified.
    - If p has a root name not followed by a root directory (e.g. "C:text.txt"), then base is inserted between p's root name and the remainder of p. Formally, p.root_name() / fs::absolute(base).root_directory() / fs::absolute(base).relative_path() / p.relative_path() is returned,
    - If p has no root name, but has a root directory (e.g. "/var/tmp/file.txt" on a POSIX system or "\users\ABC\Document.doc" on Windows, then the root name of base, if it has one, is prepended to p (on a POSIX system, p is not modified, on a Windows system, "\users\ABC\Document.doc" becomes "C:\users\ABC\Document.doc". Formally, fs::absolute(base).root_name() / p is returned.
    - If p has no root name and no root directory (e.g. "../file.txt", then the entire base is prepended to p. Formally, absolute(base) / p is returned.

2) Obtains the absolute path that identifies the file that the OS file opening API would access given the pathname p. On POSIX systems, this is equivalent to (1) with the default base (`fs::current_path()`). On Windows systems, each logical drive has its own current working directory, and so if p is not already absolute and has a root name component (e.g. "E:filename.txt", that drive's current working directory is used, which may have been set by an earlier executed program.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | path to convert to absolute form |
| base | - | path (not necessarily absolute) to serve as the starting location |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

Returns an absolute (although not necessarily canonical) path formed by combining p and base as described above.

### Exceptions

The overload that does not take an error_code& parameter throws filesystem_error on underlying OS API errors, constructed with p as the first argument, base as the second argument, and the OS error code as the error code argument. std::bad_alloc may be thrown if memory allocation fails. The overload taking an error_code& parameter sets it to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur. This overload hasnoexcept specification:noexcept

### Notes

On systems that support root names (e.g. Windows), the result of calling `absolute` on a relative path that has a root name (e.g. "D:file.txt" when the root name of base is different will usually result in a non-existent path.

### Example

Run this code

```
#include <filesystem>
#include <iostream>
namespace fs = std::experimental::filesystem;
 
int main()
{
    fs::path p = "C:cl.exe";
    std::cout << "Current path is " << fs::current_path() << '\n'
              << "Absolute path for " << p << " is " << fs::absolute(p) << '\n'
	      << "System complete path for " << p << " is "
              << fs::system_complete(p) << '\n';
}

```

Possible output:

```
Current path is "D:/local/ConsoleApplication1"
Absolute path for "C:cl.exe" is "C:/local/ConsoleApplication1/cl.exe"
System complete path for "C:cl.exe" is "C:\Program Files (x86)\Microsoft Visual Studio 12.0\VC\bin\cl.exe"

```

### See also

|  |  |
| --- | --- |
| canonical | composes a canonical path   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/fs/absolute&oldid=154819>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 July 2023, at 22:50.