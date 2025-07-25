# A list of open-source C++ libraries

From cppreference.com
< cpp‎ | links

The objective of this page is to build a comprehensive list of open-source C++ libraries, so that when one needs an implementation of particular functionality, one needn’t to waste time searching on web (DuckDuckGo, Google, Bing, etc.)

If you know a library that might be useful to others, please add a link to it here. There are no restrictions on what can be included except that the ****source**** of the library must be readily ****available**** to download.

The page is provided “as is” - with the hope of being useful, but without any warranties. Outdated, misleading or wrong links might appear here. If you’ve noticed one of these, it would be great if you fixed the error.

| Libraries: Table Of Contents |
| --- |
| - Package managers  ---   Libraries:   - Audio   - CD   - Fingerprinting   - Formats   - Tagging - Benchmarking - Communication - Concurrency - Configuration   - Command Line   - CSS   - HOCON   - JSON   - TOML   - XML   - YAML - Containers - Cryptography - Databases - Embedded languages bindings - Embedded/Realtime - File metadata - Financial Calculations - Game Engine Architecture - General Multimedia - Generic - GPS - Graphic user interface   - CopperSpice   - GTK+   - Qt   - U++ - Graphics - Graphics (3D) - Images   - Formats   - Plotting - Image Processing - Internationalization - Logging - Error handling - Math   - Automata theory   - Class Library for Numbers   - Computational geometry   - Graph theory   - Linear algebra   - Machine Learning   - Numeral Calculations   - Optimization   - Symbolic expression manipulations - Metaprogramming - PDF - Physics and Simulations - Robotics   - Perception - Serialization   - Binary serialization - Sorting - System - Terminal - Testing - Text   - Coding   - Diff/Patch   - Format   - Parse   - Search   - Template Engine - Version Control - Video - Web |

# Package managers

| Package manager | Description |
| --- | --- |
| build2 | An open-source (MIT), cross-platform build toolchain that aims to approximate Rust Cargo’s convenience for developing and packaging C/C++ projects while providing more depth and flexibility, especially in the build system. |
| cget | Cmake package retrieval. This can be used to download and install cmake packages. |
| cmodule | Non-intrusive cmake dependency management. |
| conan | Decentralized, open-source (MIT), C/C++ package manager. |
| CPM.cmake | A cmake script that adds dependency management capabilities to cmake. It’s built as a thin wrapper around cmake’s FetchContent module that adds version control, caching, a simple API and more. |
| hunter | A cmake driven cross-platform package manager for C/C++ projects. |
| spack | A package manager for supercomputers, Linux, and macOS. It makes installing scientific software easy. It isn’t tied to a particular language. |
| teaport | A cocoapods inspired dependency manager. |
| vcpkg | A C/C++ package manager for Windows, Linux, and macOS. |
| xmake | A cross-platform Lua-based C/C++ build tool and package manager. |

# Libraries

## Audio

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Amplitude Audio SDK | A cross-platform audio engine designed with the needs of games in mind. (Src) | Apache-2.0 | cmake, vcpkg |
| Aquila | An open-source and cross-platform DSP library for C++11. | MIT | cmake |
| Aubio | A C/Python library for audio and music analysis. (Src) | GPL-3.0 | make |
| audioFlux | A C library for audio and music analysis, feature extraction. | MIT |  |
| Essentia | An open-source library and tools for audio and music analysis, description and synthesis (MIR) (Src) | Affero GPLv3 |  |
| FFTW | A library for computing the DFT (SSE/SSE2/AVX/Altivec/ARM Neon). (Src) | GPL-2.0 | cmake |
| FMOD | An easy to use cross-platform audio engine and audio content creation tool for games. | Free for non-commercial/Commercial | cmake |
| KFR | A fast, modern, C++17, open-source, cross-platform DSP/DFT framework, supports Audio resampling, FIR/IIR filters, Biquad, (SSE, AVX, AVX-512, ARM NEON). (Src) | GPL-2.0 | cmake |
| libsoundio | A C library for cross-platform real-time audio input and output. (Src) | MIT | cmake |
| Maximilian | C++ Audio and Music DSP Library. | MIT | cmake |
| Miniaudio | An audio playback and capture C library. (Src) | Unlicense | single source file |
| ni-media | C++ library for reading and writing audio files. | MIT | cmake, vcpkg |
| OpenAL | A cross-platform audio API. | BSD/LGPL/Proprietary | cmake |
| PortAudio | PortAudio is a free, cross-platform, open-source, audio I/O library. (Src) | MIT | cmake, vcpkg |
| rnnoise | Recurrent neural network for audio noise reduction. | BSD-3-Clause | make |
| SELA | ****S****impl****E**** ****L****ossless ****A****udio. | MIT | cmake |
| SoLoud | Easy, portable audio engine for games. | zlib |  |
| Soundtouch | The SoundTouch is an open-source cross-platform audio processing library for changing the Tempo, Pitch and Playback Rates of audio streams or audio files. (Src) | LGPL-2.1 | make |
| Tonic | Easy and efficient audio synthesis in C++. | Unlicense |  |
| Verovio | A fast and lightweight music notation engraving library. (Src) | LGPL | cmake, qmake |
| Wav2Letter++ | A fast speech recognition toolkit written entirely in C++ and uses the ArrayFire tensor library and the flashlight machine learning library for maximum efficiency. | Unlicense | cmake |

CD

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| libkcompactdisc | A library for interfacing with CDs | GPL v2.0 | cmake |

Fingerprinting

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| chromaprint | The Chromaprint is an audio fingerprint library designed to identify near-identical audio. It trades precision and robustness for search performance. Chromaprint can use multiple FFT libraries - FFmpeg, FFTW3, KissFFT or vDSP. (Src) | MIT, LGPL 2.1 | cmake |
| libmusicbrainz | The MusicBrainz Client Library (libmusicbrainz), also known as mb_client, is a development library geared towards developers who wish to add MusicBrainz lookup capabilities to their applications. The library supports Windows, Linux and Mac OS X (Src) | LGPL-2.1 | cmake |
| libofa | An open-source audio fingerprint by MusicIP | APL | make |

Formats

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| AudioFile | A simple C++ library for reading and writing audio files. | MIT | cmake |
| audio_file | A library that handles reading and writing audio files in many common formats. (Src) | LGPL-2.1 | make |
| dr_libs | Single-file audio (FLAC, MP3, WAV) decoding libraries for C and C++. | Unlicense |  |
| flac | The FLAC stands for ****F****ree ****L****ossless ****A****udio ****C****odec, meaning that audio compressed in FLAC has no loss in quality. FLAC stands out as the fastest and most widely supported lossless audio codec, non-proprietary, and unencumbered by patents. | Open Source, BSD, GPL |  |
| LAME | LAME is a high quality MPEG Audio Layer III (MP3) encoder. | LGPL |  |
| libsndfile | A C library with C++ wrapper for reading and writing files containing sampled sound (e.g. WAV, AIFF) through one standard library interface. (Src) | LGPL-2.1 | cmake, make, vcpkg |
| minimp3 | Minimalistic MP3 decoder | CC0-1.0 | header-only |
| Opus | A totally open, royalty-free, highly versatile audio codec. | BSD | cmake |
| Vorbis | Ogg Vorbis is a fully open, non-proprietary, patent-and-royalty-free, general-purpose compressed audio format. | BSD | cmake |

Tagging

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| id3lib | An open-source, cross-platform library for reading, writing, and manipulating ID3v1 and ID3v2 tags, and retrieving some basic mp3 header info like bitrate. However, we now recommend moving to taglib :) | LGPL v2 |  |
| taglib | The TagLib Audio Metadata Library is a library for reading and editing the meta-data of several popular audio formats: ID3v1, ID3v2 for MP3 files, Ogg Vorbis comments and ID3 tags and Vorbis comments in FLAC, MPC, Speex, WavPack, TrueAudio, WAV, AIFF, MP4 and ASF files. (Src) | LGPL and MPL v1.1 |  |

## Benchmarking

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| benchmark | A library to benchmark code snippets, similar to unit tests | Apache 2.0 | cmake |
| Celero | A feature-rich C++ Benchmark Authoring Library/Framework. Supports Windows, Linux, and OSX using C++11. | Apache | cmake |
| Criterion | A micro-benchmarking library for modern C++ | MIT | header-only; cmake |
| gperftools | The 'Google Performance Tools' includes a high-performance, multi-threaded malloc implementation plus tools for benchmarking heap allocation and CPU utilization. | BSD 3-Clause "New" or "Revised" | configure |
| nanobench | A simple, fast, accurate single-header micro-benchmarking functionality for C++11/14/17/20. (Src) | MIT | header-only; cmake |
| picobench | A tiny (micro) micro-benchmarking library | MIT | header-only; cmake |
| plf::nanotimer | A lowest-overhead, cross-platform simple timer class for benchmarking. | zlib | header-only |

