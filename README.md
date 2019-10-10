# RocksDB-perf-records
This repo is to record the performace change when trying to bump RocksDB version within Flink.

## Performance comparison of RocksDB-5.17.2 and RocksDB-5.18.3
We have used [flink-benchmarks](https://github.com/dataArtisans/flink-benchmarks) to verify the performace and record the difference in [rocksdb-5774](https://github.com/facebook/rocksdb/issues/5774). Moreover, I have also verified that with rocksDB's `db_bench`, please refer to `perf-5.17.2-5.18.3` folder to know more details.
