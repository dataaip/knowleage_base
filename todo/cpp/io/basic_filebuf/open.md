# std::basic_filebuf<CharT,Traits>::open

From cppreference.com
< cpp‎ | io‎ | basic filebuf
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

Input/output library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| I/O manipulators | | | | |
| Print functions (C++23) | | | | |
| C-style I/O | | | | |
| Buffers | | | | |
| basic_streambuf | | | | |
| basic_filebuf | | | | |
| basic_stringbuf | | | | |
| basic_spanbuf(C++23) | | | | |
| strstreambuf(C++98/26\*) | | | | |
| basic_syncbuf(C++20) | | | | |
| Streams | | | | |
| Abstractions | | | | |
| ios_base | | | | |
| basic_ios | | | | |
| basic_istream | | | | |
| basic_ostream | | | | |
| basic_iostream | | | | |
| File I/O | | | | |
| basic_ifstream | | | | |
| basic_ofstream | | | | |
| basic_fstream | | | | |
| String I/O | | | | |
| basic_istringstream | | | | |
| basic_ostringstream | | | | |
| basic_stringstream | | | | |
| Array I/O | | | | |
| basic_ispanstream(C++23) | | | | |
| basic_ospanstream(C++23) | | | | |
| basic_spanstream(C++23) | | | | |
| istrstream(C++98/26\*) | | | | |
| ostrstream(C++98/26\*) | | | | |
| strstream(C++98/26\*) | | | | |
| Synchronized Output | | | | |
| basic_osyncstream(C++20) | | | | |
| Types | | | | |
| streamoff | | | | |
| streamsize | | | | |
| fpos | | | | |
| Error category interface | | | | |
| iostream_category(C++11) | | | | |
| io_errc(C++11) | | | | |

std::basic_filebuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_filebuf::basic_filebuf | | | | |
| basic_filebuf::~basic_filebuf | | | | |
| basic_filebuf::operator=(C++11) | | | | |
| basic_filebuf::swap(C++11) | | | | |
| basic_filebuf::native_handle(C++26) | | | | |
| basic_filebuf::is_open | | | | |
| ****basic_filebuf::open**** | | | | |
| basic_filebuf::close | | | | |
| Protected member functions | | | | |
| basic_filebuf::showmanyc | | | | |
| basic_filebuf::underflow | | | | |
| basic_filebuf::uflow | | | | |
| basic_filebuf::pbackfail | | | | |
| basic_filebuf::overflow | | | | |
| basic_filebuf::setbuf | | | | |
| basic_filebuf::seekoff | | | | |
| basic_filebuf::seekpos | | | | |
| basic_filebuf::sync | | | | |
| basic_filebuf::imbue | | | | |
| Non-member functions | | | | |
| swap(std::basic_filebuf)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_filebuf\* open( const char\* s, std::ios_base::openmode mode ); | (1) |  |
| basic_filebuf\* open( const std::string& str, std::ios_base::openmode mode ); | (2) | (since C++11) |
| basic_filebuf\* open( const std::filesystem::path& p,                       std::ios_base::openmode mode ); | (3) | (since C++17) |
| basic_filebuf\* open( const std::filesystem::path::value_type\* s,                       std::ios_base::openmode mode ); | (4) | (since C++17) |
|  |  |  |

If the associated file was already open (is_open() != false), returns a null pointer right away.

Otherwise, opens the file with the given name (s, p.c_str()(since C++17) or str.c_str(), depending on the overload). std::ios_base::openmode values may be written as, e.g., std::ios_base::out | std::ios_base::app.

|  |  |
| --- | --- |
| Overload (4) is only provided if `std::filesystem::path::value_type` is not char. | (since C++17) |

The file is opened as if by calling std::fopen with the second argument (file access mode) determined by the result of mode & ~std::ios_base::ate as follows, `open()` fails if the result is not some combination of flags shown in the table:

| mode & ~std::ios_base::ate | | | | | | ﻿std::fopen ﻿ access mode | Action if file already exists | Action if file does not exist |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| binary | in | out | trunc | app | noreplace (since C++23) |
| - | + | - | - | - | - | "r" | Read from start | Failure to open |
| + | + | - | - | - | - | "rb" |
| - | + | + | - | - | - | "r+" | Error |
| + | + | + | - | - | - | "r+b" |
| - | - | + | - | - | - | "w" | Destroy contents | Create new |
| - | - | + | + | - | - |
| + | - | + | - | - | - | "wb" |
| + | - | + | + | - | - |
| - | + | + | + | - | - | "w+" |
| + | + | + | + | - | - | "w+b" |
| - | - | + | - | - | + | "wx" | Failure to open | Create new |
| - | - | + | + | - | + |
| + | - | + | - | - | + | "wbx" |
| + | - | + | + | - | + |
| - | + | + | + | - | + | "w+x" |
| + | + | + | + | - | + | "w+bx" |
| - | - | + | - | + | - | "a" | Write to end | Create new |
| - | - | - | - | + | - |
| + | - | + | - | + | - | "ab" |
| + | - | - | - | + | - |
| - | + | + | - | + | - | "a+" |
| - | + | - | - | + | - |
| + | + | + | - | + | - | "a+b" |
| + | + | - | - | + | - |

If the open operation succeeds and (openmode & std::ios_base::ate) != 0 (the `ate` bit is set), repositions the file position to the end of file, as if by calling std::fseek(file, 0, SEEK_END), where file is the pointer returned by calling std::fopen. If the repositioning fails, calls close() and returns a null pointer to indicate failure.

### Parameters

|  |  |  |
| --- | --- | --- |
| s, str, p | - | the file name to open; s must point to a null-terminated string |
| openmode | - | the file opening mode, a binary OR of the std::ios_base::openmode modes |

### Return value

this on success, a null pointer on failure.

### Notes

`open()` is typically called through the constructor or the `open()` member function of std::basic_fstream.

### Example

Run this code

```
#include <fstream>
#include <iostream>
 
int main()
{
    std::string filename = "Test.b";
    std::filebuf fb;
 
    // prepare a file to read
    double d = 3.14;
    if (!fb.open(filename, std::ios::binary | std::ios::out))
    {
        std::cout << "Open file " << filename << " for write failed\n";
        return 1;
    } 
    fb.sputn(reinterpret_cast<char*>(&d), sizeof d);
    fb.close();
 
    // open file for reading
    double d2 = 0.0;
    if (!fb.open(filename, std::ios::binary | std::ios::in))
    {
        std::cout << "Open file " << filename << " for read failed\n";
        return 1;
    }
 
    auto got = fb.sgetn(reinterpret_cast<char*>(&d2), sizeof d2);
    if (sizeof(d2) != got)
        std::cout << "Read of " << filename << " failed\n";
    else
        std::cout << "Read back from file: " << d2 << '\n';
}

```

Output:

```
Read back from file: 3.14

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 596 | C++98 | `open()` could not open files in append mode | can open in append mode |

### See also

|  |  |
| --- | --- |
| is_open | checks if the associated file is open   (public member function) |
| close | flushes the put area buffer and closes the associated file   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_filebuf/open&oldid=155280>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 July 2023, at 22:32.