# Specs

- Single node
- VM details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 10.0-3

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real    16m2.594s
user    0m2.073s
sys     0m1.280s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real    31m26.096s
user    0m2.997s
sys     0m2.136s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real    0m3.453s
user    0m1.583s
sys     0m1.064s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real    0m3.441s
user    0m1.644s
sys     0m0.992s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real    0m3.296s
user    0m1.587s
sys     0m1.049s
~~~
