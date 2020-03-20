# Specs

- Single node
- Instace type: r5.xlarge
- Instance details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 9.0-4

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    0m16.134s
user    0m1.937s
sys     0m1.150s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    0m15.808s
user    0m2.015s
sys     0m1.087s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m22.457s
user    0m2.240s
sys     0m1.310s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    6m3.237s
user    0m1.442s
sys     0m0.855s
~~~
That was how much time elapsed before I grew impatient and killed the test.

5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m12.820s
user    0m2.279s
sys     0m1.227s
~~~
