# std::filesystem::directory_iterator

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | ****filesystem::directory_iterator**** | | | | | | filesystem::recursive_directory_iterator | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | filesystem::perms | | | | | | filesystem::perm_options | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

****std::filesystem::directory_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| directory_iterator::directory_iterator | | | | |
| directory_iterator::operator\*directory_iterator::operator-> | | | | |
| directory_iterator::operator= | | | | |
| incrementoperator++ | | | | |
| Non-member functions | | | | |
| begin(std::filesystem::directory_iterator)end(std::filesystem::directory_iterator) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| class directory_iterator; |  | (since C++17) |
|  |  |  |

`directory_iterator` is a LegacyInputIterator that iterates over the directory_entry elements of a directory (but does not visit the subdirectories). The iteration order is unspecified, except that each directory entry is visited only once. The special pathnames dot and dot-dot are skipped.

If the `directory_iterator` reports an error or is advanced past the last directory entry, it becomes equal to the default-constructed iterator, also known as the end iterator. Two end iterators are always equal, dereferencing or incrementing the end iterator is undefined behavior.

If a file or a directory is deleted or added to the directory tree after the directory iterator has been created, it is unspecified whether the change would be observed through the iterator.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | std::filesystem::directory_entry |
| `difference_type` | std::ptrdiff_t |
| `pointer` | const std::filesystem::directory_entry\* |
| `reference` | const std::filesystem::directory_entry& |
| `iterator_category` | std::input_iterator_tag |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a directory iterator   (public member function) |
| (destructor) | default destructor   (public member function) |
| operator= | assigns contents   (public member function) |
| operator\*operator-> | accesses the pointed-to entry   (public member function) |
| incrementoperator++ | advances to the next entry   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| begin(std::filesystem::directory_iterator)end(std::filesystem::directory_iterator)(C++17) | range-based for loop support   (function) |

Additionally, `operator==` and `operator!=` are(until C++20)`operator==` is(since C++20) provided as required by LegacyInputIterator.

It is unspecified whether `operator!=` is provided because it can be synthesized from `operator==`, and(since C++20) whether an equality operator is a member or non-member.

### Helper specializations

|  |  |  |
| --- | --- | --- |
| template<>  constexpr bool ranges::enable_borrowed_range<std::filesystem::directory_iterator> = true; |  | (since C++20) |
| template<>  constexpr bool ranges::enable_view<std::filesystem::directory_iterator> = true; |  | (since C++20) |
|  |  |  |

These specializations for `directory_iterator` make it a `borrowed_range` and a `view`.

### Notes

Many low-level OS APIs for directory traversal retrieve file attributes along with the next directory entry. The constructors and the non-const member functions of ****std::filesystem::directory_iterator**** store these attributes, if any, in the pointed-to std::filesystem::directory_entry without calling directory_entry::refresh, which makes it possible to examine the attributes of the directory entries as they are being iterated over, without making additional system calls.

### Example

Run this code

```
#include <algorithm>
#include <filesystem>
#include <fstream>
#include <iostream>
 
int main()
{
    const std::filesystem::path sandbox{"sandbox"};
    std::filesystem::create_directories(sandbox/"dir1"/"dir2");
    std::ofstream{sandbox/"file1.txt"};
    std::ofstream{sandbox/"file2.txt"};
 
    std::cout << "directory_iterator:\n";
    // directory_iterator can be iterated using a range-for loop
    for (auto const& dir_entry : std::filesystem::directory_iterator{sandbox}) 
        std::cout << dir_entry.path() << '\n';
 
    std::cout << "\ndirectory_iterator as a range:\n";
    // directory_iterator behaves as a range in other ways, too
    std::ranges::for_each(
        std::filesystem::directory_iterator{sandbox},
        [](const auto& dir_entry) { std::cout << dir_entry << '\n'; });
 
    std::cout << "\nrecursive_directory_iterator:\n";
    for (auto const& dir_entry : std::filesystem::recursive_directory_iterator{sandbox}) 
        std::cout << dir_entry << '\n';
 
    // delete the sandbox dir and all contents within it, including subdirs
    std::filesystem::remove_all(sandbox);
}

```

Possible output:

```
directory_iterator:
"sandbox/file2.txt"
"sandbox/file1.txt"
"sandbox/dir1"
 
directory_iterator as a range:
"sandbox/file2.txt"
"sandbox/file1.txt"
"sandbox/dir1"
 
recursive_directory_iterator:
"sandbox/file2.txt"
"sandbox/file1.txt"
"sandbox/dir1"
"sandbox/dir1/dir2"

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3480 | C++20 | `directory_iterator` was neither a `borrowed_range` nor a `view` | it is both |

### See also

|  |  |
| --- | --- |
| recursive_directory_iterator(C++17) | an iterator to the contents of a directory and its subdirectories   (class) |
| directory_options(C++17) | options for iterating directory contents   (enum) |
| directory_entry(C++17) | a directory entry   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/directory_iterator&oldid=177395>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 October 2024, at 19:38.