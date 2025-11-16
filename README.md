# Awesome Data Engineering

A curated list of data engineering tools for software developers. [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

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
  - [Vector Databases](#vector-databases)
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
- [AI/ML & LLM Infrastructure](#aiml--llm-infrastructure)
  - [LLM Orchestration & Frameworks](#llm-orchestration--frameworks)
  - [Model Training & Fine-tuning](#model-training--fine-tuning)
  - [Feature Stores](#feature-stores)
  - [ML Experiment Tracking](#ml-experiment-tracking)
  - [Model Serving & Deployment](#model-serving--deployment)
  - [LLM Evaluation & Monitoring](#llm-evaluation--monitoring)
  - [RAG & Knowledge Management](#rag--knowledge-management)
  - [LLM APIs & Providers](#llm-apis--providers)
  - [AI Agents & Autonomous Systems](#ai-agents--autonomous-systems)
  - [Multimodal AI](#multimodal-ai)
  - [Model Compression & Quantization](#model-compression--quantization)
  - [Data Labeling & Annotation](#data-labeling--annotation)
  - [Synthetic Data Generation](#synthetic-data-generation)
  - [LLM Security & Safety](#llm-security--safety)
  - [Edge AI & On-Device ML](#edge-ai--on-device-ml)
  - [MLOps & ML Platforms](#mlops--ml-platforms)
  - [Data Versioning for ML](#data-versioning-for-ml)
  - [NLP & Text Processing](#nlp--text-processing)
  - [Reinforcement Learning](#reinforcement-learning)
  - [Federated Learning](#federated-learning)
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
* [SSDB](https://github.com/ideawu/ssdb) - High-performance NoSQL database supporting many data structures. Alternative to Redis with disk persistence.
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

### Vector Databases

Specialized databases for storing and querying high-dimensional vectors, essential for AI/ML applications, semantic search, and RAG (Retrieval-Augmented Generation).

**Open Source**
* [Chroma](https://www.trychroma.com/) - AI-native embedding database. Simple, fast, and production-ready for LLM applications.
* [Milvus](https://milvus.io/) - Open-source vector database built for scalable similarity search. Cloud-native with GPU acceleration.
* [Weaviate](https://weaviate.io/) - Vector database with built-in vectorization and hybrid search. GraphQL and RESTful APIs.
* [Qdrant](https://qdrant.tech/) - High-performance vector search engine with Rust-based core. Extended filtering support.
* [LanceDB](https://lancedb.com/) - Embedded vector database built on Lance columnar format. Serverless and multi-modal.
* [txtai](https://github.com/neuml/txtai) - Embeddings database for semantic search, LLM orchestration, and language model workflows.
* [Vespa](https://vespa.ai/) - Big data serving engine with vector search, lexical search, and ML model inference.

**Managed / Cloud**
* [Pinecone](https://www.pinecone.io/) - Fully managed vector database for production-scale similarity search. Serverless and pod-based options.
* [Zilliz Cloud](https://zilliz.com/) - Managed Milvus with enterprise features and global deployment.
* [Weaviate Cloud](https://weaviate.io/pricing) - Managed Weaviate with automatic scaling and multi-cloud support.
* [MongoDB Atlas Vector Search](https://www.mongodb.com/products/platform/atlas-vector-search) - Vector search integrated into MongoDB Atlas.
* [PostgreSQL pgvector](https://github.com/pgvector/pgvector) - Vector similarity search extension for PostgreSQL.
* [Elasticsearch Vector Search](https://www.elastic.co/elasticsearch/vector-database) - Dense vector search capabilities in Elasticsearch.
* [Redis Vector Search](https://redis.io/docs/interact/search-and-query/search/vectors/) - Vector similarity search in Redis Stack.
* [Azure Cognitive Search](https://azure.microsoft.com/en-us/products/ai-services/cognitive-search) - AI-powered cloud search with vector search capabilities.
* [AWS OpenSearch Vector Engine](https://aws.amazon.com/opensearch-service/features/vector-engine/) - k-NN vector search in Amazon OpenSearch.

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

## AI/ML & LLM Infrastructure

Infrastructure for building, training, and deploying AI/ML models and LLM applications at scale.

### LLM Orchestration & Frameworks

Build production LLM applications with retrieval, agents, and complex workflows.

**LLM Application Frameworks**
* [LangChain](https://www.langchain.com/) - Framework for building LLM applications with chains, agents, and memory. Python and JavaScript.
* [LlamaIndex](https://www.llamaindex.ai/) - Data framework for LLM applications with advanced RAG (Retrieval-Augmented Generation) capabilities.
* [Haystack](https://haystack.deepset.ai/) - End-to-end NLP framework for building search, QA, and LLM applications.
* [Semantic Kernel](https://github.com/microsoft/semantic-kernel) - Microsoft's SDK for integrating LLMs with conventional programming languages.
* [AutoGen](https://microsoft.github.io/autogen/) - Multi-agent conversation framework from Microsoft for building LLM applications.
* [CrewAI](https://www.crewai.com/) - Framework for orchestrating role-playing autonomous AI agents.

**LLM Gateways & Proxies**
* [LiteLLM](https://www.litellm.ai/) - Call 100+ LLM APIs using the OpenAI format. Load balancing, fallbacks, and cost tracking.
* [Portkey](https://portkey.ai/) - Full-stack LLMOps platform with gateway, observability, and prompt management.
* [Helicone](https://www.helicone.ai/) - Open-source LLM observability platform with monitoring, caching, and cost tracking.
* [OpenLLM](https://github.com/bentoml/OpenLLM) - Run any open-source LLMs as OpenAI-compatible API endpoints.

**Prompt Engineering & Management**
* [PromptFlow](https://microsoft.github.io/promptflow/) - Microsoft's tool for creating LLM apps with prompt engineering and evaluation.
* [Langfuse](https://langfuse.com/) - Open-source LLM engineering platform with tracing, prompt management, and evaluation.
* [Weights & Biases Prompts](https://wandb.ai/site/prompts) - Prompt engineering and tracking integrated with W&B.
* [PromptLayer](https://promptlayer.com/) - Platform for prompt engineering with version control and observability.

### Model Training & Fine-tuning

Tools for training, fine-tuning, and optimizing machine learning models.

**Model Training Frameworks**
* [PyTorch](https://pytorch.org/) - Deep learning framework with dynamic computational graphs. Industry standard for research and production.
* [TensorFlow](https://www.tensorflow.org/) - End-to-end ML platform with production deployment capabilities.
* [JAX](https://github.com/google/jax) - High-performance ML research framework with autograd and XLA compilation from Google.
* [Keras](https://keras.io/) - High-level neural networks API running on TensorFlow.
* [MXNet](https://mxnet.apache.org/) - Flexible deep learning framework supporting multiple languages.

**LLM Fine-tuning & Training**
* [Hugging Face Transformers](https://huggingface.co/transformers/) - State-of-the-art ML models for PyTorch, TensorFlow, and JAX.
* [Axolotl](https://github.com/OpenAccess-AI-Collective/axolotl) - Tool for fine-tuning LLMs with support for various architectures and techniques.
* [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) - Unified framework for fine-tuning 100+ LLMs with PEFT methods.
* [Unsloth](https://github.com/unslothai/unsloth) - 2-5x faster LLM fine-tuning with lower memory usage.
* [Ludwig](https://ludwig.ai/) - Low-code ML framework for building custom models including LLMs.
* [DeepSpeed](https://www.deepspeed.ai/) - Deep learning optimization library for distributed training and inference from Microsoft.
* [Megatron-LM](https://github.com/NVIDIA/Megatron-LM) - Large-scale transformer model training by NVIDIA.

**Distributed Training**
* [Ray Train](https://docs.ray.io/en/latest/train/train.html) - Distributed training library supporting PyTorch, TensorFlow, and XGBoost.
* [Horovod](https://horovod.ai/) - Distributed deep learning training framework from Uber.
* [Accelerate](https://huggingface.co/docs/accelerate/) - Easy distributed training for PyTorch models from Hugging Face.

**AutoML & Neural Architecture Search**
* [AutoGluon](https://auto.gluon.ai/) - AutoML for tabular, text, and image data. State-of-the-art results with minimal code.
* [FLAML](https://microsoft.github.io/FLAML/) - Fast and lightweight AutoML library from Microsoft.
* [Optuna](https://optuna.org/) - Hyperparameter optimization framework with pruning and distributed execution.
* [Ray Tune](https://docs.ray.io/en/latest/tune/index.html) - Scalable hyperparameter tuning library.

### Feature Stores

Centralized platforms for managing, storing, and serving ML features.

* [Feast](https://feast.dev/) - Open-source feature store for ML. Standardize feature definitions and serve them consistently.
* [Tecton](https://www.tecton.ai/) - Enterprise feature platform built on Feast. Real-time and batch feature engineering.
* [Hopsworks](https://www.hopsworks.ai/) - Data platform with feature store, model serving, and vector database.
* [Feathr](https://github.com/feathr-ai/feathr) - Enterprise-grade feature store from LinkedIn supporting offline and online features.
* [Databricks Feature Store](https://www.databricks.com/product/feature-store) - Managed feature store integrated with Unity Catalog and MLflow.
* [Amazon SageMaker Feature Store](https://aws.amazon.com/sagemaker/feature-store/) - Fully managed feature store for ML.
* [Google Vertex AI Feature Store](https://cloud.google.com/vertex-ai/docs/featurestore) - Managed feature store on GCP.

### ML Experiment Tracking

Track experiments, compare results, and manage model versions.

* [MLflow](https://mlflow.org/) - Open-source platform for ML lifecycle management. Tracking, projects, models, and model registry.
* [Weights & Biases](https://wandb.ai/) - ML experiment tracking, model management, and collaboration platform.
* [Neptune.ai](https://neptune.ai/) - Metadata store for MLOps with experiment tracking and model registry.
* [ClearML](https://clear.ml/) - Open-source MLOps platform for experiment management, orchestration, and data management.
* [Comet](https://www.comet.com/) - ML experiment tracking and model production management.
* [Sacred](https://github.com/IDSIA/sacred) - Tool for configuring, organizing, logging, and reproducing experiments.
* [Guild AI](https://guild.ai/) - Experiment tracking and pipeline automation for ML.
* [Aim](https://aimstack.io/) - Easy-to-use experiment tracking for AI/ML teams.

### Model Serving & Deployment

Deploy and serve ML models in production at scale.

**Model Serving Frameworks**
* [BentoML](https://www.bentoml.com/) - Unified framework for building, shipping, and scaling ML services.
* [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Scalable model serving library built on Ray. Multi-model composition.
* [TorchServe](https://pytorch.org/serve/) - PyTorch model serving framework with multi-model support and APIs.
* [TensorFlow Serving](https://www.tensorflow.org/tfx/guide/serving) - Production serving system for TensorFlow models with gRPC and REST APIs.
* [Triton Inference Server](https://developer.nvidia.com/triton-inference-server) - NVIDIA's inference serving software for AI models across platforms.
* [Seldon Core](https://www.seldon.io/solutions/open-source-projects/core) - MLOps framework for deploying ML models on Kubernetes.
* [KServe](https://kserve.github.io/website/) - Serverless inferencing on Kubernetes. Successor to KFServing.

**LLM Serving & Inference**
* [vLLM](https://vllm.ai/) - Fast and easy LLM serving with PagedAttention and continuous batching.
* [Text Generation Inference](https://github.com/huggingface/text-generation-inference) - Production-ready LLM serving from Hugging Face.
* [Ollama](https://ollama.ai/) - Run LLMs locally with simple API. Supports Llama 2, Mistral, and more.
* [LocalAI](https://localai.io/) - Drop-in replacement REST API for OpenAI compatible with consumer-grade hardware.
* [llama.cpp](https://github.com/ggerganov/llama.cpp) - Inference of LLaMA models in pure C/C++ for efficient CPU/GPU execution.
* [Xinference](https://inference.xorbits.io/) - Powerful and unified LLM serving framework supporting various models.

**Model Optimization**
* [ONNX Runtime](https://onnxruntime.ai/) - Cross-platform ML model accelerator for optimized inference.
* [TensorRT](https://developer.nvidia.com/tensorrt) - NVIDIA's deep learning inference optimizer and runtime.
* [OpenVINO](https://www.intel.com/content/www/us/en/developer/tools/openvino-toolkit/overview.html) - Intel's toolkit for optimizing and deploying deep learning models.

**Managed ML Platforms**
* [Amazon SageMaker](https://aws.amazon.com/sagemaker/) - Fully managed ML service for building, training, and deploying models.
* [Google Vertex AI](https://cloud.google.com/vertex-ai) - Unified ML platform on GCP for building and deploying AI models.
* [Azure Machine Learning](https://azure.microsoft.com/en-us/products/machine-learning/) - Enterprise-grade ML service for the entire ML lifecycle.
* [Databricks ML](https://www.databricks.com/product/machine-learning) - Unified ML platform with MLflow, AutoML, and feature store.

### LLM Evaluation & Monitoring

Evaluate and monitor LLM performance, quality, and safety in production.

**LLM Evaluation**
* [RAGAS](https://github.com/explodinggradients/ragas) - Framework for evaluating RAG (Retrieval Augmented Generation) pipelines.
* [DeepEval](https://www.confident-ai.com/deepeval) - Unit testing for LLMs with metrics like hallucination, toxicity, and bias.
* [TruLens](https://www.trulens.org/) - Evaluation and tracking for LLM apps with feedback functions.
* [LangSmith](https://www.langchain.com/langsmith) - Platform for debugging, testing, and monitoring LLM applications.
* [OpenAI Evals](https://github.com/openai/evals) - Framework for evaluating LLMs and LLM systems.
* [Promptfoo](https://www.promptfoo.dev/) - Test and evaluate LLM prompts systematically.

**LLM Observability & Monitoring**
* [LangFuse](https://langfuse.com/) - Open-source LLM engineering platform with tracing, evaluation, and analytics.
* [Arize AI](https://arize.com/) - ML observability platform for monitoring model performance and detecting issues.
* [Evidently AI](https://www.evidentlyai.com/) - Open-source ML monitoring with drift detection and model quality evaluation.
* [Fiddler AI](https://www.fiddler.ai/) - Model performance management platform with explainability and monitoring.
* [WhyLabs](https://whylabs.ai/) - AI observability platform with data and ML monitoring.
* [Phoenix](https://phoenix.arize.com/) - Open-source AI observability for LLM applications with tracing and evaluations.

### RAG & Knowledge Management

Retrieval-Augmented Generation (RAG) frameworks and tools for building knowledge-powered AI applications.

**RAG Frameworks**
* [LlamaIndex](https://www.llamaindex.ai/) - Data framework for LLM applications with advanced RAG capabilities and index structures.
* [LangChain](https://www.langchain.com/) - Framework with document loaders, text splitters, and retrieval chains for RAG.
* [Haystack](https://haystack.deepset.ai/) - End-to-end framework for building RAG pipelines with customizable components.
* [txtai](https://github.com/neuml/txtai) - All-in-one embeddings database with semantic search and RAG workflows.
* [Canopy](https://github.com/pinecone-io/canopy) - RAG framework built on Pinecone vector database.
* [Verba](https://github.com/weaviate/Verba) - RAG application built on Weaviate for document Q&A.

**Document Processing & Parsing**
* [Unstructured](https://unstructured.io/) - Library for preprocessing documents (PDF, HTML, Word, etc.) for RAG pipelines.
* [LangChain Document Loaders](https://python.langchain.com/docs/modules/data_connection/document_loaders/) - 100+ document loaders for various file formats.
* [LlamaParse](https://github.com/run-llama/llama_parse) - Document parsing specifically optimized for RAG by LlamaIndex.
* [PyPDF](https://pypdf.readthedocs.io/) - Pure Python PDF library for reading and extracting text.
* [PDFPlumber](https://github.com/jsvine/pdfplumber) - Extract text, tables, and metadata from PDFs.
* [Docling](https://github.com/DS4SD/docling) - Document understanding and parsing from IBM Research.
* [Marker](https://github.com/VikParuchuri/marker) - Convert PDF to markdown with high accuracy.

**Document OCR & Understanding**
* [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) - Industry-standard open-source OCR engine.
* [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) - Multilingual OCR toolkit supporting 80+ languages.
* [EasyOCR](https://github.com/JaidedAI/EasyOCR) - Ready-to-use OCR with 80+ supported languages.
* [Surya](https://github.com/VikParuchuri/surya) - Multilingual document OCR toolkit with layout analysis.
* [LayoutParser](https://layout-parser.github.io/) - Unified toolkit for document layout analysis.
* [AWS Textract](https://aws.amazon.com/textract/) - ML service for extracting text and data from documents.
* [Google Document AI](https://cloud.google.com/document-ai) - Document understanding platform with pre-trained and custom models.

**Chunking & Text Splitting**
* [LangChain Text Splitters](https://python.langchain.com/docs/modules/data_connection/document_transformers/) - Various text splitting strategies for RAG.
* [Semantic Chunking](https://github.com/FullStackRetrieval-com/RetrievalTutorials) - Intelligent chunking based on semantic similarity.
* [LlamaIndex Node Parsers](https://docs.llamaindex.ai/en/stable/module_guides/loading/node_parsers/) - Document chunking and parsing strategies.

**Knowledge Graphs**
* [Neo4j](https://neo4j.com/) - Graph database for building knowledge graphs for LLM applications.
* [LlamaIndex Knowledge Graph](https://docs.llamaindex.ai/en/stable/examples/index_structs/knowledge_graph/) - Knowledge graph index for structured retrieval.
* [LangChain Neo4j](https://python.langchain.com/docs/integrations/graphs/neo4j_cypher) - Neo4j integration for graph-based RAG.
* [Memgraph](https://memgraph.com/) - In-memory graph database for real-time knowledge graphs.
* [ArangoDB](https://www.arangodb.com/) - Multi-model database with native graph support.

### LLM APIs & Providers

Access to language models via APIs and model providers.

**Proprietary LLM APIs**
* [OpenAI API](https://platform.openai.com/) - GPT-4, GPT-4 Turbo, GPT-3.5 Turbo with chat completions, embeddings, and more.
* [Anthropic Claude](https://www.anthropic.com/api) - Claude 3 (Opus, Sonnet, Haiku) with 200K context window.
* [Google Gemini](https://ai.google.dev/) - Gemini Pro and Ultra models with multimodal capabilities.
* [Cohere](https://cohere.com/) - Enterprise LLMs with Command, Embed, and Rerank models.
* [AI21 Labs](https://www.ai21.com/) - Jurassic models for text generation and comprehension.
* [Mistral AI](https://mistral.ai/) - Mistral 7B, Mixtral 8x7B, and Mistral Large via API.

**Open LLM Hosting Platforms**
* [Hugging Face Inference API](https://huggingface.co/inference-api) - Hosted inference for 150,000+ open models.
* [Replicate](https://replicate.com/) - Run open-source models with simple API. LLAMA, Stable Diffusion, etc.
* [Together AI](https://www.together.ai/) - Fast inference for open-source LLMs with competitive pricing.
* [Anyscale Endpoints](https://www.anyscale.com/endpoints) - Serverless endpoints for open LLMs on Ray infrastructure.
* [Fireworks AI](https://fireworks.ai/) - Production-scale inference for open models with 4x faster performance.
* [DeepInfra](https://deepinfra.com/) - Serverless GPU inference for popular open-source models.
* [Baseten](https://www.baseten.co/) - Deploy ML models as production-ready APIs.

**Model Hubs & Repositories**
* [Hugging Face Hub](https://huggingface.co/models) - 500,000+ pre-trained models for NLP, vision, audio, and more.
* [ONNX Model Zoo](https://github.com/onnx/models) - Pre-trained ONNX models ready for inference.
* [TensorFlow Hub](https://tfhub.dev/) - Repository of trained ML models ready for fine-tuning and deployment.
* [PyTorch Hub](https://pytorch.org/hub/) - Pre-trained model repository for PyTorch.
* [Ollama Library](https://ollama.ai/library) - Library of models optimized for local inference.

**Embeddings & Reranking**
* [OpenAI Embeddings](https://platform.openai.com/docs/guides/embeddings) - text-embedding-3-large and text-embedding-3-small.
* [Cohere Embed](https://cohere.com/embed) - Multilingual embeddings with 1024 dimensions.
* [Voyage AI](https://www.voyageai.com/) - State-of-the-art embeddings specialized for RAG applications.
* [Jina AI Embeddings](https://jina.ai/embeddings/) - 8K context embeddings for search and RAG.
* [Sentence Transformers](https://www.sbert.net/) - Open-source embeddings library with 100+ pre-trained models.
* [Cohere Rerank](https://cohere.com/rerank) - Reranking API to improve search relevance.

### AI Agents & Autonomous Systems

Frameworks and tools for building autonomous AI agents.

**Agent Frameworks**
* [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) - Autonomous GPT-4 agent for achieving goals with minimal human intervention.
* [BabyAGI](https://github.com/yoheinakajima/babyagi) - AI-powered task management system using OpenAI and Pinecone.
* [SuperAGI](https://superagi.com/) - Open-source framework for building, managing, and running autonomous AI agents.
* [AgentGPT](https://agentgpt.reworkd.ai/) - Autonomous AI agents in your browser.
* [AutoGen](https://microsoft.github.io/autogen/) - Microsoft's framework for multi-agent conversations and workflows.
* [CrewAI](https://www.crewai.com/) - Framework for orchestrating role-playing autonomous AI agents.
* [LangGraph](https://github.com/langchain-ai/langgraph) - Build stateful, multi-actor applications with LLMs using graph-based workflows.
* [Semantic Kernel Agents](https://github.com/microsoft/semantic-kernel) - Microsoft's agent framework with planners and plugins.

**Agent Tools & Plugins**
* [LangChain Tools](https://python.langchain.com/docs/modules/agents/tools/) - 50+ tools for agents (search, calculators, APIs, etc.).
* [OpenAI Function Calling](https://platform.openai.com/docs/guides/function-calling) - Native function calling for GPT models.
* [Anthropic Tool Use](https://docs.anthropic.com/claude/docs/tool-use) - Claude's function calling capabilities.
* [Gorilla](https://github.com/ShishirPatil/gorilla) - LLM for API calls - trained to call APIs accurately.
* [ToolLLM](https://github.com/OpenBMB/ToolLLM) - Open-source framework for tool learning with LLMs.

**Workflow Automation**
* [n8n](https://n8n.io/) - Workflow automation with AI node integrations.
* [Zapier AI](https://zapier.com/ai) - AI-powered workflow automation with LLM integrations.
* [Make (Integromat)](https://www.make.com/) - Visual automation platform with AI/ML integrations.
* [Flowise](https://flowiseai.com/) - Drag-and-drop tool to build LLM flows and AI agents.
* [LangFlow](https://www.langflow.org/) - Visual framework for building LangChain flows.

### Multimodal AI

Tools for working with multiple modalities: text, images, audio, video.

**Multimodal Models**
* [GPT-4 Vision](https://platform.openai.com/docs/guides/vision) - Multimodal GPT-4 with image understanding.
* [Claude 3](https://www.anthropic.com/claude) - Multimodal Claude with vision capabilities.
* [Gemini](https://deepmind.google/technologies/gemini/) - Google's natively multimodal AI model.
* [LLaVA](https://llava-vl.github.io/) - Open-source visual instruction tuning for large language models.
* [MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4) - Enhancing vision-language understanding with advanced LLMs.
* [Fuyu-8B](https://www.adept.ai/blog/fuyu-8b) - Multimodal model optimized for digital agents.

**Computer Vision**
* [OpenCV](https://opencv.org/) - Open-source computer vision library with 2500+ algorithms.
* [YOLO](https://github.com/ultralytics/ultralytics) - Real-time object detection (YOLOv8, YOLOv9).
* [Detectron2](https://github.com/facebookresearch/detectron2) - Facebook's object detection and segmentation platform.
* [SAM (Segment Anything)](https://segment-anything.com/) - Meta's segmentation model for any object.
* [CLIP](https://github.com/openai/CLIP) - Connects vision and language for zero-shot image classification.
* [Roboflow](https://roboflow.com/) - Computer vision platform for building, deploying, and scaling models.
* [Ultralytics HUB](https://ultralytics.com/hub) - Platform for training and deploying YOLOv8 models.

**Image Generation**
* [Stable Diffusion](https://stability.ai/stable-diffusion) - Open-source text-to-image generation.
* [DALL-E 3](https://openai.com/dall-e-3) - OpenAI's image generation from text descriptions.
* [Midjourney](https://www.midjourney.com/) - AI art generation platform.
* [Imagen](https://imagen.research.google/) - Google's text-to-image diffusion model.
* [ComfyUI](https://github.com/comfyanonymous/ComfyUI) - Powerful and modular stable diffusion GUI.
* [Automatic1111](https://github.com/AUTOMATIC1111/stable-diffusion-webui) - Stable Diffusion web UI.

**Speech & Audio AI**
* [Whisper](https://github.com/openai/whisper) - OpenAI's robust speech recognition model supporting 99 languages.
* [Whisper.cpp](https://github.com/ggerganov/whisper.cpp) - High-performance inference of Whisper in C/C++.
* [SpeechBrain](https://speechbrain.github.io/) - All-in-one conversational AI toolkit for speech processing.
* [Coqui TTS](https://github.com/coqui-ai/TTS) - Deep learning toolkit for text-to-speech.
* [Bark](https://github.com/suno-ai/bark) - Transformer-based text-to-audio model.
* [ElevenLabs](https://elevenlabs.io/) - AI voice generation and text-to-speech API.
* [AssemblyAI](https://www.assemblyai.com/) - Speech recognition and audio intelligence API.
* [Deepgram](https://deepgram.com/) - Real-time speech-to-text API with high accuracy.

**Video AI**
* [Runway](https://runwayml.com/) - AI tools for video editing and generation.
* [D-ID](https://www.d-id.com/) - AI-powered video generation from text.
* [Synthesia](https://www.synthesia.io/) - AI video generation platform with digital avatars.
* [PySceneDetect](https://www.scenedetect.com/) - Scene detection and video analysis.

### Model Compression & Quantization

Optimize models for faster inference and reduced memory footprint.

**Quantization Tools**
* [bitsandbytes](https://github.com/TimDettmers/bitsandbytes) - 8-bit and 4-bit quantization for LLMs and neural networks.
* [GPTQ](https://github.com/IST-DASLab/gptq) - Accurate post-training quantization for GPT models.
* [AWQ](https://github.com/mit-han-lab/llm-awq) - Activation-aware weight quantization for LLMs.
* [GGML/GGUF](https://github.com/ggerganov/ggml) - Tensor library for machine learning with quantization support.
* [llama.cpp](https://github.com/ggerganov/llama.cpp) - LLaMA inference with 4-bit quantization in C++.
* [Neural Compressor](https://github.com/intel/neural-compressor) - Intel's neural network compression toolkit.
* [ONNX Runtime Quantization](https://onnxruntime.ai/docs/performance/model-optimizations/quantization.html) - Quantize ONNX models for inference.

**Model Pruning & Distillation**
* [Distilbert](https://huggingface.co/docs/transformers/model_doc/distilbert) - Distilled version of BERT, 40% smaller and 60% faster.
* [TinyLlama](https://github.com/jzhang38/TinyLlama) - Compact 1.1B parameter LLaMA model.
* [Neural Network Distiller](https://github.com/IntelLabs/distiller) - Python package for neural network compression.
* [Knowledge Distillation](https://huggingface.co/docs/transformers/tasks/knowledge_distillation) - Hugging Face knowledge distillation guide.

**Efficient Architectures**
* [MobileBERT](https://github.com/google-research/google-research/tree/master/mobilebert) - Compact BERT for mobile devices.
* [TinyBERT](https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/TinyBERT) - 7.5x smaller and 9.4x faster than BERT.
* [ALBERT](https://github.com/google-research/ALBERT) - Lite BERT with parameter reduction techniques.
* [DistilGPT-2](https://huggingface.co/distilgpt2) - Distilled GPT-2 with 82M parameters.

### Data Labeling & Annotation

Tools for creating training datasets through labeling and annotation.

**Open Source Annotation Tools**
* [Label Studio](https://labelstud.io/) - Multi-type data labeling platform supporting text, images, audio, video, and time series.
* [CVAT](https://www.cvat.ai/) - Computer Vision Annotation Tool for image and video annotation.
* [Labelbox](https://labelbox.com/) - Data labeling platform with AI-assisted labeling.
* [Prodigy](https://prodi.gy/) - Annotation tool powered by active learning.
* [Doccano](https://github.com/doccano/doccano) - Open-source text annotation tool for NLP tasks.
* [Argilla](https://argilla.io/) - Collaboration platform for AI engineers and domain experts to build datasets.
* [LabelImg](https://github.com/HumanSignal/labelImg) - Graphical image annotation tool for object detection.
* [VGG Image Annotator (VIA)](https://www.robots.ox.ac.uk/~vgg/software/via/) - Standalone image, audio, and video annotation software.

**Commercial Annotation Platforms**
* [Scale AI](https://scale.com/) - End-to-end data labeling for ML with human-in-the-loop.
* [Appen](https://appen.com/) - AI training data services with global crowd.
* [Amazon SageMaker Ground Truth](https://aws.amazon.com/sagemaker/data-labeling/) - Data labeling service with active learning.
* [Snorkel AI](https://snorkel.ai/) - Programmatic labeling and data-centric AI platform.
* [Supervisely](https://supervise.ly/) - Computer vision annotation platform with neural network integration.

**Active Learning**
* [modAL](https://modal-python.readthedocs.io/) - Modular active learning framework for Python.
* [ALiPy](https://github.com/NUAA-AL/ALiPy) - Active learning library for Python.
* [Lightly](https://www.lightly.ai/) - Active learning for computer vision with self-supervised learning.

### Synthetic Data Generation

Generate synthetic training data for ML models.

**Synthetic Data Platforms**
* [Gretel.ai](https://gretel.ai/) - Synthetic data platform for creating privacy-safe datasets.
* [Mostly AI](https://mostly.ai/) - Synthetic data generation for structured data.
* [Synthesis AI](https://synthesis.ai/) - Synthetic data for computer vision.
* [NVIDIA Omniverse](https://www.nvidia.com/en-us/omniverse/) - Platform for creating synthetic data for robotics and autonomous vehicles.
* [Datagen](https://datagen.tech/) - Synthetic image and video data generation.

**Open Source Synthetic Data**
* [SDV (Synthetic Data Vault)](https://sdv.dev/) - Generate synthetic data for tabular, relational, and time series data.
* [CTGAN](https://github.com/sdv-dev/CTGAN) - GAN-based synthetic data generation for tabular data.
* [Faker](https://faker.readthedocs.io/) - Python library for generating fake data.
* [Mimesis](https://mimesis.name/) - High-performance fake data generator.
* [Synthetic Data Generator (SDG)](https://github.com/mostly-ai/mostly-synthetic-data-generator-open-source) - Open-source synthetic data generator.

**Text Data Augmentation**
* [TextAttack](https://github.com/QData/TextAttack) - Framework for adversarial attacks, data augmentation, and model training in NLP.
* [NLPAug](https://github.com/makcedward/nlpaug) - Data augmentation for NLP using transformers.
* [TextAugment](https://github.com/dsfsi/textaugment) - Text augmentation library for improving NLP models.

### LLM Security & Safety

Ensure safe and responsible AI deployment.

**Security & Red Teaming**
* [Garak](https://github.com/leondz/garak) - LLM vulnerability scanner and red-teaming tool.
* [PyRIT (Python Risk Identification Toolkit)](https://github.com/Azure/PyRIT) - Microsoft's framework for AI red-teaming.
* [PromptInject](https://github.com/agencyenterprise/PromptInject) - Framework for testing LLM resilience to prompt injection.
* [LLM Guard](https://llm-guard.com/) - Security toolkit for LLM applications with input/output scanning.
* [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - NVIDIA's toolkit for adding programmable guardrails to LLMs.
* [Guardrails AI](https://www.guardrailsai.com/) - Framework for adding validators and corrective actions to LLM outputs.

**Content Moderation**
* [OpenAI Moderation API](https://platform.openai.com/docs/guides/moderation) - Check if content violates OpenAI usage policies.
* [Perspective API](https://perspectiveapi.com/) - Toxicity detection API from Google Jigsaw.
* [Azure Content Safety](https://azure.microsoft.com/en-us/products/ai-services/ai-content-safety) - AI-powered content moderation service.
* [Detoxify](https://github.com/unitaryai/detoxify) - Toxic comment classification models.

**Bias Detection & Fairness**
* [AI Fairness 360](https://aif360.mybluemix.net/) - IBM toolkit for detecting and mitigating bias in ML models.
* [Fairlearn](https://fairlearn.org/) - Microsoft toolkit for assessing and improving fairness of AI systems.
* [What-If Tool](https://pair-code.github.io/what-if-tool/) - Google's tool for probing ML models without code.
* [Aequitas](http://aequitas.dssg.io/) - Bias and fairness audit toolkit.

**Privacy & Compliance**
* [Opacus](https://opacus.ai/) - PyTorch library for training models with differential privacy.
* [TensorFlow Privacy](https://github.com/tensorflow/privacy) - Library for training ML models with privacy.
* [PySyft](https://github.com/OpenMined/PySyft) - Framework for privacy-preserving ML.
* [Presidio](https://github.com/microsoft/presidio) - Context-aware PII detection and anonymization.

### Edge AI & On-Device ML

Deploy ML models on edge devices and mobile platforms.

**Mobile ML Frameworks**
* [TensorFlow Lite](https://www.tensorflow.org/lite) - Deploy ML models on mobile and edge devices.
* [PyTorch Mobile](https://pytorch.org/mobile/home/) - End-to-end workflow for mobile deployment.
* [Core ML](https://developer.apple.com/documentation/coreml) - Apple's framework for integrating ML models into iOS apps.
* [ML Kit](https://developers.google.com/ml-kit) - Google's mobile SDK for common ML tasks.
* [ONNX Runtime Mobile](https://onnxruntime.ai/docs/tutorials/mobile/) - Cross-platform inference on mobile devices.
* [MNN](https://github.com/alibaba/MNN) - Alibaba's lightweight deep learning inference engine.
* [NCNN](https://github.com/Tencent/ncnn) - High-performance neural network inference framework for mobile.
* [MediaPipe](https://mediapipe.dev/) - Google's framework for building multimodal ML pipelines.

**Edge Computing Platforms**
* [NVIDIA Jetson](https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/) - AI computing platform for edge devices.
* [Google Coral](https://coral.ai/) - Edge TPU platform for local AI acceleration.
* [Intel OpenVINO](https://www.intel.com/content/www/us/en/developer/tools/openvino-toolkit/overview.html) - Toolkit for optimizing models for Intel hardware.
* [AWS IoT Greengrass](https://aws.amazon.com/greengrass/) - Run ML inference on edge devices.
* [Azure IoT Edge](https://azure.microsoft.com/en-us/products/iot-edge/) - Deploy cloud workloads to run on edge devices.

**Model Optimization for Edge**
* [TensorRT](https://developer.nvidia.com/tensorrt) - High-performance deep learning inference optimizer for NVIDIA GPUs.
* [Apache TVM](https://tvm.apache.org/) - Deep learning compiler for CPUs, GPUs, and accelerators.
* [IREE](https://iree-org.github.io/iree/) - MLIR-based compiler for ML models targeting edge devices.

### MLOps & ML Platforms

End-to-end platforms for managing the ML lifecycle.

**Comprehensive MLOps Platforms**
* [Kubeflow](https://www.kubeflow.org/) - ML toolkit for Kubernetes with pipelines, training, and serving.
* [MLRun](https://www.mlrun.org/) - Open MLOps orchestration framework for ML pipelines.
* [Metaflow](https://metaflow.org/) - Human-friendly ML stack from Netflix for building and managing workflows.
* [ZenML](https://zenml.io/) - Extensible, open-source MLOps framework for creating production-ready pipelines.
* [Flyte](https://flyte.org/) - Kubernetes-native workflow automation platform for ML and data processing.
* [Kedro](https://kedro.org/) - Framework for creating reproducible, maintainable data science code.
* [Ploomber](https://ploomber.io/) - Build data pipelines with Jupyter notebooks.

**Experiment Management**
* [MLflow](https://mlflow.org/) - Open-source platform for managing the ML lifecycle.
* [Weights & Biases](https://wandb.ai/) - Experiment tracking, model management, and dataset versioning.
* [Neptune.ai](https://neptune.ai/) - Metadata store for MLOps.
* [ClearML](https://clear.ml/) - MLOps platform with experiment tracking and orchestration.
* [Guild AI](https://guild.ai/) - Experiment tracking and ML pipeline automation.

**Model Registry**
* [MLflow Model Registry](https://mlflow.org/docs/latest/model-registry.html) - Centralized model store with versioning and stage transitions.
* [Weights & Biases Registry](https://wandb.ai/site/model-registry) - Model registry with lineage tracking.
* [Seldon Core Model Registry](https://docs.seldon.io/projects/seldon-core/en/latest/) - Kubernetes-native model registry.

### Data Versioning for ML

Version control for datasets and ML artifacts.

* [DVC (Data Version Control)](https://dvc.org/) - Git for data science - version datasets, models, and experiments.
* [LakeFS](https://lakefs.io/) - Git-like version control for data lakes with branching and merging.
* [Pachyderm](https://www.pachyderm.com/) - Data versioning, lineage, and pipelines for ML.
* [Delta Lake](https://delta.io/) - Storage framework with versioning, time travel, and ACID transactions.
* [Git LFS](https://git-lfs.com/) - Git extension for versioning large files.
* [Quilt](https://quiltdata.com/) - Data package manager for versioning and sharing datasets.
* [Weights & Biases Artifacts](https://wandb.ai/site/artifacts) - Dataset and model versioning integrated with W&B.
* [Neptune.ai Data Versioning](https://neptune.ai/) - Track and version datasets with experiment metadata.

### NLP & Text Processing

Natural language processing tools beyond LLMs.

**NLP Libraries**
* [spaCy](https://spacy.io/) - Industrial-strength NLP library with fast entity recognition and dependency parsing.
* [NLTK](https://www.nltk.org/) - Natural Language Toolkit for symbolic and statistical NLP.
* [Stanford CoreNLP](https://stanfordnlp.github.io/CoreNLP/) - Suite of NLP tools for 50+ languages.
* [Gensim](https://radimrehurek.com/gensim/) - Topic modeling and document similarity with Word2Vec and Doc2Vec.
* [TextBlob](https://textblob.readthedocs.io/) - Simple API for common NLP tasks.
* [Stanza](https://stanfordnlp.github.io/stanza/) - Stanford NLP toolkit with neural network pipelines.

**Named Entity Recognition (NER)**
* [spaCy NER](https://spacy.io/usage/linguistic-features#named-entities) - Fast and accurate named entity recognition.
* [Flair](https://github.com/flairNLP/flair) - State-of-the-art NLP framework with NER capabilities.
* [Stanford NER](https://nlp.stanford.edu/software/CRF-NER.html) - Java-based NER tagger.
* [GLiNER](https://github.com/urchade/GLiNER) - Generalist model for Named Entity Recognition.

**Information Extraction**
* [Haystack](https://haystack.deepset.ai/) - End-to-end NLP framework for Q&A and information extraction.
* [AllenNLP](https://allennlp.org/) - NLP research library built on PyTorch.
* [Snorkel](https://www.snorkel.org/) - Programmatic labeling and weak supervision for NLP.

**Text Classification**
* [Hugging Face Transformers](https://huggingface.co/transformers/) - State-of-the-art models for text classification.
* [fastText](https://fasttext.cc/) - Facebook's library for efficient text classification and representation learning.
* [SetFit](https://github.com/huggingface/setfit) - Few-shot text classification with Sentence Transformers.

### Reinforcement Learning

Frameworks for training RL agents.

* [OpenAI Gym](https://github.com/openai/gym) - Toolkit for developing and comparing RL algorithms.
* [Stable Baselines3](https://stable-baselines3.readthedocs.io/) - Reliable implementations of RL algorithms.
* [Ray RLlib](https://docs.ray.io/en/latest/rllib/index.html) - Scalable RL library with production-grade algorithms.
* [TensorFlow Agents](https://www.tensorflow.org/agents) - RL library for TensorFlow.
* [Dopamine](https://github.com/google/dopamine) - Research framework for fast prototyping of RL algorithms.
* [ACME](https://github.com/deepmind/acme) - DeepMind's framework for building RL agents.
* [CleanRL](https://github.com/vwxyzjn/cleanrl) - High-quality single-file implementations of RL algorithms.
* [Tianshou](https://github.com/thu-ml/tianshou) - Highly modular RL library with PyTorch.

### Federated Learning

Privacy-preserving distributed machine learning.

* [Flower](https://flower.dev/) - Federated learning framework supporting PyTorch, TensorFlow, and more.
* [TensorFlow Federated](https://www.tensorflow.org/federated) - Framework for ML on decentralized data.
* [PySyft](https://github.com/OpenMined/PySyft) - Framework for encrypted, privacy-preserving ML.
* [FedML](https://fedml.ai/) - Federated learning platform for distributed and privacy-preserving ML.
* [FATE](https://fate.fedai.org/) - Industrial-grade federated learning framework.
* [OpenFL](https://github.com/intel/openfl) - Open Federated Learning framework by Intel.

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
