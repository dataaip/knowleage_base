# std::fsetpos

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopen | | | | | | freopen | | | | | | fclose | | | | | | fflush | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwide | | | | | | setbuf | | | | | | setvbuf | | | | | |  | | | | | | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetcgetc | | | | | | fgets | | | | | | fputcputc | | | | | | fputs | | | | | | getchar | | | | | | gets(until C++14) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc | | | | | | fgetws | | | | | | fputwcputwc | | | | | | fputws | | | | | | getwchar | | | | | | putwchar | | | | | | ungetwc | | | | | |  | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanf | | | | | | vscanfvfscanfvsscanf(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wscanffwscanfswscanf | | | | | | vwscanfvfwscanfvswscanf(C++11)(C++11)(C++11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintf(C++11) | | | | | | vprintfvfprintfvsprintfvsnprintf(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wprintffwprintfswprintf | | | | | | vwprintfvfwprintfvswprintf | | | | | | | File positioning | | | | | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | ****fsetpos**** | | | | | | rewind | | | | | | Error handling | | | | | | clearerr | | | | | | feof | | | | | | ferror | | | | | | perror | | | | | | Operations on files | | | | | | remove | | | | | | rename | | | | | | tmpfile | | | | | | tmpnam | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstdio>` |  |  |
| int fsetpos( std::FILE\* stream, const std::fpos_t\* pos ); |  |  |
|  |  |  |

Sets the file position indicator and the multibyte parsing state (if any) for the C file stream `stream` according to the value pointed to by `pos`.

Besides establishing new parse state and position, a call to this function undoes the effects of std::ungetc and clears the end-of-file state, if it is set.

If a read or write error occurs, the error indicator (std::ferror) for the stream is set.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | file stream to modify |
| pos | - | pointer to a fpos_t object obtained from std::fgetpos called on a stream associated with the same file |

### Return value

​0​ upon success, nonzero value otherwise. Also, sets errno on failure.

### Notes

After seeking to a non-end position in a wide stream, the next call to any output function may render the remainder of the file undefined, e.g. by outputting a multibyte sequence of a different length.

### Example

Run this code

```
#include <cstdio>
#include <cstdlib>
 
int main()
{
    // Prepare an array of floating-point values.
    const int SIZE = 5;
    double A[SIZE] = {1., 2., 3., 4., 5.};
    // Write array to a file.
    std::FILE * fp = std::fopen("test.bin", "wb");
    std::fwrite(A, sizeof(double), SIZE, fp);
    std::fclose(fp);
 
    // Read the values into array B.
    double B[SIZE];
    fp = std::fopen("test.bin", "rb");
    std::fpos_t pos;
    if (std::fgetpos(fp, &pos) != 0)      // current position: start of file
    {
       std::perror("fgetpos()");
       std::fprintf(stderr, "fgetpos() failed in file %s at line # %d\n",
                    __FILE__, __LINE__-3);
       std::exit(EXIT_FAILURE);
    }
 
    int ret_code = std::fread(B, sizeof(double), 1, fp);      // read one value
    // current position: after reading one value
    std::printf("%.1f; read count = %d\n", B[0], ret_code);   // print one value and ret_code
 
    if (std::fsetpos(fp, &pos) != 0)   // reset current position to start of file
    {
       if (std::ferror(fp))
       {
          std::perror("fsetpos()");
          std::fprintf(stderr, "fsetpos() failed in file %s at line # %d\n",
                       __FILE__, __LINE__-5);
          std::exit(EXIT_FAILURE);
       }
    }
 
    ret_code = std::fread(B, sizeof(double), 1, fp);         // re-read first value
    std::printf("%.1f; read count = %d\n", B[0], ret_code);  // print one value and ret_code
    std::fclose(fp);
 
    return EXIT_SUCCESS; 
}

```

Output:

```
1.0; read count = 1
1.0; read count = 1

```

### See also

|  |  |
| --- | --- |
| fgetpos | gets the file position indicator   (function) |
| ftell | returns the current file position indicator   (function) |
| fseek | moves the file position indicator to a specific location in a file   (function) |
| C documentation for fsetpos | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/c/fsetpos&oldid=127258>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 February 2021, at 10:09.