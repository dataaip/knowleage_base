# Error numbers

From cppreference.com
< cpp‎ | error
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

Diagnostics library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception handling | | | | | | exception | | | | | | uncaught_exceptionuncaught_exceptions(until C++20\*)(C++17) | | | | | | exception_ptr(C++11) | | | | | | make_exception_ptr(C++11) | | | | | | current_exception(C++11) | | | | | | rethrow_exception(C++11) | | | | | | nested_exception(C++11) | | | | | | throw_with_nested(C++11) | | | | | | rethrow_if_nested(C++11) | | | | | | Exception handling failures | | | | | | terminate | | | | | | terminate_handler | | | | | | get_terminate(C++11) | | | | | | set_terminate | | | | | | bad_exception | | | | | | unexpected(until C++17\*) | | | | | | unexpected_handler(until C++17\*) | | | | | | get_unexpected(until C++17\*) | | | | | | set_unexpected(until C++17\*) | | | | | | Error numbers | | | | | | ****Error codes**** | | | | | | errno | | | | | | Assertions | | | | | | assert | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exception categories | | | | | | logic_error | | | | | | invalid_argument | | | | | | domain_error | | | | | | length_error | | | | | | out_of_range | | | | | | runtime_error | | | | | | range_error | | | | | | overflow_error | | | | | | underflow_error | | | | | | tx_exception(TM TS) | | | | | | System error | | | | | | error_category(C++11) | | | | | | generic_category(C++11) | | | | | | system_category(C++11) | | | | | | error_condition(C++11) | | | | | | errc(C++11) | | | | | | error_code(C++11) | | | | | | system_error(C++11) | | | | | | Stacktrace | | | | | | stacktrace_entry(C++23) | | | | | | basic_stacktrace(C++23) | | | | | | Debugging support | | | | | | is_debugger_present(C++26) | | | | | | breakpoint_if_debugging(C++26) | | | | | | breakpoint(C++26) | | | | | |

Each of the macros defined in <cerrno> expands to integer constant expressions with type int, each with a positive value, matching most of the POSIX error codes. The following constants are defined (the implementation may define more, as long as they begin with 'E' followed by digits or uppercase letters).

