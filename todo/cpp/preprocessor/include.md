# Source file inclusion

From cppreference.com
< cpp‎ | preprocessor
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

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

Preprocessor

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| #if#ifdef#ifndef#else#elif#elifdef#elifndef#endif(C++23)(C++23) | | | | |
| #define#undef#,## operators | | | | |
| ****#include__has_include****(C++17) | | | | |
| #error#warning(C++23) | | | | |
| #pragma_Pragma(C++11) | | | | |
| #line | | | | |

Includes other source file into current source file at the line immediately after the directive.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `#include <` h-char-sequence `>` new-line | (1) |  |
|  | | | | | | | | | |
| `#include "` q-char-sequence `"` new-line | (2) |  |
|  | | | | | | | | | |
| `#include` pp-tokens new-line | (3) |  |
|  | | | | | | | | | |
| `__has_include` `(` `"` q-char-sequence `"` `)` `__has_include` `(` `<` h-char-sequence `>` `)` | (4) | (since C++17) |
|  | | | | | | | | | |
| `__has_include` `(` string-literal `)` `__has_include` `(` `<` h-pp-tokens `>` `)` | (5) | (since C++17) |
|  | | | | | | | | | |

1) Searches for a header identified uniquely by h-char-sequence and replaces the directive by the entire contents of the header.2) Searches for a source file identified by q-char-sequence and replaces the directive by the entire contents of the source file. It may fallback to (1) and treat q-char-sequence as a header identifier.3) If neither (1) nor (2) is matched, pp-tokens will undergo macro replacement. The directive after replacement will be tried to match with (1) or (2) again.4) Checks whether a header or source file is available for inclusion.5) If (4) is not matched, h-pp-tokens will undergo macro replacement. The directive after replacement will be tried to match with (4) again.

|  |  |  |
| --- | --- | --- |
| new-line | - | The new-line character |
| h-char-sequence | - | A sequence of one or more h-chars, where the appearance of any of the following is conditionally-supported with implementation-defined semantics:  - the character ' - the character " - the character \ - the character sequence // - the character sequence /\* |
| h-char | - | Any member of the source character set(until C++23)translation character set(since C++23) except new-line and > |
| q-char-sequence | - | A sequence of one or more q-chars, where the appearance of any of the following is conditionally-supported with implementation-defined semantics:  - the character ' - the character \ - the character sequence // - the character sequence /\* |
| q-char | - | Any member of the source character set(until C++23)translation character set(since C++23) except new-line and " |
| pp-tokens | - | A sequence of one or more preprocessing tokens |
| string-literal | - | A string literal |
| h-pp-tokens | - | A sequence of one or more preprocessing tokens except > |

### Explanation

1) Searches a sequence of implementation-defined places for a header identified uniquely by h-char-sequence, and causes the replacement of that directive by the entire contents of the header. How the places are specified or the header identified is implementation-defined.2) Causes the replacement of that directive by the entire contents of the source file identified by q-char-sequence. The named source file is searched for in an implementation-defined
manner. If this search is not supported, or if the search fails, the directive is reprocessed as if it reads syntax (1) with the identical contained sequence (including > characters, if any) from the original directive.3) The preprocessing tokens after `include` in the directive are processed just as in normal text (i.e., each identifier currently defined as a macro name is replaced by its replacement list of preprocessing tokens). If the directive resulting after all replacements does not match one of the two previous forms, the behavior is undefined. The method by which a sequence of preprocessing tokens between a < and a > preprocessing token pair or a pair of " characters is combined into
a single header name preprocessing token is implementation-defined.4) The header or source file identified by h-char-sequence or q-char-sequence is searched for as if that preprocessing token sequence were the pp-tokens in syntax (3), except that no further macro expansion is performed. If such a directive would not satisfy the
syntactic requirements of an `#include` directive, the program is ill-formed. The `__has_include` expression evaluates to 1 if the search for the source file succeeds, and to ​0​ if the search fails.5) This form is considered only if syntax (4) does not match, in which case the preprocessing tokens are processed just as in normal text.

|  |  |
| --- | --- |
| If the header identified by the header-name (i.e., `<` h-char-sequence `>` or `"` q-char-sequence `"`) denotes an importable header, it is implementation-defined whether the `#include` preprocessing directive is instead replaced by an import directive of the form  `import` header-name `;` new-line | (since C++20) |

`__has_include` can be expanded in the expression of #if and #elif. It is treated as a defined macro by #ifdef, #ifndef, #elifdef, #elifndef(since C++23) and defined but cannot be used anywhere else.

### Notes

Typical implementations search only standard include directories for syntax (1). The standard C++ library and the standard C library are implicitly included in these standard include directories. The standard include directories usually can be controlled by the user through compiler options.

The intent of syntax (2) is to search for the files that are not controlled by the implementation. Typical implementations first search the directory where the current file resides then falls back to (1).

When a file is included, it is processed by translation phases 1-4, which may include, recursively, expansion of the nested `#include` directives, up to an implementation-defined nesting limit. To avoid repeated inclusion of the same file and endless recursion when a file includes itself, perhaps transitively, **header guards** are commonly used: the entire header is wrapped in

```
#ifndef FOO_H_INCLUDED /* any name uniquely mapped to file name */
#define FOO_H_INCLUDED
// contents of the file are here
#endif

```

Many compilers also implement the non-standard pragma #pragma once with similar effects: it disables processing of a file if the same file (where file identity is determined in OS-specific way) has already been included.

A sequence of characters that resembles an escape sequence in q-char-sequence or h-char-sequence might result in an error, be interpreted as the character corresponding to the escape sequence, or have a completely different meaning, depending on the implementation.

A `__has_include` result of 1 only means that a header or source file with the specified name exists. It does not mean that the header or source file, when included, would not cause an error or would contain anything useful. For example, on a C++ implementation that supports both C++14 and C++17 modes (and provides __has_include in its C++14 mode as a conforming extension), __has_include(<optional>) may be 1 in C++14 mode, but actually #include <optional> may cause an error.

### Example

Run this code

```
#if __has_include(<optional>)
    #include <optional>
    #define has_optional 1
    template<class T>
    using optional_t = std::optional<T>;
#elif __has_include(<experimental/optional>)
    #include <experimental/optional>
    #define has_optional -1
    template<class T>
    using optional_t = std::experimental::optional<T>;
#else
    #define has_optional 0
    template<class V>
    class optional_t
    {
        V v{};
        bool has{};
 
    public:
        optional_t() = default;
        optional_t(V&& v) : v(v), has{true} {}
        V value_or(V&& alt) const&
        {
            return has ? v : alt;
        }
        // etc.
    };
#endif
 
#include <iostream>
 
int main()
{
    if (has_optional > 0)
        std::cout << "<optional> is present\n";
    else if (has_optional < 0)
        std::cout << "<experimental/optional> is present\n";
    else
        std::cout << "<optional> is not present\n";
 
    optional_t<int> op;
    std::cout << "op = " << op.value_or(-1) << '\n';
    op = 42;
    std::cout << "op = " << op.value_or(-1) << '\n';
}

```

Output:

```
<optional> is present
op = -1
op = 42

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 787 | C++98 | the behavior is undefined if an escape sequence is resembled in q-char-sequence or h-char-sequence | it is conditionally-supported |

### See also

|  |  |
| --- | --- |
| A list of C++ Standard Library header files | |
| C documentation for Source file inclusion | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/preprocessor/include&oldid=180179>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 February 2025, at 10:01.