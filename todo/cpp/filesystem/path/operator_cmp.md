# operator==,!=,<,<=,>,>=,<=>(std::filesystem::path)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator==operator!=operator<operator<=operator>operator>=operator<=>****(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator/ | | | | | | operator<<operator>> | | | | | | swap(std::filesystem::path) | | | | | | hash_value | | | | | | u8path | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | hash<std::filesystem::path> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | formatter<std::filesystem::path>(C++26) | | | | | |

|  |  |  |
| --- | --- | --- |
| friend bool operator==( const path& lhs, const path& rhs ) noexcept; | (1) | (since C++17) |
| friend bool operator!=( const path& lhs, const path& rhs ) noexcept; | (2) | (since C++17)  (until C++20) |
| friend bool operator<( const path& lhs, const path& rhs ) noexcept; | (3) | (since C++17)  (until C++20) |
| friend bool operator<=( const path& lhs, const path& rhs ) noexcept; | (4) | (since C++17)  (until C++20) |
| friend bool operator>( const path& lhs, const path& rhs ) noexcept; | (5) | (since C++17)  (until C++20) |
| friend bool operator>=( const path& lhs, const path& rhs ) noexcept; | (6) | (since C++17)  (until C++20) |
| friend std::strong_ordering      operator<=>( const path& lhs, const path& rhs ) noexcept; | (7) | (since C++20) |
|  |  |  |

Compares two paths lexicographically.

1) Checks whether lhs and rhs are equal. Equivalent to !(lhs < rhs) && !(rhs < lhs).2) Checks whether lhs and rhs are not equal. Equivalent to !(lhs == rhs).3) Checks whether lhs is less than rhs. Equivalent to lhs.compare(rhs) < 0.4) Checks whether lhs is less than or equal to rhs. Equivalent to !(rhs < lhs).5) Checks whether lhs is greater than rhs. Equivalent to rhs < lhs.6) Checks whether lhs is greater than or equal to rhs. Equivalent to !(lhs < rhs).7) Obtains the three-way comparison result of lhs and rhs. Equivalent to lhs.compare(rhs) <=> 0.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when std::filesystem::path is an associated class of the arguments. This prevents undesirable conversions in the presence of a using namespace std::filesystem; **using-directive**.

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | the paths to compare |

### Return value

1-6) true if the corresponding comparison yields, false otherwise.7) std::strong_ordering::less if lhs is less than rhs, otherwise std::strong_ordering::greater if rhs is less than lhs, otherwise std::strong_ordering::equal.

### Notes

Path equality and equivalence have different semantics.

In the case of equality, as determined by `operator==`, only lexical representations are compared. Therefore, path("a") == path("b") is never true.

In the case of equivalence, as determined by std::filesystem::equivalent(), it is checked whether two paths **resolve** to the same file system object. Thus equivalent("a", "b") will return true if the paths resolve to the same file.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3065 | C++17 | allowed comparison of everything convertible to `path` in the presence of a **using-directive** | made hidden friend |

### See also

|  |  |
| --- | --- |
| compare | compares the lexical representations of two paths lexicographically   (public member function) |
| equivalent(C++17) | checks whether two paths refer to the same file system object   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/path/operator_cmp&oldid=156796>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 August 2023, at 23:34.