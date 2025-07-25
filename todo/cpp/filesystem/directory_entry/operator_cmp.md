# std::filesystem::directory_entry::operator==,!=,<,<=,>,>=,<=>

From cppreference.com
< cpp‎ | filesystem‎ | directory entry
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

std::filesystem::directory_entry

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| directory_entry::directory_entry | | | | |
| Modifiers | | | | |
| directory_entry::operator= | | | | |
| directory_entry::assign | | | | |
| directory_entry::replace_filename | | | | |
| directory_entry::refresh | | | | |
| Observers | | | | |
| directory_entry::pathdirectory_entry::operator const path& | | | | |
| directory_entry::exists | | | | |
| directory_entry::is_block_file | | | | |
| directory_entry::is_character_file | | | | |
| directory_entry::is_directory | | | | |
| directory_entry::is_fifo | | | | |
| directory_entry::is_other | | | | |
| directory_entry::is_regular_file | | | | |
| directory_entry::is_socket | | | | |
| directory_entry::is_symlink | | | | |
| directory_entry::file_size | | | | |
| directory_entry::hard_link_count | | | | |
| directory_entry::last_write_time | | | | |
| directory_entry::statusdirectory_entry::symlink_status | | | | |
| ****directory_entry::operator==directory_entry::operator!=directory_entry::operator<directory_entry::operator>directory_entry::operator<=directory_entry::operator>=directory_entry::operator<=>****(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| Non-member functions | | | | |
| operator<< | | | | |

|  |  |  |
| --- | --- | --- |
| bool operator==( const directory_entry& rhs ) const noexcept; | (1) | (since C++17) |
| bool operator!=( const directory_entry& rhs ) const noexcept; | (2) | (since C++17)  (until C++20) |
| bool operator<( const directory_entry& rhs ) const noexcept; | (3) | (since C++17)  (until C++20) |
| bool operator<=( const directory_entry& rhs ) const noexcept; | (4) | (since C++17)  (until C++20) |
| bool operator>( const directory_entry& rhs ) const noexcept; | (5) | (since C++17)  (until C++20) |
| bool operator>=( const directory_entry& rhs ) const noexcept; | (6) | (since C++17)  (until C++20) |
| std::strong_ordering operator<=>( const directory_entry& rhs ) const noexcept; | (7) | (since C++20) |
|  |  |  |

Compares the path with the directory entry rhs.

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| rhs | - | directory_entry to compare |

### Return value

1) true if path() == rhs.path(), false otherwise.2) true if path() != rhs.path(), false otherwise.3) true if path() < rhs.path(), false otherwise.4) true if path() <= rhs.path(), false otherwise.5) true if path() > rhs.path(), false otherwise.6) true if path() >= rhs.path(), false otherwise.7) The result of path() <=> rhs.path().

### See also

|  |  |
| --- | --- |
| pathoperator const path& | returns the path the entry refers to   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/directory_entry/operator_cmp&oldid=160531>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 October 2023, at 09:44.