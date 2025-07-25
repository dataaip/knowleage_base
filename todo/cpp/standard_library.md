# C++ Standard Library

From cppreference.com
< cpp
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| ****Standard library**** | | | | |
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

****Standard library****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Customization point object (C++20) | | | | |
| Exposition-only entities | | | | |
| **decay-copy**(C++11) | | | | |
| **synth-three-way****synth-three-way-result**(C++20)(C++20) | | | | |

The C++ standard library provides a wide range of facilities that are usable in standard C++.

### Category

The language support library provides components that are required by certain parts of the C++ language, such as memory allocation (new/delete) and exception processing.

|  |  |
| --- | --- |
| The concepts library describes library components that C++ programs may use to perform compile-time validation of template arguments and perform function dispatch based on properties of types. | (since C++20) |

The diagnostics library provides a consistent framework for reporting errors in a C++ program, including predefined exception classes.

The memory management library provides components for memory management, including smart pointers and scoped allocator(since C++11).

|  |  |
| --- | --- |
| The metaprogramming library describes facilities for use in templates and during constant evaluation, including type traits, integer sequence,(since C++14) and rational arithmetic. | (since C++11) |

The general utilities library includes components used by other library elements, such as a predefined storage allocator for dynamic storage management, and components used as infrastructure in C++ programs, such as tuples and(since C++11) function wrappers.

The containers, iterators, ranges(since C++20), and algorithms libraries provide a C++ program with access to a subset of the most widely used algorithms and data structures.

The strings library provides support for manipulating text represented as homogeneous sequences of following types: char, char8_t(since C++20), char16_t, char32_t(since C++11), wchar_t, and any other character-like types.

The text processing library provides regular expression matching and searching(since C++11), utilities for text formatting(since C++20) and identifying text encodings(since C++26), and localization facilities.

The numerics library provides numeric algorithms and complex number components that extend support for numeric processing. The valarray component provides support for n-at-a-time processing, potentially implemented as parallel operations on platforms that support such processing. The random number component provides facilities for generating pseudo-random numbers.(since C++11)

The time library provides generally useful time utilities.

The input/output library provides the iostream components that are the primary mechanism for C++ program input and output. They can be used with other elements of the library, particularly strings, locales, and iterators.

|  |  |
| --- | --- |
| The thread support library provides components to create and manage threads, including atomic operations, mutual exclusion, and inter-thread communication. | (since C++11) |

|  |  |
| --- | --- |
| The execution support library provides a framework for managing asynchronous execution on generic execution resources. | (since C++26) |

### Library contents

The C++ standard library provides definitions for the entities and macros described in the synopses of the C++ standard library headers, unless otherwise specified.

All library entities except operator new and operator delete are defined within the namespace std or namespaces nested within namespace std (except the entities for the C standard library facilities, see below). It is unspecified whether names declared in a specific namespace are declared directly in that namespace or in an inline namespace inside that namespace.(since C++11)

#### Headers

Each element of the C++ standard library is declared or defined (as appropriate) in a **header**. A header is not necessarily a source file, nor are the sequences delimited by `<` and `>` in header names necessarily valid source file names.

The C++ standard library provides the **C++ library headers** and **additional C++ headers for C library facilities** (see 'headers' page for descriptions):

