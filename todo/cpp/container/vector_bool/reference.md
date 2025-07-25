# std::vector<bool, Alloc>::reference

From cppreference.com
< cpp‎ | container‎ | vector bool
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

std::vector<bool>

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| ****vector<bool>::reference**** | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | vector::vector | | | | | | vector::~vector | | | | | | vector::operator= | | | | | | vector::assign | | | | | | vector::assign_range(C++23) | | | | | | vector::get_allocator | | | | | | Element access | | | | | | [vector::operator[]](../vector/operator_at.html "cpp/container/vector/operator at") | | | | | | vector::at | | | | | | vector::front | | | | | | vector::back | | | | | | Iterators | | | | | | vector::beginvector::cbegin(C++11) | | | | | | vector::endvector::cend(C++11) | | | | | | vector::rbeginvector::crbegin(C++11) | | | | | | vector::rendvector::crend(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | vector::empty | | | | | | vector::size | | | | | | vector::max_size | | | | | | vector::capacity | | | | | | vector::resize | | | | | | vector::reserve | | | | | | vector::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | vector::clear | | | | | | vector::erase | | | | | | vector::insert | | | | | | vector::insert_range(C++23) | | | | | | vector::append_range(C++23) | | | | | | vector::emplace(C++11) | | | | | | vector::emplace_back(C++11) | | | | | | vector::push_back | | | | | | vector::pop_back | | | | | | vector::swap | | | | | | vector<bool>::flip | | | | | | vector<bool>::swap | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::vector<bool>) | | | | | | erase(std::vector<bool>)erase_if(std::vector<bool>)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| hash<std::vector<bool>>(C++11) | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| class reference; |  |  |
|  |  |  |

The `std::vector`<bool, Alloc> specializations define `std::vector`<bool, Alloc>::reference as a publicly-accessible nested class. `std::vector`<bool, Alloc>::reference proxies the behavior of references to a single bit in `std::vector`<bool, Alloc>.

The primary use of `std::vector`<bool, Alloc>::reference is to provide an lvalue that can be returned from operator[].

Any reads or writes to a vector that happen via a `std::vector`<bool, Alloc>::reference potentially read or write to the entire underlying vector.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the reference. There is no default constructor. The copy constructor is implicitly declared(until C++11)defaulted(since C++11). There may be internal constructor that is accessible only to `std::vector`<bool, Alloc> itself.   (public member function) |
| (destructor) | destroys the reference   (public member function) |
| operator= | assigns a bool to the referenced bit   (public member function) |
| ****operator bool**** | returns the referenced bit   (public member function) |
| flip | flips the referenced bit   (public member function) |

## std::vector<bool, Alloc>::reference::~reference

|  |  |  |
| --- | --- | --- |
| ~reference(); |  | (until C++20) |
| constexpr ~reference(); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Destroys the reference.

## std::vector<bool, Alloc>::reference::operator=

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| reference& operator=( bool x ); |  | (until C++11) |
| reference& operator=( bool x ) noexcept; |  | (since C++11)  (until C++20) |
| constexpr reference& operator=( bool x ) noexcept; |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| reference& operator=( const reference& x ); |  | (until C++11) |
| reference& operator=( const reference& x ) noexcept; |  | (since C++11)  (until C++20) |
| constexpr reference& operator=( const reference& x ) noexcept; |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| constexpr const reference& operator=( bool x ) const noexcept; | (3) | (since C++23) |
|  |  |  |

Assigns a value to the referenced bit.

### Parameters

|  |  |  |
| --- | --- | --- |
| x | - | value to assign |

### Return value

\*this

## std::vector<bool, Alloc>::reference::operator bool

|  |  |  |
| --- | --- | --- |
| operator bool() const; |  | (until C++11) |
| operator bool() const noexcept; |  | (since C++11)  (until C++20) |
| constexpr operator bool() const noexcept; |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Returns the value of the referenced bit.

### Parameters

(none)

### Return value

The referenced bit.

## std::vector<bool, Alloc>::reference::flip

|  |  |  |
| --- | --- | --- |
| void flip(); |  | (until C++11) |
| void flip() noexcept; |  | (since C++11)  (until C++20) |
| constexpr void flip() noexcept; |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Inverts the referenced bit.

### Parameters

(none)

### Return value

(none)

### Helper classes

## std::formatter<std::vector<bool, Alloc>::reference>

|  |  |  |
| --- | --- | --- |
| template< class T, class CharT >    requires /\*is-vector-bool-reference\*/<T> struct formatter<T, CharT>; |  | (since C++23) |
|  |  |  |

Specializes the std::formatter for `std::vector`<bool, Alloc>::reference. The specialization uses std::formatter<bool, CharT> as its underlying formatter (denoted as `underlying_`) where the referenced bit is converted to bool to be formatted.

The exposition-only constant /\*is-vector-bool-reference\*/<T> is true if and only if `T` denotes the type `std::vector`<bool, Alloc>::reference for some type `Alloc` and `std::vector`<bool, Alloc> is not a program-defined specialization.

#### Member functions

|  |  |  |
| --- | --- | --- |
| template< class ParseContext >  constexpr ParseContext::iterator parse( ParseContext& ctx ); | (1) | (since C++23) |
| template< class FormatContext >  FormatContext::iterator format( const T& r, FormatContext& ctx ) const; | (2) | (since C++23) |
|  |  |  |

1) Equivalent to return`underlying_`.parse(ctx);.2) Equivalent to return`underlying_`.format(r, ctx);.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| [operator[]](../vector/operator_at.html "cpp/container/vector/operator at") | access specified element   (public member function of `std::vector<T,Allocator>`) |
| swap[static] | swaps two `std::vector<bool>::`****references****   (public static member function) |

### External links

|  |
| --- |
| "Effective Modern C++" by Scott Meyers (2015), Chapter 2, Item 6: "Use the explicitly typed initializer idiom when auto deduces undesired types." (p.43-46) — describes a possible misuse of the proxy class `std::vector<bool>::reference`). |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/vector_bool/reference&oldid=178311>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 December 2024, at 08:58.