## Communication

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| ACE | Asynchronous networking, event de-multiplexing, messaging (Src) (Doc) | Custom | make |
| Apache Thrift | The Apache Thrift software framework, for scalable cross-language services development, combines a software stack with a code generation engine to build services that work efficiently and seamlessly between C++, Java, Python, PHP, Ruby, Erlang, Perl, Haskell, C#, Cocoa, JavaScript, Node.js, Smalltalk, OCaml and Delphi and other languages. (Src) | Apache-2.0 | cmake, vcpkg |
| Boost.Asio | Asynchronous and synchronous networking, timers, serial I/O | BSL-1.0 |  |
| Boost.Beast | An HTTP and WebSocket library built on top of Boost.Asio | BSL-1.0 |  |
| Breep | An event based, high-level, peer-to-peer library, allowing users to directly send and receive objects. | European Union Public License 1.1 | cmake |
| brpc | An industrial-grade RPC framework used throughout Baidu, with 1,000,000+ instances and thousands kinds of services. (Src) (Doc) | Apache 2.0 | cmake |
| C++ REST SDK | An asynchronous HTTP client and listener, asynchronous Stream, URI, JSON | MIT | cmake |
| cpp-httplib | A C++11 single-file header-only cross platform HTTP/HTTPS library | MIT | header-only; cmake |
| cpp-netlib | A C++ Network Library | BSL-1.0 | cmake |
| cppsimpleuri | A modern C++ uri & query parser | MIT | cmake |
| cpr | A modern C++ HTTP requests library | MIT | cmake |
| Crow | A C++ micro web framework (inspired by Python Flask) | BSD-3-Clause | header-only; cmake |
| curlpp | C++ wrapper for libcURL (CURL library). (Src) |  | cmake, vcpkg |
| DumaisLib | Various utilities such as WebServer, JSON, WebSocket server, REST framework (a library for creating a REST API in your c++ app) | MIT | make |
| EasyHttp | A cross-platform HTTP client library with a focus on usability and speed, supporting http response caching and more. | MIT | cmake |
| eCAL | A high performance inter-process communication library | Apache 2.0 | cmake |
| fineftp-server | An FTP-server library for Windows and Unix | MIT | cmake |
| FPNN | ****F****ast ****P****rogrammable ****N****exus ****N****etwork. High performance fully asynchronous RPC service framework. Simultaneously supporting HTTP, WebSocket, TCP, and reliable UDP. Support the development of ultra-high load servers, with corresponding client SDKs. | 未知 | make |
| gRPC | A modern open-source high performance RPC framework that can run in any environment. (Src) (Doc) | Apache-2.0 | bazel, cmake, vcpkg |
| gsoap | A C/C++ development toolkit for XML data bindings, fast WSDL/SOAP/XML Web services, WS-Security, JSON/XML-RPC RESTful services | GPLv2 |  |
| hmbdc | A lightweight and high performance C++17 message pub/sub middleware framework/lib |  | header-only |
| HTTPP | A simple, C++14, production ready HTTP-server built on top of Boost and a client built on top of libcurl. | BSD 2-Clause "Simplified" | cmake, make |
| IXWebSocket | An open-source WebSocket + HTTP library without dependency, supports SSL and the per message deflate WebSocket extension. | BSD 3-Clause "New" or "Revised" | cmake, make |
| KCP | A fast and reliable ARQ protocol that helps applications to reduce network latency. | MIT | cmake |
| libashttp | An asynchronous HTTP client library | GNU Lesser General Public v3.0 |  |
| libjson-rpc-cpp | A framework that provides cross-platform JSON-RPC (remote procedure call) support for C++, fully JSON-RPC 2.0 & 1.0 compatible. | MIT | cmake, conan |
| libnavajo | A C++ framework including a fast multithreaded http server, HTML5 Websockets, SSL, X509 and HTTP authentification, compression, cookies and advanced session management, IPv4 and IPv6 (CeCILL-C). | CeCILL-C FREE SOFTWARE LICENSE AGREEMENT | cmake |
| libtins | A network packet crafting and sniffing library (Src) (Doc) | BSD-2 | cmake, vcpkg |
| LiteNetLibPP | A lightweight reliable UDP library for games | MIT | cmake |
| mailio | MIME and email library | BSD 2-Clause "Simplified" | cmake |
| nanomsg | A fast message queue, zeromq successor |  |  |
| netif | A C++14 library for getting network addresses on Windows, Linux, macOS, and FreeBSD. | BSD 3-Clause "New" or "Revised" | header-only; cmake |
| nghttp2 | HTTP/2 C Library and tools (server, client, proxy and benchmarking tools) | MIT | cmake, configure |
| ngrest | A fast and easy in use JSON RESTful Web Services Framework | Apache 2.0 | cmake |
| nng | A fast message queue, nanomsg successor |  |  |
| Oat++ | A Web Framework: REST-API and Request implementation (Src) (Doc) | Apache 2.0 | cmake |
| omniORB | The fastest, complete and portable CORBA ORB implementation in C++ |  |  |
| OpenDDS | DDS (Data Distribution Service) implementation |  |  |
| Paho MQTT | A modern C++ client for MQTT from Eclipse |  | cmake |
| paozhu | A C++20 Web Framework Support HTTP/2 ORM WebSocket | MIT | cmake |
| PcapPlusPlus | Multi-platform C++ network sniffing and packet parsing and crafting framework. Provides C++ wrappers for many popular packet processing engines such as libpcap, Npcap, WinPcap, DPDK, AF_XDP, and PF_RING. (Src) | Unlicense | conan, homebrew, cmake, vcpkg |
| POCO | Networking: encryption, HTTP; Zip files (Doc) |  |  |
| rest_rpc | A C++11, high performance, cross-platform, easy to use RPC framework. | MIT | cmake |
| restbed | A cross-platform feature rich framework brings asynchronous RESTful functionality (secure communication over HTTP) to C++14 applications. | License | cmake |
| restc-cpp | Accessing JSON API's from C++. HTTP Client, native C++ class to/from JSON serialization, asynchronous IO trough boost::asio coroutines. C++14. | MIT | cmake |
| restful_mapper | ORM for consuming RESTful JSON APIs in C++ |  | cmake, make |
| seastar | A high performance server-side application framework, based on C++14/C++17. | Apache 2.0 | cmake, etc. |
| Silicon | The Silicon C++14 Web Framework: Fast and Robust Web APIs | MIT | cmake |
| sockpp | A simple, modern C++ socket library | BSD 3-Clause "New" or "Revised" | cmake |
| stream-client | A lightweight Boost-based client-side socket/connector/socket pool/resolver | Apache 2.0 | header-only; cmake |
| tacopie | A C++11 TCP Library | MIT | cmake |
| TAO | CORBA |  |  |
| taox11 | A C++11 based CORBA implementation | MIT |  |
| Unicomm | Asynchronous networking, high-level TCP communication framework |  |  |
| uvw | A libuv (cross-platform asynchronous I/O) wrapper in C++17 | MIT | header-only; cmake |
| WNetWrap | A WinInet wrapper in C++ | MIT |  |
| wvstreams | A C++ networking library including UniConf and a convenient D-Bus API | GPL |  |
| zeromq | A fast message queue |  |  |

## Concurrency

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| AdaptiveCpp | Provides a SYCL and C++ parallel STL offloading compiler and runtime system for CPUs and GPUs from NVIDIA, AMD, Intel | BSD-2-Clause | cmake |
| Asyncpp | An asynchronous c++ library that provides various concurrent operations | MIT | cmake |
| BlockingCollection | C++11 thread safe, multi-producer, multi-consumer blocking queue, stack & priority queue class | GPL-3.0 | header-only |
| Boost.Atomic | Provides atomic data types and operations on these data types, as well as memory ordering constraints required for coordinating multiple threads through atomic variables. | BSL-1.0 |  |
| Boost.Compute | A GPU/parallel-computing library for C++ based on OpenCL. | BSL-1.0 | cmake |
| Boost.Context | A C++11 library that provides a cooperative multitasking abstraction on a single thread. | BSL-1.0 |  |
| Boost.Interprocess | Simplifies the use of interprocess communication and synchronization mechanisms and offers a wide range of them: shared memory, memory-mapped files, semaphores, mutexes, condition variables and upgradable mutex types, named versions of the synchronization objects, file locking, message queues. | BSL-1.0 |  |
| Boost.Lockfree | Provides non-blocking (aka lock-free) concurrent data structures: a queue, a stack, and a ringbuffer (spsc_queue). | BSL-1.0 |  |
| Boost.MPI | A C++-friendly interface to the standard Message Passing Interface | BSL-1.0 |  |
| Boost.Thread | Enables the use of multiple threads of execution with shared data and means for synchronizing data between the threads. | BSL-1.0 |  |
| concurrencpp | Modern concurrency for C++. Tasks, executors, timers and C++20 coroutines. | MIT | cmake |
| dispenso | High-performance concurrency for C++. parallel_for, Futures, pipelines, timers, timed/periodic tasks, and concurrent data structures. | MIT | cmake |
| Highway | Provides performance-portable, length-agnostic SIMD/vector intrinsics. Supports: SSE3, SSE4, AVX\*, NEON, SVE\*, WASM SIMD, RISC-V, POWER. (Doc) | Apache-2.0 | cmake |
| HPX | A general purpose C++ runtime system for parallel and distributed applications of any scale (Doc) | BSL-1.0 | cmake, vcpkg |
| Intel TBB | Intel® TBB is a cross-platform C++ library for shared memory parallel programming and heterogeneous computing. The library provides: generic parallel algorithms, concurrent containers, a scalable memory allocator, work-stealing task scheduler, and low-level synchronization primitives. (Src) (Doc) | Apache-2.0 or Commercial | cmake, make |
| KOKKOS | A programming model for writing performance portable HPC applications, using CUDA, HIP, SYCL, HPX, OpenMP and C++ threads as backends (Doc) | Custom | cmake, make |
| libopenmpi | The Open MPI Project is an open-source Message Passing Interface implementation | 3-clause BSD |  |
| libsimdpp | A portable zero-overhead C++ low level SIMD library. | Boost | header-only; cmake |
| MPL | A C++-17-friendly interface to the standard Message Passing Interface | BSD 3-Clause "New" or "Revised" | header-only; cmake |
| MutexGear | A mutex-only synchronization (wheel, rwlock, work queues) C/C++11 library | The MutexGear Library | configure, msvc, make |
| OpenMP | The OpenMP API specification for parallel programming |  |  |
| PoCL | A portable retargetable open-source (LLVM based) implementation of the OpenCL standard. (Src) (Doc) | MIT | cmake |
| RaftLib | A C++17 stream-like concurrent actors that enable parallel data-flow computations | Apache-2.0 | cmake |
| SObjectizer | A small cross-platform framework for concurrent and event-driven applications in C++ by using actor and publish-subscribe models. | BSD-3-Clause | cmake, vcpkg, conan |
| stdgpu | Efficient STL-like Data Structures on the GPU | Apache 2.0 | cmake |
| subprocess | C++17/20 cross-platform library for running subprocesses | MIT | cmake, teaport |
| Taskflow | Parallel Task Programming in Modern C++ | TASKFLOW MIT | cmake |
| task-thread-pool | Fast and lightweight thread pool for C++11 and newer. | BSD-2-Clause or MIT or BSL-1.0 | cmake, vcpkg, single header |
| ThreadPool | A simple light-weight thread pool | BSD-3-Clause | header-only; cmake, make |
| thread_pool | A modern, fast, lightweight thread pool | MIT | cmake |
| Thrust | STL-like parallel algorithms and data-structures on top of CUDA, TBB, or OpenMP | Apache v2.0, Boost v1.0. | cmake |
| TimerAlarm | Timers and Alarms based on threads. | BSD-3-Clause | header-only; cmake, make |
| VexCL | A C++ vector expression template library for OpenCL, CUDA, OpenMP | MIT | cmake |
| ViennaCL | Linear algebra and algorithms with OpenMP, CUDA, and OpenCL backends. (Src) (Doc) | Custom | cmake |
| Xenium | A C++17 library that provides various concurrent data structures and reclamation schemes. | MIT | header-only; cmake |

