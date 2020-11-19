mdbench
=======

Simple filsystem metadata operations benchmark
----------------------------------------------
```
Usage: mdbench [options] [PATH]

  where options are:
    -f, --files <N>  : number of generated files per directory
    -d, --dirs  <N>  : number of generated directories to generate
    -s, --size  <N>  : size of generated files in B/K/M/G
    -n, --no-clean   : do not delete created files and directories
    -h, --help       : help message

  and PATH points to a directory where the test should run. Currect directory is
  used of not specified.
  
The file size can be specified in human friendly format, e.g.: 1K, 256M. 4G.
```

```sh
$ mdbench.py -d 100 -f 100 -s 1 /tmp/mdbench
dir creates     :  0.495ms ± 0.149ms, median  0.440ms 2021.754 op/s
file creates    :  2.521ms ± 2.809ms, median  1.900ms 396.606 op/s
file stats      :  0.276ms ± 0.110ms, median  0.263ms 3619.243 op/s
dir stats       :  0.160ms ± 0.023ms, median  0.153ms 6255.865 op/s
file removes    :  0.756ms ± 0.540ms, median  0.700ms 1323.280 op/s
dir removes     :  0.389ms ± 0.072ms, median  0.362ms 2571.091 op/s
```
