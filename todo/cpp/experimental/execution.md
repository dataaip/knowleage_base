# Execution library (since C++26)

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
| ****Execution support library**** (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

****Execution Library****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Execution concepts | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scheduler | | | | | | receiver") | | | | | | receiver_of") | | | | | | operation_state") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sender") | | | | | | sender_in") | | | | | | sender_to") | | | | | |  | | | | | | | | Execution components | | | | | | Execution contexts | | | | | | run_loop") | | | | | | Execution domains | | | | | | default_domain") | | | | | | Forward progress guarantee | | | | | | forward_progress_guarantee") | | | | | | Environments | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_env") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | get_env") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | env_of_t") | | | | | | | | Queries | | | | | | std::stop_token_of_t") | | | | | | std::get_stop_token") | | | | | | std::get_allocator") | | | | | | std::forwarding_query") | | | | | | get_scheduler") | | | | | | get_domain") | | | | | | get_forward_progress_guarantee") | | | | | | get_delegation_scheduler") | | | | | | get_completion_scheduler") | | | | | | Completion signatures | | | | | | completion_signatures") | | | | | | completion_signatures_of_t") | | | | | | transform_completion_signatures") | | | | | | transform_completion_signatures_of") | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | value_types_of_t") | | | | | | error_types_of_t") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tag_of_t") | | | | | | sends_stopped") | | | | | | | | Sender adaptor closures | | | | | | sender_adaptor_closure") | | | | | | Coroutine utility | | | | | | as_awaitable") | | | | | | with_awaitable_senders") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core operations | | | | | | Operation state | | | | | | connect connect_result_t") | | | | | | start") | | | | | | Completion | | | | | | set_value") | | | | | | set_error") | | | | | | set_stopped") | | | | | | Transformation | | | | | | transform_env") | | | | | | transform_sender") | | | | | | apply_sender") | | | | | | Sender algorithms | | | | | | Sender factories | | | | | | just | | | | | | just_error | | | | | | just_stopped | | | | | | read_env | | | | | | schedule schedule_result_t | | | | | | Sender adaptors | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | starts_on") | | | | | | continues_on") | | | | | | on | | | | | | then | | | | | | upon_error | | | | | | upon_stopped | | | | | | let_value | | | | | | let_error | | | | | | let_stopped | | | | | | schedule_from") | | | | | | when_all | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | when_all_with_variant") | | | | | | into_variant | | | | | | stopped_as_optional | | | | | | stopped_as_error | | | | | | bulk") | | | | | | split") | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | | Sender consumers | | | | | | this_thread::sync_wait | | | | | | this_thread::sync_wait_with_variant") | | | | | |  | | | | | |

The Execution library provides a framework for managing asynchronous execution on generic execution resources.

The library aims to provide vocabulary types for asynchronous operations and to allow the construction of task execution graphs in a simple, composable way.

## Library-wide definitions

- ****Sender****: A description of asynchronous work to be sent for execution. Produces an operation state (below).

:   - Senders asynchronously “send” their results to listeners called “receivers” (below).
    - Senders can be composed into ****task graphs**** using generic algorithms.
    - ****Sender factories and adaptors**** are generic algorithms that capture common async patterns in objects satisfying the sender concept.

- ****Receiver****: A generalized callback that consumes or “receives” the asynchronous results produced by a sender.

:   - Receivers have three different “channels” through which a sender may propagate results: success, failure, and canceled, so-named “value”, “error”, and “stopped”.
    - Receivers provide an extensible execution environment: a set of key/value pairs that the consumer can use to parameterize the asynchronous operation.

- ****Operation State****: An object that contains the state needed by the asynchronous operation.

:   - A sender and receiver are connected when passed to the std::execution::connect function.
    - The result of connecting a sender and a receiver is an operation state.
    - Work is not enqueued for execution until “`start`” is called on an operation state.
    - Once started, the operation state’s lifetime cannot end before the async operation is complete, and its address must be stable.

- ****Scheduler****: A lightweight handle to an execution context.

:   - An execution context is a source of asynchronous execution such as a thread pool or a GPU stream.
    - A scheduler is a factory for a sender that completes its receiver from a thread of execution owned by the execution context.

## Library utilities

### Concepts

#### Schedulers

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::scheduler(C++26) | specifies that a type is a scheduler   (concept) |

#### Senders

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::sender")(C++26) | specifies that a type is a sender   (concept) |
| execution::sender_in")(C++26) | specifies a sender that can create asynchronous operations for given associated environment type   (concept) |
| execution::sender_to")(C++26) | specifies a sender that can connect with a specific receiver type   (concept) |

#### Receivers

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::receiver")(C++26) | specifies that a type is a receiver   (concept) |
| execution::receiver_of")(C++26) | specifies that a type is a receiver for given completion signatures   (concept) |