## Configuration

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost.Program_options | The library allows to obtain program options, that is (name, value) pairs from the user, via conventional methods such as command line, config file, and environment variables. | BSL-1.0 |  |
| figcone | Read JSON, YAML, TOML, XML or INI configuration by declaring a struct | MS-PL | cmake |
| gconfmm | A cross-platform (official) C++ interface for the popular GUI library GTK, including typesafe callbacks, and a comprehensive set of widgets that are easily extensible via inheritance. ****gtkmm**** uses STL, including strings, containers, and iterators. UTF8 is supported. (Src) (Doc) | LGPLv2.1 | autotools, meson, make |
| libconfig | A simple cross-platform C/C++ library for processing structured configuration files ("\*.cfg") (Src) (Doc) | LGPL 2.1 | autotools, cmake, make |
| libconfini | An cross-platform INI parser written in C (Doc) | GPL-3.0 | autotools, make |
| uconfig | A lightweight C++17 configuration library | Apache 2.0 | header-only; cmake |

Command Line

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Argh! | A minimalist argument handler. | BSD 3-Clause | header-only; cmake, vcpkg |
| argparse (hbristow) | A slimline C++ class for parsing command-line arguments, with an interface similar to python's class of the same name. | BSD |  |
| argparse (morrisfranken) | A lightweight library for parsing command line arguments in an elegant manner. | Apache 2 | header-only; cmake |
| argparse (p-ranav) | A command-line argument parser for C++17 | MIT | header-only; cmake, vcpkg |
| args | A simple C++ argument parser library. | MIT | header-only; cmake, conan, meson, vcpkg |
| Boost.Program_options | The library allows to obtain program options, that is (name, value) pairs from the user, via conventional methods such as command line, config file, and environment variables. | BSL-1.0 |  |
| CLI11 | A C++11 command line parser that provides a rich feature set with a simple and intuitive interface. | BSD-3-Clause | header-only; cmake, meson, vcpkg |
| clipp | Powerful & Expressive Argument Parsing for Modern C++. | MIT | header-only; cmake, vcpkg |
| cmd_line_parser | Command line parser for C++17. | MIT | header-only; cmake |
| cmdlime | A C++17 library for command-line parsing that provides a concise, declarative interface with support for sub-commands, validators, and the ability to choose either the GNU, POSIX, or X11 command-line options format. | MS-PL | cmake |
| cxxopts | A lightweight C++11/C++17 command-line arguments parser, supporting the standard GNU style syntax for options. | MIT | header-only; bazel, cmake |
| fire-hpp | Create fully functional CLIs using function signatures. | BSL-1.0 | header-only; cmake |
| flags | Simple, extensible C++17 argument parser. | Unlicense | header-only; cmake |
| gflags | A library that implements command-line flags processing. It includes built-in support for standard types such as string and the ability to define flags in the source file in which they are used. | BSD | cmake |
| structopt | Parse command line arguments by defining a struct. | MIT | header-only; cmake |
| tclap | A simple C++ template library for parsing command line arguments. The library provides a simple, flexible object-oriented interface. | MIT | cmake |

CSS

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| mycss | CSS Parser |  |  |

HOCON

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| cpp-hocon | A C++ implementation of the HOCON format developed by Pupplet. |  |  |

JSON

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| ArduinoJson | C++98/11/14/17 JSON library for Arduino, IoT and embedded C++ | MIT | cmake |
| Boost.JSON | The JSON parsing, serialization, and DOM in C++11/17 | BSL-1.0 |  |
| cajun-jsonapi | A C++ API for the JSON with an emphasis on an intuitive, concise interface that mimic standard C++ as closely as possible. |  | make |
| DAW JSON Link | A C++17 library providing static C++ bindings with type checking allowing of parsing directly to user data structures without library allocation, push/pull modes, allocator support, constexpr | BSL 1.0 | cmake |
| Glaze | One of the fastest JSON library (C++23) with direct memory serialization. Also supports BEVE and CSV. | MIT | cmake, conan, build2, vcpkg |
| jansson | A C library for encoding, decoding and manipulating JSON data with UTF-8 support | MIT | cmake, make |
| jeayeson | A very sane C++14 JSON library | BSD-3 | header-only |
| jios | JSON Input Output Streams | MIT | cmake |
| JOST |  |  |  |
| json | Niels Lohmann JSON for C++11, featuring intuitive syntax | MIT | header-only; bazel, cmake, meson |
| Jsonifier | A few C++20 classes for extremely fast JSON parsing/serializing | MIT | cmake |
| JSON Voorhees | Killer JSON for C++11 (Doc) | Apache-2.0 | cmake |
| JSON++ |  |  |  |
| json11 | A tiny JSON library for C++11, providing JSON parsing and serialization. | MIT | cmake |
| JsonBox | A C++ library used to read and write JSON with ease and speed. | MIT | cmake |
| jsoncons | A library for JSON and JSON-like data formats, with JSON Pointer, JSON Patch, JSONPath, CSV, MessagePack, CBOR, BSON, UBJSON. | Custom | header-only |
| jsoncpp | A library that allows manipulating JSON values, including serialization and de-serialization, while preserving comments. | MIT | cmake, conan, vcpkg |
| libjson |  |  |  |
| minijson | A C++ DOM-less and allocation-free JSON parsing and serialization | Custom | cmake |
| Neyson | Lightweight A C++11 JSON Library | BSD-3-Clause | cmake |
| nosjob | A C++98 library for generating and consuming JSON data | MIT | make |
| qjson |  |  |  |
| rapidjson | A fast JSON parser/generator for C++ with both SAX/DOM style API, supports UTF-8/16/32, optionally uses SIMD. (Doc) | Custom | header-only; cmake, vcpkg |
| simdjson | Parse gigabytes of JSON per second taking advantage of modern micro-architectures and parallelizing with SIMD (Doc) (Kino) | Apache-2.0 | cmake, vcpkg |
| struct_mapping | Maps JSON to and from a C++ structure | MIT | cmake |
| swxJson | The most convenient C++JSON library currently in use. Read and write complex structures at any level with just one function call. The performance is approximately half that of RapidJSON. | MIT | make |
| ThorsSerializer | JSON/BSON/YAML Input Output Streams | MIT | make |
| ujson | µjson is a small, C++11, UTF-8, JSON library | cmake |  |
| yyjson | A high performance JSON library written in ANSI C | MIT | cmake |

TOML

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| toml++ | TOML parser and serializer for C++17 and later |  |  |
| toml11 | TOML parsing library based on C++11 |  |  |

XML

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| ai-xml | Serialize objects to and from XML by adding a single, minimal, function to a class. Uses libxml++ under the hood. | AGPL-3.0 | make |
| GPDS | A general purpose data serializer to serialize objects to and from XML. Uses TinyXML under the hood. |  |  |
| gSOAP | XML data bindings |  |  |
| libxml++ | The libxml++ is a C++ wrapper for the libxml XML parser C library. (Doc) | LGPL-2 |  |
| pugixml | A light-weight, simple and fast XML parser for C++ with XPath support | MIT | cmake, conan |
| tinyxml |  |  |  |
| tinyxml2 | Another and work in progress of TinyXML. |  |  |
| Xerces |  |  |  |

YAML

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| yaml-cpp | A YAML parser and emitter in C++ | MIT | cmake |

## Containers

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost.Bimap | A bidirectional maps library that offers associative containers such as `bimap<X,Y>` in which both `X` and `Y` can be used as a key. (Src) | BSL-1.0 |  |
| Boost.Container | A library that implements several well-known containers, including STL-like containers, as well as recursive containers, and new useful containers: `flat_map`, `flat_set`, `flat_multimap`, `flat_multiset`, `stable_vector`, `static_vector`, `small_vector`, `devector`. (Src) | BSL-1.0 | header-only |
| Boost.Fusion | A library for working with heterogeneous collections of **tuples**. Provides a set of containers (`vector`, `list`, `set` and `map`), along with transformed presentation of their underlying data, a.k.a **views**." (Src) | BSL-1.0 |  |
| Boost.Heap | An implementation of **priority queues** with more functionality and different performance characteristics, than STL has. (Src) | BSL-1.0 |  |
| Boost.Pointer Container | Provides containers for holding **heap-allocated objects** in an exception-safe manner and with minimal overhead. (Src) | BSL-1.0 |  |
| Boost.Tuple | Implements pre-C++11 n-`tuple` (a fixed size collection of elements) (Src) | BSL-1.0 |  |
| Boost.Variant | Implements pre-C++17 `variant` (a safe, generic, stack-based discriminated `union` container) (Src) | BSL-1.0 |  |
| C++ Allocators | STL conformant allocators for fixed size static and stack based memory + another conformant allocator that allows custom boundary allocation | BSD-3-Clause | cmake, make |
| cpp-btree | B-tree containers make better use of the CPU cache: `btree_map`, `btree_set`, `btree_multimap`, `btree_multiset`. (Src) | Apache-2.0 | header-only; cmake |
| DataFrame | C++ DataFrame for statistical, Financial, and ML analysis -- in modern C++ using native types and continuous memory storage | BSD-3-Clause | cmake, make, conan, vcpkg |
| eggs::variant | Eggs.Variant is a C++11/14/17 generic, type-safe, discriminated union. It is notable in particular for having very good constexpr support. | BSL-1.0 | cmake |
| Frozen | C++14 constexpr perfect-hashing-based immutable sets, maps, and algorithms. | Apache-2.0 | header-only; cmake |
| Immer | A library of persistent and immutable data structures | Boost | cmake |
| plf::colony | Unordered "bag-like" container which outperforms `std::` containers in high-modification scenarios while maintaining valid pointers to non-erased elements regardless of insertion and erasure. C++98/11/14/etc-compatible. See also P0447 (`std::hive`). (Src) | zlib | conan build2 |
| plf::list | A std::list implementation which sacrifices range-splicing for cache-friendliness, yielding faster insertion, erasure and iteration. C++98/03/11/14/17/20/23/26/etc-compatible. (Src) (Doc) | zlib | — |
| plf::reorderase | An extension and optimization of the "swap-and-pop"/"move-and-pop" idiom for random access containers to increase random_access container erase performance, when post-erasure order is unimportant. Covers single, range and `std::erase_if`-style erasures. C++98/11/14/etc-compatible. (Src) | zlib |  |
| plf::queue | A drop-in replacement container for the std::queue container adaptor with better performance than std::deque and std::list in a queue context. C++98/11/14/etc-compatible. (Src) | zlib |  |
| plf::stack | A drop-in replacement container for the std::stack container adaptor with better performance than std::vector and std::deque in a stack context. C++98/11/14/etc-compatible. (Src) | zlib |  |
| ring_span | A lite implementation of Arthur O'Dwyer's `ring_span`, a.k.a. circular buffer view. C++98- compatible. | BSL-1.0 | header-only; cmake |
| strict_variant | A realtime/embedded-friendly (i.e. `-fno-exceptions`/`-fno-rtti` compatible), never-empty `variant` targetting C++11. Fast, prevents many undesirable implicit conversions. | BSL-1.0 | cmake |
| Ygg | An intrusive C++11 implementation of high-performance containers and data structures such as a Red–black tree, an Interval tree and an Interval Map. | MIT | cmake |

