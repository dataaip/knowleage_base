# Standard format specification (since C++20)

From cppreference.com
< cpp‎ | utility‎ | format
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

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

Formatting library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****Standard format specification**** | | | | |
| Formatting functions | | | | |
| format(C++20) | | | | |
| format_to(C++20) | | | | |
| format_to_n(C++20) | | | | |
| formatted_size(C++20) | | | | |
| vformat(C++20) | | | | |
| vformat_to(C++20) | | | | |
| Format strings | | | | |
| basic_format_stringformat_stringwformat_string(C++20)(C++20)(C++20) | | | | |
| runtime_format(C++26) | | | | |
| Formatting concepts | | | | |
| formattable(C++23) | | | | |
| Formatter | | | | |
| formatter(C++20) | | | | |
| formatter<**pair-or-tuple**>(C++23) | | | | |
| formatter<**range**>(C++23) | | | | |
| range_formatter(C++23) | | | | |
| enable_nonlocking_formatter_optimization(C++23) | | | | |
| basic_format_parse_contextformat_parse_contextwformat_parse_context(C++20)(C++20)(C++20) | | | | |
| basic_format_contextformat_contextwformat_context(C++20)(C++20)(C++20) | | | | |
| range_format(C++23) | | | | |
| format_kind(C++23) | | | | |
| Formatting arguments | | | | |
| basic_format_arg(C++20) | | | | |
| basic_format_arg::handle(C++20) | | | | |
| basic_format_argsformat_argswformat_args(C++20)(C++20)(C++20) | | | | |
| visit_format_arg(C++20) (deprecated in C++26) | | | | |
| make_format_argsmake_wformat_args(C++20)(C++20) | | | | |
| Format error | | | | |
| format_error(C++20) | | | | |

For basic types and string types, the format specification is based on the format specification in Python.

The syntax of format specifications is:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| fill-and-align ﻿(optional) sign ﻿(optional) `#`(optional) `0`(optional) width ﻿(optional) precision ﻿(optional) `L`(optional) type ﻿(optional) |  |  |
|  | | | | | | | | | |

The sign, `#` and `0` options are only valid when an integer or floating-point presentation type is used.

### Fill and align

fill-and-align is an optional **fill** character (which can be any character other than `{` or `}`), followed by one of the **align** options `<`, `>`, `^`.

If no fill character is specified, it defaults to the space character. For a format specification in a Unicode encoding, the fill character must correspond to a single Unicode scalar value.

The meaning of **align** options is as follows:

- `<`: Forces the formatted argument to be aligned to the start of the available space by inserting n fill characters after the formatted argument. This is the default when a non-integer non-floating-point presentation type is used.
- `>`: Forces the formatted argument to be aligned to the end of the available space by inserting n fill characters before the formatted argument. This is the default when an integer or floating-point presentation type is used.
- `^`: Forces the formatted argument to be centered within the available space by inserting ⌊

  |  |
  | --- |
  | n |
  | 2 |

  ⌋ characters before and ⌈

  |  |
  | --- |
  | n |
  | 2 |

  ⌉ characters after the formatted argument.

In each case, n is the difference of the minimum field width (specified by width) and the estimated width of the formatted argument, or 0 if the difference is less than 0.

Run this code

```
#include <cassert>
#include <format>
 
int main()
{
    char c = 120;
    assert(std::format("{:6}", 42)    == "    42");
    assert(std::format("{:6}", 'x')   == "x     ");
    assert(std::format("{:*<6}", 'x') == "x*****");
    assert(std::format("{:*>6}", 'x') == "*****x");
    assert(std::format("{:*^6}", 'x') == "**x***");
    assert(std::format("{:6d}", c)    == "   120");
    assert(std::format("{:6}", true)  == "true  ");
}

```

### Sign, #, and 0

The sign option can be one of following:

- `+`: Indicates that a sign should be used for both non-negative and negative numbers. The `+` sign is inserted before the output value for non-negative numbers.
- `-`: Indicates that a sign should be used for negative numbers only (this is the default behavior).
- space: Indicates that a leading space should be used for non-negative numbers, and a minus sign for negative numbers.

Negative zero is treated as a negative number.

