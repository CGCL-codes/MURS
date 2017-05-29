# Apache Spark

Spark is a fast and general cluster computing system for Big Data.

<http://spark.apache.org/>

# Spark JobServer

Spark JobServer provides a REST server for Spark. Jobs are all submitted ot Spark JobServer, and running in
the same Spark context. We can all this as service-oriented Spark.

<https://github.com/spark-jobserver/spark-jobserver>

# MURS

MURS is a memory usage rate based scheduler which aim to mitigate the memory pressure in (service-oriented) Spark.
MURS works in the Spark executor. MURS can work in Spark stand
alone, or with Spark JobServer(advised).

## branch

There are three branches in this project:

- master: the apache spark.

- Release-1.0: MURS version 1.0.

- Develop-1.1: MURS version 1.1, but we are developing it now.

## building and configuration

The same to Apache Spark. You can add some additional configuration in the conf/spark.default.conf for MURS:

spark.murs.yellow, default: 0.4, the threshold of memory pressure.

spark.murs.samplingInterval, default: 200ms, the interval of sampler for memory pressure.

If you want to know more about MURS, please refer to the ICWS paper:
Xuanhua Shi,Xiong Zhang,Ligang He,Hai Jin,Zhixiang Ke,Song Wu, "MURS: Mitigating Memory Pressure in Service-oriented Data Processing System", in Proceedings of the 24th IEEE international Conference on Web Services (ICWS), Honolulu, Hawaii, USA, Jun. 25-30, 2017 
