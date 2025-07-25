# std::filesystem::path::compare

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::path | | | | | | path::~path | | | | | | path::operator= | | | | | | path::assign | | | | | | path::appendpath::operator/= | | | | | | path::concatpath::operator+= | | | | | | path::clear | | | | | | path::make_preferred | | | | | | path::remove_filename | | | | | | path::replace_filename | | | | | | path::replace_extension | | | | | | path::swap | | | | | | ****path::compare**** | | | | | | path::beginpath::end | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::c_strpath::nativepath::operator string_type | | | | | | path::stringpath::u8stringpath::u16stringpath::u32stringpath::wstring | | | | | | path::generic_stringpath::generic_u8stringpath::generic_u16stringpath::generic_u32stringpath::generic_wstring | | | | | | path::lexically_normalpath::lexically_relativepath::lexically_proximate | | | | | |  | | | | | |
| Path decomposition | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::root_name | | | | | | path::root_directory | | | | | | path::root_path | | | | | | path::relative_path | | | | | | path::parent_path | | | | | | path::filename | | | | | | path::stem | | | | | | path::extension | | | | | | path::empty | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::has_root_pathpath::has_root_namepath::has_root_directorypath::has_relative_pathpath::has_parent_pathpath::has_filenamepath::has_stempath::has_extension | | | | | | path::is_absolutepath::is_relative | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator/ | | | | | | operator<<operator>> | | | | | | swap(std::filesystem::path) | | | | | | hash_value | | | | | | u8path | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | hash<std::filesystem::path> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::filesystem::path>(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| int compare( const path& p ) const noexcept; | (1) | (since C++17) |
| int compare( const string_type& str ) const;  int compare( std::basic_string_view<value_type> str ) const; | (2) | (since C++17) |
| int compare( const value_type\* s ) const; | (3) | (since C++17) |
|  |  |  |

Compares the lexical representations of the path and another path.

1) If root_name().native().compare(p.root_name().native()) is nonzero, returns that value. Otherwise, if has_root_directory() != p.has_root_directory(), returns a value less than zero if `has_root_directory()` is false and a value greater than zero otherwise. Otherwise returns a value less than, equal to or greater than ​0​ if the relative portion of the path (`relative_path()`) is respectively lexicographically less than, equal to or greater than the relative portion of p (p.relative_path()). Comparison is performed element-wise, as if by iterating both paths from `begin()` to `end()` and comparing the result of `native()` for each element.2) Equivalent to compare(path(str)).3) Equivalent to compare(path(s)).

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | a path to compare to |
| str | - | a string or string view representing path to compare to |
| s | - | a null-terminated string representing path to compare to |

### Return value

A value less than ​0​ if the path is lexicographically less than the given path.

A value equal to ​0​ if the path is lexicographically equal to the given path.

A value greater than ​0​ if the path is lexicographically greater than the given path.

### Exceptions

2,3) May throw implementation-defined exceptions.

### Notes

For two-way comparisons, binary operators may be more suitable.

### Example

Run this code

```
#include <filesystem>
#include <iostream>
#include <string_view>
namespace fs = std::filesystem;
 
void demo(fs::path p1, fs::path p2, std::string_view msg)
{
    std::cout << p1;
    const int rc = p1.compare(p2); 
    if (rc < 0)
        std::cout << " < ";
    else if (rc > 0)
        std::cout << " > ";
    else
        std::cout << " == ";
    std::cout << p2 << " \t: " << msg << '\n';
}
 
int main()
{
    demo("/a/b/", "/a/b/", "simple");
    demo("/a/b/", "/a/b/c", "simple");
    demo("/a/b/../b", "/a/b", "no canonical conversion");
    demo("/a/b", "/a/b/.", "no canonical conversion");
    demo("/a/b/", "a/c", "absolute paths order after relative ones");
}

```

Output:

```
"/a/b/" == "/a/b/"      : simple
"/a/b/" < "/a/b/c"	: simple
"/a/b/../b" > "/a/b"	: no canonical conversion
"/a/b" < "/a/b/."	: no canonical conversion
"/a/b/" > "a/c"	        : absolute paths order after relative ones

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2936 | C++17 | compared all path elements directly | root name and root directory handled separately |

### See also

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++17)(C++17)(until C++20)(C++17)(until C++20)(C++17)(until C++20)(C++17)(until C++20)(C++17)(until C++20)(C++20) | lexicographically compares two paths   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/path/compare&oldid=158016>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 September 2023, at 10:36.