## Cryptography

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Botan | A cryptography Toolkit. (Src) | BSD 2-Clause "Simplified" | make |
| crypto++ | A free C++ Class Library of Cryptographic Schemes. (Src) | Boost | make |
| gnutls | A secure communications library implementing the SSL, TLS and DTLS protocols and technologies around them. (Src) | LGPL-2.1 | make |
| openssl | A robust, commercial-grade, full-featured toolkit for general-purpose cryptography and secure communication. (Src) | Apache-2.0 | make |
| TomCrypt | A fairly comprehensive, modular and portable cryptographic toolkit that provides developers with a vast array of well known published block ciphers, one-way hash functions, chaining modes, pseudo-random number generators, public key cryptography and a plethora of other routines. (Src) | public domain | cmake, make |

## Databases

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost::MySQL | MySQL client library | BSL-1.0 |  |
| cpp-redis | C++11 Lightweight Redis client: async, thread-safe, no dependency, pipelining, multi-platform. (Doc) | MIT | cmake |
| DTL | Makes ODBC record-sets look just like an STL container (Src) (Doc) |  |  |
| EasyQtSql | A lightweight C++11 (Qt based) library for quick and easy SQL querying | MIT | header-only; qmake |
| Galera | The Galera Cluster is the synchronous multi-master replication library (Galera) and a Write Set Replication (WSREP) API for MySQL/MariaDB (Src) | GPLv2 | cmake, scons |
| LevelDB | A C++ library developed by Google that handles billion-scale Key-Value data persistence storage. (Doc) | BSD-3 | cmake |
| libpqxx | The C++ connector for PostgreSQL (Src) | BSD-3 | cmake, make |
| lmdb++ | C++11 wrapper for the LMDB embedded B+ tree database library. | Unlicense | make |
| mongocxx | An official C++11 driver library for MongoDB (Doc). It offers optimized APIs for CRUD operations, indexing, and aggregation. Supporting BSON and featuring connection pooling and authentication mechanisms, it provides high-performance and scalable solutions for building C++ applications that leverage MongoDB. | Apache 2.0 | cmake |
| mysql++ | MySQL DB and tools |  |  |
| nanodbc | A small, cross-platform, C++14 wrapper for the native C ODBC API | MIT | cmake |
| ODB | An open-source, cross-platform, and cross-database object-relational mapping (ORM) system for C++. ODB supports MySQL, SQLite, PostgreSQL, Oracle, and Microsoft SQL Server relational databases as well as C++98/03 and C++11 language standards. | GPL2 and/or NCUEL |  |
| OTL | A C++ template based database library for Oracle DB, ODBC and DB2-CLI. (Src) |  |  |
| Pgfe | The PostgreSQL client (FrontEnd) API in modern C++ | Zlib | cmake |
| QTL | A friendly and lightweight C++ database library for MySQL, SQLite and ODBC. | Apache-2.0 | make |
| QUINCE | ****QU****eries ****IN**** ****C****++ ****E****xpressions (ORM+EDSL) | Boost |  |
| QxOrm | An ****O****bject ****R****elational ****M****apping (ORM) database library for C++/Qt, supports most common databases, serialization (JSON, binary, XML); standalone multi-threaded HTTP web server | GPLv3 or Proprietary |  |
| redis-cpp | A lightweight C++17 client library for executing Redis commands. | MIT | header-only; cmake |
| redis-plus-plus | A Redis client written in C++ 11, and supports Redis Sentinel, Redis Cluster, pipeline, transaction, pubsub, connection pool and STL-like interface | Apache-2.0 | cmake |
| SOCI | A plugin-based database library that embeds SQL queries in a regular C++ code; supported backends include: DB2, Firebird, MySQL, ODBC (generic backend), Oracle, PostgreSQL, SQLite3. (Src) (Doc) | Boost | cmake |
| SQLAPI++ | A middleware C++ database library that supports multiple SQL database systems: Oracle, SQL Server, DB2, Sybase, MySQL, PostgreSQL, SQLite, Informix, InterBase / Firebird, SQLBase, SQL Anywhere, ODBC, MariaDB. (Src) (Doc) | Custom | make |
| SQLiteCPP | A lean and easy to use C++ SQLite3 wrapper. | MIT | cmake, meson, vcpkg |
| SQLite ORM | An ****E****mbedded ****D****omain-****S****pecific ****L****anguage (EDSL) for SQL, as understood by SQLite, for modern C++. | AGPL-3.0, MIT | header-only; cmake, vcpkg |
| sqlpp11 | A type safe embedded domain specific language for SQL queries and results in C++. | BSD-2 | cmake |
| taoPQ | A lightweight C++17 PostgreSQL client library | Boost | cmake |

## Embedded languages bindings

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| AngelScript | A scripting language like C++. | ZLib |  |
| ChaiScript | An easy to use embedded scripting language for C++. | BSD-3-Clause |  |
| cling | An interactive C++ interpreter, built on top of Clang and LLVM to leverage RAD, creating scripts, embeddable scripting, and runtime code generation. (Src) | Custom / LGPL | cmake |
| ExprTk | A simple to use, easy to integrate and extremely efficient run-time mathematical expression parser and evaluation engine. ExprTk supports numerous forms of functional, logical and vector processing semantics and is very easily extendible. |  |  |
| Jinx | A scripting language designed for video games. | MIT | cmake |
| spidermonkey.dev | Mozilla’s JavaScript and WebAssembly Engine. |  |  |
| muparser | An extensible high performance math expression parser library written in C++. | BSD-2-Clause | cmake |
| PythonQt | A dynamic Python binding for the Qt framework. It offers an easy way to embed the Python scripting language into C++ Qt applications. | LGPL 2.1 |  |
| lua | A lightweight multi-paradigm scripting language designed primarily for embedded use. C library. | MIT | make |
| sol2 | A modern C++ library binding to Lua. | MIT | header-only; cmake |
| v8pp | Binds C++ functions and classes into V8 JavaScript engine. | BSL-1.0 | header-only; cmake |

## Embedded/Realtime

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| distortos | An object-oriented C++11 RTOS for microcontrollers (ARM, STM32) (Src) (Doc) | MPL-2.0 | cmake |
| ETL | ****E****mbedded ****T****emplate ****L****ibrary - C++03, Portable template library tailored for low resource (embedded) platforms (Src) | MIT |  |
| QP/C++ | RTOS kernel: Real-Time Embedded Frameworks based on active objects & state machines | GPLv3 |  |
| µcuREST | C++11 REST/JSON server framework for microcontrollers |  |  |

## File metadata

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| exempi |  |  |  |
| exiv2 |  |  |  |
| libkexiv2 |  |  |  |
| rarian |  |  |  |

## Financial Calculations

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| DataFrame | A C++ DataFrame for statistical, Financial, and ML analysis -- in modern C++ using native types and continuous memory storage | BSD-3-Clause | cmake, make, conan |
| QuantLib | A quantitative finance Library - A free/open-source library for quantitative finance | modified BSD |  |

## Game Engine Architecture

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Anax | An open-source C++ entity system | MIT | cmake |
| Anura | A fully-featured game engine and the tech behind the Frogatto & Friends. | Custom Open Source | make, vcpkg |
| BOX2D | A physics engine | MIT | cmake |
| EntityPlus | A C++17 Entity Component System | BSD-1.0 | cmake |
| EntityX | A fast, type-safe C++ Entity-Component system | MIT | cmake |
| EnTT | A tiny library for game dev and more written in modern C++ | MIT | header-only; cmake, bazel, conan, vcpkg, brew, cppget |

## General Multimedia

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Kigs-framework | A modular multi-purpose cross-platform framework | MIT |  |
| openFrameworks |  | MIT |  |
| SDL | ****S****imple ****D****irectMedia ****L****ayer: a cross-platform (Windows, macOS, Linux, iOS, Android, and others), low level access to audio, keyboard, mouse, joystick, and graphics hardware via that platform's graphics API (OpenGL/Direct3D/Metal/Vulkan) (Doc) (Src) | zlib | cmake |
| SFML | ****S****imple and ****F****ast ****M****ultimedia ****L****ibrary; multi-platform (Windows, Linux, macOS and soon Android & iOS); provides a simple interface to ease the development of games and multimedia applications. It is composed of five modules: system, window, graphics (over OpenGL), audio and network. | zlib/png | cmake |
| SIGIL | ****S****ound, ****I****nput, and ****G****raphics ****I****ntegration ****L****ibrary; a simple, cross-platform, minimalist library for text, shapes, input, audio, and 2D images. Supported platforms: Windows, Linux and Raspberry Pi | License | cmake |