|  |  |
| --- | --- |
| Defined in header `<cerrno>` | |
| E2BIG(C++11) | Argument list too long   (macro constant) |
| EACCES(C++11) | Permission denied   (macro constant) |
| EADDRINUSE(C++11) | Address in use   (macro constant) |
| EADDRNOTAVAIL(C++11) | Address not available   (macro constant) |
| EAFNOSUPPORT(C++11) | Address family not supported   (macro constant) |
| EAGAIN(C++11) | Resource unavailable, try again   (macro constant) |
| EALREADY(C++11) | Connection already in progress   (macro constant) |
| EBADF(C++11) | Bad file descriptor   (macro constant) |
| EBADMSG(C++11) | Bad message   (macro constant) |
| EBUSY(C++11) | Device or resource busy   (macro constant) |
| ECANCELED(C++11) | Operation canceled   (macro constant) |
| ECHILD(C++11) | No child processes   (macro constant) |
| ECONNABORTED(C++11) | Connection aborted   (macro constant) |
| ECONNREFUSED(C++11) | Connection refused   (macro constant) |
| ECONNRESET(C++11) | Connection reset   (macro constant) |
| EDEADLK(C++11) | Resource deadlock would occur   (macro constant) |
| EDESTADDRREQ(C++11) | Destination address required   (macro constant) |
| EDOM | Mathematics argument out of domain of function   (macro constant) |
| EEXIST(C++11) | File exists   (macro constant) |
| EFAULT(C++11) | Bad address   (macro constant) |
| EFBIG(C++11) | File too large   (macro constant) |
| EHOSTUNREACH(C++11) | Host is unreachable   (macro constant) |
| EIDRM(C++11) | Identifier removed   (macro constant) |
| EILSEQ(C++11) | Illegal byte sequence   (macro constant) |
| EINPROGRESS(C++11) | Operation in progress   (macro constant) |
| EINTR(C++11) | Interrupted function   (macro constant) |
| EINVAL(C++11) | Invalid argument   (macro constant) |
| EIO(C++11) | I/O error   (macro constant) |
| EISCONN(C++11) | Socket is connected   (macro constant) |
| EISDIR(C++11) | Is a directory   (macro constant) |
| ELOOP(C++11) | Too many levels of symbolic links   (macro constant) |
| EMFILE(C++11) | File descriptor value too large   (macro constant) |
| EMLINK(C++11) | Too many links   (macro constant) |
| EMSGSIZE(C++11) | Message too large   (macro constant) |
| ENAMETOOLONG(C++11) | Filename too long   (macro constant) |
| ENETDOWN(C++11) | Network is down   (macro constant) |
| ENETRESET(C++11) | Connection aborted by network   (macro constant) |
| ENETUNREACH(C++11) | Network unreachable   (macro constant) |
| ENFILE(C++11) | Too many files open in system   (macro constant) |
| ENOBUFS(C++11) | No buffer space available   (macro constant) |
| ENODATA(C++11) | No message is available on the STREAM head read queue   (macro constant) |
| ENODEV(C++11) | No such device   (macro constant) |
| ENOENT(C++11) | No such file or directory   (macro constant) |
| ENOEXEC(C++11) | Executable file format error   (macro constant) |
| ENOLCK(C++11) | No locks available   (macro constant) |
| ENOLINK(C++11) | Link has been severed   (macro constant) |
| ENOMEM(C++11) | Not enough space   (macro constant) |
| ENOMSG(C++11) | No message of the desired type   (macro constant) |
| ENOPROTOOPT(C++11) | Protocol not available   (macro constant) |
| ENOSPC(C++11) | No space left on device   (macro constant) |
| ENOSR(C++11) | No STREAM resources   (macro constant) |
| ENOSTR(C++11) | Not a STREAM   (macro constant) |
| ENOSYS(C++11) | Function not supported   (macro constant) |
| ENOTCONN(C++11) | The socket is not connected   (macro constant) |
| ENOTDIR(C++11) | Not a directory   (macro constant) |
| ENOTEMPTY(C++11) | Directory not empty   (macro constant) |
| ENOTRECOVERABLE(C++11) | State not recoverable   (macro constant) |
| ENOTSOCK(C++11) | Not a socket   (macro constant) |
| ENOTSUP(C++11) | Not supported   (macro constant) |
| ENOTTY(C++11) | Inappropriate I/O control operation   (macro constant) |
| ENXIO(C++11) | No such device or address   (macro constant) |
| EOPNOTSUPP(C++11) | Operation not supported on socket   (macro constant) |
| EOVERFLOW(C++11) | Value too large to be stored in data type   (macro constant) |
| EOWNERDEAD(C++11) | Previous owner died   (macro constant) |
| EPERM(C++11) | Operation not permitted   (macro constant) |
| EPIPE(C++11) | Broken pipe   (macro constant) |
| EPROTO(C++11) | Protocol error   (macro constant) |
| EPROTONOSUPPORT(C++11) | Protocol not supported   (macro constant) |
| EPROTOTYPE(C++11) | Protocol wrong type for socket   (macro constant) |
| ERANGE | Result too large   (macro constant) |
| EROFS(C++11) | Read-only file system   (macro constant) |
| ESPIPE(C++11) | Invalid seek   (macro constant) |
| ESRCH(C++11) | No such process   (macro constant) |
| ETIME(C++11) | Stream ioctl() timeout   (macro constant) |
| ETIMEDOUT(C++11) | Connection timed out   (macro constant) |
| ETXTBSY(C++11) | Text file busy   (macro constant) |
| EWOULDBLOCK(C++11) | Operation would block   (macro constant) |
| EXDEV(C++11) | Cross-device link   (macro constant) |

All values are required to be unique except that the values of `EOPNOTSUPP` and `ENOTSUP` may be identical and the values of `EAGAIN` and `EWOULDBLOCK` may be identical.

### Example

Run this code

```
#include <cerrno>
#include <cstring>
#include <iomanip>
#include <iostream>
 
#define SHOW(x) std::cout << std::setw(15) << #x << ": " << std::strerror(x) << '\n'
 
int main()
{
    std::cout << "Known error codes/messages:\n\n";
 
    SHOW( E2BIG );
    SHOW( EACCES );
    SHOW( EADDRINUSE );
    SHOW( EADDRNOTAVAIL );
    SHOW( EAFNOSUPPORT );
    SHOW( EAGAIN );
    SHOW( EALREADY );
    SHOW( EBADF );
    SHOW( EBADMSG );
    SHOW( EBUSY );
    SHOW( ECANCELED );
    SHOW( ECHILD );
    SHOW( ECONNABORTED );
    SHOW( ECONNREFUSED );
    SHOW( ECONNRESET );
    SHOW( EDEADLK );
    SHOW( EDESTADDRREQ );
    SHOW( EDOM );
    SHOW( EEXIST );
    SHOW( EFAULT );
    SHOW( EFBIG );
    SHOW( EHOSTUNREACH );
    SHOW( EIDRM );
    SHOW( EILSEQ );
    SHOW( EINPROGRESS );
    SHOW( EINTR );
    SHOW( EINVAL );
    SHOW( EIO );
    SHOW( EISCONN );
    SHOW( EISDIR );
    SHOW( ELOOP );
    SHOW( EMFILE );
    SHOW( EMLINK );
    SHOW( EMSGSIZE );
    SHOW( ENAMETOOLONG );
    SHOW( ENETDOWN );
    SHOW( ENETRESET );
    SHOW( ENETUNREACH );
    SHOW( ENFILE );
    SHOW( ENOBUFS );
    SHOW( ENODATA );
    SHOW( ENODEV );
    SHOW( ENOENT );
    SHOW( ENOEXEC );
    SHOW( ENOLCK );
    SHOW( ENOLINK );
    SHOW( ENOMEM );
    SHOW( ENOMSG );
    SHOW( ENOPROTOOPT );
    SHOW( ENOSPC );
    SHOW( ENOSR );
    SHOW( ENOSTR );
    SHOW( ENOSYS );
    SHOW( ENOTCONN );
    SHOW( ENOTDIR );
    SHOW( ENOTEMPTY );
    SHOW( ENOTRECOVERABLE );
    SHOW( ENOTSOCK );
    SHOW( ENOTSUP );
    SHOW( ENOTTY );
    SHOW( ENXIO );
    SHOW( EOPNOTSUPP );
    SHOW( EOVERFLOW );
    SHOW( EOWNERDEAD );
    SHOW( EPERM );
    SHOW( EPIPE );
    SHOW( EPROTO );
    SHOW( EPROTONOSUPPORT );
    SHOW( EPROTOTYPE );
    SHOW( ERANGE );
    SHOW( EROFS );
    SHOW( ESPIPE );
    SHOW( ESRCH );
    SHOW( ETIME );
    SHOW( ETIMEDOUT );
    SHOW( ETXTBSY );
    SHOW( EWOULDBLOCK );
    SHOW( EXDEV );
}

```

