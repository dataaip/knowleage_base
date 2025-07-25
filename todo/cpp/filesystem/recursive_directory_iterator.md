# std::filesystem::recursive_directory_iterator

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::path | | | | | | filesystem::filesystem_error | | | | | | filesystem::directory_entry | | | | | | filesystem::directory_iterator | | | | | | ****filesystem::recursive_directory_iterator**** | | | | | | filesystem::file_status | | | | | | filesystem::space_info | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::file_type | | | | | | filesystem::file_time_type | | | | | | filesystem::perms | | | | | | filesystem::perm_options | | | | | | filesystem::copy_options | | | | | | filesystem::directory_options | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::absolute | | | | | | filesystem::canonicalfilesystem::weakly_canonical | | | | | | filesystem::relativefilesystem::proximate | | | | | | filesystem::copy | | | | | | filesystem::copy_file | | | | | | filesystem::copy_symlink | | | | | | filesystem::create_directory filesystem::create_directories | | | | | | filesystem::create_hard_link | | | | | | filesystem::create_symlink filesystem::create_directory_symlink | | | | | | filesystem::current_path | | | | | | filesystem::temp_directory_path | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::exists | | | | | | filesystem::equivalent | | | | | | filesystem::file_size | | | | | | filesystem::hard_link_count | | | | | | filesystem::last_write_time | | | | | | filesystem::permissions | | | | | | filesystem::read_symlink | | | | | | filesystem::remove filesystem::remove_all | | | | | | filesystem::rename | | | | | | filesystem::resize_file | | | | | | filesystem::space | | | | | | filesystem::status filesystem::symlink_status | | | | | |
| File types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_block_file | | | | | | filesystem::is_character_file | | | | | | filesystem::is_directory | | | | | | filesystem::is_empty | | | | | | filesystem::status_known | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | filesystem::is_fifo | | | | | | filesystem::is_other | | | | | | filesystem::is_regular_file | | | | | | filesystem::is_socket | | | | | | filesystem::is_symlink | | | | | |

****std::filesystem::recursive_directory_iterator****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| recursive_directory_iterator::recursive_directory_iterator | | | | |
| recursive_directory_iterator::operator\*recursive_directory_iterator::operator-> | | | | |
| recursive_directory_iterator::options | | | | |
| recursive_directory_iterator::depth | | | | |
| recursive_directory_iterator::recursion_pending | | | | |
| recursive_directory_iterator::operator= | | | | |
| recursive_directory_iterator::incrementrecursive_directory_iterator::operator++ | | | | |
| recursive_directory_iterator::pop | | | | |
| recursive_directory_iterator::disable_recursion_pending | | | | |
| Non-member functions | | | | |
| begin(std::filesystem::recursive_directory_iterator)end(std::filesystem::recursive_directory_iterator) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<filesystem>` |  |  |
| class recursive_directory_iterator; |  | (since C++17) |
|  |  |  |

`recursive_directory_iterator` is a LegacyInputIterator that iterates over the directory_entry elements of a directory, and, recursively, over the entries of all subdirectories. The iteration order is unspecified, except that each directory entry is visited only once.

By default, symlinks are not followed, but this can be enabled by specifying the directory option follow_directory_symlink at construction time.

The special pathnames dot and dot-dot are skipped.

If the `recursive_directory_iterator` reports an error or is advanced past the last directory entry of the top-level directory, it becomes equal to the default-constructed iterator, also known as the end iterator. Two end iterators are always equal, dereferencing or incrementing the end iterator is undefined behavior.

If a file or a directory is deleted or added to the directory tree after the recursive directory iterator has been created, it is unspecified whether the change would be observed through the iterator.

If the directory structure contains cycles, the end iterator may be unreachable.

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
| (constructor) | constructs a recursive directory iterator   (public member function) |
| (destructor) | default destructor   (public member function) |
| Observers | |
| operator\*operator-> | accesses the pointed-to entry   (public member function) |
| options | returns the currently active options that affect the iteration   (public member function) |
| depth | returns the current recursion depth   (public member function) |
| recursion_pending | checks whether the recursion is disabled for the current directory   (public member function) |
| Modifiers | |
| operator= | assigns contents   (public member function) |
| incrementoperator++ | advances to the next entry   (public member function) |
| pop | moves the iterator one level up in the directory hierarchy   (public member function) |
| disable_recursion_pending | disables recursion until the next increment   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| begin(std::filesystem::recursive_directory_iterator)end(std::filesystem::recursive_directory_iterator) | range-based for loop support   (function) |

Additionally, `operator==` and `operator!=` are(until C++20)`operator==` is(since C++20) provided as required by LegacyInputIterator.

It is unspecified whether `operator!=` is provided because it can be synthesized from `operator==`, and(since C++20) whether an equality operator is a member or non-member.

### Helper specializations

|  |  |  |
| --- | --- | --- |
| template<>  constexpr bool ranges::enable_borrowed_range<std::filesystem::recursive_directory_iterator> = true; |  | (since C++20) |
| template<>  constexpr bool ranges::enable_view<std::filesystem::recursive_directory_iterator> = true; |  | (since C++20) |
|  |  |  |

These specializations for `recursive_directory_iterator` make it a `borrowed_range` and a `view`.

### Notes

A `recursive_directory_iterator` typically holds a reference-counted **pointer** (to satisfy shallow-copy semantics of LegacyInputIterator) to an implementation object, which holds:

- a container (such as std::vector) of non-recursive directory_iterators that forms the recursion stack,
- the recursion depth counter (accessible with depth()),
- the directory options used at construction (accessible with options()),
- the pending recursion flag (accessible with recursion_pending(), may be combined with the directory options to save space).

### Example

Run this code

```
#include <filesystem>
#include <fstream>
#include <iostream>
#include <string>
namespace fs = std::filesystem;
 
int main()
{
    std::filesystem::current_path(std::filesystem::temp_directory_path());
    std::filesystem::create_directories("sandbox/a/b");
    std::ofstream("sandbox/file1.txt");
    std::filesystem::create_symlink("a", "sandbox/syma");
 
    // Iterate over the std::filesystem::directory_entry elements explicitly
    auto entry_length{3UZ};
    for (const fs::directory_entry& dir_entry :
            fs::recursive_directory_iterator("sandbox"))
    {
        std::cout << dir_entry << '\n';
        if (auto l{dir_entry.path().string().length()}; entry_length < l)
            entry_length = l;
    }
    std::cout << std::string(entry_length + 2, '-') << '\n';
 
    // Iterate over the std::filesystem::directory_entry elements using `auto`
    for (auto const& dir_entry : fs::recursive_directory_iterator("sandbox"))
        std::cout << dir_entry << '\n';
 
    std::filesystem::remove_all("sandbox");
}

```

Possible output:

```
"sandbox/syma"
"sandbox/file1.txt"
"sandbox/a"
"sandbox/a/b"
-------------------
"sandbox/syma"
"sandbox/file1.txt"
"sandbox/a"
"sandbox/a/b"

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3480 | C++20 | `recursive_directory_iterator` was neither a `borrowed_range` nor a `view` | it is both |

### See also

|  |  |
| --- | --- |
| directory_iterator(C++17) | an iterator to the contents of the directory   (class) |
| directory_entry(C++17) | a directory entry   (class) |
| directory_options(C++17) | options for iterating directory contents   (enum) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/filesystem/recursive_directory_iterator&oldid=177394>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 October 2024, at 19:36.