## Generic

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Abseil | An open-source collection of C++ library code from Google designed to augment the C++ standard library. (Doc) (Src) | Apache-2.0 | cmake |
| Abstract Intrusive Containers | More flexible than Boost.Intrusive, but not STL-compatible. |  |  |
| Au | A C++14-compatible physical units library with no dependencies with emphasis on safety, accessibility, and performance. (Doc) | Apache 2.0 | header-only |
| BDE | The Bloomberg Development Environment core libraries from Bloomberg L.P. | Apache |  |
| Better Enums | Reflective enums (enum to string, iteration, etc.) with constexpr support. | BSD-2 | header-only, cmake, make |
| bitfield.h | Bit-field structure facility, more portable/flexible than the base language facility. |  |  |
| Boost | A large collection of generic libraries | BSL-1.0 |  |
| CAF | The C++ Actor Framework (CAF) is an open-source C++11 actor model implementation featuring lightweight & fast actor implementations, pattern matching for messages, network transparent messaging, and more | BSD |  |
| Cinder | A community-developed, free and open-source library for professional-quality creative coding in C++. (Doc) (Src) | Modified BSD | cmake |
| CommonPP | A multi-purpose library with a strong emphasis on getting metrics out of a project. | BSD |  |
| composite_op.h | Basic class data member introspection, cumbersome and often non-re-entrant, but sometimes useful. |  |  |
| cpp-mmf | A C++98 library that encapsulates memory-mapped-files for POSIX or Windows |  |  |
| cxxomfort | Backports of C++ features (C++11 to C++03 and C++1y proposals to C++11/C++03). |  |  |
| Dlib | Networking, threads, graphical interfaces, data structures, linear algebra, machine learning, XML and text parsing, numerical optimization, Bayesian nets, and numerous other tasks | Boost |  |
| eventpp | A C++ event library for callbacks, event dispatcher, and event queue. With eventpp you can easily implement signal and slot mechanism, publisher and subscriber pattern, or observer pattern. | Apache 2.0 |  |
| fcppt | Freundlich's C++ Toolkit (fcppt) is a collection of libraries focusing on improving general C++ code by providing better types and making use of functional programming. |  |  |
| Folly | Facebook open-source library. A cross-platform library of C++14 components designed with practicality and efficiency in mind. (Doc) | Apache-2.0 | cmake, vcpkg |
| GSL | C++ Core ****G****uidelines ****S****upport ****L****ibrary implementation, recommended by Bjarne Stroustrup, Herb Sutter and Co in C++ Core Guidelines | MIT | cmake, vcpkg |
| gsl-lite | A version of ISO C++ Guideline Support Library (GSL) for C++98, C++11 and later | MIT | header-only |
| GUL14 | General Utility Library for C++14 from DESY: Often-used utility functions and types, including String utilities, Statistics and Numeric functions, Containers, Debugging means, etc. (Src) | LGPL-2.1 | meson, vcpkg |
| History | Modern C++17 Undo/Redo Framework | Unlicense |  |
| hspp | An experimental library to bring Haskell Style Programming to C++. | Apache-2.0 | header-only |
| IP-DOS (tm) | IdeaFarm (tm) Piggyback Distributed Operating System: A general purpose programming environment for the C++ language. | Proprietary Open Source | Open Watcom 2.0 |
| JUCE | An extensive, mature, cross-platform C++ toolkit | GPL |  |
| Kangaru | A dependency injection container for C++11 and C++14 | MIT |  |
| Kerbal | Backports of modern STL facilities to previous standard. More features! More constexpr! | LGPL-3.0 | header-only; cmake |
| libsourcey | A cross-platform C++14 library for high speed networking and media encoding. HTTP, WebSockets, TURN, STUN, Symple and more. | LGPL-2.1 | cmake |
| LLNL/units | A run-time C++ library for working with units of measurement and conversions between them and with string representations of units and measurements | BSD 3-Clause "New" or "Revised" | cmake |
| Loki | A C++ library of designs, containing flexible implementations of common design patterns and idioms. | MIT | make |
| match(it) | A lightweight pattern-matching library for C++17 with macro-free APIs. | Apache-2.0 | header-only |
| nonstd-lite | A list of \*-lite repositories (e.g., span-lite, scope-lite, expected-lite) containing C++98/11 implementations of some of the proposed or already standardized C++17/20/23 library types, such as std::span, std::expected etc). | BSL-1.0 | header-only |
| nytl | A generic C++17 utility template library. | BSL-1.0 | header-only |
| OnPosix | C++ library providing several abstractions (e.g., threading, networking, logging, IPC, etc.) on POSIX platforms. |  |  |
| Reason | XML, xpath, regex, threads, sockets, HTTP, SQL, date-time, streams, encoding and decoding, filesystem, compression | GPL |  |
| SaferCPlusPlus | A safe compatible substitutes for unsafe C++ primitives, including pointers, int and std::vector. | Boost |  |
| Smart Enum | `to_string`, `from_string` and more for your enums. | BSL-1.0 | cmake |
| units | A compile-time dimensional analysis and unit conversion library built on c++14 with no dependencies | MIT | header-only |
| yaal | ****Y****et ****A****nother ****A****bstraction ****L****ayer - algorithms, collections, arbitrary precision calculation, generic-DSL grammar driven parsers and more | CC BY-ND-NC 4.0 | cmake |
| Yato | A modern C++(14/17) cross-platform STL-styled and STL-compatible library with implementing containers, ranges, iterators, type traits and other tools; actors system; type-safe config interface. | Apache-2.0 | cmake |
| yomm2 | An open multi-methods for C++17 | Boost |  |
| zoolib | ZooLib is a feature rich C++ toolkit. | MIT |  |

## GPS

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| gpsd | An open-source, cross-platform (Linux/Unix/BSD flavors, including Android and OS X) GPS-aware set of tools, such as a translator and replicator daemon for GPS devices, AIS radios, and other navigational sensors. ****gpsd**** is mostly written in C and Python, but also has C++ wrapper. ****gpsd**** is everywhere in mobile embedded systems. Every location-aware Android app is indirectly a ****gpsd**** client. (Doc) (Src) | BSD 2-clause | scons |

## Graphic user interface

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Brisk | Cross-platform C++20 modular GUI framework, with reactive capabilities, and scalable, GPU-accelerated rendering. (Src), (Doc) | GPL2+/Proprietary | cmake, vcpkg |
| Dear ImGui | A lightweight GUI library for C++ with minimal dependencies, portable, render-agnostic, optimized for use in 3D-pipeline-enabled apps. | MIT | vcpkg |
| FLTK | A cross-platform C++ GUI toolkit (Linux, Windows, MacOS) that provides modern GUI functionality, and supports 3D graphics via OpenGL/GLUT. Designed to be small and modular. Includes an UI builder. | LGPL ver.2 |  |
| nana | Cross-platform GUI programming in modern C++ style. (Src), (Doc) | BSL-1.0 | cmake, vcpkg |
| nanogui | A minimalistic cross-platform widget library for OpenGL 3.x or higher (Doc) |  |  |
| OWLNext | Modern update to OWL for writing GUI applications in standard C++ on Windows |  |  |
| Slint | A declarative GUI toolkit to build native user interfaces for desktop, embedded, and microcontrollers. (Src), (Doc) | GPL 3, Royalty-free, or Commercial | cmake |
| tiny file dialogs | A set of C/C++ cross-platform file dialogs (no init, no main loop, 6 modal function calls) |  | header-only |
| U++ | A cross-platform (Windows, GNU/Linux, macOS) rapid application development framework with bundled IDE. C++17 Compatible. (Doc) (Src) | BSD-3-Clause | make |
| WxWidgets | A free and open-source cross-platform (Windows, GNU/Linux, macOS) C++ framework for writing advanced GUI applications using native controls. (Doc) | Modified LGPL | cmake, make |
| xtd | A modern C++17/20 framework to create console, GUI and unit tests applications on Windows, macOS, Linux, iOS, and Android. (Src) (Doc) | MIT | cmake |

CopperSpice

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| CopperSpice | A set of C++ libraries used to develop cross-platform software applications. It uses modern idiomatic C++ and integrates seamlessly with the STL. CopperSpice was derived from the Qt framework. (Doc) (Src) | LGPL-2.1 | cmake |
| CsSignal | A standalone C++ thread aware signal/slot library | LGPL-2.1 | cmake |
| CsString | A standalone C++ Unicode aware string library | LGPL-2.1 | cmake |
| libGuarded | A standalone C++ multithreading library for managing access to shared data | LGPL-2.1 | cmake |

GTK+

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| evince |  |  |  |
| flowcanvas |  |  |  |
| glibmm |  |  |  |
| goocanvasmm |  |  |  |
| gtkmm | A cross-platform C++ interface for the GTK+ GUI library. | LGPL |  |
| libglademm |  |  |  |
| libgnomecanvasmm |  |  |  |
| webkitgtk |  |  |  |

Qt

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| libdbusmenu-qt | A small library designed to make sharing and displaying of menu structures over DBus simple and easy to use. It works for both QT and GTK+ and makes building menus simple. |  |  |
| Qt | (Doc) (Src) |  |  |
| QuickQanava | A C++14 network/graph visualization library / Qt node editor. | BSD 2.0 | cmake |
| qwt5 | Qt Widgets for Technical Applications |  |  |
| qwtplot3d |  |  |  |

U++

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| U++ | A C++ cross-platform rapid application development framework focused on programmers productivity. It includes a set of libraries (GUI, SQL, etc.), and an integrated development environment. (Src/Bin) | BSD |  |
| upp-components | A collection of 3rd party packages for U++ like `TerminalCtrl`, `MessageCtrl` etc. | BSD-3-Clause |  |

## Graphics

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| bgfx | A powerful cross-platform (Windows, Mac, Linux, iOS, Android, Web) 2D/3D graphics rendering shader-aware library with rendering backends: DX, OpenGL, Metal, WebGL, Vulkan etc. (Doc) | BSD-2 | make |
| cairomm | A C++ wrapper for the cairo graphics library that is 2D library with support for multiple output devices: X Window, Quartz, Win32, image buffers, PostScript, PDF, SVG, OpenGL (experimental). | LGPL |  |
| dfpsr | A 2D, 3D and isometric software renderer with desktop GUI toolkit, minimalistic dependency, designed for long time maintenance and can run without any 3D accelerated drivers | zlib |  |
| gegl | ****Ge****neric ****G****raphics ****L****ibrary (GEGL) is a data flow based image processing framework, providing floating-point processing and non-destructive image processing capabilities. (Src) | LGPL |  |
| io2d | A reference implementation of P0267, the proposed 2D graphics API for ISO C++ | BSL-1.0 | cmake |
| nanovg | An antialiased 2D vector drawing library in C on top of OpenGL for UI and visualizations, with ports to DX11/Metal/bgfx. | zlib |  |
| nux | An OpenGL toolkit | LGPL v3 |  |
| pangomm | The official C++ interface for the Pango font layout library. (Src) | LGPL v2.1 | make |
| Skia | An open-source 2D-graphics library written in C++. Skia Graphics Engine is used in Google Chrome, Chrome OS, Mozilla Firefox, Android, LibreOffice, Flutter, etc. ****Skia**** has several back-ends: software rasterization, (PDF) output, OpenGL, SVG, etc. | New BSD |  |
| TXLib | TX Library is a tiny 2D graphics library for Win32 written in C++. |  |  |
| ULIS | A cross-platform C++14 library for generic digital image processing, 2D software rasterizer, unlimited image formats (`u8`, `u16`, `u32`, float, double), Custom bit-ordered memory layout, All Photoshop pixel blending modes + 11 additional modes, Color models (RGB, HSL, HSV, CMYK, ...), Color-managed pipelines, Color Space support (icm profiles and device-independant), Optimized algorithms with multithreading, Optimized algorithms with SIMD Extensions (SSE2), Image pools and caches for optimisations, Memory storage of animated image sequences. | Custom (free-of-charge for non-commercial purposes only) | cmake |

