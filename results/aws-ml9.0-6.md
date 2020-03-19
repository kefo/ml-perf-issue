# Specs

- Single node
- VM details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 9.0-6

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    0m15.216s
user    0m1.937s
sys     0m1.161s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    0m15.119s
user    0m1.961s
sys     0m1.143s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m10.989s
user    0m1.853s
sys     0m1.106s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    1m44.523s
user    0m3.133s
sys     0m1.552s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m12.883s
user    0m2.314s
sys     0m1.254s
~~~