#### Operation states

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::operation_state")(C++26) | specifies that a type is an operation state   (concept) |

### Utility components

#### Execution contexts

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::run_loop")(C++26) | execution resource holding a thread-safe MPSC task queue and a manually-driven event loop   (class) |

#### Execution domains

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::default_domain")(C++26) | default execution domain tag type that dispatches transformations from a sender tag   (class) |
| execution::transform_sender")(C++26) | transforms into a new sender under a given execution domain tag   (function template) |
| execution::transform_env")(C++26) | transforms into a new queryable object under a given execution domain tag   (function template) |
| execution::apply_sender")(C++26) | consumes a sender using a given sender consumer tag with a set of arguments and returns its result under a given execution domain tag   (function template) |

#### Forward progress guarantee

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::forward_progress_guarantee")(C++26) | specifies a forward progress guarantee of execution agents created by the scheduler's associated execution resource   (enum) |

#### Environments

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::prop")(C++26) | builds a queryable object from a query object and a value   (class template) |
| execution::env")(C++26) | aggregates several queryable objects into one queryable object   (class template) |
| execution::get_env")(C++26) | returns the associated queryable object for its given argument (customization point object) |

#### Queries

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| forwarding_query")(C++26) | asks a query object whether it should be forwarded through queryable adaptors (customization point object) |
| get_allocator")(C++26) | asks a queryable object for its associated allocator (customization point object) |
| get_stop_token")(C++26) | asks a queryable object for its associated stop token (customization point object) |
| execution::get_domain")(C++26) | asks a queryable object for its associated execution domain tag (customization point object) |
| execution::get_scheduler")(C++26) | asks a queryable object for its associated scheduler (customization point object) |
| execution::get_delegation_scheduler")(C++26) | asks a queryable object for a scheduler that can be used to delegate work to for the purpose of forward progress delegation (customization point object) |
| execution::get_completion_scheduler")(C++26) | obtains the completion scheduler associated with a completion tag from a sender's attributes (customization point object) |
| execution::get_forward_progress_guarantee")(C++26) | asks a scheduler about its execution::forward_progress_guarantee (customization point object) |

#### Completion signatures

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::completion_signatures")(C++26) | type that encodes a set of completion signatures   (class template) |
| execution::get_completion_signatures")(C++26) | obtains the completion signatures of a sender (customization point object) |
| execution::transform_completion_signatures")(C++26) | transforms one set of completion signatures into another (alias template) |
| execution::transform_completion_signatures_of")(C++26) | transforms completion signatures of a sender (alias template) |
| execution::tag_of_t")(C++26) | obtains the tag type of a sender (alias template) |
| execution::value_types_of_t")(C++26) | obtains the value completion type of a sender (alias template) |
| execution::error_types_of_t")(C++26) | obtains the error completion type of a sender (alias template) |
| execution::sends_stopped")(C++26) | determines whether the sender supports stopped completion (variable template) |

#### Coroutine utility

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::as_awaitable")(C++26) | transforms an expression into awaitable object within a particular coroutine (customization point object) |
| execution::with_awaitable_senders")(C++26) | when used as the base class of a coroutine promise type, enables senders to be awaitable within that coroutine type   (class template) |

### Core operations

#### Operation state

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::connect")(C++26) | connects a `sender`") with a `receiver`") (customization point object) |
| execution::start")(C++26) | starts the asynchronous operation associated with an `operation_state`") object (customization point object) |

#### Completion functions

These functions are called by senders to announce the completion of the work to their receivers.

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::set_value")(C++26) | value completion function indicating successful completion (customization point object) |
| execution::set_error")(C++26) | error completion function indicating that an error occurred during calculation or scheduling (customization point object) |
| execution::set_stopped")(C++26) | stopped completion function indicating that an operation ended before it could achieve success or failure (customization point object) |

### Sender algorithms

|  |  |
| --- | --- |
|  | This section is incomplete Reason: WIP update to current standard in progress |

#### Sender factories

A sender factory is a function that returns a sender and whose parameters have types for which the `sender`") concept is false.

The following are sender factories:

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::just(C++26) | Accepts a variadic number of arguments and returns a sender that, when connected and started, completes synchronously by passing the arguments to the receiver's value completion function (customization point object) |
| execution::just_error(C++26) | Accepts a single argument and returns a sender that, when connected and started, completes synchronously by passing the argument to the receiver's error completion function (customization point object) |
| execution::just_stopped(C++26) | creates a sender that completes immediately by calling its receiver's `set_stopped` (customization point object) |
| execution::read_env(C++26) | creates a sender that queries its receiver's associated environment (customization point object) |
| execution::schedule(C++26) | prepares a task graph for execution on a given scheduler (customization point object) |

