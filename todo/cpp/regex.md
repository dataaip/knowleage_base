# Regular expressions library (since C++11)

From cppreference.com
< cpp
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
| ****Regular expressions library**** (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

****Regular expressions library****

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
| syntax_option_type(C++11) | | | | |
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

The regular expressions library provides a class that represents regular expressions, which are a kind of mini-language used to perform pattern matching within strings. Almost all operations with regexes can be characterized by operating on several of the following objects:

- ****Target sequence****. The character sequence that is searched for a pattern. This may be a range specified by two iterators, a null-terminated character string or a std::string.

- ****Pattern****. This is the regular expression itself. It determines what constitutes a match. It is an object of type std::basic_regex, constructed from a string with special grammar.

- ****Matched array****. The information about matches may be retrieved as an object of type std::match_results.

- ****Replacement string****. This is a string that determines how to replace the matches.

### Regular expression grammars

Patterns and replacement strings support the following regular expression grammars:

- Modified ECMAScript regular expression grammar. This is the default grammar.
- Basic POSIX regular expression grammar.
- Extended POSIX regular expression grammar.
- The regular expression grammar used by the awk utility in POSIX.
- The regular expression grammar used by the grep utility in POSIX. This is effectively the same as the basic POSIX regular expression grammar, with the addition of newline '\n' as an alternation separator.
- The regular expression grammar used by the grep utility, with the -E option, in POSIX. This is effectively the same as the extended POSIX regular expression grammar, with the addition of newline '\n' as an alternation separator in addition to '|'.

Some grammar variations (such as case-insensitive matching) are also avaliable, see this page for details.

### Main classes

These classes encapsulate a regular expression and the results of matching a regular expression within a target sequence of characters.

|  |  |
| --- | --- |
| basic_regex(C++11) | regular expression object   (class template) |
| sub_match(C++11) | identifies the sequence of characters matched by a sub-expression   (class template) |
| match_results(C++11) | identifies one regular expression match, including all sub-expression matches   (class template) |

### Algorithms

These functions are used to apply the regular expression encapsulated in a regex to a target sequence of characters.

|  |  |
| --- | --- |
| regex_match(C++11) | attempts to match a regular expression to an entire character sequence   (function template) |
| regex_search(C++11) | attempts to match a regular expression to any part of a character sequence   (function template) |
| regex_replace(C++11) | replaces occurrences of a regular expression with formatted replacement text   (function template) |

### Iterators

The regex iterators are used to traverse the entire set of regular expression matches found within a sequence.

|  |  |
| --- | --- |
| regex_iterator(C++11) | iterates through all regex matches within a character sequence   (class template) |
| regex_token_iterator(C++11) | iterates through the specified sub-expressions within all regex matches in a given string or through unmatched substrings   (class template) |

### Exceptions

This class defines the type of objects thrown as exceptions to report errors from the regular expressions library.

|  |  |
| --- | --- |
| regex_error(C++11) | reports errors generated by the regular expressions library   (class) |

### Traits

The regex traits class is used to encapsulate the localizable aspects of a regex.

|  |  |
| --- | --- |
| regex_traits(C++11) | provides metainformation about a character type, required by the regex library   (class template) |

### Constants

|  |  |
| --- | --- |
| Defined in namespace `std::regex_constants` | |
| syntax_option_type(C++11) | general options controlling regex behavior   (typedef) |
| match_flag_type(C++11) | options specific to matching   (typedef) |
| error_type(C++11) | describes different types of matching errors   (typedef) |

### Example

Run this code

```
#include <iostream>
#include <iterator>
#include <regex>
#include <string>
 
int main()
{
    std::string s = "Some people, when confronted with a problem, think "
        "\"I know, I'll use regular expressions.\" "
        "Now they have two problems.";
 
    std::regex self_regex("REGULAR EXPRESSIONS",
        std::regex_constants::ECMAScript | std::regex_constants::icase);
    if (std::regex_search(s, self_regex))
        std::cout << "Text contains the phrase 'regular expressions'\n";
 
    std::regex word_regex("(\\w+)");
    auto words_begin = 
        std::sregex_iterator(s.begin(), s.end(), word_regex);
    auto words_end = std::sregex_iterator();
 
    std::cout << "Found "
              << std::distance(words_begin, words_end)
              << " words\n";
 
    const int N = 6;
    std::cout << "Words longer than " << N << " characters:\n";
    for (std::sregex_iterator i = words_begin; i != words_end; ++i)
    {
        std::smatch match = *i;
        std::string match_str = match.str();
        if (match_str.size() > N)
            std::cout << "  " << match_str << '\n';
    }
 
    std::regex long_word_regex("(\\w{7,})");
    std::string new_s = std::regex_replace(s, long_word_regex, "[$&]");
    std::cout << new_s << '\n';
}

```

Output:

```
Text contains the phrase 'regular expressions'
Found 20 words
Words longer than 6 characters:
  confronted
  problem
  regular
  expressions
  problems
Some people, when [confronted] with a [problem], think 
"I know, I'll use [regular] [expressions]." Now they have two [problems].

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex&oldid=172322>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 June 2024, at 09:54.