## Graphics (3D)

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| assimp | 3D model loading | BSD-3 | cmake, vcpkg |
| bgfx | A cross-platform, graphics API agnostic, "Bring Your Own Engine/Framework" style rendering library. | BSD-2 | make, vcpkg |
| Diligent Engine | A modern cross-platform low-level 3D graphics library. | Apache-2.0 | cmake |
| Epoxy | A modern successor to GLEW. Abstracts difference between some kinds of GL contexts, which makes it sometimes simpler to use than GLEW. Used by GTK+ project since 2015. | MIT | meson, vcpkg |
| G3D | The G3D Innovation Engine is a fully featured, open-source, cross-platform (Windows, Linus, Mac OS) 3D game engine written in C/C++. G3D is used in commercial games, research papers, simulators, and university courses. It supports real-time and offline hardware rendering, ray tracing, model loading, linear algebra, and GP-computation on GPUs. Supports 3DS, OBJ, MP4, PNG, JPG, MD3 and many other formats, includes a native OpenGL skinnable GUI. (Src) (Doc) | BSD-2 |  |
| GLAD | A customizable, lightweight library for loading OpenGL functions |  |  |
| GLEW | An OpenGL functions loader (Src) | EXTGL/BSD/MIT | make, vcpkg |
| GLFW | An OpenGL window manager (Src) (Doc) | zlib/libpng | cmake, vcpkg |
| GLM | The Open****GL**** ****M****athematics (GLM) is a C++ mathematics library for graphics software based on GLSL spec. | The Happy Bunny / MIT | header-only; cmake, vcpkg |
| Godot | A full featured multi-platform 2D and 3D game engine in C++17 with a GUI editor written on itself and a python-inspired script language. | MIT | scons |
| hlsl++ | A C++ math library for rendering using HLSL syntax. Supports SSE and NEON | MIT | header-only |
| Horde3D | A small open-source 3D rendering engine. It is written in an effort to create a graphics engine that offers the stunning visual effects expected in next-generation games being lightweight and as clean as possible. | EPL |  |
| Irrlicht | The Irrlicht Engine is an open-source realtime 3D engine written in C++. It is cross-platform, using D3D, OpenGL and its own software renderers. | zlib/libpng | make, vcpkg |
| klein | A C++11/14/17 SSE-optimized Projective Geometric Algebra library for graphics and animation | MIT | cmake, vcpkg |
| Magnum | A lightweight and modular C++11/C++14 graphics middleware for games and data visualization (Src) | Custom | cmake |
| O3DE | The ****O****pen-source ****3D**** ****E****ngine (former Amazon's Lumberyard) is a C++ multi-platform 3D engine to build AAA games, cinema-quality 3D worlds, and high-fidelity simulations. Includes physics simulation, script engine, networking, and more. (Doc) | Apache 2.0 | cmake |
| Ogre3D | The OGRE is an Object-Oriented Graphics Rendering Engine - a multipurpose visualization library, suitable for scientific visualization, games, simulation, virtual reality and other graphic projects. It is multi-platform and very robust, with a good documentation. | MIT | cmake, vcpkg |
| Open CASCADE | SDK for 3D CAD/CAM/CAE applications (Src) | LGPL-2.1 | cmake |
| OpenGL | 3D language, graphics and SDK for developing 3D applications. | Khronos (MIT) |  |
| OpenSceneGraph | OpenSceneGraph is an open-source high performance 3D graphics toolkit, used by application developers in fields such as visual simulation, games, virtual reality, scientific visualization and modelling. (Src) (Doc) | Custom, GNU LGPL | cmake, vcpkg |
| Visionaray | A C++ ray tracing template library. | MIT | cmake |
| VTK | Visualization Toolkit (VTK) is an open-source software for manipulating and displaying scientific data. It comes with state-of-the-art tools for 3D rendering, a suite of widgets for 3D interaction, and extensive 2D plotting capability. | BSD-3 | cmake, vcpkg |
| Vulkan | A low-level API that removes many of the abstractions found in previous generation graphics APIs. This is great for delivering maximum performance, but has the side effect of exposing more complexity to the developer. Fortunately, several excellent tutorials exist to help clear this hurdle and get productive quickly. | Khronos (MIT) | make, vcpkg |

## Images

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Adobe/boost GIL | A high-level generic library, focused on algorithms that operate on 2D images. Very limited I/O options. | BSL-1.0 |  |
| agge | Anti-Grain Evolution. A 2D graphics engine for speed and quality in C++ | MIT | cmake |
| FreeImage | An Open-Source library project for developers who would like to support popular graphics image formats like PNG, BMP, JPEG, TIFF and others | GPLv2, GPLv3, FIPL |  |
| FreeImageRe | A fork from the Open-Source library FreeImage v3.18 to support image codecs updates and adjust for comfortable usage. All original formats and plugins are maintained. | GPLv2, GPLv3, FIPL | cmake |
| GraphicsMagick | Reading, writing, and manipulating images in over 88 major formats. Forked from ImageMagick in 2002 | Copyright | Mercurial |
| SAIL | Reading and writing static, animated, multi-paged images along with their meta data and ICC profiles. Converting capabilities. Targets simplicity and speed. | MIT | cmake |
| stb | A set of C/C++ game-dev oriented libraries featuring image loader/writer/resizer, font text rasterizer, type-safe containers, ogg vorbis decoder, real-time DXT compressor, Perlin noise generator, lexer for pet DSLs, fast sprintf, and more. | MIT, Custom | header-only |

Formats

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| djvulibre |  |  |  |
| imagemagick |  |  |  |
| Kaitai Struct C++ runtime |  |  |  |
| libraw |  |  |  |
| openexr |  |  |  |
| poppler |  |  |  |
| qimageblitz |  |  |  |
| SVG++ |  |  |  |

Plotting

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Matplot++ | A ****gnuplot**** based C++ Graphics Library for Data Visualization. ****Matplot++**** can take advantage of the following libs: OpenCV, OpenGL, LAPACK, BLAS, FFTW, JPEG, TIFF, ZLIB, PNG, GLAD, GLFW3. (Doc) | MIT | cmake |
| plotutils | The GNU ****plotutils**** package contains ****libplot****, a C/C++ library for exporting 2-D vector graphics in many file formats, both vector and bitmap. ****libplot**** can animate 2-D vector graphics and uses a Postscript-like API for file export and graphics animations. | GPL |  |
| sciplot | A modern C++ scientific plotting library powered by gnuplot, with the export to PDF, SVG, PNG, EPS, etc. | MIT | header-only; cmake, vcpkg |

## Image Processing

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| dlib |  |  |  |
| Halide | A C++-embedded DSL for high-performance processing of images and tensors. | MIT | cmake, vcpkg |
| ITK - Insight Toolkit | ITK is an open-source, cross-platform library that provides developers with an extensive suite of software tools for image analysis. Developed through extreme programming methodologies, ITK builds on a proven, spatially-oriented architecture for processing, segmentation, and registration of scientific images in two, three, or more dimensions. | Apache 2.0 | cmake |
| opencv |  |  |  |
| OTB |  |  |  |

## Internationalization

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| gettext | GNU internationalization library. | GPL | make |
| ICU | ****I****nternational ****C****omponents for ****U****nicode is a mature, widely used set of C/C++ libraries providing Unicode and Globalization support for software applications. (Src) | icu4c/LICENSE | make |
| spirit-po | A small library which parses po-files and provides an interface similar to GNU libintl. Based on boost::spirit. | BSL-1.0 | header-only |
| uni-algo | Unicode Algorithms Implementation for C/C++ | MIT/Unlicense | cmake, conan, vcpkg |

## Logging

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Backward | Printing nice Python-styled stack traces with colors and source snippets, especially on crashes. | MIT | header-only; cmake, conan |
| Boost.Log | A cross-platform logging library that is simple to use, extensible, and performant. | BSL-1.0 |  |
| clutchlog | Single-header logging system which targets versatile DEBUGGING instead of service event storage. | BSD | cmake |
| glog | Google Logging Library for C++98 based on C++-style streams | License | bazel, cmake, vcpkg |
| Log4cplus | Cross-platform, C++17 Logging API (modeled after the Java log4j API) providing thread-safe, flexible, and arbitrarily granular control over log management and configuration. | BSD (two clause) or Apache 2.0 | Autotools, cmake, Visual Studio |
| Log4cpp | A library of C++ classes for flexible logging to files, syslog, IDSA and other destinations. | LGPL |  |
| log4cxx | Apache log4cxx is a logging framework for C++ patterned after Apache log4j. (Src) | Apache | cmake |
| lwlog | An extremely fast synchronous and asynchronous C++17 logging library | MIT | cmake |
| Pantheios | A diagnostic logging API library, offering a combination of type-safety, efficiency, genericity and extensibility | BSD-style |  |
| plog | A portable and simple log for C++ in less than 1000 lines of code | MPL-2.0 |  |
| Quill | A cross-platform, C++14 Asynchronous Low Latency Logging Library | MIT | cmake |
| spdlog | A super fast C++ logging library | MIT | header-only; cmake, conan |

## Error handling

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost.LEAF | A lightweight error-handling library for C++11: single-header format, no dependencies, no dynamic memory allocations, can be used with or without exception handling, multi-threading ready. (Src) | BSL-1.0 | header-only, cmake |

## Math

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| alglib | ALGLIB is a cross-platform (Windows/POSIX/Linux) numerical analysis and data processing library. ALGLIB features include: Data analysis, Optimization and nonlinear solvers, Interpolation, Linear algebra and linear solvers, FFT and many others. | Free (GPL/Personal/Academic) and Commercial |  |
| ArrayFire | A cross-platform (Windows/OSX/Linux) general purpose HPC (CPU/GPU/OpenCL/CUDA/GPGPU) library for parallel computing. ArrayFire domains are: Vector Algorithms, Image Processing, Computer Vision, Signal Processing, Linear Algebra, Statistics, and more. (Src) | Custom |  |
| Boost.Math | Includes several contributions in the domain of mathematics: Floating Point Utilities, Mathematical Constants, Statistical Distributions and Functions, Statistics, Vector Functionals - Norms, Special Functions, Root Finding & Minimization Algorithms, Polynomials and Rational Functions, Interpolation, Quadrature and Differentiation, Filters, Complex Number Functions, Quaternions, Octonions, Integer Utilities (Greatest Common Divisor and Least Common Multiple), Series, Rationals and Continued Fractions. | BSL-1.0 |  |
| Boost.Random | Provides a variety of generators and distributions to produce random numbers having useful properties, such as uniform distribution. | BSL-1.0 |  |
| Boost.SafeNumerics | C++14, Guaranteed Correct Integer Arithmetic, a drop-in replacement for the built-in integer types. | BSL-1.0 | header-only |
| cpp-measures | A C++11 library to handle physical measures | MPL-2.0 | header-only |
| G+Smo | A cross-platform library for isogeometric analysis (Doc) | MPL-2.0 | cmake |
| GNU MP bignum C++ interface | A C++ convenience class interface that offers overloaded functions and operators. The GMP is a free C library for arbitrary precision arithmetic, operating on signed integers, rational and floating-point numbers. | GNU LGPL v3 and GNU GPL v2 |  |
| libmpdec++ | A cross-platform C library (with C++ wrappers) for correctly-rounded arbitrary precision decimal floating-point arithmetic. | BSD-2-Clause | make, nmake |
| NTL | A Library for doing Number Theory. NTL is a high-performance, portable C++ library providing data structures and algorithms for manipulating signed, arbitrary length integers, and for vectors, matrices, and polynomials over the integers and over finite fields. | LGPLv2.1+ |  |
| PCGrand | PCG is a family of simple fast space-efficient statistically good algorithms for random number generation. Unlike many general-purpose RNGs, they are also hard to predict. | Apache |  |
| stats++ | Advanced, comprehensive statistical software: data collection and preprocessing, statistics, machine learning, and optimization, with open C++ source code. |  |  |
| StatsLib | A template library of statistical distribution functions. | Apache-2.0 | header-only |

Automata theory

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| yasmine | A C++11 UML state machine framework (Doc) (Src) | License |  |

Class Library for Numbers

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| BigNumber | A C++ class for creating and computing arbitrary-length integers | Apache 2.0 | cmake |
| Boost.Multiprecision | The Multiprecision Library provides integer, rational, floating-point, and complex types in C++ that have more ****range and precision**** than C++'s ordinary fundamental (built-in) types. | BSL-1.0 |  |
| cln | CLN is a library for efficient computations with all kinds of numbers in arbitrary precision. | GPL |  |
| CNL | ****C****ompositional ****N****umeric ****L****ibrary - fixed-precision numeric types | BSL-1.0 | cmake, conan |
| fpm | A C++11 ****f****ixed-****p****oint ****m****ath library that provides standard library's floating-point functionality on integers. Useful if your target platform lacks an FPU, or deterministic calculations required. | MIT | header-only; cmake |
| Universal Numbers | A C++17/20 template library providing plug-in replacements for the native arithmetic types (integer/decimal/fixed-point/floating-point/posits/logarithmic/interval) | MIT | cmake, vcpkg, conan |

Computational geometry

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost.Geometry | Boost.Geometry (aka ****G****eneric ****G****eometry ****L****ibrary, GGL), defines concepts, primitives and algorithms for solving geometry problems. Boost.Geometry contains a dimension-agnostic, coordinate-system-agnostic and scalable kernel, based on concepts, meta-functions and tag dispatching. Supported algorithms are: calculation of area, length, perimeter, centroid, convex hull, intersection (clipping), within (point in polygon), distance, envelope (bounding box), simplify, transform, and much more. The library supports high precision arithmetic numbers | BSL-1.0 |  |
| CGAL | Computational geometry algorithms library | GPL-3.0 or commercial | cmake |
| PCL | Point Cloud library |  |  |
| pmp-library | Polygon Mesh Processing Library |  |  |
| Wykobi | Computational geometry library |  |  |

Graph theory

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost.Graph |  | BSL-1.0 |  |
| CXXGraph | A C++17 library for graph representation, manipulation, partitioning and algorithms | AGPL-3.0 | header-only; cmake |
| GTpo | A C++14 directed graphs modelling library, part of QuickQanava project | BSD | qmake, cmake |
| LEMON | ****L****ibrary for ****E****fficient ****M****odeling and ****O****ptimization in ****N****etworks implements common data structures and algorithms focusing on combinatorial optimization, graphs and networks. (Doc) | License |  |
| NGraph | A simple (Network) Graph library in C++ |  |  |
| OGDF | ****O****pen ****G****raph algorithms and ****D****ata structures ****F****ramework - is a C++ library for graph algorithms, in particular for automatic graph drawing. | GPL v2 or v3 |  |

Linear algebra

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Armadillo | A C++ template library for linear algebra and scientific computing featuring wrappers for OpenBLAS, Intel MKL, LAPACK, ATLAS, ARPACK, SuperLU and FFTW. Useful for ML, pattern recognition, DSP, bioinformatics, statistics, finance, etc. | Apache 2.0 |  |
| Blasw | A C++11 BLAS and Parts of LAPACK Wrapper | BSD-3-Clause | header-only; cmake |
| Blaze |  |  |  |
| Blitz++ | A C++ template class library that provides high-performance dense arrays and vectors, random number generators, and small vectors. | GPL-3.0, LGPL-3.0, Custom | cmake |
| Boost.uBLAS | A C++ template class library that provides BLAS level 1, 2, 3 functionality for dense, packed and sparse matrices. Uses expression templates. | BSL-1.0 |  |
| C++ Matrix | High performance and accurate (e.g. edge cases) matrix math library with expression template arithmetic operators | BSD-3-Clause | cmake, make |
| DecompLib | A C++11 library to decompose a vector into a set of positive definite weighted basis vectors. | MIT | header-only |
| Dlib - linear algebra tools |  |  |  |
| Eigen | A C++ template library for linear algebra: matrices, vectors, numerical solvers, and related algorithms. | MPL2 | cmake, conan |
| ETL |  |  |  |
| IT++ |  |  |  |
| Matrix | Easy-to-use Scientific Computing library in/for C++ available for Linux and Windows. | MIT | cmake |
| NumCpp | A C++ template library implementing the Python's NumPy | MIT | header-only; cmake, vcpkg, conan |
| PETSc | A suite of data structures and routines for the parallel solution of scientific applications modeled by partial differential equations. It supports MPI, and GPUs through CUDA or OpenCL, as well as hybrid MPI-GPU. |  |  |
| Spectra | ****Sp****arse ****E****igenvalue ****C****omputation ****T****oolkit as a ****R****edesigned ****A****RPACK is an open-source C++ library for large scale eigenvalue problems, built on top of Eigen linear algebra library (also open-source and header-only). (Src) | MPL-2.0 | header-only; cmake, vcpkg |
| Tense | A fast C++17 expression template matrix and tensor library | BSD-3-Clause | header-only; cmake |
| xtensor | A C++ library meant for numerical analysis with multi-dimensional array expressions. | BSD |  |

Machine Learning

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Dlib | A machine learning tools |  |  |
| FANN | A ****F****ast ****A****rtificial ****N****eural ****N****etwork library |  |  |
| gaenari | A C++17 based incremental decision tree | Apache-2.0 | cmake |
| liblinear |  |  |  |
| libtorch | A C++ frontend to the popular PyTorch Python library (backend is written in C++) | BSD-style | cmake |
| MLPACK | A machine learning package |  |  |
| Shogun | A large scale machine learning toolbox |  |  |
| stats++ |  |  |  |
| tensorflow | An Open Source Machine Learning Framework for Everyone; provides stable C++ API and written mainly in C++ | Apache-2.0 | bazel |

Numeral Calculations

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| LibBF | An arbitrary precision numerical calculation library developed by Bellard with a sample program that calculates π to billions of bits | MIT |  |

Optimization

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| ceres-solver | An open-source C++ library for modeling and solving large, complicated optimization problems. It is a feature rich, mature and performant library which has been used in production at Google since 2010. | Apache | cmake, conan |
| OptimLib | A C++11 library of numerical optimization methods for nonlinear functions. |  |  |

Symbolic expression manipulations

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| CasADi | A symbolic framework for nonlinear optimization and algorithmic differentiation. Supports C++ code generation for symbolic expressions and dynamic connection of compiled generated code. | LGPLv3.0 | cmake |
| ExprTk | The C++ Mathematical Expression Toolkit Library (ExprTk) is a simple to use, easy to integrate and extremely efficient run-time mathematical expression parser and evaluation engine. ExprTk supports numerous forms of functional, logical and vector processing semantics and is very easily extendible. | MIT | header-only |
| GiNaC | A library for creating integrated systems that embed symbolic manipulations together with more established areas of computer science (like computation-intense numeric applications, graphical interfaces, etc.) under one roof. | GPLv3 |  |
| mathiu.cpp | A simple computer algebra system in C++17 | Apache-2.0 | cmake |
| SEMT | A compile-time symbolic differentiation | License | make |
| SymbolicC++ | A general-purpose computer algebra system | GPLv2 | autoconf |
| SymCC | A compiler wrapper which embeds symbolic execution into the program during compilation, and an associated run-time support library. In essence, the compiler inserts code that computes symbolic expressions for each value in the program. The actual computation happens through calls to the support library at run time. | GPLv3 | cmake |
| SymEngine | A standalone fast C++ symbolic manipulation library. | MIT | cmake |
| ViennaMath | A symbolic math library that enables a convenient instantiation, manipulation, and evaluation of mathematical expressions at run time and compile-time. | MIT | cmake |

## Metaprogramming

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost.CallableTraits | A C++11/17 library for the compile-time inspection and manipulation of all 'callable' types. A successor to Boost.FunctionTypes. | BSL-1.0 | header-only |
| Boost.Hana | A new metaprogramming library for both types and values | BSL-1.0 |  |
| Boost.Metaparse | A compile-time parser library, producing types, values, and metafunctions from compile-time strings | BSL-1.0 |  |
| Boost.Mp11 | A C++11 metaprogramming library for compile-time manipulation of data structures that contain types. | BSL-1.0 | header-only |
| Boost.MPL | An original metaprogramming library, targeted at C++03, slow | BSL-1.0 |  |
| Boost.PFR | A C++14 library for basic reflection (without macros): visiting members of a user defined type by index, IO streaming. | BSL-1.0 | header-only |
| Boost.Proto | A library for building expression template-backed EDSLs | BSL-1.0 |  |
| Brigand | Uses eager metafunctions, optimized for best performance |  |  |
| CoMeta | A lightweight C++14 metaprogramming library |  | header-only |
| Meta | Uses eager metafunctions, middle ground between metal and brigand wrt performance |  |  |
| Metal | Uses eager metafunctions, 100% SFINAE-friendly |  |  |
| refl-cpp | A modern compile-time reflection library for C++ with support for overloads, templates, attributes and proxies |  |  |
| Refureku | A C++17 runtime reflection and code generation library | MIT | cmake |
| visit_struct | A miniature reflection library, providing structure visitors for C++11/14. Self-contained, 200-400 lines of code depending how you count. |  |  |

## PDF

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| HARU | A free, cross-platform, open-source library for generating PDF files. (Doc) (Src) | Zlib | cmake |
| JagPDF | A free, open-source library for generating PDF (Doc) | MIT |  |
| PoDoFo | A free portable C++17 library to work with the PDF | LGPL-2.0 | cmake, conan, vcpkg |
| PDF-Writer | A high performance C++ library for creating, **modifying** and parsing PDF files | Apache-2.0 | cmake, conan, vcpkg |

## Physics and Simulations

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Bullet | A physics simulation for games, visual effects, robotics and reinforcement learning |  |  |
| HELICS | A co-simulation framework for synchronizing time and exchanging data between different types of simulators | BSD 3-Clause "New" or "Revised" | cmake |
| ProjectCHRONO | An open-source multi-physics simulation engine |  |  |
| ReactPhysics3D | A C++ physics engine library for 3D simulations and game |  |  |

## Robotics

Perception

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| GTSAM | Sensor Fusion, SLAM, SFM, VO, Computer vision (Src) | BSD | cmake |
| opencv | Computer vision and perception, Calibration, Feature Matching (Src) (Doc) | BSD, Apache 2 | cmake |

## Serialization

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Boost.Serialization |  | BSL-1.0 |  |
| C++ XML objects |  |  |  |
| cereal | A C++11 serialization | BSD |  |
| cista | A simple, high-performance, zero-copy C++ serialization & reflection library. (Src) | MIT | cmake |
| cppcodec | A C++11 library to encode/decode base64, base32 and hex with consistent, flexible API | MIT | header-only |
| GPDS | A general purpose data serializer to serialize objects to and from XML. Uses TinyXML under the hood. |  |  |
| gSOAP | An accurate XML serialization |  |  |
| iguana | A modern, universal and easy-to-use serialization engine developed in C++17, based on compile-time Reflection. Supported formats: JSON, XML, user-defined. | Apache-2.0 | cmake |
| jios | JSON serialization | MIT | cmake |
| protobuf | Protocol Buffers (a.k.a., protobuf) is Google's language-neutral, platform-neutral, extensible mechanism for serializing structured data, including .proto files compiler. (Doc) | Custom | bazel, cmake |
| rpnx-serial | A library that can (de)serialize types like std::map, std::vector, etc. |  |  |
| Serio | A fast lightweight C++ serialization library | BSD-3-Clause | header-only; cmake |
| ThorsSerializer | A C++ serialization library for JSON | MIT | make |
| yaml-cpp |  |  |  |
| YAS | ****Y****et ****A****nother ****S****erialization is a C++11 library w/o third-party libraries dependencies. Archives can be binary, text, JSON | Boost | header-only |

Binary serialization

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| binn | A binary serialization library designed to be compact, fast, and easy to use, itself an implementation of the same name format. |  |  |
| blobify | A C++17 library that infers the serialized layout from the structure definition alone. | Boost | header-only; cmake |
| bson-cxx | A C++11 implementation of BSON format. |  | scons |
| fast_ber | A C++11 high-performance serialization using BER/DER encoding rules. Encoding layout is defined by ASN.1 schemas. |  |  |
| UBjsonCpp | A high-performance UBJson read-write library based on C++14 |  |  |

## Sorting

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Cpp-sort | A collection of various sorting algorithms in a simple package. | MIT |  |
| Indiesort | A function template that allows std::sort (and other random access sort functions) to be used with non-random-access containers. It also increases the performance of sorting large objects in random-access containers and arrays | zlib |  |
| Timsort | A stable sorting function template which outperforms which outperforms quicksort-based algorithms including std::sort, for reversed or semi-sorted data. | MIT |  |

## System

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Infoware | A C++ library for pulling system and hardware information, without hitting the command line. | Creative Commons v1.0 | cmake |

## Terminal

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| cli | A cross-platform library for interactive command line interfaces in modern C++. | BSL-1.0 | header-only; cmake, make, nmake, vcpkg |
| cwidget | A high-level terminal interface library for C++, modeled on GTK+ and Qt, but using curses "enwiki:Curses (programming library)") as its display layer | GPL v2.0 | make |
| replxx | A readline and libedit replacement that supports UTF-8, syntax highlighting & hints. |  |  |