#### Pipeable sender adaptors

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::sender_adaptor_closure")(C++26) | helper base class template for defining a pipeable sender adaptor closure object   (class template) |

#### Sender adaptors

A sender adaptor is a function returning a sender whose parameters include at least one whose type satisfies the `sender`") concept, and for which the returned sender is a parent sender of the adaptor function's sender arguments.

The following are sender adaptors:

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::execution` | |
| execution::starts_on")(C++26) | adapts a provided sender into one that will start an execution on the provided scheduler's execution resource (customization point object) |
| execution::continues_on")(C++26) | adapts a provided sender into one that completes on the provided scheduler's execution resource (customization point object) |
| execution::on(C++26) | adapts a provided sender to transfer execution to a provided scheduler's execution resource on which the sender or the continuation runs, and then transfers execution back to the original resource (customization point object) |
| execution::schedule_from")(C++26) | schedules work dependent on the completion of a provided sender onto a provided scheduler's execution resource (customization point object) |
| execution::then(C++26) | chains the task graph by the input sender with a node represents invoking the provided function with the values sent by the input sender as arguments (customization point object) |
| execution::upon_error(C++26) | chains the task graph by the input sender with a node representing invoking the provided function with the error sent by the input sender if an error occurred (customization point object) |
| execution::upon_stopped(C++26) | chains the task graph by the input sender with a node representing invoking the provided function with the stopped behavior by the input sender if a "stopped" signal is sent (customization point object) |
| execution::let_value(C++26) | returns a sender which represents a node chained to the input sender, which when started, invokes the provided function with the values sent by the input sender as arguments (customization point object) |
| execution::let_error(C++26) | returns a sender which represents a node chained to the input sender, which invokes the provided function with the error from the input sender, if occurred (customization point object) |
| execution::let_stopped(C++26) | returns a sender which represents a node chained to the input sender, which invokes the provided function with the stop token from the input sender, if the "stopped" signal is sent (customization point object) |
| execution::bulk")(C++26) | creates a multi-shot sender that invokes the function with every index in the provided shape along with the values sent by the input sender. The sender completes once all invocations have completed, or an error has occurred (customization point object) |
| execution::split")(C++26) | if the provided sender is a multi-shot sender, returns that sender, otherwise, returns a multi-shot sender which sends values equivalent to the values sent by the provided sender (customization point object) |
| execution::when_all(C++26) | adapts multiple input senders into a sender that completes once all of the input senders have completed (customization point object) |
| execution::when_all_with_variant")(C++26) | adapts multiple input senders, with each possibly having multiple completion signatures, into a sender that completes once all of the input senders have completed (customization point object) |
| execution::into_variant(C++26) | returns a sender which sends a variant of tuples of all the possible sets of types sent by the input sender (customization point object) |
| execution::stopped_as_optional(C++26) | returns a sender that maps the value channel to std::optional<std::decay_t<T>> and the stopped channel to std::nullopt (customization point object) |
| execution::stopped_as_error(C++26) | returns a sender that maps the stopped channel to an error (customization point object) |

#### Sender consumers

A sender consumer is an algorithm that takes one or more senders as parameters and that does not return a sender.

|  |  |
| --- | --- |
| Defined in header `<execution>` | |
| Defined in namespace `std::this_thread` | |
| this_thread::sync_wait(C++26) | blocks current thread until the specified sender completes and returns its async result (customization point object) |
| this_thread::sync_wait_with_variant")(C++26) | blocks current thread until the specified sender with possibly multiple completion signatures completes and returns its async result (customization point object) |

### Example

A version of this example is available on godbolt.org, where it uses stdexec, an experimental reference implementation of std::execution.

Run this code

```
#include <cstdio>
#include <execution>
#include <string>
#include <thread>
#include <utility>
using namespace std::literals;
 
int main()
{
    std::execution::run_loop loop;
 
    std::jthread worker(&
    {
        std::stop_callback cb{st, [&]{ loop.finish(); }};
        loop.run();
    });
 
    std::execution::sender auto hello = std::execution::just("hello world"s);
    std::execution::sender auto print
        = std::move(hello)
        | std::execution::then([](std::string msg)
        {
            return std::puts(msg.c_str());
        });
 
    std::execution::scheduler auto io_thread = loop.get_scheduler();
    std::execution::sender auto work = std::execution::on(io_thread, std::move(print));
 
    auto [result] = std::this_thread::sync_wait(std::move(work)).value();
 
    return result;
}

```

Output:

```
hello world

```

### See also

|  |  |
| --- | --- |
| async(C++11) | runs a function asynchronously (potentially in a new thread) and returns a std::future that will hold the result   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/execution&oldid=179211>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 January 2025, at 12:59.