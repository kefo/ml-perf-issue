# Specs

AWS VPC
3-node ML cluster
Instance types: r5.4xlarge
    Memory (per instance): 128GB
    VCPUS (per instance): 16
ML Version: 9.0-10

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
...
real    0m25.805s
user    0m1.938s
sys     0m1.179s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
...
~~~
Do not know how long this will take.  I don't have the patience.


3)
~~~bash
$ time ./perf_test values_query_good
...
real    0m3.981s
user    0m1.751s
sys     0m1.114s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
...
real    0m54.682s
user    0m3.381s
sys     0m1.638s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
...
real    0m26.853s
user    0m3.358s
sys     0m1.779s
~~~