## Testing

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| bandit | A human-friendly unit testing for C++11. (Src) | MIT | cmake |
| Boost.Test | A C++03/11/14/17 unit testing library, available on a wide range of platforms and compilers. (Src) | BSL-1.0 | cmake, b2 |
| Catch2 | A modern, C++-native, test framework for unit-tests, TDD and BDD - using C++14, C++17 and later | Boost | cmake |
| cppunit | A C++ port of the famous JUnit framework for unit testing | LGPL-2.1 | make |
| CUTE | A ****C****++ ****U****nit ****T****esting ****E****asier (no reliance on static initialization for registration), integrated into Cevelop for TDD | MIT | header-only |
| doctest | A lightest feature-rich C++ single-header testing framework for unit tests and TDD | MIT | header-only; cmake |
| ELFspy | Testing in isolation with fakes and spies - Linux only | GPL-2.0 | make |
| faker-cxx | A modern C++20 Faker library for generating testing data. | MIT | cmake |
| Google Test | Google Testing and Mocking Framework. (Src) | BSD 3-Clause "New" or "Revised" | bazel, cmake |
| lest | A C++11-native tiny framework for unit-tests, TDD and BDD (includes C++98 variant). | Boost | header-only; cmake |
| liblittletest | A portable testing framework | LGPL-2.1 | header-only |
| snitch | A lightweight C++20 testing framework. | Boost | cmake |
| tunit | A modern C++17 unit testing library on Windows, macOS, Linux, iOS, and Android. Office site | MIT | cmake |

