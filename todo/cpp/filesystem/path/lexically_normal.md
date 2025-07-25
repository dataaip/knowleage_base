# std::filesystem::path::lexically_normal, std::filesystem::path::lexically_relative, std::filesystem::path::lexically_proximate

From cppreference.com
< cpp‎ | filesystem‎ | path
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

std::filesystem::path

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member constants | | | | |
| path::native_formatpath::generic_formatpath::auto_format | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::path | | | | | | path::~path | | | | | | path::operator= | | | | | | path::assign | | | | | | path::appendpath::operator/= | | | | | | path::concatpath::operator+= | | | | | | path::clear | | | | | | path::make_preferred | | | | | | path::remove_filename | | | | | | path::replace_filename | | | | | | path::replace_extension | | | | | | path::swap | | | | | | path::compare | | | | | | path::beginpath::end | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::c_strpath::nativepath::operator string_type | | | | | | path::stringpath::u8stringpath::u16stringpath::u32stringpath::wstring | | | | | | path::generic_stringpath::generic_u8stringpath::generic_u16stringpath::generic_u32stringpath::generic_wstring | | | | | | ****path::lexically_normalpath::lexically_relativepath::lexically_proximate**** | | | | | |  | | | | | |
| Path decomposition | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::root_name | | | | | | path::root_directory | | | | | | path::root_path | | | | | | path::relative_path | | | | | | path::parent_path | | | | | | path::filename | | | | | | path::stem | | | | | | path::extension | | | | | | path::empty | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::has_root_pathpath::has_root_namepath::has_root_directorypath::has_relative_pathpath::has_parent_pathpath::has_filenamepath::has_stempath::has_extension | | | | | | path::is_absolutepath::is_relative | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator/ | | | | | | operator<<operator>> | | | | | | swap(std::filesystem::path) | | | | | | hash_value | | | | | | u8path | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | hash<std::filesystem::path> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::filesystem::path>(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| path lexically_normal() const; | (1) | (since C++17) |
| path lexically_relative( const path& base ) const; | (2) | (since C++17) |
| path lexically_proximate( const path& base ) const; | (3) | (since C++17) |
|  |  |  |

1) Returns \*this converted to normal form in its generic format.2) Returns \*this made relative to base.

:   - First, if root_name() != base.root_name() is true or is_absolute() != base.is_absolute() is true or (!has_root_directory() && base.has_root_directory()) is true or any filename in relative_path() or base.relative_path() can be interpreted as a root-name, returns a default-constructed path.
    - Otherwise, first determines the first mismatched element of \*this and base as if by auto [a, b] = mismatch(begin(), end(), base.begin(), base.end()), then

    :   - if a == end() and b == base.end(), returns path("."),
        - otherwise, define N as the number of nonempty filename elements that are neither dot nor dot-dot in b, base.end()), minus the number of dot-dot filename elements, If N < 0, returns a default-constructed path,
        - otherwise, if N = 0 and a == end() || a->empty(), returns path("."),
        - otherwise returns an object composed from

        :   - a default-constructed path() followed by
            - N applications of operator/=(path("..")), followed by
            - one application of operator/= for each element in the half-open range `[`a`,`end()`)`.

3) If the value of lexically_relative(base) is not an empty path, return it. Otherwise return \*this.

### Parameters

(none)

### Return value

1) The normal form of the path.2) The relative form of the path.3) The proximate form of the path.

### Exceptions

May throw implementation-defined exceptions.

### Notes

These conversions are purely lexical. They do not check that the paths exist, do not follow symlinks, and do not access the filesystem at all. For symlink-following counterparts of `lexically_relative` and `lexically_proximate`, see [relative and proximate.

On Windows, the returned `path` has backslashes (the preferred separators).

On POSIX, no filename in a relative path is acceptable as a root-name.

### Example

Run this code

```
#include <cassert>
#include <filesystem>
#include <iostream>
namespace fs = std::filesystem;
 
int main()
{
    assert(fs::path("a/./b/..").lexically_normal() == "a/");
    assert(fs::path("a/.///b/../").lexically_normal() == "a/");
    assert(fs::path("/a/d").lexically_relative("/a/b/c") == "../../d");
    assert(fs::path("/a/b/c").lexically_relative("/a/d") == "../b/c");
    assert(fs::path("a/b/c").lexically_relative("a") == "b/c");
    assert(fs::path("a/b/c").lexically_relative("a/b/c/x/y") == "../..");
    assert(fs::path("a/b/c").lexically_relative("a/b/c") == ".");
    assert(fs::path("a/b").lexically_relative("c/d") == "../../a/b");
    assert(fs::path("a/b").lexically_relative("/a/b") == "");
    assert(fs::path("a/b").lexically_proximate("/a/b") == "a/b");
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3070 | C++17 | a filename that can also be a root-name may cause surprising result | treated as error case |
| LWG 3096 | C++17 | trailing "/" and "/." are handled incorrectly | corrected |

### See also

|  |  |
| --- | --- |
| relativeproximate(C++17) | composes a relative path   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/path/lexically_normal&oldid=158038>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 September 2023, at 22:24.