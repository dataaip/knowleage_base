# std::filesystem::u8path

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::path | | | | | | path::~path | | | | | | path::operator= | | | | | | path::assign | | | | | | path::appendpath::operator/= | | | | | | path::concatpath::operator+= | | | | | | path::clear | | | | | | path::make_preferred | | | | | | path::remove_filename | | | | | | path::replace_filename | | | | | | path::replace_extension | | | | | | path::swap | | | | | | path::compare | | | | | | path::beginpath::end | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::c_strpath::nativepath::operator string_type | | | | | | path::stringpath::u8stringpath::u16stringpath::u32stringpath::wstring | | | | | | path::generic_stringpath::generic_u8stringpath::generic_u16stringpath::generic_u32stringpath::generic_wstring | | | | | | path::lexically_normalpath::lexically_relativepath::lexically_proximate | | | | | |  | | | | | |
| Path decomposition | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::root_name | | | | | | path::root_directory | | | | | | path::root_path | | | | | | path::relative_path | | | | | | path::parent_path | | | | | | path::filename | | | | | | path::stem | | | | | | path::extension | | | | | | path::empty | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | path::has_root_pathpath::has_root_namepath::has_root_directorypath::has_relative_pathpath::has_parent_pathpath::has_filenamepath::has_stempath::has_extension | | | | | | path::is_absolutepath::is_relative | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator/ | | | | | | operator<<operator>> | | | | | | swap(std::filesystem::path) | | | | | | hash_value | | | | | | ****u8path**** | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | hash<std::filesystem::path> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::filesystem::path>(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| template< class Source >  std::filesystem::path u8path( const Source& source ); | (1) | (since C++17)  (deprecated in C++20) |
| template< class InputIt >  std::filesystem::path u8path( InputIt first, InputIt last ); | (2) | (since C++17)  (deprecated in C++20) |
|  |  |  |

Constructs a path `p` from a UTF-8 encoded sequence of chars or char8_ts(since C++20), supplied either as an std::string, or as std::string_view, or as a null-terminated multibyte string, or as a first, last) iterator pair.

- If `path::value_type` is char and native encoding is UTF-8, constructs a path directly as if by path(source) or path(first, last). Note: this is the typical situation of a POSIX system that uses Unicode, such as Linux.
- Otherwise, if `path::value_type` is wchar_t and native encoding is UTF-16 (this is the situation on Windows), or if `path::value_type` is char16_t (native encoding guaranteed UTF-16) or char32_t (native encoding guaranteed UTF-32), then first converts the UTF-8 character sequence to a temporary string `tmp` of type `path::string_type` and then the new path is constructed as if by path(tmp).
- Otherwise (for non-UTF-8 narrow character encodings and for non-UTF-16 wchar_t), first converts the UTF-8 character sequence to a temporary UTF-32-encoded string `tmp` of type [std::u32string, and then the new path is constructed as if by path(tmp) (this path is taken on a POSIX system with a non-Unicode multibyte or single-byte encoded filesystem).

### Parameters

|  |  |  |
| --- | --- | --- |
| source | - | a UTF-8 encoded std::string, std::string_view, a pointer to a null-terminated multibyte string, or an input iterator with char value type that points to a null-terminated multibyte string |
| first, last | - | pair of LegacyInputIterators that specify a UTF-8 encoded character sequence |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |
| -The value type of `Source` or `InputIt` must be char or char8_t.(since C++20) | | |

### Return value

The path constructed from the input string after conversion from UTF-8 to the filesystem's native character encoding.

### Exceptions

May throw std::bad_alloc if memory allocation fails.

### Notes

On systems where native path format differs from the generic path format (neither Windows nor POSIX systems are examples of such OSes), if the argument to this function is using generic format, it will be converted to native.

### Example

Run this code

```
#include <cstdio>
#ifdef _MSC_VER
#include <fcntl.h>
#include <io.h>
#else
#include <clocale>
#include <locale>
#endif
#include <filesystem>
#include <fstream>
 
int main()
{
#ifdef _MSC_VER
    _setmode(_fileno(stderr), _O_WTEXT);
#else
    std::setlocale(LC_ALL, "");
    std::locale::global(std::locale(""));
#endif
 
    std::filesystem::path p(u8"要らない.txt");
    std::ofstream(p) << "File contents"; // Prior to LWG2676 uses operator string_type()
                                         // on MSVC, where string_type is wstring, only
                                         // works due to non-standard extension.
                                         // Post-LWG2676 uses new fstream constructors
 
    // Native string representation can be used with OS-specific APIs
#ifdef _MSC_VER
    if (std::FILE* f = _wfopen(p.c_str(), L"r"))
#else
    if (std::FILE* f = std::fopen(p.c_str(), "r"))
#endif
    {
        for (int ch; (ch = fgetc(f)) != EOF; std::putchar(ch))
        {}
        std::fclose(f);
    }
 
    std::filesystem::remove(p);
}

```

Possible output:

```
File contents

```

### See also

|  |  |
| --- | --- |
| path(C++17) | represents a path   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/path/u8path&oldid=158113>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 September 2023, at 10:26.