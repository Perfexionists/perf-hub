# Metrics

Curated list of various metrics, key performance indicators or other measurable aspects of performance.

  - *Cache Utilization Rate (CUR)*: the percentage of cache lines holding the actual heap objects,
      used to evaluate cache capacity misses.
      - source: MemPerf: Profiling Allocator-Induced Performance Slowdowns
      - usage: a memory allocator with higher internal fragmentation may have a lower cache
          utilization rate; an allocator with higher cache utilization rate will have a better
          performance.

  - *Conflict Miss Score (CMS)*: for given cache set $s$, it is the ration $CMS_s =
      \frac{MissRatio_s}{MissRatio_{avg}}$, where $MissRatio_s$ is cache miss rate of cache set $s$
      and $MissRatio_{avg}$ is the average miss ratio. Then, *CMS* is computed as $CMS =
      \sum{i=0}{n}(CMS_{S_i} \times c^i)$, where $c$ is reduction coefficient, to adjust the CMS of
      each cache set in relation to its ranking by miss ration. By default $c = 0.5$, which ensures
      that the cache set with the highest miss ratio recieves the full CMS score, while each
      subsequent set's score is reduced by half. The rationale is that allocator-induced conflicts
      are more likely to occur in a few cache sets
      - source: MemPerf: Profiling Allocator-Induced Performance Slowdowns
      - usage: the rationale is to model situations, when multiple allocated objects are mapped to the
          same cache set.

  - *False Sharing Score (FSS)*: computed as $FSS = \sum{i=0}{n}(FSS_{c_i} \times c^i)$, where
      $FSS_c = MissRatio_c \times 100$. THe $c$ is a reduction coefficient, introduced to adjust
      the FSS of each cache line in relation to its ranking by miss ratio.
      - source: MemPerf: Profiling Allocator-Induced Performance Slowdowns
      - usage: the rationale is to model, when an allocator allocates different objects in the same
          cache line to different threads, and these threads are accessing these objects
          concurently.

  - *Page Utilization Rate (PUR)*: the percentage of pages holding the heap objects; used for
      measuring the memory allocator's impact related to TLB misses.
      - source: MemPerf: Profiling Allocator-Induced Performance Slowdowns
      - usage: a memory allocator with a lower page utilization rate potentially causes more TLB misses,
          and therefore worse performance.