| C++ library headers | | | | |
| --- | --- | --- | --- | --- |
| <algorithm> | <iomanip> | <list> | <ostream> | <streambuf> |
| <bitset> | <ios> | <locale> | <queue> | <string> |
| <complex> | <iosfwd> | <map> | <set> | <typeinfo> |
| <deque> | <iostream> | <memory> | <sstream> | <utility> |
| <exception> | <istream> | <new> | <stack> | <valarray> |
| <fstream> | <iterator> | <numeric> | <stdexcept> | <vector> |
| <functional> | <limits> |  |  |  |
| Headers added in C++11 | | | | |
| <array> | <condition_variable> | <mutex> | <scoped_allocator> | <type_traits> |
| <atomic> | <forward_list> | <random> | <system_error> | <typeindex> |
| <chrono> | <future> | <ratio> | <thread> | <unordered_map> |
| <codecvt> | <initializer_list> | <regex> | <tuple> | <unordered_set> |
| Headers added in C++14 | | | | |
| <shared_mutex> |  |  |  |  |
| Headers added in C++17 | | | | |
| <any> | <execution> | <memory_resource> | <string_view> | <variant> |
| <charconv> | <filesystem> | <optional> |  |  |
| Headers added in C++20 | | | | |
| <barrier> | <concepts> | <latch> | <semaphore> | <stop_token> |
| <bit> | <coroutine> | <numbers> | <source_location> | <syncstream> |
| <compare> | <format> | <ranges> | <span> | <version> |
| Headers added in C++23 | | | | |
| <expected> | <flat_set> | <mdspan> | <spanstream> | <stdfloat> |
| <flat_map> | <generator> | <print> | <stacktrace> |  |
| Headers added in C++26 | | | | |
| <debugging> | <inplace_vector> | <rcu> | <simd> | <text_encoding> |
| <hazard_pointer> | <linalg> |  |  |  |
| Removed headers | | | | |
| <codecvt> | (since C++11)(deprecated in C++17)(removed in C++26) | | | |
| <strstream> | (deprecated in C++98)(removed in C++26) | | | |

| C++ headers for C library facilities | | | |
| --- | --- | --- | --- |
| <cassert> | <clocale> | <cstdarg> | <cstring> |
| <cctype> | <cmath> | <cstddef> | <ctime> |
| <cerrno> | <csetjmp> | <cstdio> | <cwchar> |
| <cfloat> | <csignal> | <cstdlib> | <cwctype> |
| <climits> |  |  |  |
| Headers added in C++11 | | | |
| <cfenv> | <cinttypes> | <cstdint> | <cuchar> |
| Removed headers | | | | |
| <ccomplex> | (since C++11)(deprecated in C++17)(removed in C++20) | | | |
| <ciso646> | (removed in C++20) | | | |
| <cstdalign> | (since C++11)(deprecated in C++17)(removed in C++20) | | | |
| <cstdbool> | (since C++11)(deprecated in C++17)(removed in C++20) | | | |
| <ctgmath> | (since C++11)(deprecated in C++17)(removed in C++20) | | | |

A freestanding implementation has an implementation-defined set of headers, see here for the minimal requirement on the set of headers.

### C standard library

The C++ standard library also makes available the facilities of the C standard library, suitably adjusted to ensure static type safety. The descriptions of many library functions rely on the C standard library for the semantics of those functions.

In some cases, the signatures specified in standard C++ may be different from the signatures in the C standard library, and additional overloads may be declared, but the behavior and the preconditions (including those implied by C's restrict)(since C++17) are the same unless otherwise stated.

For compatibility with the C standard library, the C++ standard library provides the C headers listed below. The intended use of these headers is for interoperability only. It is possible that C++ source files need to include one of these headers in order to be valid ISO C. Source files that are not intended to also be valid ISO C should not use any of the C headers. See here for descriptions.

| C headers | | | |
| --- | --- | --- | --- |
| <assert.h> | <limits.h> | <stdarg.h> | <string.h> |
| <ctype.h> | <locale.h> | <stddef.h> | <time.h> |
| <errno.h> | <math.h> | <stdio.h> | <wchar.h> |
| <float.h> | <setjmp.h> | <stdlib.h> | <wctype.h> |
| <iso646.h> | <signal.h> |  |  |
| Headers added in C++11 | | | |
| <complex.h> | <inttypes.h> | <stdbool.h> | <tgmath.h> |
| <fenv.h> | <stdalign.h> | <stdint.h> | <uchar.h> |
| Headers added in C++23 | | | |
| <stdatomic.h> |  |  |  |
| Headers added in C++26 | | | |
| <stdbit.h>") | <stdchkint.h>") |  |  |