The sign option applies to floating-point infinity and NaN.

Run this code

```
#include <cassert>
#include <format>
#include <limits>
 
int main()
{
    double inf = std::numeric_limits<double>::infinity();
    double nan = std::numeric_limits<double>::quiet_NaN();
    assert(std::format("{0:},{0:+},{0:-},{0: }", 1)   == "1,+1,1, 1");
    assert(std::format("{0:},{0:+},{0:-},{0: }", -1)  == "-1,-1,-1,-1");
    assert(std::format("{0:},{0:+},{0:-},{0: }", inf) == "inf,+inf,inf, inf");
    assert(std::format("{0:},{0:+},{0:-},{0: }", nan) == "nan,+nan,nan, nan");
}

```

The `#` option causes the **alternate form** to be used for the conversion.

- For integral types, when binary, octal, or hexadecimal presentation type is used, the alternate form inserts the prefix (`0b`, `0`, or `0x`) into the output value after the sign character (possibly space) if there is one, or add it before the output value otherwise.
- For floating-point types, the alternate form causes the result of the conversion of finite values to always contain a decimal-point character, even if no digits follow it. Normally, a decimal-point character appears in the result of these conversions only if a digit follows it. In addition, for `g` and `G` conversions, trailing zeros are not removed from the result.

The `0` option pads the field with leading zeros (following any indication of sign or base) to the field width, except when applied to an infinity or NaN. If the `0` character and an **align** option both appear, the `0` character is ignored.

Run this code

```
#include <cassert>
#include <format>
 
int main()
{
    char c = 120;
    assert(std::format("{:+06d}", c)   == "+00120");
    assert(std::format("{:#06x}", 0xa) == "0x000a");
    assert(std::format("{:<06}", -42)  == "-42   "); // 0 is ignored because of '<'
}

```

### Width and precision

width is either a positive decimal number, or a nested replacement field (`{}` or `{`**n**`}`). If present, it specifies the minimum field width.

precision is a dot (`.`) followed by either a non-negative decimal number or a nested replacement field. This field indicates the precision or maximum field size. It can only be used with floating-point and string types.

- For floating-point types, this field specifies the formatting precision.
- For string types, it provides an upper bound for the estimated width (see below) of the prefix of the string to be copied to the output. For a string in a Unicode encoding, the text to be copied to the output is the longest prefix of whole extended grapheme clusters whose estimated width is no greater than the precision.

If a nested replacement field is used for width or precision, and the corresponding argument is not of integral type(until C++23)standard signed or unsigned integer type(since C++23), or is negative, an exception of type std::format_error is thrown.

```
float pi = 3.14f;
assert(std::format("{:10f}", pi)           == "  3.140000"); // width = 10
assert(std::format("{:{}f}", pi, 10)       == "  3.140000"); // width = 10
assert(std::format("{:.5f}", pi)           == "3.14000");    // precision = 5
assert(std::format("{:.{}f}", pi, 5)       == "3.14000");    // precision = 5
assert(std::format("{:10.5f}", pi)         == "   3.14000"); // width = 10, precision = 5
assert(std::format("{:{}.{}f}", pi, 10, 5) == "   3.14000"); // width = 10, precision = 5
 
auto b1 = std::format("{:{}f}", pi, 10.0); // throws: width is not of integral type
auto b2 = std::format("{:{}f}", pi, -10);  // throws: width is negative
auto b3 = std::format("{:.{}f}", pi, 5.0); // throws: precision is not of integral type

```

The width of a string is defined as the estimated number of column positions appropriate for displaying it in a terminal.

For the purpose of width computation, a string is assumed to be in an implementation-defined encoding. The method of width computation is unspecified, but for a string in a Unicode encoding, implementation should estimate the width of the string as the sum of estimated widths of the first code points in its extended grapheme clusters. The estimated width is 2 for the following code points, and is 1 otherwise:

- Any code point whose Unicode property `East_Asian_Width` has value Fullwidth (`F`) or Wide (`W`)
- U+4DC0 - U+4DFF (Yijing Hexagram Symbols)
- U+1F300 – U+1F5FF (Miscellaneous Symbols and Pictographs)
- U+1F900 – U+1F9FF (Supplemental Symbols and Pictographs)

