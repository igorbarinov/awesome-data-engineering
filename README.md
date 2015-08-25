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
10. [Monitoring] (#monitoring)
11. [Docker](#docker)

# Databases
- Relational
	* [MySQL] (http://www.mysql.com/) The world's most popular open source database.
	* [MariaDB] (https://mariadb.org/) An enhanced, drop-in replacement for MySQL.
	* [PostgreSQL] (http://www.postgresql.org/) The world's most advanced open source database.
	* [Amazon RDS] (http://aws.amazon.com/rds/) Amazon RDS makes it easy to set up, operate, and scale a relational database in the cloud. 
	* [Crate.IO] (https://crate.io/) Scalable SQL database with the NOSQL goodies.
- Key-Value
	* [Redis] (http://redis.io/) An open source, BSD licensed, advanced key-value cache and store.
	* [Riak] (https://docs.basho.com/riak/latest/) A distributed database designed to deliver maximum data availability by distributing data across multiple servers.
	* [AWS DynamoDB] (http://aws.amazon.com/dynamodb/) A fast and flexible NoSQL database service for all applications that need consistent, single-digit millisecond latency at any scale.
	* [HyperDex](https://github.com/rescrv/HyperDex) HyperDex is a scalable, searchable key-value store
	* [SSDB](http://ssdb.io) A high performance NoSQL database supporting many data structures, an alternative to Redis
	* [Kyoto Tycoon]() Kyoto Tycoon is a lightweight network server on top of the Kyoto Cabinet key-value database, built for high-performance and concurrency
- Column
	* [Cassandra] (http://cassandra.apache.org/) The right choice when you need scalability and high availability without compromising performance.
		* [Cassandra Calculator] (http://www.ecyrd.com/cassandracalculator/) This simple form allows you to try out different values for your Apache Cassandra cluster and see what the impact is for your application.	
	* [HBase] (http://hbase.apache.org/) The Hadoop database, a distributed, scalable, big data store.
	* [Infobright] (http://www.infobright.org) Column oriented, open-source analytic database provides both speed and efficiency.  
	* [AWS Redshift] (http://aws.amazon.com/redshift/) A fast, fully managed, petabyte-scale data warehouse that makes it simple and cost-effective to analyze all your data using your existing business intelligence tools.
- Document
	* [MongoDB] (https://www.mongodb.org/) An open-source, document database designed for ease of development and scaling. 
	* [Elasticsearch] (https://www.elastic.co/) Search & Analyze Data in Real Time.
	* [Couchbase] (http://www.couchbase.com/) The highest performing NoSQL distributed database.
	* [RethinkDB](http://rethinkdb.com/) The open-source database for the realtime web.
- Graph
	* [Neo4j] (http://neo4j.com/) The world’s leading graph database.
	* [OrientDB] (http://orientdb.com/orientdb/) 2nd Generation Distributed Graph Database with the flexibility of Documents in one product with an Open Source commercial friendly license.
	* [ArangoDB] (https://www.arangodb.com/) A distributed free and open-source database with a flexible data model for documents, graphs, and key-values. 
	* [Titan] (http://thinkaurelius.github.io/titan/) A scalable graph database optimized for storing and querying graphs containing hundreds of billions of vertices and edges distributed across a multi-machine cluster.
	* [FlockDB](https://github.com/twitter/flockdb) A distributed, fault-tolerant graph database by Twitter.
- Distributed
	* [DAtomic](http://www.datomic.com) The fully transactional, cloud-ready, distributed database.
	* [Apache Geode](http://geode.incubator.apache.org) An open source, distributed, in-memory database for scale-out applications.
- Timeseries
	* [InfluxDB](https://github.com/influxdb/influxdb) Scalable datastore for metrics, events, and real-time analytics.
	* [OpenTSDB](https://github.com/OpenTSDB/opentsdb) A scalable, distributed Time Series Database.
	* [kairosdb](https://github.com/kairosdb/kairosdb) Fast scalable time series database.

# Data Ingestion
* [Kafka] (http://kafka.apache.org/) Publish-subscribe messaging rethought as a distributed commit log.
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
* [AWS Kinesis] (http://aws.amazon.com/kinesis/) A fully managed, cloud-based service for real-time data processing over large, distributed data streams.
* [RabbitMQ](http://rabbitmq.com) Robust messaging for applications.
* [FluentD](http://www.fluentd.org) An open source data collector for unified logging layer.
* [Apache Scoop](https://sqoop.apache.org) A tool designed for efficiently transferring bulk data between Apache Hadoop and structured datastores such as relational databases.
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
* [SeaweedFS](https://github.com/chrislusf/seaweedfs) Seaweed-FS is a simple and highly scalable distributed file system. There are two objectives: to store billions of files! to serve the files fast! Instead of supporting full POSIX file system semantics, Seaweed-FS choose to implement only a key~file mapping. Similar to the word "NoSQL", you can call it as "NoFS".

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
* [VoltDB](http://voltdb.com/)

# Batch Processing
* [Hadoop MapReduce] (http://hadoop.apache.org/docs/current/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html) Hadoop MapReduce is a software framework for easily writing applications which process vast amounts of data (multi-terabyte data-sets) in-parallel on large clusters (thousands of nodes) of commodity hardware in a reliable, fault-tolerant manner
* [Spark] (https://spark.apache.org/)
	* [Spark Packages](http://spark-packages.org) A community index of packages for Apache Spark
	* [Deep Spark](https://github.com/Stratio/deep-spark) Connecting Apache Spark with different data stores 
	* [Spark RDD API Examples](http://homepage.cs.latrobe.edu.au/zhe/ZhenHeSparkRDDAPIExamples.html) by Zhen He
	* [Livy](https://github.com/cloudera/hue/tree/master/apps/spark/java#welcome-to-livy-the-rest-spark-server) Livy, the REST Spark Server
* [AWS EMR] (http://aws.amazon.com/elasticmapreduce/) A web service that makes it easy to quickly and cost-effectively process vast amounts of data.
* [Flink](https://flink.apache.org/) An open source platform for scalable batch and stream data processing.
* [Tez] (https://tez.apache.org/) An application framework which allows for a complex directed-acyclic-graph of tasks for processing data.
- Batch ML
	* [H2O] (http://h2o.ai/) Fast scalable machine learning API for smarter applications.
	* [Mahout] (http://mahout.apache.org/) An environment for quickly creating scalable performant machine learning applications.
	* [Spark MLlib] (https://spark.apache.org/docs/1.2.1/mllib-guide.html) Spark’s scalable machine learning library consisting of common learning algorithms and utilities, including classification, regression, clustering, collaborative filtering, dimensionality reduction, as well as underlying optimization primitives.
- Batch Graph
	* [GraphLab Create] (https://dato.com/products/create/) A machine learning platform that enables data scientists and app developers to easily create intelligent apps at scale.
	* [Giraph] (http://giraph.apache.org/) An iterative graph processing system built for high scalability. 
	* [Spark GraphX] (https://spark.apache.org/graphx/) Apache Spark's API for graphs and graph-parallel computation. 
- Batch SQL
	* [Presto] (https://prestodb.io/docs/current/index.html) A distributed SQL query engine designed to query large data sets distributed over one or more heterogeneous data sources.
	* [Hive] (http://hive.apache.org) Data warehouse software facilitates querying and managing large datasets residing in distributed storage. 
		* [Hivemall](https://github.com/myui/hivemall) Scalable machine learning library for Hive/Hadoop.
		* [PyHive] (https://github.com/dropbox/PyHive) Python interface to Hive and Presto.
	* [Drill] (https://drill.apache.org/) Schema-free SQL Query Engine for Hadoop, NoSQL and Cloud Storage.

# Charts and Dashboards
* [Highcharts] (http://www.highcharts.com/) A charting library written in pure JavaScript, offering an easy way of adding interactive charts to your web site or web application.
* [ZingChart](http://www.zingchart.com/) Fast JavaScript charts for any data set.
* [C3.js](http://c3js.org) D3-based reusable chart library.
* [D3.js] (http://d3js.org/) A JavaScript library for manipulating documents based on data.
	* [D3Plus] (http://d3plus.org) D3's simplier, easier to use cousin. Mostly predefined templates that you can just plug data in.
* [SmoothieCharts](http://smoothiecharts.org) A JavaScript Charting Library for Streaming Data.
* [PyXley](https://github.com/stitchfix/pyxley) Python helpers for building dashboards using Flask and React

# Frameworks
* [Luigi] (https://github.com/spotify/luigi) Luigi is a Python module that helps you build complex pipelines of batch jobs.
	* [CronQ](https://github.com/seatgeek/cronq) An application cron-like system. [Used](http://chairnerd.seatgeek.com/building-out-the-seatgeek-data-pipeline/) w/Luige 
* [Cascading] (http://www.cascading.org/) Java based application development platform.
* [Airflow] (https://github.com/airbnb/airflow) Airflow is a system to programmaticaly author, schedule and monitor data pipelines.
* [Azkeban] (https://azkaban.github.io/) Azkaban is a batch workflow job scheduler created at LinkedIn to run Hadoop jobs. Azkaban resolves the ordering through job dependencies and provides an easy to use web user interface to maintain and track your workflows. 
* [Oozie](http://oozie.apache.org/) Oozie is a workflow scheduler system to manage Apache Hadoop jobs

# ELK Elastic Logstash Kebana
* [docker-logstash](https://github.com/pblittle/docker-logstash) A highly configurable logstash (1.4.4) docker image running Elasticsearch (1.7.0) and Kibana (3.1.2).
* [elasticsearch-jdbc](https://github.com/jprante/elasticsearch-jdbc) JDBC importer for Elasticsearch
* [ZomboDB](https://github.com/zombodb/zombodb) Postgres Extension that allows creating an index backed by Elasticsearch

# Docker
* [Gockerize](https://github.com/aerofs/gockerize) Package golang service into minimal docker containers
* [Flocker](https://github.com/ClusterHQ/flocker) Easily manage Docker containers & their data
* [Rancher](http://rancher.com/rancher-os/) RancherOS is a 20mb Linux distro that runs the entire OS as Docker containers
* [Kontena](http://www.kontena.io/) Application Containers for Masses
* [Weave](https://github.com/weaveworks/weave) Weaving Docker containers into applications http://weave.works
* [Zodiac](https://github.com/CenturyLinkLabs/zodiac) A lightweight tool for easy deployment and rollback of dockerized applications
* [cAdvisor](https://github.com/google/cadvisor) Analyzes resource usage and performance characteristics of running containers
* [Micro S3 persistence](https://github.com/shinymayhem/micro-s3-persistence) Docker microservice for saving/restoring volume data to S3
* [Dockup](https://github.com/tutumcloud/dockup) Docker image to backup/restore your Docker container volumes to AWS S3


# Datasets
## Realtime
* [Instagram Realtime](https://instagram.com/developer/realtime/) Real-time photo updates provide your application with instant notifications of new photos as they are posted on Instagram.
* [Twitter Realtime](https://dev.twitter.com/streaming/overview) The Streaming APIs give developers low latency access to Twitter’s global stream of Tweet data.
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
