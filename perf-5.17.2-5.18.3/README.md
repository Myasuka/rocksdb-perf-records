# Performance comparaion between rocksdb-5.17.2 and rocksdb-5.18.3

## Execution commands to run benchmark

Command to test on rocksDB-5.17.2
~~~ bash
./rocksdb-5.17.2/db_bench  --benchmarks=fillseq,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom --db=/home/chagan.ty/rocksdb-benchmark/db-5.17.2-1m --disable_wal=1 --num=1000000   --column_family_distribution=0,100 --key_size=6 --value_size=8 --num_column_families=2  --use_existing_db=0  --threads=1  --numdistinct=1000000
~~~

Command to test on rocksDB-5.18.3
~~~ bash
./rocksdb-5.18.3/db_bench  --benchmarks=fillseq,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom,readrandom --db=/home/chagan.ty/rocksdb-benchmark/db-5.18.3-1m --disable_wal=1 --num=1000000   --column_family_distribution=0,100 --key_size=6 --value_size=8 --num_column_families=2  --use_existing_db=0  --threads=1  --numdistinct=1000000
~~~

## Logs and Options of RocksDB when running tests
Please refer to folder `rocksdb-5.17.2.log` and `rocksdb-5.18.3.log`, which contain the logs and options files.

## Performance results
The machine details:
~~~
Initializing RocksDB Options from the specified file
Initializing RocksDB Options from command-line flags
RocksDB:    version 5.17
Date:       Thu Oct 10 16:33:41 2019
CPU:        96 * Intel(R) Xeon(R) Platinum 8163 CPU @ 2.50GHz
CPUCache:   33792 KB
Keys:       6 bytes each
Values:     8 bytes each (4 bytes after compression)
Entries:    1000000
Prefix:    0 bytes
Keys per prefix:    0
RawSize:    13.4 MB (estimated)
FileSize:   9.5 MB (estimated)
Write rate: 0 bytes/second
Read rate: 0 ops/second
Compression: Snappy
Memtablerep: skip_list
Perf Level: 1
~~~

Some experimental results:
~~~
DB path: [/home/chagan.ty/rocksdb-benchmark/db-5.17.2-1m]
readrandom   :       1.047 micros/op 955337 ops/sec;   12.8 MB/s (1000000 of 1000000 found)

DB path: [/home/chagan.ty/rocksdb-benchmark/db-5.18.3-1m]
readrandom   :       1.129 micros/op 886123 ops/sec;   11.8 MB/s (1000000 of 1000000 found)
~~~
