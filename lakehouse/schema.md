# Data Lake Job Metadata Framework

This document defines the metadata control-plane tables that govern jobs, datasets, sources, and targets in the data lake.

---
MD_JOBS
Comment: Holds high-level job definitions, linking sources, targets, and datasets.

MD_JOBS_DET
Comment: Stores detailed runtime parameters for each job (e.g., S3 bucket names, tokens, expected headers).

MD_JOBS_RELATIONSHIPS
Comment: Defines upstream-to-downstream job relationships used to orchestrate event-driven and metadata-driven pipeline execution.

MD_JOB_CONFIG
Comment: Stores configuration and trigger details for jobs (e.g., EventBridge rule names, Step Function names, status flags).

MD_JOB_EXECUTION
Comment: Tracks every execution instance of a job, including start time, end time, and status.

MD_DATASETS
Comment: Defines datasets managed in the data lake, including dataset identifiers, database/table names, and status.

MD_SRC
Comment: Master list of sources feeding the data lake, including source name and enabled flag.

MD_SRC_DET
Comment: Key-value details for each source (e.g., auth type, connection info, endpoints).

MD_TGT
Comment: Master list of targets in the data lake (e.g., Raw, Curated, Results zones).

MD_TGT_DET
Comment: Key-value details for each target (e.g., S3 bucket paths, formats, permissions).

---
# Data Lake Logical Data Model Framework

This document defines the metadata control-plane tables that govern the data model generation in the data lake.

---
MD_MODEL_SUBJECT	
Comment: Stores subject area definitions and source locations used by the Data Model Factory to discover and generate data models.

MD_MODEL_OBJECT	
Comment: Stores metadata objects (worksheets, files, tables, or other assets) discovered within a subject area and targeted for model generation.

MD_MODEL_COLUMN	
Comment: Stores source column metadata and mapping attributes used to generate dimension, fact, and staging table structures.

MD_MODEL_Mapping	
Comment: Stores mappings between source data elements and logical model objects and columns.

MD_MODEL_RUN	
Comment: Stores execution history and processing status for Data Model Factory discovery and model generation runs.
