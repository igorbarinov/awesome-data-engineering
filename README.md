Awesome Data Engineering
==========================
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
A curated list of data engineering tools for software developers

List of content

1. [Databases] (#databases)
2. [Ingestion](#data-ingestion)
3. [File System] (#file-system)
4. [File Format](#file-format)
5. [Stream Processing](#stream-processing)
6. [Batch Processing] (#batch-processing)
7. [Charts and Dashboards] (#charts-and-dashboards)
8. [Frameworks] (#frameworks)
9. [Datasets](#datasets)
9. [Monitoring] (#monitoring)

# Databases
- Relational
	* [MySQL] (http://www.mysql.com/)
	* [MariaDB] (https://mariadb.org/) An enhanced, drop-in replacement for MySQL
	* [PostgreSQL] (http://www.postgresql.org/)
	* [Amazon RDS] (http://aws.amazon.com/rds/)
	* [Crate.IO] (https://crate.io/) Scalable SQL database with the NOSQL goodies
- Key-Value
	* [Redis] (http://redis.io/)
	* [Riak] (https://docs.basho.com/riak/latest/)
	* [AWS DynamoDB] (http://aws.amazon.com/dynamodb/)
	* [HyperDex](https://github.com/rescrv/HyperDex) HyperDex is a scalable, searchable key-value store
	* [SSDB](http://ssdb.io) A high performance NoSQL database supporting many data structures, an alternative to Redis
- Column
	* [Cassandra] (http://cassandra.apache.org/)
	* [HBase] (http://hbase.apache.org/)
	* [Infobright] (http://www.infobright.org)
	* [AWS Redshift] (http://aws.amazon.com/redshift/)
- Document
	* [MongoDB] (https://www.mongodb.org/)
	* [Elasticsearch] (https://www.elastic.co/)
	* [Couchbase] (http://www.couchbase.com/)
	* [RethinkDB](http://rethinkdb.com/) The open-source database for the realtime web
- Graph
	* [Neo4j] (http://neo4j.com/)
	* [OrientDB] (http://orientdb.com/orientdb/)
	* [ArangoDB] (https://www.arangodb.com/)
	* [Titan] (http://thinkaurelius.github.io/titan/)
	* [FlockDB](https://github.com/twitter/flockdb) A distributed, fault-tolerant graph database by Twitter
- Distributed
	* [DAtomic](http://www.datomic.com)
	* [Apache Geode](http://geode.incubator.apache.org) 
- Timeseries
	* [InfluxDB](https://github.com/influxdb/influxdb) Scalable datastore for metrics, events, and real-time analytics
	* [OpenTSDB](https://github.com/OpenTSDB/opentsdb) A scalable, distributed Time Series Database.
	* [kairosdb](https://github.com/kairosdb/kairosdb) Fast scalable time series database

# Data Ingestion
* [Kafka] (http://kafka.apache.org/)
	* [Camus](https://github.com/linkedin/camus) LinkedIn's Kafka to HDFS pipeline.
	* [BottledWater](https://github.com/confluentinc/bottledwater-pg) Change data capture from PostgreSQL into Kafka
	* [kafkat](https://github.com/airbnb/kafkat) Simplified command-line administration for Kafka brokers
	* [kafkacat](https://github.com/edenhill/kafkacat) Generic command line non-JVM Apache Kafka producer and consumer
	* [pg-kafka](https://github.com/xstevens/pg_kafka) A PostgreSQL extension to produce messages to Apache Kafka
	* [librdkafka](https://github.com/edenhill/librdkafka) The Apache Kafka C/C++ library
	* [kafka-docker](https://github.com/wurstmeister/kafka-docker) Kafka in Docker
	* [kafka-manager](https://github.com/yahoo/kafka-manager) A tool for managing Apache Kafka
	* [kafka-node](https://github.com/SOHU-Co/kafka-node) Node.js client for Apache Kafka 0.8
	* [Secor] (https://github.com/pinterest/secor) Pinterest's Kafka to S3 distributed consumer
* [AWS Kinesis] (http://aws.amazon.com/kinesis/)
* [RabbitMQ](http://rabbitmq.com)
* [FluentD](http://www.fluentd.org)
* [Apache Scoop](https://sqoop.apache.org)
* [Luigi](https://github.com/spotify/luigi) Python module that helps you build complex pipelines of batch jobs

# File System
* [HDFS] (https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html)
	* [Snakebit](https://github.com/spotify/snakebite) A pure python HDFS client
* [AWS S3] (http://aws.amazon.com/s3/)
* [Tachyon] (http://tachyon-project.org/) Tachyon is a memory-centric distributed storage system enabling reliable data sharing at memory-speed across cluster frameworks, such as Spark and MapReduce
* [CEPH](http://ceph.com/) Ceph is a unified, distributed storage system designed for excellent performance, reliability and scalability
* [OrangeFS](http://www.orangefs.org/) Orange File System is a branch of the Parallel Virtual File System
* [SnackFS](https://github.com/tuplejump/snackfs-release) SnackFS is our bite-sized, lightweight HDFS compatible FileSystem built over Cassandra
* [GlusterFS](http://www.gluster.org/) Gluster Filesystem
* [XtreemFS](http://www.xtreemfs.org/) fault-tolerant distributed file system for all storage needs

# File Format
* [Apache Avro](https://avro.apache.org) Apache Avro™ is a data serialization system
* [Apache Parquet](https://parquet.apache.org) Apache Parquet is a columnar storage format available to any project in the Hadoop ecosystem, regardless of the choice of data processing framework, data model or programming language.
	* [Snappy](https://github.com/google/snappy) A fast compressor/decompressor. Used with Parquet
	* [PigZ](http://zlib.net/pigz/) A parallel implementation of gzip for modern
multi-processor, multi-core machines
* [Apache Thrift](https://thrift.apache.org) The Apache Thrift software framework, for scalable cross-language services development
* [ProtoBuf](https://github.com/google/protobuf) Protocol Buffers - Google's data interchange format
* [SequenceFile](http://wiki.apache.org/hadoop/SequenceFile) SequenceFile is a flat file consisting of binary key/value pairs. It is extensively used in MapReduce as input/output formats
* [Kryo](https://github.com/EsotericSoftware/kryo) Kryo is a fast and efficient object graph serialization framework for Java

# Stream Processing
* [Spark Streaming](https://spark.apache.org/streaming/) Spark Streaming makes it easy to build scalable fault-tolerant streaming applications.
* [Apache Flink](https://flink.apache.org/) Apache Flink is a streaming dataflow engine that provides data distribution, communication, and fault tolerance for distributed computations over data streams.
* [Apache Storm](https://storm.apache.org) Apache Storm is a free and open source distributed realtime computation system
* [Apache Samza](https://samza.apache.org) Apache Samza is a distributed stream processing framework
* [Apache NiFi](https://nifi.incubator.apache.org) is an easy to use, powerful, and reliable system to process and distribute data

# Batch Processing
* [Hadoop MapReduce] (http://hadoop.apache.org/docs/current/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html) Hadoop MapReduce is a software framework for easily writing applications which process vast amounts of data (multi-terabyte data-sets) in-parallel on large clusters (thousands of nodes) of commodity hardware in a reliable, fault-tolerant manner
* [Spark] (https://spark.apache.org/)
	* [Spark Packages](http://spark-packages.org) A community index of packages for Apache Spark
	* [Deep Spark](https://github.com/Stratio/deep-spark) Connecting Apache Spark with different data stores 
	* [Spark RDD API Examples](http://homepage.cs.latrobe.edu.au/zhe/ZhenHeSparkRDDAPIExamples.html) by Zhen He
* [AWS EMR] (http://aws.amazon.com/elasticmapreduce/)
* [Flink](https://flink.apache.org/)
* [Tez] (https://tez.apache.org/)
- Batch ML
	* [H2O] (http://h2o.ai/)
	* [Mahout] (http://mahout.apache.org/)
	* [Spark MLlib] (https://spark.apache.org/docs/1.2.1/mllib-guide.html)
- Batch Graph
	* [GraphLab] (https://dato.com/products/create/)
	* [Giraph] (http://giraph.apache.org/)
	* [Spark GraphX] (https://spark.apache.org/graphx/)
- Batch SQL
	* [Presto] (https://prestodb.io/docs/current/index.html)
	* [Hive] (http://hive.apache.org)
		* [Hivemall](https://github.com/myui/hivemall) Scalable machine learning library for Hive/Hadoop 
		* [PyHive] (https://github.com/dropbox/PyHive) Python interface to Hive and Presto
	* [Drill] (https://drill.apache.org/)

# Charts and Dashboards
* [Highcharts] (http://www.highcharts.com/)
* [ZingChart](http://www.zingchart.com/)
* [C3.js](http://c3js.org) D3-based reusable chart library
* [D3] (http://d3js.org/)
	* [D3Plus] (http://d3plus.org) D3's simplier, easier to use cousin. Mostly predefined templates that you can just plug data in.
* [SmoothieCharts](http://smoothiecharts.org)
* [PyXley](https://github.com/stitchfix/pyxley)Python helpers for building dashboards using Flask and React

# Frameworks
* [Luigi] (https://github.com/spotify/luigi) Luigi is a Python module that helps you build complex pipelines of batch jobs.
	* [CronQ](https://github.com/seatgeek/cronq) An application cron-like system. [Used](http://chairnerd.seatgeek.com/building-out-the-seatgeek-data-pipeline/) w/Luige 
* [Cascading] (http://www.cascading.org/) Java based application development platform.
* [Airflow] (https://github.com/airbnb/airflow) Airflow is a system to programmaticaly author, schedule and monitor data pipelines.
* [Azkeban] (https://azkaban.github.io/) Azkaban is a batch workflow job scheduler created at LinkedIn to run Hadoop jobs. Azkaban resolves the ordering through job dependencies and provides an easy to use web user interface to maintain and track your workflows. 

# ELK Elastic Logstash Kebana
* [docker-logstash](https://github.com/pblittle/docker-logstash)
* [elasticsearch-jdbc](https://github.com/jprante/elasticsearch-jdbc) JDBC importer for Elasticsearch
* [ZomboDB](https://github.com/zombodb/zombodb) Postgres Extension that allows creating an index backed by Elasticsearch

# Docker
* [Flocker](https://github.com/ClusterHQ/flocker) Easily manage Docker containers & their data
* [Rancher](http://rancher.com/rancher-os/) RancherOS is a 20mb Linux distro that runs the entire OS as Docker containers


# Datasets
## Realtime
* [Instagram Realtime](https://instagram.com/developer/realtime/)
* [Twitter Realtime](https://dev.twitter.com/streaming/overview)
* [Firebase Realtime](https://www.firebase.com/docs/open-data/) Airport delays, Parking,  Cryptocurrencies, Earthquakes, Transit, Weather

## Data Dumps
* [GitHub Archive] (https://www.githubarchive.org/) GitHub's public timeline since 2011, updated every hour
* [Common Crawl] (https://commoncrawl.org/) Open source repository of web crawl data
* [Wikipedia] (https://dumps.wikimedia.org/enwiki/latest/) Wikipedia's complete copy of all wikis, in the form of wikitext source and metadata embedded in XML. A number of raw database tables in SQL form are also available.

Cheers to [The Data Engineering Ecosystem: An Interactive Map](http://insightdataengineering.com/blog/pipeline_map.html)

Inspired by the [awesome](https://github.com/sindresorhus/awesome) list. Created by [Insight Data Engineering](http://insightdataengineering.com) fellows.

# Monitoring

## Prometheus
* [Prometheus.io](https://github.com/prometheus/prometheus) An open-source service monitoring system and time series database
* [HAProxy Exporter](https://github.com/prometheus/haproxy_exporter) Simple server that scrapes HAProxy stats and exports them via HTTP for Prometheus consumption

## License

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Igor Barinov](http://github.com/igorbarinov/) has waived all copyright and related or neighboring rights to this work.
