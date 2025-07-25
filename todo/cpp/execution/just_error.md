# std::execution::just_error

From cppreference.com
< cpp‎ | execution
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

Execution Library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Execution concepts | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scheduler | | | | | | receiver") | | | | | | receiver_of") | | | | | | operation_state") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sender") | | | | | | sender_in") | | | | | | sender_to") | | | | | |  | | | | | | | | Execution components | | | | | | Execution contexts | | | | | | run_loop") | | | | | | Execution domains | | | | | | default_domain") | | | | | | Forward progress guarantee | | | | | | forward_progress_guarantee") | | | | | | Environments | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_env") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | get_env") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | env_of_t") | | | | | | | | Queries | | | | | | std::stop_token_of_t") | | | | | | std::get_stop_token") | | | | | | std::get_allocator") | | | | | | std::forwarding_query") | | | | | | get_scheduler") | | | | | | get_domain") | | | | | | get_forward_progress_guarantee") | | | | | | get_delegation_scheduler") | | | | | | get_completion_scheduler") | | | | | | Completion signatures | | | | | | completion_signatures") | | | | | | completion_signatures_of_t") | | | | | | transform_completion_signatures") | | | | | | transform_completion_signatures_of") | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | value_types_of_t") | | | | | | error_types_of_t") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tag_of_t") | | | | | | sends_stopped") | | | | | | | | Sender adaptor closures | | | | | | sender_adaptor_closure") | | | | | | Coroutine utility | | | | | | as_awaitable") | | | | | | with_awaitable_senders") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core operations | | | | | | Operation state | | | | | | connect connect_result_t") | | | | | | start") | | | | | | Completion | | | | | | set_value") | | | | | | set_error") | | | | | | set_stopped") | | | | | | Transformation | | | | | | transform_env") | | | | | | transform_sender") | | | | | | apply_sender") | | | | | | Sender algorithms | | | | | | Sender factories | | | | | | just | | | | | | ****just_error**** | | | | | | just_stopped | | | | | | read_env | | | | | | schedule schedule_result_t | | | | | | Sender adaptors | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | starts_on") | | | | | | continues_on") | | | | | | on | | | | | | then | | | | | | upon_error | | | | | | upon_stopped | | | | | | let_value | | | | | | let_error | | | | | | let_stopped | | | | | | schedule_from") | | | | | | when_all | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | when_all_with_variant") | | | | | | into_variant | | | | | | stopped_as_optional | | | | | | stopped_as_error | | | | | | bulk") | | | | | | split") | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | | Sender consumers | | | | | | this_thread::sync_wait | | | | | | this_thread::sync_wait_with_variant") | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<execution>` |  |  |
| inline constexpr just_error_t just_error{};  struct just_error_t { /\*unspecified\*/ }; |  | (since C++26)  (customization point object) |
| Call signature |  |  |
| execution::sender auto just_error( auto&& error ); |  | (since C++26) |
|  |  |  |

A sender factory that returns a sender which completes immediately by calling the receiver’s `set_error()`").

Let e be a subexpression represented by an input error which will be injected and returned by the receiver. The expression just_error(e) is expression-equivalent to /\*make-sender\*/(just_error, /\*product-type\*/(e))

### Customization point objects

The name `execution::just_error` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. The cv-unqualified version of its type is a tag type denoted as `execution::just_error_t`.

All instances of `execution::just_error_t` are equal. The effects of invoking different instances of type `execution::just_error_t` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `execution::just_error` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `execution::just_error` above, `execution::just_error_t` models

- std::invocable<execution::just_error_t, Args...>,
- std::invocable<const execution::just_error_t, Args...>,
- std::invocable<execution::just_error_t&, Args...>, and
- std::invocable<const execution::just_error_t&, Args...>.

Otherwise, no function call operator of `execution::just_error_t` participates in overload resolution.

### Notes

If the provided error is an lvalue reference, a copy is made inside the returned sender and a non-const lvalue reference to the copy is sent to the receiver’s set_error. If the provided value is an rvalue reference, it is moved into the returned sender and an rvalue reference to it is sent to the receiver’s `set_error`.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/execution/just_error&oldid=176807>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 October 2024, at 16:40.