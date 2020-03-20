# Specs

- Single node
- Instace type: r5.xlarge
- Instance details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 9.0-9

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    0m15.594s
user    0m1.900s
sys     0m1.183s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    0m15.668s
user    0m1.911s
sys     0m1.220s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m14.204s
user    0m2.215s
sys     0m1.400s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    1m39.342s
user    0m3.217s
sys     0m1.585s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m12.767s
user    0m2.376s
sys     0m1.237s
~~~