Except otherwise noted, the contents of each header `cxxx` is the same as that of the corresponding header `xxx.h` as specified in the C standard library. In the C++ standard library, however, the declarations (except for names which are defined as macros in C) are within namespace scope of the namespace std. It is unspecified whether these names (including any overloads added) are first declared within the global namespace scope and are then injected into namespace std by explicit using-declarations.

Names which are defined as macros in C (assert, offsetof, setjmp, va_arg, va_end and va_start) must be defined as macros in the C++ standard library, even if C grants license for implementation as functions.

Names that are defined as functions in C must be defined as functions in the C++ standard library. This disallows the practice, allowed in C, of providing a masking macro in addition to the function prototype. The only way to achieve equivalent inline behavior in C++ is to provide a definition as an extern inline function.

Identifiers that are keywords or operators in C++ cannot be defined as macros in C++ standard library headers. In particular, including the standard header <iso646.h> has no effect.

#### Names associated with safe functions in standard C (since C++17)

If any C++ header is included, it is implementation-defined whether any of the following C standard Annex K names is declared in the global namespace (none of them is declared in namespace std):

| C standard Annex K names | | | |
| --- | --- | --- | --- |
| abort_handler_s | mbstowcs_s | strncat_s | vswscanf_s |
| asctime_s | memcpy_s | strncpy_s | vwprintf_s |
| bsearch_s | memmove_s | strtok_s | vwscanf_s |
| constraint_handler_t | memset_s | swprintf_s | wcrtomb_s |
| ctime_s | printf_s | swscanf_s | wcscat_s |
| errno_t | qsort_s | tmpfile_s | wcscpy_s |
| fopen_s | RSIZE_MAX | TMP_MAX_S | wcsncat_s |
| fprintf_s | rsize_t | tmpnam_s | wcsncpy_s |
| freopen_s | scanf_s | vfprintf_s | wcsnlen_s |
| fscanf_s | set_constraint_handler_s | vfscanf_s | wcsrtombs_s |
| fwprintf_s | snprintf_s | vfwprintf_s | wcstok_s |
| fwscanf_s | snwprintf_s | vfwscanf_s | wcstombs_s |
| gets_s | sscanf_s | vprintf_s | wmemcpy_s |
| gmtime_s | mbstowcs_s | vscanf_s | vswscanf_s |
| abort_handler_s | strcat_s | vsnprintf_s | wmemmove |
| ignore_handler_s | strcpy_s | vsnwprintf_s | wprintf_s |
| localtime_s | strerrorlen_s | vsprintf_s | wscanf_s |
| L_tmpnam_s | strerror_s | vsscanf_s |  |
| mbsrtowcs_s | strlen_s | vswprintf_s |  |

### Using the library

#### Including headers

The entities in the C++ standard library are defined in headers, whose contents are made available to a translation unit when it contains the appropriate #include preprocessing directive.

A translation unit may include library headers in any order. Each may be included more than once, with no effect different from being included exactly once, except that the effect of including either <cassert> or <assert.h> depends each time on the lexically current definition of NDEBUG.

A translation unit can only include a header outside of any declaration or definition, and lexically before the first reference in that translation unit to any of the entities declared in that header. No diagnostic is required.

|  |  |
| --- | --- |
| In module units, headers can only be included in global module fragments. | (since C++20) |

