# cpp/compiler support/vendors

From cppreference.com
< cpp‎ | compiler support

### Individual vendor compatibility checklists

#### GCC (updated 2025-01)

- C++11 core language support status (complete as of 4.8.1, except for N2670, which is implemented by no compiler and removed in C++23)
- C++14 core language support status (complete as of 5.1)
- C++17 core language support status (complete as of 7.1)
- C++20 core language support status(complete as of 11.0, except part of modules)
- C++23 core language support status
- C++26 core language support status
- C++11 library support status (complete as of 5.1)
- C++14 library support status (complete as of 5.1)
- C++17 library support status (complete as of 12.0)
- C++20 library support status (complete as of 14.0)
- C++23 library support status
- Technical Specifications support status
- Core language defect report status

#### Clang (updated 2025-01)

- Real-time libc++ conformance status
- C++11 core language support status (complete as of 3.3)
- C++11 library support status (complete as of 2012-07-29)
- C++14 core language support status (complete as of 3.4)
- C++14 library support status (complete as of 3.5)
- C++17 core language support status (complete as of 5.0)
- C++17 library support status
- C++20 core language support status
- C++20 library support status
- C++23 core language support status
- C++23 library support status
- C++26 core language support status
- C++26 library support status
- Technical Specifications support status
- Core language defect report status

#### Apple Clang (updated 2025-01)

- Xcode toolchain versions on Wikipedia
- Xcode C++ language and C++ standard library support
- Xcode release notes
- C++20/23/26 support status in Xcode 16

#### Microsoft Visual Studio (updated 2025-01)

- Microsoft C/C++ language conformance (Visual Studio 2015 and later)
- Upcoming releases Visual Studio 2022 change log
- C++17/20 Features and Fixes in Visual Studio 2019
- STL Features and Fixes in VS 2017 15.8
- C++17 Announcing: MSVC Conforms to the C++ Standard (complete as of 15.7)
- C++17 Features And STL Fixes In VS 2017 15.5
- C++17 Features And STL Fixes In VS 2017 15.3
- C++11/C++14/C++17 core language and library status in VS2017.3
- C++11/C++14/C++17 core language support status
  - C++11/14/17 core language support status in VS2010, VS2012, VS2013, and VS2015
  - VS2013 vs. VS2015 CTP0
  - VS2013 vs. VS2015 CTP1
  - VS2013 vs. VS2015 CTP3 (includes the roadmap table)
  - VS2015 ("VS14") preview
  - VS2015 ("VS14") release candidate (C++11 remains incomplete, but C++17 support appears)
  - VS2019
- C++11 and C++14 library support status
- C++11/14/17 Features In VS 2015 RTM including core language and standard library (including technical specifications)
- C++14/17 features in VS 2015 Update 2 standard library library is feature complete up to current C++17 with few minor issues (some defect reports, some constexprs, etc)
- C++14/17 Features and STL Fixes in VS “15” Preview 5 including a detailed C++17 status table

#### Intel C++ (updated 2023-01)

- C++11 core language support status (complete as of 15.0)
- C++14 core language support status (functionally complete as of 17.0 - N3664 is an optimization)
- C++17 core language support status (incomplete)
- C++20 core language support status (incomplete)
- C++17 features of Intel 19.0 beta
- Intel does not ship an implementation of the C++ standard library, except for
  - Parallel STL (an implementation of the C++17 standard library algorithms with support for execution policies)
- Intel's compatibility with versions of libstdc++ from GCC

#### EDG (updated 2025-01)

- C++11 core language support status
- C++14 core language support status
- C++17 core language support status
- C++20 core language support status
- C++23 core language support status
- C++26 core language support status
- EDG does not ship an implementation of the C++ standard library

#### Oracle C++ (updated 2017-07)

- Version number is compiler version, not Oracle Studio version
- C++11 core language support status in 5.13
  - Missing C++11 support added in 5.14 (page has a typo, and still says 5.13)
- C++14 features added in 5.14
  - Full C++14 support added in 5.15.
- Oracle ships 4 implementations of the C++ standard library:
  - libCstd (RogueWave Standard Library version 2), predates C++98
  - stlport4 (STLport Standard Library version 4.5.3), predates C++03
  - stdcxx4 (Apache Standard Library version 4), predates C++11
  - libstdc++ (GCC runtime library, support for C++11 and C++14 depending on release)

#### IBM XL C++ (updated 2018-05)

- IBM XL C++ for Linux
  - Core language support status: C++11 complete as of 13.1.6, C++14 partial in 16.1.0
  - IBM does not ship an implementation of C++ standard library for Linux (uses GNU libstdc++)
- IBM XL C++ for AIX
  - Core language support status: C++11 partial in 13.1.3 and 16.1.0 (xlC frontend), complete in 16.1.0 (xlclang frontend)
  - IBM ships a version of Dinkumware library for AIX with full support for C++ TR1, including <regex>, but no C++11
  - IBM XL C/C++ compilers features

#### HP aCC

- HP aC++ A.06.28 release notes (including C++11 core language features)
- HP ships a version of RogueWave STL 2.0 implementation of the C++98 standard library

#### Digital Mars C++

- C++11 core language support status

#### Embarcadero C++

- Language features compliance status (RAD Studio 10.1 Berlin), including C++11 features supported by legacy and Clang-enhanced compilers (based on Clang 3.3)
- Language features compliance status (RAD Studio 10.3 Rio), including C++11 features supported by legacy compilers and C++11, C++14, and C++17 features supported by the Clang-enhanced compilers (based on Clang 5.0)

#### Cray (updated 2023-02)

- Cray C and C++ Reference Manual (8.4) For version 8.4, claims all of C++14 is supported except alignas
- Cray C and C++ Reference Manual (8.6) For version 8.6, claims all of C++14 is supported
- Cray C and C++ Reference Manual (9.1) for version 9.1 doesn't claim support beyond C++14
- HPE Cray Clang C and C++ Quick Reference (14.0) (S-2179) Versions from 11 onward (through at least 14) are based on Clang, and are generally expected to have corresponding language support. Features that entail 'interesting' code generation or linking behaviors such as coroutines or modules may lag behind, since the compiler supports generating code for GPUs and other similarly limited devices

#### Portland Group (PGI) (updated 2019-01)

- Release notes for 2016 claim C++14 support, except "generalized constexpr and constexpr member functions and implicit const, variable templates, clarifying memory allocation (merged allocation)"
- Release notes for 2018
- Reference manual of PGI 19.1
- PGI does not ship an implementation of C++ standard library

#### Nvidia Cuda nvcc (updated 2023-01-12)

- CUDA C++ Programming Guide (v12.0)
- All C++17 language features are supported in nvcc version 11.0 and later, subject to restrictions described here
- All C++20 language features are supported in nvcc version 12.0 and later, subject to restrictions described here
- NVCC does not ship a C++ standard library implementation

#### Texas Instruments (updated 2018-05)

- cl430 version v18.1.0 claims C++14 support

#### Analog Devices (updated 2018-05)

- CrossCore Embedded Studio 2.8.0 for SHARC claims C++11 support
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/compiler_support/vendors&oldid=179841>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 January 2025, at 01:09.