# std::text_encoding::aliases_view

From cppreference.com
< cpp‎ | text‎ | text encoding
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

std::text_encoding

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| Creation | | | | |
| text_encoding::text_encoding") | | | | |
| text_encoding::literal | | | | |
| text_encoding::environment | | | | |
| Observers | | | | |
| text_encoding::mib | | | | |
| text_encoding::name | | | | |
| text_encoding::aliases | | | | |
| text_encoding::environment_is | | | | |
| Helpers | | | | |
| text_encoding::**comp-name** | | | | |
| Non-member functions | | | | |
| operator==(std::text_encoding) | | | | |
| Member types | | | | |
| text_encoding::id | | | | |
| ****text_encoding::aliases_view**** | | | | |
| Helper classes | | | | |
| hash<std::text_encoding> | | | | |

|  |  |  |
| --- | --- | --- |
| class text_encoding::aliases_view      : public ranges::view_interface<text_encoding::aliases_view> |  | (since C++26) |
|  |  |  |

The nested class `text_encoding::aliases_view` is a `view` over aliases of the character encoding.

Let r denote an instance of `aliases_view`. For a non-empty range r:

- r.front() is the primary name of the registered character encoding,
- r contains the aliases of the registered character encoding such that the order of the aliases is unspecified,
- each element in r is a non-null and non-empty null-terminated byte string encoded in the literal character encoding and comprising only characters from the basic character set, and
- r does not contain duplicate values when compared with std::strcmp.

These are the following type properties of `text_encoding::aliases_view`:

- it models `copyable`, `random_access_range`, and `borrowed_range`.
- it is not required to satisfy `common_range` and `default_initializable`.
- both ranges::range_value_t<text_encoding​::​aliases_view> and ranges::range_reference_t<text_encoding::aliases_view> denote const char\*.
- ranges::iterator_t<text_encoding::aliases_view> is a ConstexprIterator.

### Member functions

|  |  |
| --- | --- |
| begin | returns an iterator of implementation-defined type to the beginning of the aliases view   (public member function) |
| end | returns a sentinel of implementation-defined type of the aliases view   (public member function) |
| Inherited from std::ranges::view_interface | |
| empty | returns whether the derived view is empty. Provided if it satisfies `sized_range` or `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](../../ranges/view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

## std::text_encoding::aliases_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr /\*implementation-defined\*/ begin() const; |  | (since C++26) |
|  |  |  |

Returns an iterator of implementation-defined type to the beginning of r.

## std::text_encoding::aliases_view::end

|  |  |  |
| --- | --- | --- |
| constexpr /\*implementation-defined\*/ end() const; |  | (since C++26) |
|  |  |  |

Returns a sentinel of implementation-defined type of r.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| aliases | returns a `view` over aliases of the current character encoding   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/text/text_encoding/aliases_view&oldid=179310>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 January 2025, at 20:40.