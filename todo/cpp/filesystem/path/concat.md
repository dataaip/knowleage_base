# std::filesystem::path::concat, std::filesystem::path::operator+=

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::path | | | | | | path::~path | | | | | | path::operator= | | | | | | path::assign | | | | | | path::appendpath::operator/= | | | | | | ****path::concatpath::operator+=**** | | | | | | path::clear | | | | | | path::make_preferred | | | | | | path::remove_filename | | | | | | path::replace_filename | | | | | | path::replace_extension | | | | | | path::swap | | | | | | path::compare | | | | | | path::beginpath::end | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::c_strpath::nativepath::operator string_type | | | | | | path::stringpath::u8stringpath::u16stringpath::u32stringpath::wstring | | | | | | path::generic_stringpath::generic_u8stringpath::generic_u16stringpath::generic_u32stringpath::generic_wstring | | | | | | path::lexically_normalpath::lexically_relativepath::lexically_proximate | | | | | |  | | | | | |
| Path decomposition | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::root_name | | | | | | path::root_directory | | | | | | path::root_path | | | | | | path::relative_path | | | | | | path::parent_path | | | | | | path::filename | | | | | | path::stem | | | | | | path::extension | | | | | | path::empty | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::has_root_pathpath::has_root_namepath::has_root_directorypath::has_relative_pathpath::has_parent_pathpath::has_filenamepath::has_stempath::has_extension | | | | | | path::is_absolutepath::is_relative | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator/ | | | | | | operator<<operator>> | | | | | | swap(std::filesystem::path) | | | | | | hash_value | | | | | | u8path | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | hash<std::filesystem::path> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::filesystem::path>(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| path& operator+=( const path& p ); | (1) | (since C++17) |
| path& operator+=( const string_type& str );  path& operator+=( std::basic_string_view<value_type> str ); | (2) | (since C++17) |
| path& operator+=( const value_type\* ptr ); | (3) | (since C++17) |
| path& operator+=( value_type x ); | (4) | (since C++17) |
| template< class CharT >  path& operator+=( CharT x ); | (5) | (since C++17) |
| template< class Source >  path& operator+=( const Source& source ); | (6) | (since C++17) |
| template< class Source >  path& concat( const Source& source ); | (7) | (since C++17) |
| template< class InputIt >  path& concat( InputIt first, InputIt last ); | (8) | (since C++17) |
|  |  |  |

Concatenates the current path and the argument

1-3,6,7) Appends path(p).native() to the pathname stored in \*this in the native format. This directly manipulates the value of native() and may not be portable between operating systems.4,5) Same as return \*this += std::basic_string_view(&x, 1);.8) Same as return \*this += path(first, last);.

(6) and (7) participate in overload resolution only if `Source` and `path` are not the same type, and either:

- `Source` is a specialization of std::basic_string or std::basic_string_view, or
- std::iterator_traits<std::decay_t<Source>>::value_type is valid and denotes a possibly const-qualified encoding character type (char, char8_t, (since C++20)char16_t, char32_t, or wchar_t).

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | path to append |
| str | - | string or string view to append |
| ptr | - | pointer to the beginning of a null-terminated string to append |
| x | - | single character to append |
| source | - | std::basic_string, std::basic_string_view, null-terminated multicharacter string, or an input iterator pointing to a null-terminated multicharacter sequence, which represents a path name (either in portable or in native format) |
| first, last | - | pair of LegacyInputIterators that specify a multicharacter sequence that represents a path name |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -The value type of `InputIt` must be one of the encoded character types (char, wchar_t, char16_t and char32_t). | | |
| -`CharT` must be one of the encoded character types (char, wchar_t, char16_t and char32_t). | | |

### Return value

\*this

### Exceptions

May throw std::bad_alloc if memory allocation fails.

### Notes

Unlike with append() or operator/=, additional directory separators are never introduced.

### Example

Run this code

```
#include <filesystem>
#include <iostream>
#include <string>
 
int main()
{
    std::filesystem::path p1; // an empty path
    p1 += "var"; // does not insert a separator
    std::cout << R"("" + "var" --> )" << p1 << '\n';
    p1 += "lib"; // does not insert a separator
    std::cout << R"("var" + "lib" --> )" << p1 << '\n';
    auto str = std::string{"1234567"};
    p1.concat(std::begin(str) + 3, std::end(str) - 1);
    std::cout << "p1.concat --> " << p1 << '\n';
}

```

Output:

```
"" + "var" --> "var"
"var" + "lib" --> "varlib"
p1.concat --> "varlib456"

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3055 | C++17 | the specification of concatenating a single character was ill-formed | made well-formed |
| LWG 3244 | C++17 | constraint that `Source` cannot be `path` was missing | added |

### See also

|  |  |
| --- | --- |
| appendoperator/= | appends elements to the path with a directory separator   (public member function) |
| operator/(C++17) | concatenates two paths with a directory separator   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/path/concat&oldid=158017>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 September 2023, at 10:49.