Run this code

```
#include <cassert>
#include <format>
 
int main()
{
    assert(std::format("{:.^5s}",   "🐱")    == ".🐱..");
    assert(std::format("{:.5s}",    "🐱🐱🐱") == "🐱🐱");
    assert(std::format("{:.<5.5s}", "🐱🐱🐱") == "🐱🐱.");
}

```

### L (locale-specific formatting)

The `L` option causes the locale-specific form to be used. This option is only valid for arithmetic types.

- For integral types, the locale-specific form inserts the appropriate digit group separator characters according to the context's locale.
- For floating-point types, the locale-specific form inserts the appropriate digit group and radix separator characters according to the context's locale.
- For the textual representation of `bool`, the locale-specific form uses the appropriate string as if obtained with std::numpunct::truename or std::numpunct::falsename.

### Type

The type option determines how the data should be presented.

The available string presentation types are:

- none, `s`: Copies the string to the output.

|  |  |
| --- | --- |
| - `?`: Copies the escaped string (see below) to the output. | (since C++23) |

The available integer presentation types for integral types other than char, wchar_t, and bool are:

- `b`: Binary format. Produces the output as if by calling std::to_chars(first, last, value, 2). The base prefix is `0b`.
- `B`: same as `b`, except that the base prefix is `0B`.
- `c`: Copies the character static_cast<CharT>(value) to the output, where `CharT` is the character type of the format string. Throws std::format_error if value is not in the range of representable values for `CharT`.
- `d`: Decimal format. Produces the output as if by calling std::to_chars(first, last, value).
- `o`: Octal format. Produces the output as if by calling std::to_chars(first, last, value, 8). The base prefix is `0` if the corresponding argument value is non-zero and is empty otherwise.
- `x`: Hex format. Produces the output as if by calling std::to_chars(first, last, value, 16). The base prefix is `0x`.
- `X`: same as `x`, except that it uses uppercase letters for digits above 9 and the base prefix is `0X`.
- none: same as `d`.

The available char and wchar_t presentation types are:

- none, `c`: Copies the character to the output.
- `b`, `B`, `d`, `o`, `x`, `X`: Uses integer presentation types with the value static_cast<unsigned char>(value) or static_cast<std::make_unsigned_t<wchar_t>>(value) respectively.

|  |  |
| --- | --- |
| - `?`: Copies the escaped character (see below) to the output. | (since C++23) |

The available bool presentation types are:

- none, `s`: Copies textual representation (`true` or `false`, or the locale-specific form) to the output.
- `b`, `B`, `d`, `o`, `x`, `X`: Uses integer presentation types with the value static_cast<unsigned char>(value).

The available floating-point presentation types are:

- `a`: If **precision** is specified, produces the output as if by calling std::to_chars(first, last, value, std::chars_format::hex, precision) where precision is the specified precision; otherwise, the output is produced as if by calling std::to_chars(first, last, value, std::chars_format::hex).
- `A`: same as `a`, except that it uses uppercase letters for digits above 9 and uses `P` to indicate the exponent.
- `e`: Produces the output as if by calling std::to_chars(first, last, value, std::chars_format::scientific, precision) where precision is the specified precision, or 6 if precision is not specified.
- `E`: same as `e`, except that it uses `E` to indicate the exponent.
- `f`, `F`: Produces the output as if by calling std::to_chars(first, last, value, std::chars_format::fixed, precision) where precision is the specified precision, or 6 if precision is not specified.
- `g`: Produces the output as if by calling std::to_chars(first, last, value, std::chars_format::general, precision) where precision is the specified precision, or 6 if precision is not specified.
- `G`: same as `g`, except that it uses `E` to indicate the exponent.
- none: If **precision** is specified, produces the output as if by calling std::to_chars(first, last, value, std::chars_format::general, precision) where precision is the specified precision; otherwise, the output is produced as if by calling std::to_chars(first, last, value).

For lower-case presentation types, infinity and NaN are formatted as `inf` and `nan`, respectively.
For upper-case presentation types, infinity and NaN are formatted as `INF` and `NAN`, respectively.

The available pointer presentation types (also used for std::nullptr_t) are:

