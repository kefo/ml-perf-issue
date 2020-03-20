# Specs

- Single node
- Instace type: r5.xlarge
- Instance details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 9.0-3

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    0m4.612s
user    0m1.746s
sys     0m0.991s

~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    0m4.442s
user    0m1.716s
sys     0m1.010s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m4.407s
user    0m1.684s
sys     0m1.012s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    0m3.691s
user    0m1.712s
sys     0m1.017s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m3.480s
user    0m1.628s
sys     0m1.028s
~~~