|  |  |
| --- | --- |
| Importing headers The C++ library headers, or, for a freestanding implementation, the subset of such headers that are provided by the implementation, are collectively known as the **importable C++ library headers**.  The contents of importable C++ library headers are made available to a translation unit when it contains the appropriate import declaration. | (since C++20) |
| Importing modules The C++ standard library provides the following **C++ library modules**:   - The named module std exports declarations in namespace `std` that are provided by the importable C++ library headers (e.g. std::rotr from <bit>) and the C++ headers for C library facilities (e.g. std::puts from <cstdio>). It additionally exports declarations in the global namespace for the storage allocation and deallocation functions that are provided by <new> (e.g. ::operator new). - The named module std.compat exports the same declarations as the named module std, and additionally exports declarations in the global namespace corresponding to the declarations in namespace `std` that are provided by the C++ headers for C library facilities (e.g. ::fclose).   For each declaration in the standard library,   - the module it attaches to is unspecified, and - it denotes the same entity regardless of whether it was made reachable through including a header, importing a header unit, or importing a C++ library module.  | Feature-test macro | Value | Std | Feature | | --- | --- | --- | --- | | `__cpp_lib_modules` | `202207L` | (C++23) | Standard library modules std and std.compat | | (since C++23) |

#### Linkage

Entities in the C++ standard library have storage duration#external linkage. Unless otherwise specified, objects and functions have the default extern "C++" linkage.

Whether a name from the C standard library declared with external linkage has extern "C" or extern "C++" linkage is implementation-defined. The C++ standard recommends using extern "C++" in this case.

Objects and functions defined in the library and required by a C++ program are included in the program prior to program startup.

### Requirements on standard library implementations

#### Guarantees

A C++ header must provide declarations and definitions that appear in

- the synopsis of that header, or
- the synopsis of another header which is appeared to be included in the synopsis of that header.

For types and macros defined in multiple headers (such as NULL), including any number of these headers in any order never violates the one definition rule.

Unless otherwise specified, all object-like macros defined by the C standard library that expand to integral constant expressions can be used in `#if` preprocessing directives.

Calling a standard library non-member function signature always results in actually calling that function. Therefore a conforming standard library implementation cannot define additional non-member functions that may be called by a valid C++ program.

Non-member function signatures are never declared with additional default arguments.

Unless otherwise specified, calls made by functions in the standard library to non-operator, non-member functions do not use functions from another namespace which are found through argument-dependent name lookup.

For each friend declaration of a function (template) within a class (template) definition, no other declaration is provided for that function (template).

|  |  |
| --- | --- |
| Standard library function signatures can only be declared as constexpr if they are required to be constexpr (libstdc++ cmath is notably non-conforming here). If a header provides any non-defining declarations of constexpr functions or constructors, the corresponding definitions should also be provided within that header.  Unless otherwise specified, each standard library function should meet each of the following requirements to prevent data races:   - A C++ standard library function cannot (directly or indirectly) access objects accessible by threads other than the current thread unless the objects are accessed (directly or indirectly) via the function’s arguments, including this. - A C++ standard library function cannot (directly or indirectly) modify objects accessible by threads other than the current thread unless the objects are accessed (directly or indirectly) via the function’s non-const arguments, including this.   - For example, an object with static storage duration cannot be used for internal purposes without synchronization because doing so can cause a data race even in programs that do not explicitly share objects between threads. - A C++ standard library function cannot access objects indirectly accessible via its arguments or via elements of its container arguments except by invoking functions required by its specification on those container elements. - An operation on iterators obtained by calling a standard library container or string member function can access, but not modify, the underlying container.   - In particular, container operations that invalidate iterators conflict with operations on iterators associated with that container. - A C++ standard library function can only perform all operations solely within the current thread if those operations have effects that are visible to users.   - Operations without visible side effects can be parallelized. | (since C++11) |

For each class defined in the C++ standard library required to be derived from another class defined in the C++ standard library,

- the base class must be virtual if it is specified as virtual,
- the base class cannot be virtual if it is not specified as virtual, and
- unless otherwise specified, types with distinct names shall be distinct types.

|  |  |
| --- | --- |
| Unless otherwise specified, all types specified in the C++ standard library are non-final types. | (since C++11) |

