# std::filesystem::directory_entry

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | ****filesystem::directory_entry**** | | | | | | filesystem::directory_iterator | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | filesystem::perms | | | | | | filesystem::perm_options | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

****std::filesystem::directory_entry****

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
| directory_entry::operator==directory_entry::operator!=directory_entry::operator<directory_entry::operator>directory_entry::operator<=directory_entry::operator>=directory_entry::operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| Non-member functions | | | | |
| operator<< | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| class directory_entry; |  | (since C++17) |
|  |  |  |

Represents a directory entry. The object stores a `path` as a member and may also store additional file attributes (hard link count, status, symlink status, file size, and last write time) during directory iteration.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a directory entry   (public member function) |
| (destructor) | default destructor   (public member function) |
| Modifiers | |
| operator= | assigns contents   (public member function) |
| assign | assigns contents   (public member function) |
| replace_filename | sets the filename   (public member function) |
| refresh | updates the cached file attributes   (public member function) |
| Observers | |
| pathoperator const path& | returns the path the entry refers to   (public member function) |
| exists | checks whether directory entry refers to existing file system object   (public member function) |
| is_block_file | checks whether the directory entry refers to block device   (public member function) |
| is_character_file | checks whether the directory entry refers to a character device   (public member function) |
| is_directory | checks whether the directory entry refers to a directory   (public member function) |
| is_fifo | checks whether the directory entry refers to a named pipe   (public member function) |
| is_other | checks whether the directory entry refers to an **other** file   (public member function) |
| is_regular_file | checks whether the directory entry refers to a regular file   (public member function) |
| is_socket | checks whether the directory entry refers to a named IPC socket   (public member function) |
| is_symlink | checks whether the directory entry refers to a symbolic link   (public member function) |
| file_size | returns the size of the file to which the directory entry refers   (public member function) |
| hard_link_count | returns the number of hard links referring to the file to which the directory entry refers   (public member function) |
| last_write_time | gets the time of the last data modification of the file to which the directory entry refers   (public member function) |
| statussymlink_status | status of the file designated by this directory entry; status of the file/symlink designated by this directory entry   (public member function) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | compares two directory entries   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator<< | performs stream output on a directory entry   (function) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3171 | C++17 | `directory_entry` couldn't be inserted by `operator<<` because of LWG2989 | output enabled again |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/directory_entry&oldid=164723>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 December 2023, at 12:45.