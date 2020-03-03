# Specs

- LC, VMs
- 3-node ML cluster
- VM details: 
    - Memory (per box): 64GB
    - CPUS (per box): 8
- ML Version: 8.0-7.1

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
...
real    0m39.426s
user    0m0.906s
sys     0m1.346s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    0m29.348s
user    0m0.853s
sys     0m1.282s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m7.034s
user    0m0.803s
sys     0m0.974s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    0m5.661s
user    0m0.808s
sys     0m0.949s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m5.751s
user    0m0.805s
sys     0m0.989s
~~~
