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
