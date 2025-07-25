# std::ftell

From cppreference.com
< cpp‎ | io‎ | c
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

C-style I/O

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | |
| Functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopen | | | | | | freopen | | | | | | fclose | | | | | | fflush | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwide | | | | | | setbuf | | | | | | setvbuf | | | | | |  | | | | | | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetcgetc | | | | | | fgets | | | | | | fputcputc | | | | | | fputs | | | | | | getchar | | | | | | gets(until C++14) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc | | | | | | fgetws | | | | | | fputwcputwc | | | | | | fputws | | | | | | getwchar | | | | | | putwchar | | | | | | ungetwc | | | | | |  | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanf | | | | | | vscanfvfscanfvsscanf(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wscanffwscanfswscanf | | | | | | vwscanfvfwscanfvswscanf(C++11)(C++11)(C++11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintf(C++11) | | | | | | vprintfvfprintfvsprintfvsnprintf(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wprintffwprintfswprintf | | | | | | vwprintfvfwprintfvswprintf | | | | | | | File positioning | | | | | | ****ftell**** | | | | | | fgetpos | | | | | | fseek | | | | | | fsetpos | | | | | | rewind | | | | | | Error handling | | | | | | clearerr | | | | | | feof | | | | | | ferror | | | | | | perror | | | | | | Operations on files | | | | | | remove | | | | | | rename | | | | | | tmpfile | | | | | | tmpnam | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstdio>` |  |  |
| long ftell( std::FILE\* stream ); |  |  |
|  |  |  |

Returns the current value of the file position indicator for the file stream `stream`.

If the stream is open in binary mode, the value obtained by this function is the number of bytes from the beginning of the file.

If the stream is open in text mode, the value returned by this function is unspecified and is only meaningful as the input to std::fseek.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | file stream to examine |

### Return value

File position indicator on success or -1L if failure occurs. Also sets errno on failure.

### Notes

On Windows, `_ftelli64` can be used to work with files larger than 2 GiB.

### Example

Demonstrates `std::ftell()` with error checking. Writes then reads a few floating-point (FP) values to/from a file.

Run this code

```
#include <cstdio>
#include <cstdlib>
#include <iostream>
 
// If the condition is not met then exit the program with error message.
void check(bool condition, const char* func, int line)
{
    if (condition)
        return;
    std::perror(func);
    std::cerr << func << " failed in file " << __FILE__ << " at line # " << line - 1
              << '\n';
    std::exit(EXIT_FAILURE);
}
 
int main()
{
    // Prepare an array of FP values.
    constexpr int SIZE {5};
    double A[SIZE] = {1.1, 2.2, 3.3, 4.4, 5.5};
 
    // Write array to a file.
    const char* fname = "/tmp/test.bin";
    FILE* file = std::fopen(fname, "wb");
    check(file != NULL, "fopen()", __LINE__);
 
    const int write_count = std::fwrite(A, sizeof(double), SIZE, file);
    check(write_count == SIZE, "fwrite()", __LINE__);
 
    std::fclose(file);
 
    // Read the FP values into array B.
    double B[SIZE];
    file = std::fopen(fname, "rb");
    check(file != NULL, "fopen()", __LINE__);
 
    long pos = std::ftell(file); // position indicator at start of file
    check(pos != -1L, "ftell()", __LINE__);
    std::cout << "pos: " << pos << '\n';
 
    const int read_count = std::fread(B, sizeof(double), 1, file); // read one FP value
    check(read_count == 1, "fread()", __LINE__);
 
    pos = std::ftell(file); // position indicator after reading one FP value
    check(pos != -1L, "ftell()", __LINE__);
    std::cout << "pos: " << pos << '\n';
    std::cout << "B[0]: " << B[0] << '\n'; // print one FP value
 
    return EXIT_SUCCESS;
}

```

Possible output:

```
pos: 0
pos: 8
B[0]: 1.1

```

### See also

|  |  |
| --- | --- |
| fgetpos | gets the file position indicator   (function) |
| fseek | moves the file position indicator to a specific location in a file   (function) |
| fsetpos | moves the file position indicator to a specific location in a file   (function) |
| tellg | returns the input position indicator   (public member function of `std::basic_istream<CharT,Traits>`) |
| tellp | returns the output position indicator   (public member function of `std::basic_ostream<CharT,Traits>`) |
| C documentation for ftell | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/c/ftell&oldid=178172>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 December 2024, at 08:16.