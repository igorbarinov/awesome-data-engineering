# Changelog

All notable changes to awesome-data-engineering will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **AI/ML & LLM Infrastructure** - Comprehensive new section covering:
  - Vector Databases (Chroma, Milvus, Weaviate, Qdrant, Pinecone, etc.)
  - LLM Orchestration & Frameworks (LangChain, LlamaIndex, Haystack, AutoGen, etc.)
  - Model Training & Fine-tuning (PyTorch, Hugging Face, Axolotl, DeepSpeed, etc.)
  - Feature Stores (Feast, Tecton, Hopsworks, etc.)
  - ML Experiment Tracking (MLflow, Weights & Biases, Neptune, etc.)
  - Model Serving & Deployment (BentoML, vLLM, TorchServe, Triton, etc.)
  - LLM Evaluation & Monitoring (RAGAS, LangSmith, Arize, etc.)
- Modern Data Stack tools (2020-2025):
  - Data Ingestion: Airbyte, Meltano, dlt, Redpanda
  - Data Transformation: dbt, SQLMesh, Polars
  - Orchestration: Dagster, Prefect, Kestra, Mage
  - Data Lakes: Apache Iceberg, Delta Lake, Apache Hudi, XTable
  - Lakehouse: Unity Catalog, Apache Polaris, Nessie, LakeFS
  - Data Quality: Great Expectations, Soda, elementary-data
  - Data Observability: Monte Carlo, OpenMetadata
  - Data Catalogs: DataHub, OpenMetadata, Amundsen
  - Reverse ETL: Census, Hightouch, Grouparoo
  - Semantic Layer: Cube, dbt Semantic Layer
  - Embedded Analytics: DuckDB, MotherDuck
- GitHub Actions for:
  - Automated link checking
  - Markdown linting
  - Quality assurance
- Community health files:
  - SECURITY.md - Security policy and vulnerability reporting
  - CODE_OF_CONDUCT.md - Community guidelines
  - LICENSE - CC0 1.0 Universal license
  - Issue templates for adding tools, reporting broken links, and updates
  - Pull request template with comprehensive checklist
- Enhanced contributing guidelines with:
  - Clear quality standards
  - Format requirements and examples
  - Submission guidelines
  - What to include vs. exclude

### Changed
- **Complete restructuring** - Reorganized by data lifecycle (ingestion → storage → transformation → orchestration → processing → quality → governance → activation → visualization)
- **All markdown syntax fixed** - Removed spaces in link formatting throughout
- **Improved descriptions** - Made all descriptions action-oriented and clear
- **Updated table of contents** - Added proper anchor links and new sections
- **Enhanced visual hierarchy** - Improved heading structure and organization
- **Modernized cloud data warehouses** - Separated and expanded section (Snowflake, BigQuery, Databricks SQL, etc.)
- **Expanded time-series databases** - Added TimescaleDB, QuestDB, VictoriaMetrics
- **Updated streaming section** - Added modern tools (RisingWave, ksqlDB, Materialize)
- **Expanded serialization formats** - Added Apache Arrow, MessagePack, FlatBuffers
- **Enhanced dashboarding frameworks** - Added Streamlit, Dash, Gradio, Panel

### Fixed
- Awesome badge URL (deprecated rawgit.com CDN → awesome.re)
- SSDB URL (broken http://ssdb.io → GitHub repository)
- Removed broken insightdataengineering.com link
- All malformed markdown links with spaces

### Removed
- Outdated or deprecated tools
- Broken links that couldn't be fixed

## [1.0.0] - 2024-11-16

### Initial Modern Release
- Transformed from dated 2016 collection to definitive 2024-2025 resource
- 100+ modern tools added across all categories
- Production-ready infrastructure with automated quality checks
- Comprehensive AI/ML/LLM coverage
- Enterprise-grade documentation and governance

---

## Contributing

See [CONTRIBUTING.md](contributing.md) for information on how to contribute to this changelog and the project.

## Maintainers

This project is maintained by the awesome-data-engineering community. See [CONTRIBUTORS](https://github.com/duyet/awesome-data-engineering/graphs/contributors) for the full list of contributors.
