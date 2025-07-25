# Convenience aliases for containers using polymorphic allocators (library fundamentals TS)

From cppreference.com
< cpp‎ | experimental‎ | lib extensions
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

Polymorphic allocator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| polymorphic_allocator | | | | |
| ****Convenience aliases for containers using `polymorphic_allocator`**** | | | | |
| Memory resource classes | | | | |
| memory_resource | | | | |
| synchronized_pool_resource | | | | |
| unsynchronized_pool_resource | | | | |
| monotonic_buffer_resource | | | | |
| resource_adaptor | | | | |
| Global memory resources | | | | |
| new_delete_resource | | | | |
| null_memory_resource | | | | |
| get_default_resource | | | | |
| set_default_resource | | | | |
| Type-erased allocator support for existing classes | | | | |
| function | | | | |
| packaged_task | | | | |
| promise | | | | |

The following convenience aliases and alias templates for containers using polymorphic allocators are defined in the `std::experimental::pmr` namespace.

### Strings

|  |  |
| --- | --- |
| Alias/alias template | Alias for |
| Defined in header `<experimental/string>` | |
| template<class CharT,  class Traits=std::char_traits<CharT>>   using basic_string = | std::basic_string<CharT, Traits,      polymorphic_allocator<CharT>>; |
| using string = | pmr::basic_string<char>; |
| using wstring = | pmr::basic_string<wchar_t>; |
| using u16string = | pmr::basic_string<char16_t>; |
| using u32string = | pmr::basic_string<char32_t>; |

### Sequence containers

|  |  |
| --- | --- |
| Alias template | Alias for |
| Defined in header `<experimental/vector>` | |
| template<class T> using vector = | std::vector<T, polymorphic_allocator<T>>; |
| Defined in header `<experimental/deque>` | |
| template<class T> using deque = | std::deque<T, polymorphic_allocator<T>>; |
| Defined in header `<experimental/forward_list>` | |
| template<class T> using forward_list = | std::forward_list<T, polymorphic_allocator<T>>; |
| Defined in header `<experimental/list>` | |
| template<class T> using list = | std::list<T, polymorphic_allocator<T>>; |

### Associative containers

|  |  |
| --- | --- |
| Alias template | Alias for |
| Defined in header `<experimental/map>` | |
| template<class Key, class T,   class Compare=std::less<Key>>   using map = | std::map<Key, T, Compare,      polymorphic_allocator<std::pair<const Key, T>>>; |
| template<class Key, class T,   class Compare=std::less<Key>>   using multimap = | std::multimap<Key, T, Compare,      polymorphic_allocator<std::pair<const Key, T>>>; |
| Defined in header `<experimental/set>` | |
| template<class Key,  class Compare=std::less<Key>>   using set = | std::set<Key, Compare,      polymorphic_allocator<Key>>; |
| template<class Key,  class Compare=std::less<Key>>   using multiset = | std::multiset<Key, Compare,      polymorphic_allocator<Key>>; |

### Unordered associative containers

|  |  |
| --- | --- |
| Alias template | Alias for |
| Defined in header `<experimental/unordered_map>` | |
| template<class Key, class T,   class Hash = std::hash<Key>,            class Pred = std::equal_to<Key>>   using unordered_map = | std::unordered_map<Key, T, Hash, Pred,      polymorphic_allocator<std::pair<const Key, T>>>; |
| template<class Key, class T,   class Hash = std::hash<Key>,            class Pred = std::equal_to<Key>>   using unordered_multimap = | std::unordered_multimap<Key, T, Hash, Pred,      polymorphic_allocator<std::pair<const Key, T>>>; |
| Defined in header `<experimental/unordered_set>` | |
| template<class Key,   class Hash = std::hash<Key>,            class Pred = std::equal_to<Key>>   using unordered_set = | std::unordered_set<Key, Hash, Pred,      polymorphic_allocator<Key>>; |
| template<class Key,   class Hash = std::hash<Key>,            class Pred = std::equal_to<Key>>   using unordered_multiset = | std::unordered_multiset<Key, Hash, Pred,      polymorphic_allocator<Key>>; |

### `match_results`

|  |  |
| --- | --- |
| Alias/alias template | Alias for |
| Defined in header `<experimental/regex>` | |
| template<class BidirIt>   using match_results = | std::match_results<BidirIt,      polymorphic_allocator<std::sub_match<BidirIt>>>; |
| using cmatch = | pmr::match_results<const char\*>; |
| using wcmatch = | pmr::match_results<const wchar_t\*>; |
| using smatch = | pmr::match_results<pmr::string::const_iterator>; |
| using wsmatch = | pmr::match_results<pmr::wstring::const_iterator>; |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/lib_extensions/pmr_container&oldid=146958>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 January 2023, at 09:13.