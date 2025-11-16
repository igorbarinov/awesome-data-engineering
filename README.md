# Awesome Data Engineering

A curated list of data engineering tools for software developers. [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Organized by the **data lifecycle** - from ingestion to insights. Each tool is chosen for production readiness, active maintenance, and real-world impact.

> Last updated: November 2024

## Contents

- [Data Ingestion](#data-ingestion)
- [Data Storage](#data-storage)
  - [Relational Databases](#relational-databases)
  - [Key-Value Stores](#key-value-stores)
  - [Wide-Column Stores](#wide-column-stores)
  - [Document Databases](#document-databases)
  - [Graph Databases](#graph-databases)
  - [Time-Series Databases](#time-series-databases)
  - [Cloud Data Warehouses](#cloud-data-warehouses)
  - [Data Lakes & Lakehouses](#data-lakes--lakehouses)
  - [File Systems](#file-systems)
  - [Serialization Formats](#serialization-formats)
- [Data Transformation](#data-transformation)
- [Orchestration & Workflow](#orchestration--workflow)
- [Stream Processing](#stream-processing)
- [Batch Processing](#batch-processing)
- [Data Quality & Observability](#data-quality--observability)
- [Data Discovery & Governance](#data-discovery--governance)
- [Reverse ETL](#reverse-etl)
- [Analytics & Visualization](#analytics--visualization)
- [Infrastructure & Deployment](#infrastructure--deployment)
- [Learning Resources](#learning-resources)

---

## Data Ingestion

Build robust data pipelines to move data from sources to destinations.

**Modern ELT Platforms**
* [Airbyte](https://airbyte.com/) - Open-source ELT platform with 600+ connectors. Production-ready 1.0 released September 2024.
* [Meltano](https://meltano.com/) - Open-source ELT built on Singer taps and targets. Strong orchestration and CLI-first workflow.
* [dlt](https://dlthub.com/) - Python library for building custom data pipelines with automatic schema inference and evolution.
* [Fivetran](https://www.fivetran.com/) - Fully managed ELT with 400+ connectors. Merged with dbt in 2024 for integrated transformation.

**Message Queues & Streaming Ingestion**
* [Apache Kafka](https://kafka.apache.org/) - Distributed event streaming platform. De facto standard used by 100,000+ organizations.
  * [Kafka Connect](https://docs.confluent.io/platform/current/connect/index.html) - Framework for connecting Kafka with external systems.
  * [Camus](https://github.com/linkedin/camus) - LinkedIn's Kafka to HDFS pipeline.
  * [BottledWater](https://github.com/confluentinc/bottledwater-pg) - Change data capture from PostgreSQL into Kafka.
  * [kafkat](https://github.com/airbnb/kafkat) - Simplified command-line admin for Kafka brokers by Airbnb.
  * [kafkacat](https://github.com/edenhill/kafkacat) - Generic non-JVM Kafka producer and consumer CLI.
  * [librdkafka](https://github.com/edenhill/librdkafka) - Apache Kafka C/C++ library.
  * [kafka-docker](https://github.com/wurstmeister/kafka-docker) - Kafka in Docker.
  * [kafka-manager](https://github.com/yahoo/kafka-manager) - Tool for managing Apache Kafka by Yahoo.
  * [Secor](https://github.com/pinterest/secor) - Pinterest's Kafka to S3 distributed consumer.
* [Redpanda](https://redpanda.com/) - Kafka-compatible streaming platform written in C++. Claims 10x performance improvement.
* [AWS Kinesis](https://aws.amazon.com/kinesis/) - Fully managed real-time data streaming service for AWS.
* [RabbitMQ](https://www.rabbitmq.com/) - Robust messaging broker for applications.
* [Apache Pulsar](https://pulsar.apache.org/) - Cloud-native distributed messaging and streaming platform with multi-tenancy.

**Data Transfer & Migration**
* [FluentD](https://www.fluentd.org/) - Open-source data collector for unified logging layer.
* [Embulk](https://www.embulk.org/) - Open-source bulk data loader for transferring data between databases, storages, file formats, and cloud services.
* [Apache Sqoop](https://sqoop.apache.org/) - Tool for bulk data transfer between Apache Hadoop and relational databases.
* [Gobblin](https://github.com/apache/gobblin) - Universal data ingestion framework for Hadoop from LinkedIn.

---

## Data Storage

### Relational Databases

* [PostgreSQL](https://www.postgresql.org/) - Advanced open-source relational database with strong ACID compliance and extensibility.
* [MySQL](https://www.mysql.com/) - World's most popular open-source database. Default choice for web applications.
  * [TiDB](https://github.com/pingcap/tidb) - Distributed NewSQL database compatible with MySQL protocol.
  * [Percona XtraBackup](https://www.percona.com/software/mysql-database/percona-xtrabackup) - Free, open-source, complete online backup for Percona Server, MySQL, and MariaDB.
  * [mysql_utils](https://github.com/pinterest/mysql_utils) - Pinterest MySQL management tools.
* [MariaDB](https://mariadb.org/) - Enhanced, drop-in replacement for MySQL.
* [RQLite](https://github.com/rqlite/rqlite) - Lightweight distributed relational database using SQLite and Raft consensus protocol.
* [Amazon RDS](https://aws.amazon.com/rds/) - Managed relational database service supporting PostgreSQL, MySQL, MariaDB, Oracle, and SQL Server.
* [CockroachDB](https://www.cockroachlabs.com/) - Distributed SQL database built for cloud-native applications with PostgreSQL compatibility.

### Key-Value Stores

* [Redis](https://redis.io/) - In-memory data structure store used as database, cache, and message broker. Sub-millisecond latency.
* [AWS DynamoDB](https://aws.amazon.com/dynamodb/) - Fully managed NoSQL database with single-digit millisecond performance at any scale.
* [Riak](https://riak.com/) - Distributed database delivering maximum availability by distributing data across multiple servers.
* [etcd](https://etcd.io/) - Distributed key-value store for distributed systems coordination. Used by Kubernetes.
* [SSDB](http://ssdb.io/) - High-performance NoSQL database supporting many data structures. Alternative to Redis with disk persistence.
* [Kyoto Tycoon](https://github.com/alticelabs/kyoto) - Lightweight network server on Kyoto Cabinet key-value database. Built for high concurrency.

### Wide-Column Stores

* [Apache Cassandra](https://cassandra.apache.org/) - Distributed NoSQL database for handling large amounts of data with high availability and no single point of failure.
  * [CCM](https://github.com/riptano/ccm) - Script to easily create and destroy Cassandra clusters on localhost.
  * [ScyllaDB](https://www.scylladb.com/) - NoSQL database compatible with Cassandra. Written in C++ for better performance.
* [Apache HBase](https://hbase.apache.org/) - Distributed, scalable big data store. The Hadoop database.
* [AWS Redshift](https://aws.amazon.com/redshift/) - Fast, fully managed, petabyte-scale data warehouse service.
* [Google BigQuery](https://cloud.google.com/bigquery) - Serverless, highly scalable data warehouse with built-in machine learning.
* [ClickHouse](https://clickhouse.com/) - Open-source column-oriented DBMS for real-time analytics with millisecond query latency.
* [Apache Druid](https://druid.apache.org/) - Real-time analytics database for fast slice-and-dice analytics on large datasets.

### Document Databases

* [MongoDB](https://www.mongodb.com/) - Document database designed for ease of development and scaling. JSON-like documents.
  * [Percona Server for MongoDB](https://www.percona.com/software/mongodb/percona-server-for-mongodb) - Enhanced, fully compatible, drop-in replacement for MongoDB with enterprise features.
  * [MemDB](https://github.com/rain1017/memdb) - Distributed transactional in-memory database based on MongoDB.
* [Elasticsearch](https://www.elastic.co/) - Distributed search and analytics engine. Built on Apache Lucene.
* [Couchbase](https://www.couchbase.com/) - Distributed NoSQL cloud database with built-in caching for sub-millisecond data operations.
* [RethinkDB](https://rethinkdb.com/) - Open-source database for real-time web applications. Push JSON to apps in realtime.
* [CouchDB](https://couchdb.apache.org/) - Database that uses JSON for documents and JavaScript for queries. Built for offline-first apps.

### Graph Databases

* [Neo4j](https://neo4j.com/) - Native graph database for connected data. Uses Cypher query language.
* [ArangoDB](https://www.arangodb.com/) - Multi-model database supporting documents, graphs, and key-values in one engine.
* [OrientDB](https://orientdb.org/) - Multi-model database combining graph and document models with SQL support.
* [Amazon Neptune](https://aws.amazon.com/neptune/) - Fully managed graph database supporting Property Graph and RDF.
* [Apache TinkerPop](https://tinkerpop.apache.org/) - Graph computing framework for graph databases and analytics.
* [JanusGraph](https://janusgraph.org/) - Scalable graph database optimized for storing and querying graphs with billions of vertices and edges.

### Time-Series Databases

* [InfluxDB](https://www.influxdata.com/) - Purpose-built time-series database for metrics, events, and real-time analytics.
* [TimescaleDB](https://www.timescale.com/) - PostgreSQL extension for time-series data. Provides automatic partitioning and optimized queries.
* [OpenTSDB](https://github.com/OpenTSDB/opentsdb) - Scalable, distributed time-series database built on HBase.
* [KairosDB](https://github.com/kairosdb/kairosdb) - Fast, scalable time-series database built on Cassandra.
* [Prometheus](https://prometheus.io/) - Open-source monitoring system with time-series database. Pull-based metrics collection.
* [Graphite](https://graphiteapp.org/) - Enterprise-ready monitoring tool storing numeric time-series data.
* [QuestDB](https://questdb.io/) - High-performance time-series database with SQL support and InfluxDB line protocol compatibility.
* [VictoriaMetrics](https://victoriametrics.com/) - Fast, cost-effective monitoring solution and time-series database.

### Cloud Data Warehouses

Modern cloud-native data warehouses with separation of storage and compute.

* [Snowflake](https://www.snowflake.com/) - Cloud data platform with elastic scaling, zero-copy cloning, and multi-cloud support.
* [Google BigQuery](https://cloud.google.com/bigquery) - Serverless data warehouse with built-in machine learning and BI Engine.
* [Databricks SQL](https://www.databricks.com/product/databricks-sql) - Lakehouse platform combining data warehouse and data lake on Delta Lake.
* [Amazon Redshift](https://aws.amazon.com/redshift/) - Petabyte-scale data warehouse with ML capabilities and federated query.
* [Azure Synapse Analytics](https://azure.microsoft.com/en-us/services/synapse-analytics/) - Unified analytics service combining data warehouse and big data analytics.
* [Firebolt](https://www.firebolt.io/) - Cloud data warehouse built for extreme performance on large-scale analytics.

### Data Lakes & Lakehouses

Storage systems and table formats for massive-scale data lakes.

**Table Formats**
* [Apache Iceberg](https://iceberg.apache.org/) - High-performance table format for huge analytic datasets. Industry-leading adoption in 2024.
* [Delta Lake](https://delta.io/) - Open-source storage framework bringing ACID transactions to data lakes. Used by 60% of Fortune 500.
* [Apache Hudi](https://hudi.apache.org/) - Transactional data lake platform with record-level insert, update, and delete capabilities.
* [Apache XTable](https://xtable.apache.org/) - Omnitable format enabling interoperability between Iceberg, Delta Lake, and Hudi.

**Lakehouse Platforms**
* [Databricks Lakehouse](https://www.databricks.com/) - Unified platform combining data warehouses and data lakes with Delta Lake and Unity Catalog.
* [Dremio](https://www.dremio.com/) - Lakehouse platform with self-service analytics and semantic layer on open formats.
* [Starburst](https://www.starburst.io/) - Analytics engine based on Trino for lakehouse architectures.

**Catalogs & Governance**
* [Apache Polaris](https://polaris.io/) - Open catalog for Apache Iceberg. Open-sourced by Snowflake in 2024.
* [Unity Catalog](https://www.unitycatalog.io/) - Unified governance for lakehouse data. Open-sourced by Databricks in 2024.
* [Nessie](https://projectnessie.org/) - Git-like version control for Iceberg tables with transactional metadata.
* [LakeFS](https://lakefs.io/) - Data version control providing Git-like operations on object storage.

### File Systems

* [HDFS](https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-hdfs/HdfsDesign.html) - Hadoop Distributed File System for storing large datasets across clusters.
  * [Snakebite](https://github.com/spotify/snakebite) - Pure Python HDFS client by Spotify.
* [Amazon S3](https://aws.amazon.com/s3/) - Object storage service with industry-leading scalability and durability.
  * [smart_open](https://github.com/RaRe-Technologies/smart_open) - Utils for streaming large files from S3, HDFS, Azure, and local filesystems.
* [MinIO](https://min.io/) - High-performance object storage compatible with S3 API. Self-hosted alternative to cloud storage.
* [Apache Ozone](https://ozone.apache.org/) - Scalable, distributed object store for Hadoop and cloud-native environments.
* [Ceph](https://ceph.io/) - Unified distributed storage system providing object, block, and file storage.
* [GlusterFS](https://www.gluster.org/) - Scalable network filesystem for cloud storage and media streaming.
* [SeaweedFS](https://github.com/seaweedfs/seaweedfs) - Fast distributed storage system for billions of files with O(1) disk seeks.
* [JuiceFS](https://juicefs.com/) - Distributed POSIX file system built on object storage for cloud-native applications.

### Serialization Formats

Efficient data formats for storage and transmission.

* [Apache Parquet](https://parquet.apache.org/) - Columnar storage format for Hadoop ecosystem. Optimal for analytical queries.
  * [Snappy](https://github.com/google/snappy) - Fast compression/decompression library. Used with Parquet and Avro.
* [Apache Avro](https://avro.apache.org/) - Data serialization system with rich data structures and compact binary format.
* [Apache ORC](https://orc.apache.org/) - Optimized Row Columnar format. Smallest, fastest columnar storage for Hadoop.
* [Protocol Buffers](https://protobuf.dev/) - Google's language-neutral, platform-neutral extensible mechanism for serializing structured data.
* [Apache Thrift](https://thrift.apache.org/) - Framework for scalable cross-language services development with data serialization.
* [Apache Arrow](https://arrow.apache.org/) - Cross-language in-memory columnar format for efficient analytics and zero-copy data sharing.
* [MessagePack](https://msgpack.org/) - Efficient binary serialization format like JSON but faster and smaller.
* [FlatBuffers](https://flatbuffers.dev/) - Memory-efficient serialization library by Google. Access data without parsing/unpacking.

---

## Data Transformation

Transform raw data into analytics-ready datasets.

**SQL-based Transformation**
* [dbt (Data Build Tool)](https://www.getdbt.com/) - Transform data in your warehouse using SQL and software engineering best practices. Industry standard for analytics engineering.
  * [dbt-core](https://github.com/dbt-labs/dbt-core) - Open-source version of dbt for self-managed deployment.
  * [dbt Cloud](https://www.getdbt.com/product/dbt-cloud/) - Managed dbt service with IDE, orchestration, and semantic layer.
* [SQLMesh](https://sqlmesh.com/) - Next-generation data transformation framework addressing dbt scalability challenges with virtual environments.
* [Dataform](https://cloud.google.com/dataform) - SQL workflow tool for data teams to develop and maintain data pipelines in BigQuery.

**Python-based Transformation**
* [Apache Spark](https://spark.apache.org/) - Unified analytics engine for large-scale data processing with built-in modules for SQL, streaming, ML, and graph processing.
  * [PySpark](https://spark.apache.org/docs/latest/api/python/) - Python API for Spark.
  * [Spark SQL](https://spark.apache.org/sql/) - Module for working with structured data using SQL.
  * [Spark Packages](https://spark-packages.org/) - Community index of packages for Apache Spark.
* [Polars](https://www.pola.rs/) - Lightning-fast DataFrame library written in Rust with Python and Node.js bindings.
* [Pandas](https://pandas.pydata.org/) - Python data analysis and manipulation library providing DataFrames.
* [Dask](https://www.dask.org/) - Parallel computing library that scales Python. Native parallel analytics with familiar APIs.

---

## Orchestration & Workflow

Coordinate and schedule data pipelines.

* [Apache Airflow](https://airflow.apache.org/) - Platform to programmatically author, schedule, and monitor workflows. Industry standard with 3.0 adding event-driven capabilities.
  * [Astronomer](https://www.astronomer.io/) - Managed Airflow service with enterprise features and multi-cloud support.
* [Dagster](https://dagster.io/) - Data orchestrator for machine learning, analytics, and ETL. Asset-centric approach focusing on data products.
* [Prefect](https://www.prefect.io/) - Modern workflow orchestration with negative engineering and dataflow automation.
* [Kestra](https://kestra.io/) - Declarative data orchestration platform using YAML. Event-driven workflows with real-time triggers.
* [Mage](https://www.mage.ai/) - Modern data pipeline tool for ETL/ELT with notebook-style interface and real-time streaming.
* [Luigi](https://github.com/spotify/luigi) - Python module for building complex pipelines of batch jobs. Battle-tested at Spotify.
* [Apache Oozie](https://oozie.apache.org/) - Workflow scheduler system for managing Apache Hadoop jobs.
* [Azkaban](https://azkaban.github.io/) - Batch workflow job scheduler created at LinkedIn for Hadoop jobs.
* [Temporal](https://temporal.io/) - Workflow engine for building resilient applications with sophisticated orchestration.

---

## Stream Processing

Process data in real-time as it arrives.

**Stream Processing Engines**
* [Apache Flink](https://flink.apache.org/) - Distributed stream processing framework with stateful computations and event-time processing.
* [Apache Kafka Streams](https://kafka.apache.org/documentation/streams/) - Client library for building streaming applications with Kafka.
* [Apache Spark Streaming](https://spark.apache.org/streaming/) - Scalable fault-tolerant streaming processing using micro-batches.
* [Apache Storm](https://storm.apache.org/) - Distributed real-time computation system for processing unbounded streams.
* [Apache Samza](https://samza.apache.org/) - Distributed stream processing framework with Kafka integration.
* [RisingWave](https://risingwave.com/) - Distributed SQL streaming database using PostgreSQL wire protocol.
* [Faust](https://faust.readthedocs.io/) - Python stream processing library for Kafka Streams-like processing.
* [ksqlDB](https://ksqldb.io/) - Database for building stream processing applications on Kafka using SQL.

**Real-time Databases**
* [Apache Pinot](https://pinot.apache.org/) - Real-time distributed OLAP datastore for user-facing analytics with sub-second query latency.
* [ClickHouse](https://clickhouse.com/) - Column-oriented database for real-time analytics queries.
* [Materialize](https://materialize.com/) - Streaming SQL database that maintains materialized views over streaming data.

---

## Batch Processing

Process large volumes of data in scheduled batches.

**Processing Frameworks**
* [Apache Spark](https://spark.apache.org/) - Unified analytics engine for batch and stream processing at scale.
* [Apache Hadoop MapReduce](https://hadoop.apache.org/docs/current/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html) - Software framework for distributed processing of large datasets.
* [Apache Flink](https://flink.apache.org/) - Stream and batch processing with unified API.
* [Apache Tez](https://tez.apache.org/) - Application framework for complex directed-acyclic-graph (DAG) of tasks.
* [AWS EMR](https://aws.amazon.com/emr/) - Cloud big data platform for processing vast amounts of data using Spark, Hadoop, and Presto.
* [Google Dataflow](https://cloud.google.com/dataflow) - Fully managed streaming and batch data processing service based on Apache Beam.

**Query Engines**
* [Trino](https://trino.io/) - Fast distributed SQL query engine for big data analytics. Formerly PrestoSQL.
* [Apache Presto](https://prestodb.io/) - Distributed SQL query engine for querying large datasets across heterogeneous sources.
* [Apache Drill](https://drill.apache.org/) - Schema-free SQL query engine for Hadoop, NoSQL, and cloud storage.
* [Apache Hive](https://hive.apache.org/) - Data warehouse software for querying and managing large datasets in distributed storage.
  * [Hivemall](https://github.com/apache/incubator-hivemall) - Scalable machine learning library for Hive/Hadoop.
  * [PyHive](https://github.com/dropbox/PyHive) - Python interface to Hive and Presto.

**Machine Learning**
* [Apache Spark MLlib](https://spark.apache.org/mllib/) - Scalable machine learning library with classification, regression, clustering, and collaborative filtering.
* [H2O.ai](https://www.h2o.ai/) - Open-source platform for building ML models at scale.
* [Apache Mahout](https://mahout.apache.org/) - Distributed linear algebra framework for building scalable ML algorithms.

---

## Data Quality & Observability

Monitor, test, and ensure data reliability.

**Data Quality Testing**
* [Great Expectations](https://greatexpectations.io/) - Python framework for validating, documenting, and profiling data with declarative expectations.
* [Soda](https://www.soda.io/) - Data quality testing platform using SQL-like checks. Available as Soda Core (open-source) and Soda Cloud.
* [dbt-expectations](https://github.com/calogica/dbt-expectations) - Great Expectations tests packaged for dbt projects.
* [elementary-data](https://www.elementary-data.com/) - Open-source data observability for dbt with anomaly detection that learns from historical patterns.

**Data Observability**
* [Monte Carlo](https://www.montecarlodata.com/) - Data observability platform detecting data issues across freshness, volume, schema, and quality.
* [Datadog Data Observability](https://www.datadoghq.com/) - Monitoring and observability for data pipelines integrated with infrastructure monitoring.
* [OpenMetadata](https://open-metadata.org/) - Open-source metadata platform with data quality, profiling, lineage, and discovery.

**Data Profiling**
* [Apache Griffin](https://griffin.apache.org/) - Data quality solution for big data with profiling, measuring, and validating capabilities.
* [Pandas Profiling](https://github.com/ydataai/ydata-profiling) - Generate profile reports from pandas DataFrames with statistics and visualizations.

---

## Data Discovery & Governance

Find, understand, and govern your data assets.

**Data Catalogs**
* [DataHub](https://datahubproject.io/) - Modern data catalog with data discovery, observability, and governance. LinkedIn open-source.
* [OpenMetadata](https://open-metadata.org/) - Unified metadata platform for data discovery, quality, and collaboration.
* [Amundsen](https://www.amundsen.io/) - Data discovery and metadata engine by Lyft. Improves data team productivity.
* [Apache Atlas](https://atlas.apache.org/) - Metadata management and governance framework for Hadoop.
* [CKAN](https://ckan.org/) - Open-source data management system for powering data portals and catalogs.

**Data Lineage**
* [Marquez](https://marquezproject.ai/) - Open-source metadata service for collection, aggregation, and visualization of dataset lineage.
* [OpenLineage](https://openlineage.io/) - Open framework for data lineage collection and analysis.

**Commercial Data Governance**
* [Alation](https://www.alation.com/) - Enterprise data catalog with AI-powered search and collaborative governance.
* [Collibra](https://www.collibra.com/) - Data intelligence platform for data governance, quality, and privacy.
* [Atlan](https://atlan.com/) - Active metadata platform with embedded collaboration and data governance.

---

## Reverse ETL

Sync data from warehouses to operational systems.

* [Airbyte Reverse ETL](https://airbyte.com/) - Open-source reverse ETL capabilities integrated into Airbyte platform.
* [Census](https://www.getcensus.com/) - Operational analytics platform syncing warehouse data to 200+ business tools.
* [Hightouch](https://hightouch.com/) - Data activation platform for reverse ETL from warehouses to SaaS tools.
* [Grouparoo](https://www.grouparoo.com/) - Open-source reverse ETL acquired by Airbyte. Relaunched in 2024 with TypeScript plugins.

---

## Analytics & Visualization

Transform data into insights and visualizations.

**Business Intelligence Platforms**
* [Apache Superset](https://superset.apache.org/) - Modern data exploration and visualization platform. Open-source alternative to Tableau.
* [Metabase](https://www.metabase.com/) - Easy-to-use open-source BI tool for teams to ask questions and learn from data.
* [Redash](https://redash.io/) - Connect and query data sources, build dashboards, and share insights.
* [Tableau](https://www.tableau.com/) - Industry-leading visual analytics platform for business intelligence.
* [Looker](https://cloud.google.com/looker) - Enterprise BI platform with semantic modeling layer (LookML). Acquired by Google.
* [Power BI](https://powerbi.microsoft.com/) - Business analytics service by Microsoft for interactive visualizations.

**Charting Libraries**
* [D3.js](https://d3js.org/) - JavaScript library for manipulating documents based on data using web standards.
* [Plotly](https://plotly.com/) - Graphing library for interactive, publication-quality graphs.
* [Apache ECharts](https://echarts.apache.org/) - Powerful, interactive charting and visualization library.
* [Chart.js](https://www.chartjs.org/) - Simple yet flexible JavaScript charting library.
* [Highcharts](https://www.highcharts.com/) - Modern SVG-based charting library with extensive chart types.
* [C3.js](https://c3js.org/) - D3-based reusable chart library for quick chart creation.

**Embedded Analytics**
* [DuckDB](https://duckdb.org/) - In-process OLAP database. Version 1.0 released June 2024. Used for embedded analytics at scale.
* [MotherDuck](https://motherduck.com/) - Serverless analytics platform built on DuckDB for collaborative analytics.
* [Cube](https://cube.dev/) - Headless BI platform and semantic layer with universal SQL API for building data apps.

**Semantic Layer / Metrics Layer**
* [Cube](https://cube.dev/) - Headless BI with semantic layer, caching, and access control for data apps.
* [dbt Semantic Layer](https://www.getdbt.com/product/semantic-layer/) - Centralized metrics definitions integrated with dbt. Powered by MetricFlow.
* [Metriql](https://metriql.com/) - Headless BI and metrics layer for modern data stack.

**Dashboarding Frameworks**
* [Streamlit](https://streamlit.io/) - Turn Python scripts into shareable web apps for ML and data science.
* [Dash](https://plotly.com/dash/) - Low-code framework for building data apps in Python, R, Julia, and F#.
* [Gradio](https://gradio.app/) - Build and share ML web apps in Python.
* [Panel](https://panel.holoviz.org/) - Create custom interactive dashboards, reports, and data apps in Python.

---

## Infrastructure & Deployment

Deploy and manage data infrastructure at scale.

**Containerization & Orchestration**
* [Docker](https://www.docker.com/) - Platform for developing, shipping, and running applications in containers.
* [Kubernetes](https://kubernetes.io/) - Container orchestration platform for automating deployment, scaling, and management.
* [Apache Mesos](https://mesos.apache.org/) - Cluster manager providing resource isolation and sharing across distributed applications.

**Data Infrastructure Tools**
* [Terraform](https://www.terraform.io/) - Infrastructure as code tool for building, changing, and versioning infrastructure.
* [Pulumi](https://www.pulumi.com/) - Modern infrastructure as code using familiar programming languages.
* [Ansible](https://www.ansible.com/) - Automation platform for configuration management and application deployment.

**Monitoring & Observability**
* [Prometheus](https://prometheus.io/) - Open-source monitoring system with time-series database and alerting.
  * [HAProxy Exporter](https://github.com/prometheus/haproxy_exporter) - Exports HAProxy stats for Prometheus consumption.
* [Grafana](https://grafana.com/) - Open-source analytics and monitoring platform with beautiful dashboards.
* [Datadog](https://www.datadoghq.com/) - Monitoring and security platform for cloud applications.
* [New Relic](https://newrelic.com/) - Observability platform for monitoring and debugging production systems.

**Logging**
* [Elastic Stack (ELK)](https://www.elastic.co/elastic-stack/) - Elasticsearch, Logstash, and Kibana for log aggregation and analysis.
  * [docker-logstash](https://github.com/pblittle/docker-logstash) - Configurable Logstash Docker image with Elasticsearch and Kibana.
  * [elasticsearch-jdbc](https://github.com/jprante/elasticsearch-jdbc) - JDBC importer for Elasticsearch.
* [Fluentd](https://www.fluentd.org/) - Unified logging layer for collecting, filtering, and routing log data.
* [Loki](https://grafana.com/oss/loki/) - Horizontally scalable log aggregation system inspired by Prometheus.

---

## Learning Resources

### Real-time Datasets

* [Twitter API](https://developer.twitter.com/en/docs) - Real-time access to Twitter's stream of tweets and user data.
* [Eventsim](https://github.com/Interana/eventsim) - Event data simulator generating pseudo-random events for testing streaming pipelines.
* [Reddit Streaming](https://www.reddit.com/r/datasets/comments/3mk1vg/realtime_data_is_available_including_comments/) - Real-time stream of Reddit comments, submissions, and links.
* [Wikimedia Event Streams](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams) - Real-time streams of Wikipedia edits, page views, and events.

### Data Dumps

* [GitHub Archive](https://www.gharchive.org/) - GitHub's public timeline since 2011, updated hourly.
* [Common Crawl](https://commoncrawl.org/) - Open repository of web crawl data with petabytes of data.
* [Wikipedia Dumps](https://dumps.wikimedia.org/) - Complete copies of all Wikimedia wikis in XML and SQL formats.
* [Stack Exchange Data Dump](https://archive.org/details/stackexchange) - Creative Commons data dump of all Stack Exchange sites.
* [AWS Open Data Registry](https://registry.opendata.aws/) - Discover and share datasets available via AWS.
* [Google Dataset Search](https://datasetsearch.research.google.com/) - Search engine for datasets across the web.

---

## Related Resources

* [The Data Engineering Ecosystem: An Interactive Map](http://xyz.insightdataengineering.com/blog/pipeline_map.html) - Visual map of the data engineering landscape.
* [Awesome Data Science](https://github.com/academic/awesome-datascience) - Curated list of data science resources.
* [Awesome Big Data](https://github.com/0xnr/awesome-bigdata) - Curated list of big data frameworks, resources, and tools.
* [Awesome ETL](https://github.com/pawl/awesome-etl) - Curated list of ETL frameworks, libraries, and software.
* [Awesome Streaming](https://github.com/manuzhang/awesome-streaming) - Curated list of streaming frameworks and applications.

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](contributing.md) first.

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Igor Barinov](https://github.com/igorbarinov/) has waived all copyright and related or neighboring rights to this work.
