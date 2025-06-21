# Awesome Data Engineering [![Awesome](https://awesome.re/badge-flat2.svg)](https://github.com/sindresorhus/awesome)

> A curated list of awesome things related to Data Engineering.

## Contents

- [Databases](#databases)
- [Data Comparison](#data-comparison)
- [Data Ingestion](#data-ingestion)
- [File System](#file-system)
- [Serialization format](#serialization-format)
- [Stream Processing](#stream-processing)
- [Batch Processing](#batch-processing)
- [Charts and Dashboards](#charts-and-dashboards)
- [Workflow](#workflow)
- [Data Lake Management](#data-lake-management)
- [ELK Elastic Logstash Kibana](#elk-elastic-logstash-kibana)
- [Docker](#docker)
- [Datasets](#datasets)
  - [Realtime](#realtime)
  - [Data Dumps](#data-dumps)
- [Monitoring](#monitoring)
  - [Prometheus](#prometheus)
- [Profiling](#profiling)
  - [Data Profiler](#data-profiler)
- [Testing](#testing)
- [Community](#community)
  - [Forums](#forums)
  - [Conferences](#conferences)
  - [Podcasts](#podcasts)
  - [Books](#books)

## Databases

- Relational
  - [RQLite](https://github.com/rqlite/rqlite) - Replicated SQLite using the Raft consensus protocol.
  - [MySQL](https://www.mysql.com/) - The world's most popular open source database.
    - [TiDB](https://github.com/pingcap/tidb) - TiDB is a distributed NewSQL database compatible with MySQL protocol.
    - [Percona XtraBackup](https://www.percona.com/software/mysql-database/percona-xtrabackup) - Percona XtraBackup is a free, open source, complete online backup solution for all versions of Percona Server, MySQL® and MariaDB®.
    - [mysql_utils](https://github.com/pinterest/mysql_utils) - Pinterest MySQL Management Tools.
  - [MariaDB](https://mariadb.org/) - An enhanced, drop-in replacement for MySQL.
  - [PostgreSQL](https://www.postgresql.org/) - The world's most advanced open source database.
  - [Amazon RDS](https://aws.amazon.com/rds/) - Amazon RDS makes it easy to set up, operate, and scale a relational database in the cloud.
  - [Crate.IO](https://crate.io/) - Scalable SQL database with the NOSQL goodies.
- Key-Value
  - [Redis](https://redis.io/) - An open source, BSD licensed, advanced key-value cache and store.
  - [Riak](https://docs.basho.com/riak/kv/) - A distributed database designed to deliver maximum data availability by distributing data across multiple servers.
  - [AWS DynamoDB](https://aws.amazon.com/dynamodb/) - A fast and flexible NoSQL database service for all applications that need consistent, single-digit millisecond latency at any scale.
  - [HyperDex](https://github.com/rescrv/HyperDex) - HyperDex is a scalable, searchable key-value store. Deprecated.
  - [SSDB](https://ssdb.io) - A high performance NoSQL database supporting many data structures, an alternative to Redis.
  - [Kyoto Tycoon](https://github.com/alticelabs/kyoto) - Kyoto Tycoon is a lightweight network server on top of the Kyoto Cabinet key-value database, built for high-performance and concurrency.
  - [IonDB](https://github.com/iondbproject/iondb) - A key-value store for microcontroller and IoT applications.
- Column
  - [Cassandra](https://cassandra.apache.org/) - The right choice when you need scalability and high availability without compromising performance.
    - [Cassandra Calculator](https://www.ecyrd.com/cassandracalculator/) - This simple form allows you to try out different values for your Apache Cassandra cluster and see what the impact is for your application.
    - [CCM](https://github.com/pcmanus/ccm) - A script to easily create and destroy an Apache Cassandra cluster on localhost.
    - [ScyllaDB](https://github.com/scylladb/scylla) - NoSQL data store using the seastar framework, compatible with Apache Cassandra.
  - [HBase](https://hbase.apache.org/) - The Hadoop database, a distributed, scalable, big data store.
  - [AWS Redshift](https://aws.amazon.com/redshift/) - A fast, fully managed, petabyte-scale data warehouse that makes it simple and cost-effective to analyze all your data using your existing business intelligence tools.
  - [FiloDB](https://github.com/filodb/FiloDB) - Distributed. Columnar. Versioned. Streaming. SQL.
  - [Vertica](https://www.vertica.com) - Distributed, MPP columnar database with extensive analytics SQL.
  - [ClickHouse](https://clickhouse.tech) - Distributed columnar DBMS for OLAP. SQL.
- Document
  - [MongoDB](https://www.mongodb.com) - An open-source, document database designed for ease of development and scaling.
    - [Percona Server for MongoDB](https://www.percona.com/software/mongo-database/percona-server-for-mongodb) - Percona Server for MongoDB® is a free, enhanced, fully compatible, open source, drop-in replacement for the MongoDB® Community Edition that includes enterprise-grade features and functionality.
    - [MemDB](https://github.com/rain1017/memdb) - Distributed Transactional In-Memory Database (based on MongoDB).
  - [Elasticsearch](https://www.elastic.co/) - Search & Analyze Data in Real Time.
  - [Couchbase](https://www.couchbase.com/) - The highest performing NoSQL distributed database.
  - [RethinkDB](https://rethinkdb.com/) - The open-source database for the realtime web.
  - [RavenDB](https://ravendb.net/) - Fully Transactional NoSQL Document Database.
- Graph
  - [Neo4j](https://neo4j.com/) - The world's leading graph database.
  - [OrientDB](https://orientdb.com) - 2nd Generation Distributed Graph Database with the flexibility of Documents in one product with an Open Source commercial friendly license.
  - [ArangoDB](https://www.arangodb.com/) - A distributed free and open-source database with a flexible data model for documents, graphs, and key-values.
  - [Titan](https://titan.thinkaurelius.com) - A scalable graph database optimized for storing and querying graphs containing hundreds of billions of vertices and edges distributed across a multi-machine cluster.
  - [FlockDB](https://github.com/twitter-archive/flockdb) - A distributed, fault-tolerant graph database by Twitter. Deprecated.
- Distributed
  - [DAtomic](https://www.datomic.com) - The fully transactional, cloud-ready, distributed database.
  - [Apache Geode](https://geode.apache.org/) - An open source, distributed, in-memory database for scale-out applications.
  - [Gaffer](https://github.com/gchq/Gaffer) - A large-scale graph database.
- Timeseries
  - [InfluxDB](https://github.com/influxdata/influxdb) - Scalable datastore for metrics, events, and real-time analytics.
  - [OpenTSDB](https://github.com/OpenTSDB/opentsdb) - A scalable, distributed Time Series Database.
  - [QuestDB](https://questdb.io/) - A relational column-oriented database designed for real-time analytics on time series and event data.
  - [kairosdb](https://github.com/kairosdb/kairosdb) - Fast scalable time series database.
  - [Heroic](https://github.com/spotify/heroic) - A scalable time series database based on Cassandra and Elasticsearch, by Spotify.
  - [Druid](https://github.com/apache/incubator-druid) - Column oriented distributed data store ideal for powering interactive applications.
  - [Riak-TS](https://basho.com/products/riak-ts/) - Riak TS is the only enterprise-grade NoSQL time series database optimized specifically for IoT and Time Series data.
  - [Akumuli](https://github.com/akumuli/Akumuli) - Akumuli is a numeric time-series database. It can be used to capture, store and process time-series data in real-time. The word "akumuli" can be translated from esperanto as "accumulate".
  - [Rhombus](https://github.com/Pardot/Rhombus) - A time-series object store for Cassandra that handles all the complexity of building wide row indexes.
  - [Dalmatiner DB](https://github.com/dalmatinerdb/dalmatinerdb) - Fast distributed metrics database.
  - [Blueflood](https://github.com/rackerlabs/blueflood) - A distributed system designed to ingest and process time series data.
  - [Timely](https://github.com/NationalSecurityAgency/timely) - Timely is a time series database application that provides secure access to time series data based on Accumulo and Grafana.
- Other
  - [Tarantool](https://github.com/tarantool/tarantool/) - Tarantool is an in-memory database and application server.
  - [GreenPlum](https://github.com/greenplum-db/gpdb) - The Greenplum Database (GPDB) - An advanced, fully featured, open source data warehouse. It provides powerful and rapid analytics on petabyte scale data volumes.
  - [cayley](https://github.com/cayleygraph/cayley) - An open-source graph database. Google.
  - [Snappydata](https://github.com/SnappyDataInc/snappydata) - SnappyData: OLTP + OLAP Database built on Apache Spark.
  - [TimescaleDB](https://www.timescale.com/) - Built as an extension on top of PostgreSQL, TimescaleDB is a time-series SQL database providing fast analytics, scalability, with automated data management on a proven storage engine.
  - [DuckDB](https://duckdb.org/) - DuckDB is a fast in-process analytical database that has zero external dependencies, runs on Linux/macOS/Windows, offers a rich SQL dialect, and is free and extensible.

## Data Comparison

- [datacompy](https://github.com/capitalone/datacompy) - DataComPy is a Python library that facilitates the comparison of two DataFrames in pandas, Polars, Spark and more. The library goes beyond basic equality checks by providing detailed insights into discrepancies at both row and column levels.

## Data Ingestion

- [Kafka](https://kafka.apache.org/) - Publish-subscribe messaging rethought as a distributed commit log.
  - [BottledWater](https://github.com/confluentinc/bottledwater-pg) - Change data capture from PostgreSQL into Kafka. Deprecated.
  - [kafkat](https://github.com/airbnb/kafkat) - Simplified command-line administration for Kafka brokers.
  - [kafkacat](https://github.com/edenhill/kafkacat) - Generic command line non-JVM Apache Kafka producer and consumer.
  - [pg-kafka](https://github.com/xstevens/pg_kafka) - A PostgreSQL extension to produce messages to Apache Kafka.
  - [librdkafka](https://github.com/edenhill/librdkafka) - The Apache Kafka C/C++ library.
  - [kafka-docker](https://github.com/wurstmeister/kafka-docker) - Kafka in Docker.
  - [kafka-manager](https://github.com/yahoo/kafka-manager) - A tool for managing Apache Kafka.
  - [kafka-node](https://github.com/SOHU-Co/kafka-node) - Node.js client for Apache Kafka 0.8.
  - [Secor](https://github.com/pinterest/secor) - Pinterest's Kafka to S3 distributed consumer.
  - [Kafka-logger](https://github.com/uber/kafka-logger) - Kafka-winston logger for Node.js from Uber.
- [AWS Kinesis](https://aws.amazon.com/kinesis/) - A fully managed, cloud-based service for real-time data processing over large, distributed data streams.
- [RabbitMQ](https://www.rabbitmq.com/) - Robust messaging for applications.
- [dlt](https://www.dlthub.com) - A fast&simple pipeline building library for python data devs, runs in notebooks, cloud functions, airflow, etc.
- [FluentD](https://www.fluentd.org) - An open source data collector for unified logging layer.
- [Embulk](https://www.embulk.org) - An open source bulk data loader that helps data transfer between various databases, storages, file formats, and cloud services.
- [Apache Sqoop](https://sqoop.apache.org) - A tool designed for efficiently transferring bulk data between Apache Hadoop and structured datastores such as relational databases.
- [Heka](https://github.com/mozilla-services/heka) - Data Acquisition and Processing Made Easy. Deprecated.
- [Gobblin](https://github.com/apache/incubator-gobblin) - Universal data ingestion framework for Hadoop from LinkedIn.
- [Nakadi](https://nakadi.io) - Nakadi is an open source event messaging platform that provides a REST API on top of Kafka-like queues.
- [Pravega](https://www.pravega.io) - Pravega provides a new storage abstraction - a stream - for continuous and unbounded data.
- [Apache Pulsar](https://pulsar.apache.org/) - Apache Pulsar is an open-source distributed pub-sub messaging system.
- [AWS Data Wrangler](https://github.com/awslabs/aws-data-wrangler) - Utility belt to handle data on AWS.
- [Airbyte](https://airbyte.io/) - Open-source data integration for modern data teams.
- [Artie](https://www.artie.com/) - Real-time data ingestion tool leveraging change data capture.
- [Sling](https://slingdata.io/) - Sling is CLI data integration tool specialized in moving data between databases, as well as storage systems.
- [Meltano](https://meltano.com/) - CLI & code-first ELT.
  - [Singer SDK](https://sdk.meltano.com) - The fastest way to build custom data extractors and loaders compliant with the Singer Spec.
- [Google Sheets ETL](https://github.com/fulldecent/google-sheets-etl) - Live import all your Google Sheets to your data warehouse.
- [CsvPath Framework](https://www.csvpath.org/) - A delimited data preboarding framework that fills the gap between MFT and the data lake.

## File System

- [HDFS](https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-hdfs/HdfsDesign.html) - A distributed file system designed to run on commodity hardware.
  - [Snakebite](https://github.com/spotify/snakebite) - A pure python HDFS client.
- [AWS S3](https://aws.amazon.com/s3/) - Object storage built to retrieve any amount of data from anywhere.
  - [smart_open](https://github.com/RaRe-Technologies/smart_open) - Utils for streaming large files (S3, HDFS, gzip, bz2).
- [Alluxio](https://www.alluxio.org/) - Alluxio is a memory-centric distributed storage system enabling reliable data sharing at memory-speed across cluster frameworks, such as Spark and MapReduce.
- [CEPH](https://ceph.com/) - Ceph is a unified, distributed storage system designed for excellent performance, reliability, and scalability.
- [JuiceFS](https://github.com/juicedata/juicefs) - JuiceFS is a high-performance Cloud-Native file system driven by object storage for large-scale data storage.
- [OrangeFS](https://www.orangefs.org/) - Orange File System is a branch of the Parallel Virtual File System.
- [SnackFS](https://github.com/tuplejump/snackfs-release) - SnackFS is our bite-sized, lightweight HDFS compatible file system built over Cassandra.
- [GlusterFS](https://www.gluster.org/) - Gluster Filesystem.
- [XtreemFS](https://www.xtreemfs.org/) - Fault-tolerant distributed file system for all storage needs.
- [SeaweedFS](https://github.com/chrislusf/seaweedfs) - Seaweed-FS is a simple and highly scalable distributed file system. There are two objectives: to store billions of files! to serve the files fast! Instead of supporting full POSIX file system semantics, Seaweed-FS choose to implement only a key~file mapping. Similar to the word "NoSQL", you can call it as "NoFS".
- [S3QL](https://github.com/s3ql/s3ql/) - S3QL is a file system that stores all its data online using storage services like Google Storage, Amazon S3, or OpenStack.
- [LizardFS](https://lizardfs.com/) - LizardFS Software Defined Storage is a distributed, parallel, scalable, fault-tolerant, Geo-Redundant and highly available file system.

## Serialization format

- [Apache Avro](https://avro.apache.org) - Apache Avro™ is a data serialization system.
- [Apache Parquet](https://parquet.apache.org) - Apache Parquet is a columnar storage format available to any project in the Hadoop ecosystem, regardless of the choice of data processing framework, data model or programming language.
  - [Snappy](https://github.com/google/snappy) - A fast compressor/decompressor. Used with Parquet.
  - [PigZ](https://zlib.net/pigz/) - A parallel implementation of gzip for modern multi-processor, multi-core machines.
- [Apache ORC](https://orc.apache.org/) - The smallest, fastest columnar storage for Hadoop workloads.
- [Apache Thrift](https://thrift.apache.org) - The Apache Thrift software framework, for scalable cross-language services development.
- [ProtoBuf](https://github.com/protocolbuffers/protobuf) - Protocol Buffers - Google's data interchange format.
- [SequenceFile](https://wiki.apache.org/hadoop/SequenceFile) - SequenceFile is a flat file consisting of binary key/value pairs. It is extensively used in MapReduce as input/output formats.
- [Kryo](https://github.com/EsotericSoftware/kryo) - Kryo is a fast and efficient object graph serialization framework for Java.

## Stream Processing

- [Apache Beam](https://beam.apache.org/) - Apache Beam is a unified programming model that implements both batch and streaming data processing jobs that run on many execution engines.
- [Spark Streaming](https://spark.apache.org/streaming/) - Spark Streaming makes it easy to build scalable fault-tolerant streaming applications.
- [Apache Flink](https://flink.apache.org/) - Apache Flink is a streaming dataflow engine that provides data distribution, communication, and fault tolerance for distributed computations over data streams.
- [Apache Storm](https://storm.apache.org) - Apache Storm is a free and open source distributed realtime computation system.
- [Apache Samza](https://samza.apache.org) - Apache Samza is a distributed stream processing framework.
- [Apache NiFi](https://nifi.apache.org/) - An easy to use, powerful, and reliable system to process and distribute data.
- [Apache Hudi](https://hudi.apache.org/) - An open source framework for managing storage for real time processing, one of the most interesting feature is the Upsert.
- [CocoIndex](https://github.com/cocoindex-io/cocoindex) - An open source ETL framework to build fresh index for AI. 
- [VoltDB](https://voltdb.com/) - VoltDb is an ACID-compliant RDBMS which uses a [shared nothing architecture](https://en.wikipedia.org/wiki/Shared-nothing_architecture).
- [PipelineDB](https://github.com/pipelinedb/pipelinedb) - The Streaming SQL Database.
- [Spring Cloud Dataflow](https://cloud.spring.io/spring-cloud-dataflow/) - Streaming and tasks execution between Spring Boot apps.
- [Bonobo](https://www.bonobo-project.org/) - Bonobo is a data-processing toolkit for python 3.5+.
- [Robinhood's Faust](https://github.com/faust-streaming/faust) - Forever scalable event processing & in-memory durable K/V store as a library with asyncio & static typing.
- [HStreamDB](https://github.com/hstreamdb/hstream) - The streaming database built for IoT data storage and real-time processing.
- [Kuiper](https://github.com/emqx/kuiper) - An edge lightweight IoT data analytics/streaming software implemented by Golang, and it can be run at all kinds of resource-constrained edge devices.
- [Zilla](https://github.com/aklivity/zilla) - - An API gateway built for event-driven architectures and streaming that supports standard protocols such as HTTP, SSE, gRPC, MQTT, and the native Kafka protocol.
- [SwimOS](https://github.com/swimos/swim-rust) - A framework for building real-time streaming data processing applications that supports a wide range of ingestion sources.

## Batch Processing

- [Hadoop MapReduce](https://hadoop.apache.org/docs/current/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html) - Hadoop MapReduce is a software framework for easily writing applications which process vast amounts of data (multi-terabyte data-sets) - in-parallel on large clusters (thousands of nodes) - of commodity hardware in a reliable, fault-tolerant manner.
- [Spark](https://spark.apache.org/) - A multi-language engine for executing data engineering, data science, and machine learning on single-node machines or clusters.
  - [Spark Packages](https://spark-packages.org) - A community index of packages for Apache Spark.
  - [Deep Spark](https://github.com/Stratio/deep-spark) - Connecting Apache Spark with different data stores. Deprecated.
  - [Spark RDD API Examples](https://homepage.cs.latrobe.edu.au/zhe/ZhenHeSparkRDDAPIExamples.html) - Examples by Zhen He.
  - [Livy](https://livy.incubator.apache.org) - The REST Spark Server.
  - [Delight](https://github.com/datamechanics/delight) - A free & cross platform monitoring tool (Spark UI / Spark History Server alternative).
- [AWS EMR](https://aws.amazon.com/emr/) - A web service that makes it easy to quickly and cost-effectively process vast amounts of data.
- [Data Mechanics](https://www.datamechanics.co) - A cloud-based platform deployed on Kubernetes making Apache Spark more developer-friendly and cost-effective.
- [Tez](https://tez.apache.org/) - An application framework which allows for a complex directed-acyclic-graph of tasks for processing data.
- [Bistro](https://github.com/asavinov/bistro) - A light-weight engine for general-purpose data processing including both batch and stream analytics. It is based on a novel unique data model, which represents data via _functions_ and processes data via _columns operations_ as opposed to having only set operations in conventional approaches like MapReduce or SQL.
- [Substation](https://github.com/brexhq/substation) - Substation is a cloud native data pipeline and transformation toolkit written in Go.
- Batch ML
  - [H2O](https://www.h2o.ai/) - Fast scalable machine learning API for smarter applications.
  - [Mahout](https://mahout.apache.org/) - An environment for quickly creating scalable performant machine learning applications.
  - [Spark MLlib](https://spark.apache.org/docs/latest/ml-guide.html) - Spark's scalable machine learning library consisting of common learning algorithms and utilities, including classification, regression, clustering, collaborative filtering, dimensionality reduction, as well as underlying optimization primitives.
- Batch Graph
  - [GraphLab Create](https://turi.com/products/create/docs/) - A machine learning platform that enables data scientists and app developers to easily create intelligent apps at scale.
  - [Giraph](https://giraph.apache.org/) - An iterative graph processing system built for high scalability.
  - [Spark GraphX](https://spark.apache.org/graphx/) - Apache Spark's API for graphs and graph-parallel computation.
- Batch SQL
  - [Presto](https://prestodb.github.io/docs/current/index.html) - A distributed SQL query engine designed to query large data sets distributed over one or more heterogeneous data sources.
  - [Hive](https://hive.apache.org) - Data warehouse software facilitates querying and managing large datasets residing in distributed storage.
    - [Hivemall](https://github.com/apache/incubator-hivemall) - Scalable machine learning library for Hive/Hadoop.
    - [PyHive](https://github.com/dropbox/PyHive) - Python interface to Hive and Presto.
  - [Drill](https://drill.apache.org/) - Schema-free SQL Query Engine for Hadoop, NoSQL and Cloud Storage.

## Charts and Dashboards

- [Highcharts](https://www.highcharts.com/) - A charting library written in pure JavaScript, offering an easy way of adding interactive charts to your web site or web application.
- [ZingChart](https://www.zingchart.com/) - Fast JavaScript charts for any data set.
- [C3.js](https://c3js.org) - D3-based reusable chart library.
- [D3.js](https://d3js.org/) - A JavaScript library for manipulating documents based on data.
  - [D3Plus](https://d3plus.org) - D3's simpler, easier to use cousin. Mostly predefined templates that you can just plug data in.
- [SmoothieCharts](https://smoothiecharts.org) - A JavaScript Charting Library for Streaming Data.
- [PyXley](https://github.com/stitchfix/pyxley) - Python helpers for building dashboards using Flask and React.
- [Plotly](https://github.com/plotly/dash) - Flask, JS, and CSS boilerplate for interactive, web-based visualization apps in Python.
- [Apache Superset](https://github.com/apache/incubator-superset) - Apache Superset (incubating) - A modern, enterprise-ready business intelligence web application.
- [Redash](https://redash.io/) - Make Your Company Data Driven. Connect to any data source, easily visualize and share your data.
- [Metabase](https://github.com/metabase/metabase) - Metabase is the easy, open source way for everyone in your company to ask questions and learn from data.
- [PyQtGraph](https://www.pyqtgraph.org/) - PyQtGraph is a pure-python graphics and GUI library built on PyQt4 / PySide and numpy. It is intended for use in mathematics / scientific / engineering applications.
- [Seaborn](https://seaborn.pydata.org) - A Python visualization library based on matplotlib. It provides a high-level interface for drawing attractive statistical graphics.

## Workflow

- [Luigi](https://github.com/spotify/luigi) - Luigi is a Python module that helps you build complex pipelines of batch jobs.
- [CronQ](https://github.com/seatgeek/cronq) - An application cron-like system. [Used](https://chairnerd.seatgeek.com/building-out-the-seatgeek-data-pipeline/) w/Luige. Deprecated.
- [Cascading](https://www.cascading.org/) - Java based application development platform.
- [Airflow](https://github.com/apache/airflow) - Airflow is a system to programmatically author, schedule, and monitor data pipelines.
- [Azkaban](https://azkaban.github.io/) - Azkaban is a batch workflow job scheduler created at LinkedIn to run Hadoop jobs. Azkaban resolves the ordering through job dependencies and provides an easy-to-use web user interface to maintain and track your workflows.
- [Oozie](https://oozie.apache.org/) - Oozie is a workflow scheduler system to manage Apache Hadoop jobs.
- [Pinball](https://github.com/pinterest/pinball) - DAG based workflow manager. Job flows are defined programmatically in Python. Support output passing between jobs.
- [Dagster](https://github.com/dagster-io/dagster) - Dagster is an open-source Python library for building data applications.
- [Hamilton](https://github.com/dagworks-inc/hamilton) - Hamilton is a lightweight library to define data transformations as a directed-acyclic graph (DAG). If you like dbt for SQL transforms, you will like Hamilton for Python processing.
- [Kedro](https://kedro.readthedocs.io/en/latest/) - Kedro is a framework that makes it easy to build robust and scalable data pipelines by providing uniform project templates, data abstraction, configuration and pipeline assembly.
- [Dataform](https://dataform.co/) - An open-source framework and web based IDE to manage datasets and their dependencies. SQLX extends your existing SQL warehouse dialect to add features that support dependency management, testing, documentation and more.
- [Census](https://getcensus.com/) - A reverse-ETL tool that let you sync data from your cloud data warehouse to SaaS applications like Salesforce, Marketo, HubSpot, Zendesk, etc. No engineering favors required—just SQL.
- [dbt](https://getdbt.com/) - A command line tool that enables data analysts and engineers to transform data in their warehouses more effectively.
- [Kestra](https://kestra.io/) - Scalable, event-driven, language-agnostic orchestration and scheduling platform to manage millions of workflows declaratively in code.
- [RudderStack](https://github.com/rudderlabs/rudder-server) - A warehouse-first Customer Data Platform that enables you to collect data from every application, website and SaaS platform, and then activate it in your warehouse and business tools.
- [PACE](https://github.com/getstrm/pace) - An open source framework that allows you to enforce agreements on how data should be accessed, used, and transformed, regardless of the data platform (Snowflake, BigQuery, DataBricks, etc.)
- [Prefect](https://prefect.io/) - Prefect is an orchestration and observability platform. With it, developers can rapidly build and scale resilient code, and triage disruptions effortlessly.
- [Multiwoven](https://github.com/Multiwoven/multiwoven) - The open-source reverse ETL, data activation platform for modern data teams.
- [SuprSend](https://www.suprsend.com/products/workflows) - Create automated workflows and logic using API's for your notification service. Add templates, batching, preferences, inapp inbox with workflows to trigger notifications directly from your data warehouse.
- [Kestra](https://github.com/kestra-io/kestra) - A versatile open source orchestrator and scheduler built on Java, designed to handle a broad range of workflows with a language-agnostic, API-first architecture.
- [Mage](https://www.mage.ai) - Open-source data pipeline tool for transforming and integrating data.

## Data Lake Management

- [lakeFS](https://github.com/treeverse/lakeFS) - lakeFS is an open source platform that delivers resilience and manageability to object-storage based data lakes.
- [Project Nessie](https://github.com/projectnessie/nessie) - Project Nessie is a Transactional Catalog for Data Lakes with Git-like semantics. Works with Apache Iceberg tables.
- [Ilum](https://ilum.cloud/) - Ilum is a modular Data Lakehouse platform that simplifies the management and monitoring of Apache Spark clusters across Kubernetes and Hadoop environments.
- [Gravitino](https://github.com/apache/gravitino) - Gravitino is an open-source, unified metadata management for data lakes, data warehouses, and external catalogs. 

## ELK Elastic Logstash Kibana

- [docker-logstash](https://github.com/pblittle/docker-logstash) - A highly configurable Logstash (1.4.4) - Docker image running Elasticsearch (1.7.0) - and Kibana (3.1.2).
- [elasticsearch-jdbc](https://github.com/jprante/elasticsearch-jdbc) - JDBC importer for Elasticsearch.
- [ZomboDB](https://github.com/zombodb/zombodb) - Postgres Extension that allows creating an index backed by Elasticsearch.

## Docker

- [Gockerize](https://github.com/redbooth/gockerize) - Package golang service into minimal Docker containers.
- [Flocker](https://github.com/ClusterHQ/flocker) - Easily manage Docker containers & their data.
- [Rancher](https://rancher.com/rancher-os/) - RancherOS is a 20mb Linux distro that runs the entire OS as Docker containers.
- [Kontena](https://www.kontena.io/) - Application Containers for Masses.
- [Weave](https://github.com/weaveworks/weave) - Weaving Docker containers into applications.
- [Zodiac](https://github.com/CenturyLinkLabs/zodiac) - A lightweight tool for easy deployment and rollback of dockerized applications.
- [cAdvisor](https://github.com/google/cadvisor) - Analyzes resource usage and performance characteristics of running containers.
- [Micro S3 persistence](https://github.com/figadore/micro-s3-persistence) - Docker microservice for saving/restoring volume data to S3.
- [Rocker-compose](https://github.com/grammarly/rocker-compose) - Docker composition tool with idempotency features for deploying apps composed of multiple containers. Deprecated.
- [Nomad](https://github.com/hashicorp/nomad) - Nomad is a cluster manager, designed for both long-lived services and short-lived batch processing workloads.
- [ImageLayers](https://imagelayers.io/) - Visualize Docker images and the layers that compose them.

## Datasets

### Realtime

- [Twitter Realtime](https://developer.twitter.com/en/docs/tweets/filter-realtime/overview) - The Streaming APIs give developers low latency access to Twitter's global stream of Tweet data.
- [Eventsim](https://github.com/Interana/eventsim) - Event data simulator. Generates a stream of pseudo-random events from a set of users, designed to simulate web traffic.
- [Reddit](https://www.reddit.com/r/datasets/comments/3mk1vg/realtime_data_is_available_including_comments/) - Real-time data is available including comments, submissions and links posted to reddit.

### Data Dumps

- [GitHub Archive](https://www.gharchive.org/) - GitHub's public timeline since 2011, updated every hour.
- [Common Crawl](https://commoncrawl.org/) - Open source repository of web crawl data.
- [Wikipedia](https://dumps.wikimedia.org/enwiki/latest/) - Wikipedia's complete copy of all wikis, in the form of Wikitext source and metadata embedded in XML. A number of raw database tables in SQL form are also available.

## Monitoring

### Prometheus

- [Prometheus.io](https://github.com/prometheus/prometheus) - An open-source service monitoring system and time series database.
- [HAProxy Exporter](https://github.com/prometheus/haproxy_exporter) - Simple server that scrapes HAProxy stats and exports them via HTTP for Prometheus consumption.

## Profiling

### Data Profiler
- [Data Profiler](https://github.com/capitalone/dataprofiler) - The DataProfiler is a Python library designed to make data analysis, monitoring, and sensitive data detection easy.


## Testing

- [Grai](https://github.com/grai-io/grai-core/) - A data catalog tool that integrates into your CI system exposing downstream impact testing of data changes. These tests prevent data changes which might break data pipelines or BI dashboards from making it to production.
- [DQOps](https://github.com/dqops/dqo) - An open-source data quality platform for the whole data platform lifecycle from profiling new data sources to applying full automation of data quality monitoring.
- [DataKitchen](https://datakitchen.io/) -  Open Source Data Observability for end-to-end Data Journey Observability, data profiling, anomaly detection, and auto-created data quality validation tests.
- [RunSQL](https://runsql.com/) - Free online SQL playground for MySQL, PostgreSQL, and SQL Server. Create database structures, run queries, and share results instantly.

## Community

### Forums

- [/r/dataengineering](https://www.reddit.com/r/dataengineering/) - News, tips, and background on Data Engineering.
- [/r/etl](https://www.reddit.com/r/ETL/) - Subreddit focused on ETL.

### Conferences

- [Data Council](https://www.datacouncil.ai/about) - Data Council is the first technical conference that bridges the gap between data scientists, data engineers and data analysts.

### Podcasts

- [Data Engineering Podcast](https://www.dataengineeringpodcast.com/) - The show about modern data infrastructure.
- [The Data Stack Show](https://datastackshow.com/) - A show where they talk to data engineers, analysts, and data scientists about their experience around building and maintaining data infrastructure, delivering data and data products, and driving better outcomes across their businesses with data.

### Books

- [Snowflake Data Engineering](https://www.manning.com/books/snowflake-data-engineering) - A practical introduction to data engineering on the Snowflake cloud data platform.
- [Best Data Science Books](https://www.appliedaicourse.com/blog/data-science-books/) - This blog offers a curated list of top data science books, categorized by topics and learning stages, to aid readers in building foundational knowledge and staying updated with industry trends.
