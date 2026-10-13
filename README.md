# Awesome-External-Data-Virtualization

## Top External Data Virtualization Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Federated Queries, Zero-Copy Integration & Logical Data Layers*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **External Data Virtualization**. These tools enable organizations to query data across disparate sources—databases, data lakes, APIs, and SaaS applications—without physically moving or replicating it, creating a unified logical data layer for analytics and applications.



**Examples** include Salesforce Connect, Denodo Platform, Starburst Galaxy, Dremio Cloud, CData Connect Cloud, IBM Cloud Pak for Data, Presto Cloud, Trino, TIBCO Data Virtualization, and AWS Athena (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, federated query engines, and open data virtualization—ideal for data engineers, architects, and developers seeking transparent, vendor-independent data access.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Salesforce Connect](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/platform_connect_intro.htm)**  

  Data virtualization layer within Salesforce that surfaces external data as External Objects. Supports OData, GraphQL, and custom adapters. Zero-copy architecture—data is queried live from source systems only when needed, never stored or cached by Salesforce. Avoids ETL replication and keeps data compliant with data movement regulations. Works with AWS RDS via AppSync, DynamoDB, and any GraphQL API .



- **[Denodo Platform](https://www.denodo.com/)**  

  Enterprise data virtualization platform with 200+ connectors. Provides a logical data layer for integrating, managing, and delivering data across warehouses, lakes, and cloud applications without replication. Features GenAI assistant, advanced semantics, and universal data services (SQL, REST, GraphQL). Agora cloud service separates control plane (managed by Denodo) from execution plane (runs in customer's cloud) for data sovereignty .



- **[Starburst Galaxy](https://www.starburst.io/)**  

  Fully managed Trino service for federated analytics across data lakes, databases, and warehouses. Features query federation, data lake analytics on Iceberg/Delta/Hudi, and cross-source joins without data movement.



- **[Dremio Cloud](https://www.dremio.com/)**  

  Fully managed lakehouse with data virtualization capabilities. Apache Iceberg-based catalog with REST API compatibility. Features federated queries across diverse sources, AI-powered SQL functions, autonomous reflections, elastic engines that scale to zero, and hosted MCP server for AI agents. Consumption-based pricing (DCUs) with free trial credits .



- **[CData Connect Cloud](https://www.cdata.com/cloud/)**  

  Data Connectivity-as-a-Service platform with 300+ source connectors and 100+ destination integrations. Provides live, real-time data access without ETL pipelines or data replication. Virtual datasets blend data across sources. Exposes data via RESTful APIs, OData, and standard database protocols (TDS). SOC2 compliant with granular access controls. AI SQL query generator for natural language querying .



- **[IBM Cloud Pak for Data](https://www.ibm.com/products/cloud-pak-for-data)**  

  Enterprise data platform with Data Virtualization service. Accesses physical data from multiple sources through a single virtual semantic layer without moving or copying. Supports dozens of relational and non-relational sources. Integrates with IBM Knowledge Catalog for governed data publishing. Query virtual objects via built-in SQL editor or consume in dashboards, catalogs, and applications .



- **[Presto Cloud](https://prestodb.io/)**  

  Managed distributed SQL query engine for big data. Originally designed at Facebook as successor to Hive/MapReduce for interactive queries on multi-petabyte warehouses. SQL-on-Anything architecture with pluggable connectors for HDFS, S3, relational databases, NoSQL, and Kafka. Low-latency startup for interactive analytics .



- **[Trino](https://trino.io/)**  

  Open-source distributed SQL query engine for federated analytics against heterogeneous data sources. Queries gigabytes to petabytes from multiple sources. Adaptive multi-tenant system running hundreds of concurrent queries, scaling to thousands of workers. Not a general-purpose database—designed for OLAP and data warehousing workloads .



- **[TIBCO Data Virtualization](https://www.tibco.com/products/data-virtualization)**  

  Enterprise data virtualization platform with 350+ pre-built connectors. Creates a single logical data layer that is governed, secure, and self-service. Time-to-solution 5–10X faster than traditional ETL. Features pushdown engine, MPP scaling, caching options, and Studio design tool. Customers report up to 75% reduced data access costs .



- **[AWS Athena](https://aws.amazon.com/athena/)**  

  Serverless interactive query service for analyzing data directly in Amazon S3 using standard SQL. Also supports Apache Spark without infrastructure management. Pay only for queries run. Scales automatically for parallel query execution on large datasets .



## Open-Source GitHub Projects



- **[Trino](https://github.com/trinodb/trino)**  

  Distributed SQL query engine (Apache-2.0) for federated analytics. The open-source engine underlying Starburst Galaxy. 10k+ GitHub stars. Connects to HDFS, S3, relational databases, Cassandra, Kafka, and more. Coordinator/worker architecture for horizontal scaling. Extensible connector design reduces integration complexity .



- **[PrestoDB](https://github.com/prestodb/presto)**  

  Distributed SQL query engine (Apache-2.0) originally developed at Facebook. Foundation for Presto Cloud and predecessor to Trino. 15k+ GitHub stars. SQL-on-Anything architecture with pluggable data source connectors. Optimized for low-latency interactive queries on big data .



- **[Apache Calcite](https://github.com/apache/calcite)**  

  Dynamic data management framework (Apache-2.0) providing SQL parsing, validation, and query optimization. Foundation for many data virtualization engines including Trino and Dremio. Pluggable adapter architecture for custom data sources.



- **[Apache Drill](https://github.com/apache/drill)**  

  Schema-free SQL query engine (Apache-2.0) for Hadoop, NoSQL, and cloud storage. Features self-describing data exploration without schema definitions. 3k+ GitHub stars. Supports nested data and schema discovery at query time.



- **[Apache Arrow](https://github.com/apache/arrow)**  

  Cross-language development platform (Apache-2.0) for in-memory data. Columnar format enabling zero-copy data exchange between query engines, pandas, and databases. Foundation for high-performance data virtualization—Dremio uses Arrow Flight for JDBC/ODBC/REST access .



- **[Substrait](https://github.com/substrait-io/substrait)**  

  Cross-language specification (Apache-2.0) for representing query plans. Enables interoperability between different query engines and data sources. Emerging standard for data virtualization portability.



- **[Apache Iceberg](https://github.com/apache/iceberg)**  

  Open table format (Apache-2.0) for huge analytic datasets. Enables multiple query engines (Trino, Spark, Flink) to access the same data. Dremio's catalog is Iceberg REST Catalog SPEC compatible, allowing connection from any Iceberg-supporting tool .



- **[MCP Server (Dremio)](https://github.com/dremio/dremio-mcp)**  

  Open-source MCP server for Dremio (license varies). Connects AI agents (Claude, Cursor) to Dremio instances for natural language data querying. Part of Dremio Cloud's hosted MCP integration .



- **[Presto Gateway](https://github.com/prestodb/presto-gateway)**  

  Proxy and load balancer for Presto clusters (Apache-2.0). Routes queries to appropriate clusters, supports dynamic cluster registration, and enables query queuing.



### Additional Strong Open-Source Options



- **[Apache Hive](https://github.com/apache/hive)** — Data warehouse software (Apache-2.0) for reading, writing, and managing large datasets in distributed storage.

- **[Apache Spark SQL](https://github.com/apache/spark)** — Spark module (Apache-2.0) for structured data processing with DataFrame API and SQL support.

- **[Metabase](https://github.com/metabase/metabase)** — Open-source BI tool (AGPL-3.0) with native query support and data virtualization via JDBC drivers.

- **[Apache Superset](https://github.com/apache/superset)** — Open-source BI platform (Apache-2.0) with SQL Lab for federated querying across databases.

- Community **n8n** workflows for data virtualization automation and cross-source orchestration.



**Frameworks for building custom systems**: Combine **Trino** or **PrestoDB** as the federated query engine with **Apache Iceberg** for open table format storage, **Apache Arrow** for high-performance data exchange, **Apache Calcite** for SQL optimization, and **PostgreSQL** for metadata persistence — creating a fully self-hosted, enterprise-grade external data virtualization platform.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Data virtualization platforms handling enterprise data must comply with data protection regulations (GDPR, CCPA, etc.) and data residency requirements.

- Self-hosted open-source solutions require proper security hardening, query performance tuning, and ongoing maintenance. Zero-copy architectures reduce data movement risk but introduce query-time dependencies on source system availability.



---



**Made for data engineers, architects, analytics teams, and developers building transparent data virtualization solutions.**  

Let's make External Data Virtualization more open, data-driven, and efficient.