If a function defined in the C++ standard library is specified to throw an exception (in a particular situation) of a given type, the exception thrown can only have that type or a type derived from that type so that an exception handler for the base type can catch it.

Functions from the C standard library can only throw exceptions when such a function calls a program-supplied function that throws an exception (qsort() and bsearch() meet this condition).

Destructor operations defined in the C++ standard library never throw exceptions. Every destructor in the C++ standard library behaves as if it had a non-throwing exception specification.

|  |  |
| --- | --- |
| If a function in the C++ standard library report errors via a std::error_code object, that object's category() member must return std::system_category() for errors originating from the operating system, or a reference to an implementation-defined std::error_category object for errors originating elsewhere. The possible values of value() for each of these error categories should be defined.  Objects of types defined in the C++ standard library may be moved from. Move operations can either be explicitly specified or implicitly generated. Unless otherwise specified, such moved-from objects will be placed in a valid but unspecified state.  An object of a type defined in the C++ standard library may be move-assigned to itself. Unless otherwise specified, such an assignment places the object in a valid but unspecified state. | (since C++11) |

#### Implementation freedom

It is unspecified whether any member or non-member functions in the C++ standard library are defined as inline.

For a non-virtual C++ standard library member function, a different set of member function signatures can be declared, provided that any call to that member function that would select an overload from the given set of declarations behaves as if that overload was selected. This allows, for instance:

- adding parameters with default arguments,
- replacing a member function with default arguments with two or more member functions with equivalent behavior, or
- adding additional signatures for a member function name.

Unless otherwise specified, it is implementation-defined which functions in the C++ standard library may be recursively reentered.

|  |  |
| --- | --- |
| C++ standard library implementations can share their own internal objects between threads if the objects are not visible to users and are protected against data races. | (since C++11) |

It is unspecified whether any function signature or class in the C++ standard library is a friend of another class in the C++ standard library.

The names and global function signatures described here are reserved to the implementation.

Any class in the C++ standard library can be derived from a class with a name reserved to the implementation. If a class defined in the C++ standard library is required to be derived from other classes in the C++ standard library, that class can be derived directly from the required base or indirectly through a hierarchy of base classes with names reserved to the implementation.

If a function defined in the C++ standard library is not specified to throw an exception but does not have a non-throwing exception specification, the exception thrown is implementation-defined, but its type should be std::exception or any type derived from std::exception.

The exception specification for a non-virtual function can be strengthened by adding a non-throwing exception specification.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 1 | C++98 | the language linkages of the names from the C standard library were unspecified | they are implementation-defined |
| LWG 119 | C++98 | the exception specifications of virtual functions could be strengthened | only allowed for non-virtual functions |
| LWG 147 | C++98 | the specification on non-member functions only considered global functions | also considers non-global functions |
| LWG 225 | C++98 | standard library functions might call non-member functions from other namespaces due to argument-dependent lookup | prohibited unless otherwise specified |
| LWG 336 | C++98 | <strstream> was not a C++ library header | it is a C++ library header |
| LWG 343 | C++98 | library header dependencies were not specified | specified (listed in synopses) |
| LWG 456 | C++98 | C++ headers for C library facilities could only provide definitions in namespace std | allowed to define in global namespace and then inject into namespace std |
| LWG 465 | C++98 | identifiers that are keywords or operators in C++ could be defined as macros in C++ standard library headers (only <ciso646> is required not to define them as macros) | all C++ standard library headers cannot define them as macros |
| LWG 1178 | C++98 | C++ headers must include a C++ header that contains any needed definition | C++ headers must provide declarations and definitions that are directly or indirectly included in its synopsis |
| LWG 2013 | C++11 | it was unspecified whether the functions not required by the standard to be constexpr can be declared constexpr by the standard library | prohibited |
| LWG 2225 | C++98 | a diagnostic was required if a header is included at an incorrect position | no diagnostic is required in this case |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/standard_library&oldid=179112>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 22:37.