# Specs

- Single node
- Instace type: r5.xlarge
- Instance details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 9.0-10

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

This run provides a series of results that function as a baseline test of the version of ML installed when 
the performance issue was first discovered.  See other Single node, 32GB, 4 vCPU instance tests

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    0m18.007s
user    0m2.038s
sys     0m1.163s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
?
~~~
I let this run for 44 minutes and then killed it.

3)
~~~bash
$ time ./perf_test values_query_good
real    0m6.547s
user    0m2.339s
sys     0m1.118s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    1m41.644s
user    0m3.234s
sys     0m1.528s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m3.731s
user    0m1.675s
sys     0m1.014s
~~~
