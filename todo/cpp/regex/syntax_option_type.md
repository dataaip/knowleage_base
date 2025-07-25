# std::regex_constants::syntax_option_type

From cppreference.com
< cpp‎ | regex
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

Regular expressions library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_regex(C++11) | | | | |
| sub_match(C++11) | | | | |
| match_results(C++11) | | | | |
| Algorithms | | | | |
| regex_match(C++11) | | | | |
| regex_search(C++11) | | | | |
| regex_replace(C++11) | | | | |
| Iterators | | | | |
| regex_iterator(C++11) | | | | |
| regex_token_iterator(C++11) | | | | |
| Exceptions | | | | |
| regex_error(C++11) | | | | |
| Traits | | | | |
| regex_traits(C++11) | | | | |
| Constants | | | | |
| ****syntax_option_type****(C++11) | | | | |
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| using syntax_option_type = /\* implementation-defined \*/; | (1) | (since C++11) |
| constexpr syntax_option_type icase      = /\* unspecified \*/;  constexpr syntax_option_type nosubs     = /\* unspecified \*/;  constexpr syntax_option_type optimize   = /\* unspecified \*/;  constexpr syntax_option_type collate    = /\* unspecified \*/;  constexpr syntax_option_type ECMAScript = /\* unspecified \*/;  constexpr syntax_option_type basic      = /\* unspecified \*/;  constexpr syntax_option_type extended   = /\* unspecified \*/;  constexpr syntax_option_type awk        = /\* unspecified \*/;  constexpr syntax_option_type grep       = /\* unspecified \*/; constexpr syntax_option_type egrep      = /\* unspecified \*/; | (2) | (since C++11)  (inline since C++17) |
| inline constexpr syntax_option_type multiline = /\* unspecified \*/; | (3) | (since C++17) |
|  |  |  |

1) The `syntax_option_type` is a BitmaskType that contains options that govern how regular expressions behave.2,3) The possible values (`icase`, `optimize`, etc.) for type (1) are duplicated inside std::basic_regex.

### Constants

|  |  |
| --- | --- |
| Grammar option | Effect(s) |
| `ECMAScript` | Use the Modified ECMAScript regular expression grammar. |
| `basic` | Use the basic POSIX regular expression grammar (grammar documentation). |
| `extended` | Use the extended POSIX regular expression grammar (grammar documentation). |
| `awk` | Use the regular expression grammar used by the **awk** utility in POSIX (grammar documentation). |
| `grep` | Use the regular expression grammar used by the **grep** utility in POSIX. This is effectively the same as the `basic` option with the addition of newline '\n' as an alternation separator. |
| `egrep` | Use the regular expression grammar used by the **grep** utility, with the **-E** option, in POSIX. This is effectively the same as the `extended` option with the addition of newline '\n' as an alternation separator in addition to '|'. |
| Grammar variation | Effect(s) |
| `icase` | Character matching should be performed without regard to case. |
| `nosubs` | When performing matches, all marked sub-expressions `(expr)` are treated as non-marking sub-expressions `(?:expr)`. No matches are stored in the supplied std::regex_match structure and mark_count() is zero. |
| `optimize` | Instructs the regular expression engine to make matching faster, with the potential cost of making construction slower. For example, this might mean converting a non-deterministic FSA to a deterministic FSA. |
| `collate` | Character ranges of the form **"[a-b]"** will be locale sensitive. |
| `multiline` (C++17) | Specifies that `^` shall match the beginning of a line and `$` shall match the end of a line, if the ECMAScript engine is selected. |

At most one grammar option can be chosen out of `ECMAScript`, `basic`, `extended`, `awk`, `grep`, `egrep`. If no grammar is chosen, `ECMAScript` is assumed to be selected. The other options serve as variations, such that std::regex("meow", std::regex::icase) is equivalent to std::regex("meow", std::regex::ECMAScript|std::regex::icase).

### Notes

Because POSIX uses "leftmost longest" matching rule (the longest matching subsequence is matched, and if there are several such subsequences, the first one is matched), it is not suitable, for example, for parsing markup languages: a POSIX regex such as "<tag[^>]\*>.\*</tag>" would match everything from the first "<tag" to the last "</tag>", including every "</tag>" and "<tag>" in-between. On the other hand, ECMAScript supports non-greedy matches, and the ECMAScript regex "<tag[^>]\*>.\*?</tag>" would match only until the first closing tag.

### Example

Illustrates the difference in the matching algorithm between ECMAScript and POSIX regular expressions:

Run this code

```
#include <iostream>
#include <regex>
#include <string>
 
int main()
{
    std::string str = "zzxayyzz";
    std::regex re1(".*(a|xayy)"); // ECMA
    std::regex re2(".*(a|xayy)", std::regex::extended); // POSIX
 
    std::cout << "Searching for .*(a|xayy) in zzxayyzz:\n";
    std::smatch m;
    std::regex_search(str, m, re1);
    std::cout << "  ECMA (depth first search) match: " << m[0] << '\n';
    std::regex_search(str, m, re2);
    std::cout << "  POSIX (leftmost longest)  match: " << m[0] << '\n';
}

```

Output:

```
Searching for .*(a|xayy) in zzxayyzz:
  ECMA (depth first search) match: zzxa
  POSIX (leftmost longest)  match: zzxayy

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2053 | C++11 | the constants were declared static | removed the static specifier |

### See also

|  |  |
| --- | --- |
| basic_regex(C++11) | regular expression object   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/syntax_option_type&oldid=173768>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 July 2024, at 02:59.