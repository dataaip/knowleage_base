# std::ios_base

From cppreference.com
< cpp‎ | io
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
| ****ios_base**** | | | | |
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

****std::ios_base****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ios_base::ios_base | | | | |
| ios_base::~ios_base | | | | |
| ios_base::operator= | | | | |
| Formatting | | | | |
| ios_base::flags | | | | |
| ios_base::setf | | | | |
| ios_base::unsetf | | | | |
| ios_base::precision | | | | |
| ios_base::width | | | | |
| Locales | | | | |
| ios_base::imbue | | | | |
| ios_base::getloc | | | | |
| Internal extensible array | | | | |
| ios_base::xalloc | | | | |
| ios_base::iword | | | | |
| ios_base::pword | | | | |
| Miscellaneous | | | | |
| ios_base::register_callback | | | | |
| ios_base::sync_with_stdio | | | | |
| Member classes | | | | |
| ios_base::failure | | | | |
| ios_base::Init | | | | |
| Member types | | | | |
| ios_base::openmode | | | | |
| ios_base::fmtflags | | | | |
| ios_base::iostate | | | | |
| ios_base::seekdir | | | | |
| ios_base::event | | | | |
| ios_base::event_callback | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ios>` |  |  |
| class ios_base; |  |  |
|  |  |  |

The class `ios_base` is a multipurpose class that serves as the base class for all I/O stream classes. It maintains several kinds of data:

1) state information: stream status flags.2) control information: flags that control formatting of both input and output sequences and the imbued locale.3) private storage: indexed extensible data structure that allows both long and void\* members, which may be implemented as two arbitrary-length arrays or a single array of two-element structs or another container.4) callbacks: arbitrary number of user-defined functions to be called from imbue(), std::basic_ios::copyfmt(), and ~ios_base().

Typical implementation holds member constants corresponding to all values of fmtflags, iostate, openmode, and seekdir shown below, member variables to maintain current precision, width, and formatting flags, the exception mask, the buffer error state, a resizeable container holding the callbacks, the currently imbued locale, the private storage, and a static integer variable for xalloc().

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the object   (protected member function) |
| (destructor)[virtual] | destructs the object   (virtual public member function) |
| operator= | assigns to the stream   (public member function) |
| Formatting | |
| flags | manages format flags   (public member function) |
| setf | sets specific format flag   (public member function) |
| unsetf | clears specific format flag   (public member function) |
| precision | manages decimal precision of floating point operations   (public member function) |
| width | manages field width   (public member function) |
| Locales | |
| imbue | sets locale   (public member function) |
| getloc | returns current locale   (public member function) |
| Internal extensible array | |
| xalloc[static] | returns a program-wide unique integer that is safe to use as index to pword() and iword()   (public static member function) |
| iword | resizes the private storage if necessary and access to the long element at the given index   (public member function) |
| pword | resizes the private storage if necessary and access to the void\* element at the given index   (public member function) |
| Miscellaneous | |
| register_callback | registers event callback function   (public member function) |
| sync_with_stdio[static] | sets whether C++ and C I/O libraries are interoperable   (public static member function) |
| Member classes | |
| failure | stream exception   (public member class) |
| Init | initializes standard stream objects   (public member class) |

|  |  |
| --- | --- |
| Member types and constants | |
| Type | Explanation |
| openmode | stream open mode type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | app | seek to the end of stream before each write | | binary | open in binary mode | | in | open for reading | | out | open for writing | | trunc | discard the contents of the stream when opening | | ate | seek to the end of stream immediately after open | | noreplace (C++23) | open in exclusive mode |    (typedef) |
| fmtflags | formatting flags type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | dec | use decimal base for integer I/O: see std::dec | | oct | use octal base for integer I/O: see std::oct | | hex | use hexadecimal base for integer I/O: see std::hex | | basefield | dec | oct | hex. Useful for masking operations | | left | left adjustment (adds fill characters to the right): see std::left | | right | right adjustment (adds fill characters to the left): see std::right | | internal | internal adjustment (adds fill characters to the internal designated point): see std::internal | | adjustfield | left | right | internal. Useful for masking operations | | scientific | generate floating point types using scientific notation, or hex notation if combined with fixed: see std::scientific | | fixed | generate floating point types using fixed notation, or hex notation if combined with scientific: see std::fixed | | floatfield | scientific | fixed. Useful for masking operations | | boolalpha | insert and extract bool type in alphanumeric format: see std::boolalpha | | showbase | generate a prefix indicating the numeric base for integer output, require the currency indicator in monetary I/O: see std::showbase | | showpoint | generate a decimal-point character unconditionally for floating-point number output: see std::showpoint | | showpos | generate a + character for non-negative numeric output: see std::showpos | | skipws | skip leading whitespace before certain input operations: see std::skipws | | unitbuf | flush the output after each output operation: see std::unitbuf | | uppercase | replace certain lowercase letters with their uppercase equivalents in certain output operations: see std::uppercase |    (typedef) |
| iostate | state of the stream type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | goodbit | no error | | badbit | irrecoverable stream error | | failbit | input/output operation failed (formatting or extraction error) | | eofbit | associated input sequence has reached end-of-file |    (typedef) |
| seekdir | seeking direction type The following constants are also defined:   |  |  | | --- | --- | | Constant | Explanation | | beg | the beginning of a stream | | end | the ending of a stream | | cur | the current position of stream position indicator |    (typedef) |
| event | specifies event type   (enum) |
| event_callback | callback function type   (typedef) |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  | | --- | --- | | Deprecated member types | | | Type | Explanation | | `io_state` (deprecated) | integer type that may be used like `iostate` | | `open_mode` (deprecated) | integer type that may be used like `openmode` | | `seek_dir` (deprecated) | integer type that may be used like `seekdir` | | `streamoff` (deprecated) | unspecified type that may be used like `off_type`, not necessarily std::streamoff | | `streampos` (deprecated) | unspecified type that may be used like `pos_type`, not necessarily std::streampos | | (until C++17) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 1357 (N3110) | C++98 | `std::ios_base` defined operator~, operator& and operator| for types `openmode`, `fmtflags` and `iostate`, violating the requirements of BitmaskType[[1]](ios_base.html#cite_note-1) | removed these definitions |

1. ↑ A BitmaskType needs to support bitwise opertaions on its own. The bitwise operation support should not be provided externally.

### See also

|  |  |
| --- | --- |
| basic_ios | manages an arbitrary stream buffer   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/ios_base&oldid=156251>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 August 2023, at 21:38.