- none, `p`: If std::uintptr_t is defined, produces the output as if by calling std::to_chars(first, last, reinterpret_cast<std::uintptr_t>(value), 16) with the prefix `0x` added to the output; otherwise, the output is implementation-defined.

|  |  |
| --- | --- |
| - `P`: same as `p`, except that it uses uppercase letters for digits above 9 and the base prefix is `0X`. | (since C++26) |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Formatting escaped characters and strings A character or string can be formatted as **escaped** to make it more suitable for debugging or for logging.  Escaping is done as follows:   - For each well-formed code unit sequence that encodes a character **C**:   - If **C** is one of the characters in the following table, the corresponding escape sequence is used.   | Character | Escape sequence | Notes | | --- | --- | --- | | horizontal tab (byte 0x09 in ASCII encoding) | `\t` |  | | line feed - new line (byte 0x0a in ASCII encoding) | `\n` |  | | carriage return (byte 0x0d in ASCII encoding) | `\r` |  | | double quote (byte 0x22 in ASCII encoding) | `\"` | Used only if the output is a double-quoted string | | single quote (byte 0x27 in ASCII encoding) | `\'` | Used only if the output is a single-quoted string | | backslash (byte 0x5c in ASCII encoding) | `\\` |  |   - Otherwise, if **C** is not the space character (byte 0x20 in ASCII encoding), and either   - the associated character encoding is a Unicode encoding and   - **C** corresponds to a Unicode scalar value whose Unicode property `General_Category` has a value in the groups `Separator` (`Z`) or `Other` (`C`), or - **C** is not immediately preceded by a non-escaped character, and **C** corresponds to a Unicode scalar value which has the Unicode property `Grapheme_Extend=Yes`, or   - the associated character encoding is not a Unicode encoding and **C** is one of an implementation-defined set of separator or non-printable characters  the escape sequence is `\u{hex-digit-sequence}`, where `hex-digit-sequence` is the shortest hexadecimal representation of **C** using lower-case hexadecimal digits.   - Otherwise, **C** is copied as is.   - A code unit sequence that is a shift sequence has unspecified effect on the output and further decoding of the string. - Other code units (i.e. those in ill-formed code unit sequences) are each replaced with `\x{hex-digit-sequence}`, where `hex-digit-sequence` is the shortest hexadecimal representation of the code unit using lower-case hexadecimal digits.   The escaped string representation of a string is constructed by escaping the code unit sequences in the string, as described above, and quoting the result with double quotes.  The escaped representation of a character is constructed by escaping it as described above, and quoting the result with single quotes.  Compiler Explorer demo: Run this code  ```text #include <print>   int main() {     std::println("[{:?}]", "h\tllo");             // prints: ["h\tllo"]     std::println("[{:?}]", "Спасибо, Виктор ♥!"); // prints: ["Спасибо, Виктор ♥!"]     std::println("[{:?}] [{:?}]", '\'', '"');     // prints: ['\'', '"']       // The following examples assume use of the UTF-8 encoding     std::println("[{:?}]", std::string("\0 \n \t \x02 \x1b", 9));                                              // prints: ["\u{0} \n \t \u{2} \u{1b}"]     std::println("[{:?}]", "\xc3\x28");      // invalid UTF-8                                              // prints: ["\x{c3}("]     std::println("[{:?}]", "\u0301");        // prints: ["\u{301}"]     std::println("[{:?}]", "\\\u0301");      // prints: ["\\\u{301}"]     std::println("[{:?}]", "e\u0301\u0323"); // prints: ["ẹ́"] } ``` | (since C++23) |

### Notes

In most of the cases the syntax is similar to the old `%`-formatting, with the addition of the `{}` and with `:` used instead of `%`. For example, "%03.2f" can be translated to "{:03.2f}".

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_format_uchar` | `202311L` | (C++20) (DR) | Formatting of code units as unsigned integers |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3721 | C++20 | zero is not allowed for the width field in standard format specification | zero is permitted if specified via a replacement field |
| P2909R4 | C++20 | char or wchar_t might be formatted as out-of-range unsigned integer values | code units are converted to the corresponding unsigned type before such formatting |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/spec&oldid=178346>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 December 2024, at 18:01.