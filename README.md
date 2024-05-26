# Performance Assets Hub

Curated list of performance assets, such as links to profilers, performance analysis tools, tips for better performance, scripts for anything related to performance.

- :+1: recommended tool.
- :classical-building: old tool (possibly not maintained anymore) with last commit more that 5
    years ago.

## Table of Contents

- [Performance Assets Hub](#performance-assets-hub)
  - [Table of Contents](#table-of-contents)
  - [Profiling](#profiling)
    - [Generic](#generic)
    - [C/C++](#cc)
    - [Java](#java)
    - [Python](#python)
    - [C#](#c)
    - [Web](#web)
    - [Go](#go)
  - [Instrumentation](#instrumentation)
    - [eBPF](#ebpf)
    - [Other Frameworks](#other-frameworks)
  - [Benchmarking](#benchmarking)
    - [Benchmarking Tools](#benchmarking-tools)
    - [Benchmarks](#benchmarks)
  - [Workload Generators](#workload-generators)
    - [Fuzz Testing](#fuzz-testing)
  - [Other Performance Tools](#other-performance-tools)
    - [Performance Managers](#performance-managers)
    - [Performance Monitoring](#performance-monitoring)
    - [Other Analysers](#other-analysers)
    - [Visualization](#visualization)
  - [Static Analysis](#static-analysis)
    - [Resource Bounds Analysis](#resource-bounds-analysis)
    - [Worst-Case Execution Time](#worst-case-execution-time)
  - [Other Assets](#other-assets)
    - [Allocators](#allocators)
    - [Recommended Blogs And Sites](#recommended-blogs-and-sites)
    - [Other assets](#other-assets)
  - [Contributing](#contributing)

## Profiling

### Generic

  - [bytehound](https://github.com/koute/bytehound): a memory profiler for Linux.
  - [ftrace](https://www.kernel.org/doc/html/v5.0/trace/ftrace.html): a tracer for debugging and/or
      analyzing latencies and performance issues outside of user-space; focused on kernel.
  - [perf](https://perf.wiki.kernel.org/index.php/Main_Page): linux profiling with performance counters; state-of-the-art for profiling in Linux; we recommend to read Brendan Gregg's [perf Examples](https://www.brendangregg.com/perf.html).
  - [perf-tools](https://github.com/brendangregg/perf-tools): a performance analysis tools based on
      Linux perf_events and ftrace.
  - [firefox Profiler](https://profiler.firefox.com/): a web app for Firefox performance analysis; you can import perf profiles (among other) and use it as a GUI.
  - [strace](https://strace.io/): a diagnostic, debugging and instructional userspace utility for
      linux; used for monitoring between processes and linux kernel.
  - [Intel Advisor](https://www.intel.com/content/www/us/en/developer/tools/oneapi/advisor.html#gs.9u8xng): a design and analysis tool for developing performant code; for efficient CPU Code, GPU offload, etc.
  - [Intel VTune
      Profiler](https://www.intel.com/content/www/us/en/developer/tools/oneapi/vtune-profiler.html):
      profiler for many languages, including C, C++, C#, Python, etc.

### C/C++

  - [Coz](https://github.com/plasma-umass/coz): a profiler for C/C++ and Rust code that can measure the optimization potential of code.
  - [gprof](https://ftp.gnu.org/old-gnu/Manuals/gprof-2.9.1/html_mono/gprof.html): a hybrid instrumentation and sampling-based performance profiler.
  - [massif](https://valgrind.org/info/tools.html#massif): a heap profiler from Valgrind tool suite.
  - [OProfile](https://oprofile.sourceforge.io/): an open-source statistical profiler for Linux systems with low overhead.

### Java

  - [soot](https://soot-oss.github.io/soot/): a framework for analyzing and transforming Java and android applications.
  - [SootUp](https://soot-oss.github.io/SootUp/latest/): new rehaul of the soot static analysis framework.
  - [YourKit](https://www.yourkit.com/): low overhead profiler for Java EE and Jave SE platforms.

### Python 

  - [memray](https://github.com/bloomberg/memray): :+1:
 a memory profiler for python.
  - [Scalene](https://github.com/plasma-umass/scalene): a Python CPU+GPU+memory profiler with AI-powered optimization proposals.
  - [py-spy](https://github.com/benfred/py-spy): a light-weight sampling profiler for Python programs.

### C#

  - [perfview](https://github.com/Microsoft/perfview): a CPU and memory performance analysis tool
      mainly for windows and .NET applications.
  - [YourKit](https://www.yourkit.com/): easy-to-use performance and memory .NET profiler for
      Windows, Linux an macOS.

### Web

  - [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview/): an open-source, automated tool for improving quality of web pages (includes performance analysis).
  - [firefox Profiler](https://profiler.firefox.com/): a web app for Firefox performance analysis; you can import perf profiles (among other) and use it as a GUI.

### Go

  - [fgprof](https://github.com/felixge/fgprof): a sampling Go profiler for On-CPU and Off-cpu time.

## Instrumentation

### eBPF

  - [Andrii Nakryiko's Blog](https://nakryiko.com/): a blog with good tutorials for starting with eBPF.
  - [Awesome eBPF](https://github.com/zoidyzoidzoid/awesome-ebpf): a curated list of awesome projects related to eBPF.
  - [eBPF](https://ebpf.io/): a main hub for starting with eBPF.

### Other Frameworks

  - [Jalangi](https://github.com/Samsung/jalangi2): a framework for writing dynamic analyses for JavaScript.
  - [Lunatik](https://github.com/luainkernel/lunatik): a framework for scripting the linux kernel with lua.
  - [PIN](https://www.intel.com/content/www/us/en/developer/articles/tool/pin-a-dynamic-binary-instrumentation-tool.html): a dynamic binary instrumentation tool for C/C++ programs.
  - [SystemTap](https://sourceware.org/systemtap/): a dynamic binary instrumentation tools.
  - [Triton](https://triton-library.github.io/): a dynamic binary analysis library that allows one to build own program analysis tools.
  - [javassist](https://github.com/jboss-javassist/javassist): a java bytecode engineering toolkit.
  - [PyVyPR](https://pyvypr.github.io/home/): a prototype framework for creating runtime analysis of Python code.

## Benchmarking

### Benchmarking Tools

  - [BenchExec](https://github.com/sosy-lab/benchexec): a framework for reliable benchmarking and resource measurements.
  - [pycobench](https://github.com/Perfexionists/pycobench): a fork of
      [ondrik/pycobench](https://github.com/ondrik/pycobench) a lightweight benchmarking tool from
      our Perfexionists group.

### Benchmarks

  - [CORAL-2 Benchmarks](https://asc.llnl.gov/coral-2-benchmarks): a benchmark by advanced simulation and computing group.
  - [Renaissance Suite](https://renaissance.dev/): a modern, open, and diversified benchmark suite for the JVM.

## Workload Generators

### Fuzz Testing

  - [AFL](https://github.com/google/AFL) :classical-building: americal fuzzy lop: an original
      security-oriented fuzzer (many fuzzers build upon this).
  - [badger](https://github.com/isstac/badger): :classical-building: a complexity analysis with
      fuzzing and symbolic execution.
  - [perffuzz](https://github.com/carolemieux/perffuzz): :classical-building: automatic generation of pathological
      inputs for C/C++ programs; a performance fuzztesting tool.

## Other Performance Tools

### Performance Managers

  - [perun](https://github.com/Perfexionists/perun): :+1: our performance control system that manages
      profiles, automatization and history.
  - [gopper](https://github.com/sealuzh/gopper)/[hopper](https://github.com/sealuzh/hopper): a collection of scripts for performance history analysis of Java programs.
  - [newrelic](https://newrelic.com/): continuous monitoring of programs.
  - [PerfCI](https://github.com/JesperStromblad/perfci): a toolchain for automated performance testing under Continuous Integration.
  - [prometheus](https://prometheus.io/): a monitoring system and a time-series database.

### Performance Monitoring

  - [Kieker](https://github.com/kieker-monitoring/kieker): a monitoring framework for application
      performance monitoring and dynamic software analysis.
  - [likwid](https://github.com/RRZE-HPC/likwid): a performance monitoring and benchmarking suite.

### Other Analysers

  - [CCprof](https://github.com/proywm/CCProf): a lightweight detection of cache conflicts.
  - [Feather](https://github.com/WitchTools/Feather): a featherlight on-the-fly false-sharing detection tools.
  - [Linux Crisis Tools](https://www.brendangregg.com/blog/2024-03-24/linux-crisis-tools.html): a blogpost from Brendan Gregg, which list useful tools for performance monitoring or debugging.
  - [SyncPerf](https://github.com/mejbah/SyncPerf): a lightweight profiler to detect and categorize root causes of synchronization related performance issues in multithreaded programs.

### Visualizations

  - [flamescope](https://github.com/Netflix/flamescope): a visualization tool for exploring different time ranges as Flame Graphs.
  - [hotspot](https://github.com/KDAB/hotspot): the linux perf GUI for performance analysis; standalone tool for interpreting results of perf.
  - [pprof](https://github.com/google/pprof): a tool for visualization and analysis of profiling data in perf or `*.proto` format.

## Static Analysis

  - [Static Analysis Tools](https://github.com/analysis-tools-dev/static-analysis): a curated list of static analysis tools and linters for all programming languages.

### Resource Bounds Analysis

  - [CoFloCo](https://github.com/aeflores/CoFloCo): a static analysis tool for automatic symbolic
      complexity of upper and lower bounds of imperative and recursive programs.
  - [FBInfer](https://fbinfer.com/): a static analysis tool that includes measuring of complexity of code.

### Worst-case Exeuction Time

  - [Bound-T](http://www.bound-t.com/): static analysis of the machine code that computes upper
      bounds on the execution time and stack usage of embedded programs.
  - [Chronos](https://www.comp.nus.edu.sg/~rpembed/chronos/): a timing analysis of embedded
      software.

## Other Assets

### Allocators

  - [Hoard](http://hoard.org/): a fast, scalable memory-efficient memory allocator; corss-platform.
  - [jemalloc](https://jemalloc.net/): a general purpose malloc implementation with fragmentation avoidance and scalable concurrency support.
  - [TCMalloc](https://github.com/google/tcmalloc): a google's customized implementation of `malloc()` and `operator new`; a fast multi-threaded implementation.

### Recommended Blogs And Sites

  - [Accidentaly Quadratic](https://accidentallyquadratic.tumblr.com/): a blog with various performance bugs found in production and applications.
  - [Big-O Cheat Sheet](https://www.bigocheatsheet.com/): a page that covers the space and time Big-O complexities of common algorithms used in Computer Science.
  - [Brendan Gregg's Homepage](https://brendangregg.com/): a Brendan Gregg's Homepage with lots of information about performance analysis, eBPF, perf, etc.
  - [Peak Memory Usage of a Linux Process](https://www.baeldung.com/linux/process-peak-memory-usage): a simple guide how to measure peak memory of your applications.

### Other assets

  - [bootlin](https://elixir.bootlin.com/linux/latest/source): cross reference for linux kernel sources and headers.
  - [Font Awesome](https://fontawesome.com/): a lots of free icons to be used in visualizations.
  - [Highcharts.js](https://www.highcharts.com/): a highly scalable javascript library for building visualizations of the data.
  - [plotly](https://plotly.com/): a library supporting many programming languages (JS, Python, etc.) for building visualizations of the data.
  - [seaborn](https://seaborn.pydata.org/index.html): a matplotlib-based Python visualization library for building lightweight visualizations of the data.

## Contributing

If you would like to contribute, please send us a PR, we will review your addition, and if deemed
suitable for our list we will include it.
