# Glossary

Curated list of various terms that are used in performance analysis.

  - *Baseline* and *Target*: refers to two subsequent units (metrics, profiles, measurements,
      results, etc.) that are being compared and corresponds to new (analysed) system, i.e.
      *target*, and old (previously computed) system, i.e. *baseline*.

  - *Profile*: collection of measurements of resource consumption.

  - *Shadow Memory*: a technique that counts the memory separatly in a continuous block and can be
      used for further analysis or quick computations.

  - *Offline profiling*: the profile is generated after the program's execution is complete; it is
      used for post-mortem analysis, regression detection or for next secondary (non-profiled)
      compilation.

  - *Online profiling*: the profile is provided while the program is running, and the program
      or its interpretation changes based on the current hot sections.

  - *Feedback Directed Optimizations*: uses profiling to monitor the execution of the program; the
      program is then either compiled wrt to the profiles, or the interpretation is modified wrt to
      the profiling data.

  - *Edge Profiling*: computes frequency of each edge between basic blocks; naive approach adds
      counters either to source or target (if there are multiple target, one needs to add
      additional BB between); the optimal way is to instrument BB according to maximum spanning
      tree.
  
  - *Path Profiling*: computes frequency of each path in the program CFG; optimal way is using path
      numbering based on Ball & Laurus algorithm.

  - *Branch Spectra*: the set of conditional branches that were exercised with the execution of the
      program *P*. We can indicate that merely the conditional branch was taken (Branch-hit
      spectrum), or count the number of times it was taken (Branch-count spectrum).

  - *Path Spectra*: the set of loop-free intraprocedural paths that were exercised with the
      execution of the program *P*. We can indicate that merely the path was taken (Path-hit
      spectrum), or count the number of times it was taken (Path-count spectrum)

  - *Complete-path Spectrum*: records the complete path that is traversed as $P$ is executed.

  - *Data-dependence Spectra*: records the set of definition-use pairs that are exercised as $P$ is
      executed. We can indicate that merely the def-use pair was exercised (Data-dependence-hit
      spectrum), or count the number of times it was exercised (Data-dependence-count spectrum).

  - *Output spectrum*: records the output of $P$ as it executes.
  - *Execution-trace spectrum*: records the sequence of program statements traversed as $P$
      executes.
