# std::iscntrl

From cppreference.com
< cpp‎ | string‎ | byte
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

Null-terminated byte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character classification | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | isalnum | | | | | | isalpha | | | | | | islower | | | | | | isupper | | | | | | isdigit | | | | | | isxdigit | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | ****iscntrl**** | | | | | | isgraph | | | | | | isspace | | | | | | isprint | | | | | | ispunct | | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | |
| Conversions to numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atof | | | | | | atoiatolatoll(C++11) | | | | | | strtolstrtoll(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoulstrtoull(C++11) | | | | | | strtofstrtodstrtold(C++11)(C++11) | | | | | | strtoimaxstrtouimax(C++11)(C++11) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpy | | | | | | strncpy | | | | | | strxfrm | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcat | | | | | | strncat | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtok | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cctype>` |  |  |
| int iscntrl( int ch ); |  |  |
|  |  |  |

Checks if the given character is a control character as classified by the currently installed C locale. In the default, "C" locale, the control characters are the characters with the codes `0x00-0x1F` and `0x7F`.

The behavior is undefined if the value of ch is not representable as unsigned char and is not equal to EOF.

### Parameters

|  |  |  |
| --- | --- | --- |
| ch | - | character to classify |

### Return value

Non-zero value if the character is a control character, zero otherwise.

### Notes

Like all other functions from <cctype>, the behavior of `std::iscntrl` is undefined if the argument's value is neither representable as unsigned char nor equal to EOF. To use these functions safely with plain chars (or signed chars), the argument should first be converted to unsigned char:

```
bool my_iscntrl(char ch)
{
    return std::iscntrl(static_cast<unsigned char>(ch));
}

```

Similarly, they should not be directly used with standard algorithms when the iterator's value type is char or signed char. Instead, convert the value to unsigned char first:

```
int count_cntrls(const std::string& s)
{
    return std::count_if(s.begin(), s.end(),
                      // static_cast<int(*)(int)>(std::iscntrl)         // wrong
                      // [](int c){ return std::iscntrl(c); }           // wrong
                      // [](char c){ return std::iscntrl(c); }          // wrong
                         [](unsigned char c){ return std::iscntrl(c); } // correct
                        );
}

```

### Example

Run this code

```
#include <cctype>
#include <clocale>
#include <iostream>
 
int main()
{
    unsigned char c = '\x94'; // the control code CCH in ISO-8859-1
 
    std::cout << "iscntrl(\'\\x94\', default C locale) returned "
              << std::boolalpha << !!std::iscntrl(c) << '\n';
 
    std::setlocale(LC_ALL, "en_GB.iso88591");
    std::cout << "iscntrl(\'\\x94\', ISO-8859-1 locale) returned "
              << !!std::iscntrl(c) << '\n';
 
}

```

Possible output:

```
iscntrl('\x94', default C locale) returned false
iscntrl('\x94', ISO-8859-1 locale) returned true

```

### See also

|  |  |
| --- | --- |
| iscntrl(std::locale) | checks if a character is classified as a control character by a locale   (function template) |
| iswcntrl | checks if a wide character is a control character   (function) |
| C documentation for iscntrl | |

| ASCII values | | | characters | ****iscntrl****  iswcntrl | isprint  iswprint | isspace  iswspace | isblank  iswblank | isgraph  iswgraph | ispunct  iswpunct | isalnum  iswalnum | isalpha  iswalpha | isupper  iswupper | islower  iswlower | isdigit  iswdigit | isxdigit  iswxdigit |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| decimal | hexadecimal | octal |
| 0–8 | `\x0`–`\x8` | `\0`–`\10` | control codes (`NUL`, etc.) | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 9 | `\x9` | `\11` | tab (`\t`) | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 10–13 | `\xA`–`\xD` | `\12`–`\15` | whitespaces (`\n`, `\v`, `\f`, `\r`) | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 14–31 | `\xE`–`\x1F` | `\16`–`\37` | control codes | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 32 | `\x20` | `\40` | space | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 33–47 | `\x21`–`\x2F` | `\41`–`\57` | `!"#$%&'()*+,-./` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 48–57 | `\x30`–`\x39` | `\60`–`\71` | `0123456789` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** |
| 58–64 | `\x3A`–`\x40` | `\72`–`\100` | `:;<=>?@` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 65–70 | `\x41`–`\x46` | `\101`–`\106` | `ABCDEF` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** |
| 71–90 | `\x47`–`\x5A` | `\107`–`\132` | `GHIJKLMNOP` `QRSTUVWXYZ` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 91–96 | `\x5B`–`\x60` | `\133`–`\140` | `[\]^_`` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 97–102 | `\x61`–`\x66` | `\141`–`\146` | `abcdef` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** |
| 103–122 | `\x67`–`\x7A` | `\147`–`\172` | `ghijklmnop` `qrstuvwxyz` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** |
| 123–126 | `\x7B`–`\x7E` | `\172`–`\176` | `{|}~` | ****`0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`≠0`**** | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |
| 127 | `\x7F` | `\177` | backspace character (`DEL`) | ****`≠0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** | ****`0`**** |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/iscntrl&oldid=172927>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 June 2024, at 23:16.