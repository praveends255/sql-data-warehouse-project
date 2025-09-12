# Data Layer Table – Bronze, Silver, Gold

| Aspect | Bronze Layer | Silver Layer | Gold Layer |
|---|---|---|---|
| **Definition** | Raw, unprocessed data as-is from sources. | Cleaned and standardized data (intermediate layer). | Business-ready, curated data for analytics. |
| **Objective** | Traceability & debugging (intermediate layer). | Prepare data for analysis. | Provide data to be consumed for reporting & analytics. |
| **Object Type** | Tables | Tables | Views |
| **Load Method** | Full Load (Truncate & Insert) | Full Load (Truncate & Insert) | None (served from curated views) |
| **Data Transformation** | None (as-is) | Data Cleaning; Data Standardization; Data Normalization; Derived Columns; Data Enrichment; Data Integration; Data Aggregation; Business Logic & Rules | Minimal transformation; data already curated |
| **Data Modeling** | None (as-is) | None (as-is) | Star schema; Aggregated objects; Flat tables |
| **Target Audience** | Data Engineers; Data Analysts | Data Engineers; Data Analysts | Business Users |
| **Typical Activities — Analysing** | Interview source-system experts; analyze raw patterns and traceability. | Explore and understand the data; validate business logic. | Explore and understand business objects; validate analytics-ready datasets. |
| **Typical Activities — Coding** | Data ingestion scripts; initial parsing and persistence. | Data cleansing scripts; transformations, derived columns, aggregations. | Build/optimize views, reporting extracts, performance tuning. |
| **Typical Activities — Validating** | Data completeness and schema checks. | Data flow validation and correctness checks. | Data integration checks, SLA validation, business sign-off. |
| **Docs & Versioning** | Document processes; version code and configs in Git. | Document transforms and pipelines; version in Git. | Document data models and semantic definitions; version in Git. |
| **Source System Interview** | Business context & ownership: who owns the data? what process does it support? | Same as Bronze, with focus on required transformations and constraints. | Confirm business owners, SLAs, and reporting requirements. |
| **System & Data Documentation** | Architecture & storage (SQL Server, Oracle, AWS, Azure, etc.); integration capabilities (API, Kafka, file extract, direct DB); incremental vs full loads; data scope and historical needs; expected extract size and volume limitations; performance impact considerations; authentication & authorization (tokens, SSH keys, VPN, IP whitelisting). | Refer to Bronze plus transformation details and lineage. | Refer to Bronze/Silver plus final data model, catalog entries, and access controls. |

