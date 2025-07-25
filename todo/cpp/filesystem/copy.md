# std::filesystem::copy

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | ****filesystem::copy**** | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| void copy( const std::filesystem::path& from,             const std::filesystem::path& to ); | (1) | (since C++17) |
| void copy( const std::filesystem::path& from,  const std::filesystem::path& to, std::error_code& ec ); | (2) | (since C++17) |
| void copy( const std::filesystem::path& from,  const std::filesystem::path& to, std::filesystem::copy_options options ); | (3) | (since C++17) |
| void copy( const std::filesystem::path& from,  const std::filesystem::path& to,             std::filesystem::copy_options options, std::error_code& ec ); | (4) | (since C++17) |
|  |  |  |

Copies files and directories, with a variety of options.

1,2) The default, equivalent to (3,4) with `copy_options::none` used as options.3,4) Copies the file or directory from to file or directory to, using the copy options indicated by options. The behavior is undefined if there is more than one option in any of the copy_options option group present in options (even in the `copy_file` group).

The behavior is as follows:

- First, before doing anything else, obtains type and permissions of from by no more than a single call to

:   - std::filesystem::symlink_status, if `copy_options::skip_symlinks`, `copy_options::copy_symlinks`, or `copy_options::create_symlinks` is present in options;
    - std::filesystem::status otherwise.

- If necessary, obtains the status of to, by no more than a single call to

:   - std::filesystem::symlink_status, if `copy_options::skip_symlinks` or `copy_options::create_symlinks` is present in options;
    - std::filesystem::status otherwise (including the case where `copy_options::copy_symlinks` is present in options).

- If either from or to has an implementation-defined file type, the effects of this function are implementation-defined.
- If from does not exist, reports an error.
- If from and to are the same file as determined by std::filesystem::equivalent, reports an error.
- If either from or to is not a regular file, a directory, or a symlink, as determined by std::filesystem::is_other, reports an error.
- If from is a directory, but to is a regular file, reports an error.
- If from is a symbolic link, then

:   - If `copy_options::skip_symlink` is present in options, does nothing.
    - Otherwise, if to does not exist and `copy_options::copy_symlinks` is present in options, then behaves as if copy_symlink(from, to).
    - Otherwise, reports an error.

- Otherwise, if from is a regular file, then

:   - If `copy_options::directories_only` is present in options, does nothing.
    - Otherwise, if `copy_options::create_symlinks` is present in options, creates a symlink to to. Note: from must be an absolute path unless to is in the current directory.
    - Otherwise, if `copy_options::create_hard_links` is present in options, creates a hard link to to.
    - Otherwise, if to is a directory, then behaves as if copy_file(from, to/from.filename(), options) (creates a copy of from as a file in the directory to).
    - Otherwise, behaves as if copy_file(from, to, options) (copies the file).

- Otherwise, if from is a directory and `copy_options::create_symlinks` is set in options, reports an error with an error code equal to std::make_error_code(std::errc::is_a_directory).
- Otherwise, if from is a directory and either options has `copy_options::recursive` or is `copy_options::none`,

:   - If to does not exist, first executes create_directory(to, from) (creates the new directory with a copy of the old directory's attributes).
    - Then, whether to already existed or was just created, iterates over the files contained in from as if by for (const std::filesystem::directory_entry& x : std::filesystem::directory_iterator(from)) and for each directory entry, recursively calls copy(x.path(), to/x.path().filename(), options | in-recursive-copy), where **in-recursive-copy** is a special bit that has no other effect when set in options. (The sole purpose of setting this bit is to prevent recursive copying subdirectories if options is `copy_options::none`.)

- Otherwise does nothing.

### Parameters

|  |  |  |
| --- | --- | --- |
| from | - | path to the source file, directory, or symlink |
| to | - | path to the target file, directory, or symlink |
| ec | - | out-parameter for error reporting in the non-throwing overload |

### Return value

(none)

### Exceptions

Any overload not marked `noexcept` may throw std::bad_alloc if memory allocation fails.

1,3) Throws std::filesystem::filesystem_error on underlying OS API errors, constructed with from as the first path argument, to as the second path argument, and the OS error code as the error code argument.2,4) Sets a std::error_code& parameter to the OS API error code if an OS API call fails, and executes ec.clear() if no errors occur.

### Notes

The default behavior when copying directories is the non-recursive copy: the files are copied, but not the subdirectories:

```
// Given
// /dir1 contains /dir1/file1, /dir1/file2, /dir1/dir2
// and /dir1/dir2 contains /dir1/dir2/file3
// After
std::filesystem::copy("/dir1", "/dir3");
// /dir3 is created (with the attributes of /dir1)
// /dir1/file1 is copied to /dir3/file1
// /dir1/file2 is copied to /dir3/file2

```

While with `copy_options::recursive`, the subdirectories are also copied, with their content, recursively.

```
// ...but after
std::filesystem::copy("/dir1", "/dir3", std::filesystem::copy_options::recursive);
// /dir3 is created (with the attributes of /dir1)
// /dir1/file1 is copied to /dir3/file1
// /dir1/file2 is copied to /dir3/file2
// /dir3/dir2 is created (with the attributes of /dir1/dir2)
// /dir1/dir2/file3 is copied to /dir3/dir2/file3

```

### Example

Run this code

```
#include <cstdlib>
#include <filesystem>
#include <fstream>
#include <iostream>
namespace fs = std::filesystem;
 
int main()
{
    fs::create_directories("sandbox/dir/subdir");
    std::ofstream("sandbox/file1.txt").put('a');
    fs::copy("sandbox/file1.txt", "sandbox/file2.txt"); // copy file
    fs::copy("sandbox/dir", "sandbox/dir2"); // copy directory (non-recursive)
    const auto copyOptions = fs::copy_options::update_existing
                           | fs::copy_options::recursive
                           | fs::copy_options::directories_only
                           ;
    fs::copy("sandbox", "sandbox_copy", copyOptions); 
    static_cast<void>(std::system("tree"));
    fs::remove_all("sandbox");
    fs::remove_all("sandbox_copy");
}

```

Possible output:

```
.
├── sandbox
│   ├── dir
│   │   └── subdir
│   ├── dir2
│   ├── file1.txt
│   └── file2.txt
└── sandbox_copy
    ├── dir
    │   └── subdir
    └── dir2
 
8 directories, 2 files

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3013 | C++17 | `error_code` overload marked noexcept but can allocate memory | noexcept removed |
| LWG 2682 | C++17 | attempting to create a symlink for a directory succeeds but does nothing | reports an error |

### See also

|  |  |
| --- | --- |
| copy_options(C++17) | specifies semantics of copy operations   (enum) |
| copy_symlink(C++17) | copies a symbolic link   (function) |
| copy_file(C++17) | copies file contents   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/copy&oldid=157937>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2023, at 08:38.