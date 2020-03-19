# Specs

- LC, VMs
- 3-node ML cluster
- VM details: 
    - Memory (per box): 64GB
    - CPUS (per box): 8
- ML Version: 8.0-7.1

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

This run provides a series of results that function as a baseline test of the version of ML 
installed on-prem when the performance issue was first discovered. This is the performance
of the currently installed version.

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    0m46.231s
user    0m0.869s
sys     0m1.438s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    0m43.438s
user    0m0.899s
sys     0m1.386s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m10.398s
user    0m0.850s
sys     0m1.209s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    0m5.808s
user    0m0.781s
sys     0m1.029s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m5.629s
user    0m0.784s
sys     0m0.977s
~~~
