# Standard library header <cerrno>

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | ****<cerrno>**** | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header was originally in the C standard library as <errno.h>.

This header is part of the error handling library.

### Macros

|  |  |
| --- | --- |
| errno | macro which expands to POSIX-compatible thread-local error number variable (macro variable) |
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
| EILSEQ | Illegal byte sequence   (macro constant) |
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
| ENODATA(C++11) (deprecated in C++23) | No message is available on the STREAM head read queue   (macro constant) |
| ENODEV(C++11) | No such device   (macro constant) |
| ENOENT(C++11) | No such file or directory   (macro constant) |
| ENOEXEC(C++11) | Executable file format error   (macro constant) |
| ENOLCK(C++11) | No locks available   (macro constant) |
| ENOLINK(C++11) | Link has been severed   (macro constant) |
| ENOMEM(C++11) | Not enough space   (macro constant) |
| ENOMSG(C++11) | No message of the desired type   (macro constant) |
| ENOPROTOOPT(C++11) | Protocol not available   (macro constant) |
| ENOSPC(C++11) | No space left on device   (macro constant) |
| ENOSR(C++11) (deprecated in C++23) | No STREAM resources   (macro constant) |
| ENOSTR(C++11) (deprecated in C++23) | Not a STREAM   (macro constant) |
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
| ETIME(C++11) (deprecated in C++23) | Stream `ioctl()` timeout   (macro constant) |
| ETIMEDOUT(C++11) | Connection timed out   (macro constant) |
| ETXTBSY(C++11) | Text file busy   (macro constant) |
| EWOULDBLOCK(C++11) | Operation would block   (macro constant) |
| EXDEV(C++11) | Cross-device link   (macro constant) |

### Notes

Although the header `<cerrno>` is based on the C standard library header <errno.h>, the majority of the macros defined by `<cerrno>` were adopted by C++ from the POSIX standard, rather than the C standard library.

### Synopsis

```
#define errno /* see description */
#define E2BIG /* see description */           // freestanding
#define EACCES /* see description */          // freestanding
#define EADDRINUSE /* see description */      // freestanding
#define EADDRNOTAVAIL /* see description */   // freestanding
#define EAFNOSUPPORT /* see description */    // freestanding
#define EAGAIN /* see description */          // freestanding
#define EALREADY /* see description */        // freestanding
#define EBADF /* see description */           // freestanding
#define EBADMSG /* see description */         // freestanding
#define EBUSY /* see description */           // freestanding
#define ECANCELED /* see description */       // freestanding
#define ECHILD /* see description */          // freestanding
#define ECONNABORTED /* see description */    // freestanding
#define ECONNREFUSED /* see description */    // freestanding
#define ECONNRESET /* see description */      // freestanding
#define EDEADLK /* see description */         // freestanding
#define EDESTADDRREQ /* see description */    // freestanding
#define EDOM /* see description */            // freestanding
#define EEXIST /* see description */          // freestanding
#define EFAULT /* see description */          // freestanding
#define EFBIG /* see description */           // freestanding
#define EHOSTUNREACH /* see description */    // freestanding
#define EIDRM /* see description */           // freestanding
#define EILSEQ /* see description */          // freestanding
#define EINPROGRESS /* see description */     // freestanding
#define EINTR /* see description */           // freestanding
#define EINVAL /* see description */          // freestanding
#define EIO /* see description */             // freestanding
#define EISCONN /* see description */         // freestanding
#define EISDIR /* see description */          // freestanding
#define ELOOP /* see description */           // freestanding
#define EMFILE /* see description */          // freestanding
#define EMLINK /* see description */          // freestanding
#define EMSGSIZE /* see description */        // freestanding
#define ENAMETOOLONG /* see description */    // freestanding
#define ENETDOWN /* see description */        // freestanding
#define ENETRESET /* see description */       // freestanding
#define ENETUNREACH /* see description */     // freestanding
#define ENFILE /* see description */          // freestanding
#define ENOBUFS /* see description */         // freestanding
#define ENODEV /* see description */          // freestanding
#define ENOENT /* see description */          // freestanding
#define ENOEXEC /* see description */         // freestanding
#define ENOLCK /* see description */          // freestanding
#define ENOLINK /* see description */         // freestanding
#define ENOMEM /* see description */          // freestanding
#define ENOMSG /* see description */          // freestanding
#define ENOPROTOOPT /* see description */     // freestanding
#define ENOSPC /* see description */          // freestanding
#define ENOSYS /* see description */          // freestanding
#define ENOTCONN /* see description */        // freestanding
#define ENOTDIR /* see description */         // freestanding
#define ENOTEMPTY /* see description */       // freestanding
#define ENOTRECOVERABLE /* see description */ // freestanding
#define ENOTSOCK /* see description */        // freestanding
#define ENOTSUP /* see description */         // freestanding
#define ENOTTY /* see description */          // freestanding
#define ENXIO /* see description */           // freestanding
#define EOPNOTSUPP /* see description */      // freestanding
#define EOVERFLOW /* see description */       // freestanding
#define EOWNERDEAD /* see description */      // freestanding
#define EPERM /* see description */           // freestanding
#define EPIPE /* see description */           // freestanding
#define EPROTO /* see description */          // freestanding
#define EPROTONOSUPPORT /* see description */ // freestanding
#define EPROTOTYPE /* see description */      // freestanding
#define ERANGE /* see description */          // freestanding
#define EROFS /* see description */           // freestanding
#define ESPIPE /* see description */          // freestanding
#define ESRCH /* see description */           // freestanding
#define ETIMEDOUT /* see description */       // freestanding
#define ETXTBSY /* see description */         // freestanding
#define EWOULDBLOCK /* see description */     // freestanding
#define EXDEV /* see description */           // freestanding

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 288 | C++98 | the macro `EILSEQ` was not defined in `<cerrno>` | defined |

### See also

- Description for the error number values
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/cerrno&oldid=158957>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2023, at 01:02.