## Text

Coding

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| strsuite | A C++20 library to manage strings with different encodings | LGPL3.0 | cmake |
| uchardet | Guesses a string encoding, basically the same as the `uchardet` function in Python. | MOZILLA PUBLIC LICENSE v1.1 | cmake |
| win-iconv | A character set encoding conversion library for Linux and Mac. The Windows implementation of `iconv` is based on the Win32 Character Set Conversion API. | public domain | cmake |

Diff/Patch

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| diff_match_patch | Create and apply patches for strings (requires Qt) | Apache 2.0 | qmake |

Format

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| coformat | A companion C++ library for std::format to enable text colorization and styling. | public domain | header-only |
| fmt | An open-source formatting library providing a fast and safe alternative to C stdio and C++ iostreams. Prototype for C++20 std::format family. | License | cmake, conan |

Parse

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| BNFlite | A lightweight grammar parser library | MIT | header-only |
| Boost.Spirit | A set of C++17 libraries for parsing and output generation implemented as ****D****omain ****S****pecific ****E****mbedded ****L****anguages (DSEL) using Expression templates and Template Meta-Programming. The Spirit libraries enable a target grammar to be written exclusively in C++. (Src) (Doc) | BSL-1.0 | cmake |
| CTRE | Fast ****C****ompile-****T****ime ****R****egular ****E****xpressions with support for matching/searching/capturing during compile-time or runtime. | Apache-2.0 | header-only, cmake, vcpkg |
| lexy | A C++17 parser combinator library which allows you to write a parser by specifying it in a convenient C++ DSL with all the flexibility and control of a handwritten parser. Supports UTF-8/16/32. (Doc) | BSL-1.0 | cmake |
| PEGTL | ****P****arsing ****E****xpression ****G****rammar ****T****emplate ****L****ibrary is a zero-dependency C++17 header-only parser combinator library for creating parsers according to a Parsing Expression Grammar (PEG). | Boost | header-only |

Search

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| clucene | The CLucene is a cross-platform, full-featured, open-source indexing and searching engine/API. (Src) (Doc) | LGPL v2.1 | cmake |
| Step20 | Ukkonen's online algorithm for constructing Suffix tree, Manber's algorithm for constructing Suffix array. | MIT | header-only |
| xapian | An open-source search engine with indexing facilities (Src) (Doc) | GPL v2+ | make |

Template Engine

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| inja | A template engine for C++17. | MIT | header-only; cmake, conan, vcpkg, etc. |
| Jinja2C++ | A C++14/17 implementation of Jinja2 templates | MPL-2.0 | cmake, conan |

## Version Control

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| coo-semver | A C++ operation library for semantic version numbers. |  |  |
| LibGit2 | A version control system Git's core library. |  |  |

## Video

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| crystalhd |  |  |  |
| gstreamermm |  |  |  |
| libmatroska |  |  |  |
| libVLC |  |  |  |
| mjpegtools |  |  |  |
| OpenH264 | A multi-platform, multi-architecture, open-source library which supports H.264 encoding and decoding (Src) | BSD-2 Clause | meson |

## Web

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Chromium Embedded |  |  |  |
| cpp-jwt |  |  |  |
| Drogon | A C++14/17 based HTTP web application framework running on Linux/macOS/Unix/Windows. |  |  |
| ffead-cpp | A ****f****ramework ****f****or ****E****nterprise ****A****pplication ****D****evelopment in ****C****++, HTTP1/HTTP2/HTTP3 compliant, supports multiple server backends | Apache 2.0 | cmake |
| libhttpserver | A C++ library for building high performance RESTful web servers. Built upon `libmicrohttpd` to provide a simple API for developers to create HTTP services in C++. | LGPL-v2.1 | autotools |
| libkcddb |  |  |  |
| liblastfm |  |  |  |
| libmusicbrainz5 |  |  |  |
| libnavajo |  |  |  |
| Molybden | An SDK for building cross-platform C++ desktop apps with HTML/CSS/JS GUI. (Doc) (Src) | License | npm |
| oatpp | A powerful portable lightweight and zero-dependency web-framework for IoT and high-performance web-services. |  |  |
| QtWebApp | HTTP(s) Server in C++ inspired by Java Servlets |  |  |
| Tufão | An asynchronous web framework for C++11 built on top of Qt (Doc) | LGPL-2.1, GPL-2.0 | cmake |
| uri-template | URI Templates expansion and reverse-matching for C++ | Apache 2.0 | cmake |
| userver | The C++ Asynchronous Framework | Apache 2.0 | cmake |
| Wt | Widgets and building blocks for web apps, built-in security, PDF rendering, 2D and 3D painting, ORM, charting, authentication frameworks. (Doc) (Src) | GNU GPL or Commercial |  |

### See also

|  |  |
| --- | --- |
| C documentation for Non-ANSI/ISO Libraries | |

### External links

|  |  |
| --- | --- |
| 1. | List of C++ unit testing frameworks — at Wikipedia |
| 2. | A curated list of (awesome) header-only C++ libraries — at GitHub |
| 3. | A curated list of (awesome) C++ and C libraries — at GitHub |
| 4. | Boost C++ libraries — at Boost.org |
| 5. | A huge list of C++ open-source games and frameworks — at GitHub.io |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/links/libs&oldid=180168>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2025, at 23:43.