Possible output:

```
Known error codes/messages:
 
          E2BIG: Argument list too long
         EACCES: Permission denied
     EADDRINUSE: Address already in use
  EADDRNOTAVAIL: Cannot assign requested address
   EAFNOSUPPORT: Address family not supported by protocol
         EAGAIN: Resource temporarily unavailable
       EALREADY: Operation already in progress
          EBADF: Bad file descriptor
        EBADMSG: Bad message
          EBUSY: Device or resource busy
      ECANCELED: Operation canceled
         ECHILD: No child processes
   ECONNABORTED: Software caused connection abort
   ECONNREFUSED: Connection refused
     ECONNRESET: Connection reset by peer
        EDEADLK: Resource deadlock avoided
   EDESTADDRREQ: Destination address required
           EDOM: Numerical argument out of domain
         EEXIST: File exists
         EFAULT: Bad address
          EFBIG: File too large
   EHOSTUNREACH: No route to host
          EIDRM: Identifier removed
         EILSEQ: Invalid or incomplete multibyte or wide character
    EINPROGRESS: Operation now in progress
          EINTR: Interrupted system call
         EINVAL: Invalid argument
            EIO: Input/output error
        EISCONN: Transport endpoint is already connected
         EISDIR: Is a directory
          ELOOP: Too many levels of symbolic links
         EMFILE: Too many open files
         EMLINK: Too many links
       EMSGSIZE: Message too long
   ENAMETOOLONG: File name too long
       ENETDOWN: Network is down
      ENETRESET: Network dropped connection on reset
    ENETUNREACH: Network is unreachable
         ENFILE: Too many open files in system
        ENOBUFS: No buffer space available
        ENODATA: No data available
         ENODEV: No such device
         ENOENT: No such file or directory
        ENOEXEC: Exec format error
         ENOLCK: No locks available
        ENOLINK: Link has been severed
         ENOMEM: Cannot allocate memory
         ENOMSG: No message of desired type
    ENOPROTOOPT: Protocol not available
         ENOSPC: No space left on device
          ENOSR: Out of streams resources
         ENOSTR: Device not a stream
         ENOSYS: Function not implemented
       ENOTCONN: Transport endpoint is not connected
        ENOTDIR: Not a directory
      ENOTEMPTY: Directory not empty
ENOTRECOVERABLE: State not recoverable
       ENOTSOCK: Socket operation on non-socket
        ENOTSUP: Operation not supported
         ENOTTY: Inappropriate ioctl for device
          ENXIO: No such device or address
     EOPNOTSUPP: Operation not supported
      EOVERFLOW: Value too large for defined data type
     EOWNERDEAD: Owner died
          EPERM: Operation not permitted
          EPIPE: Broken pipe
         EPROTO: Protocol error
EPROTONOSUPPORT: Protocol not supported
     EPROTOTYPE: Protocol wrong type for socket
         ERANGE: Numerical result out of range
          EROFS: Read-only file system
         ESPIPE: Illegal seek
          ESRCH: No such process
          ETIME: Timer expired
      ETIMEDOUT: Connection timed out
        ETXTBSY: Text file busy
    EWOULDBLOCK: Resource temporarily unavailable
          EXDEV: Invalid cross-device link

```

### See also

|  |  |
| --- | --- |
| errc(C++11) | the std::error_condition enumeration listing all standard <cerrno> macro constants   (class) |
| errno | macro which expands to POSIX-compatible thread-local error number variable (macro variable) |
| perror | displays a character string corresponding of the current error to stderr   (function) |
| strerror | returns a text version of a given error code   (function) |
| C documentation for Error numbers | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/error/errno_macros&oldid=157320>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 August 2023, at 11:21.