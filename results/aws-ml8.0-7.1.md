# Specs

- Single node
- Instace type: r5.xlarge
- Instance details: 
    - Memory: 32GB
    - CPUS: 4
- ML Version: 8.0-7.1

Data loaded into a one-forest database.  Tests executed on localhost of that
forest.

Truncated LCSH to the first 5 million lines (to speed up load times for increased testing).


# Runs


1)
~~~bash
$ time ./perf_test filter_query_good
real	0m13.064s
user	0m1.752s
sys	    0m1.039s
~~~


2)
~~~bash
$ time ./perf_test filter_query_bad
real	0m12.772s
user	0m1.644s
sys	    0m1.162s
~~~


3)
~~~bash
$ time ./perf_test values_query_good
real	0m6.041s
user	0m1.669s
sys	    0m0.984s
~~~


4)
~~~bash
$ time ./perf_test values_query_bad
real	0m6.120s
user	0m1.668s
sys	    0m0.980s
~~~


5)
~~~bash
$ time ./perf_test values_query_better_but
real	0m5.522s
user	0m1.588s
sys	    0m1.056s
~~~
