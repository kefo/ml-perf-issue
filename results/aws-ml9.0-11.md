# Specs

- Single node
- Instace type: r5.xlarge
- Instance details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 9.0-11

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    15m53.212s
user    0m2.193s
sys     0m1.150s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    15m32.626s
user    0m2.562s
sys     0m1.609s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m4.236s
user    0m1.627s
sys     0m1.030s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    0m3.469s
user    0m1.605s
sys     0m1.050s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m3.401s
user    0m1.711s
sys     0m0.947s
~~~
