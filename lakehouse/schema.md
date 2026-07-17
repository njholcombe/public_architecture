# Data Platform Metadata Framework
Comment: This document defines the metadata control plane that governs logical models, physical platform objects, datasets, sources, targets, jobs, orchestration, and execution across the metadata-driven data platform.

---
# Data Platfrorm Data Model Discovery Framework
Comment: This document defines the metadata control-plane tables that govern the logical data model generation in the data lake.

---
MD_MODEL_SUBJECT
Comment: Stores subject area definitions and source locations used by the Data Model Factory to discover and generate data models.

MD_MODEL_OBJECT
Comment: Stores metadata objects (worksheets, files, tables, or other assets) discovered within a subject area and targeted for model generation.

MD_MODEL_ATTRIBUTE
Comment: Stores the logical attributes that define each business object within the data model. Attributes represent the business fields used during physical object generation.

MD_MODEL_MAPPING
Comment: Stores mappings between source data elements and logical model objects and columns.

MD_MODEL_RUN
Comment: Stores execution history and processing status for Data Model Factory discovery and model generation runs.

---
# Data Platform Data Model & Object Generator Framework
Comment: This document defines the metadata control-plane tables that govern the physical data model generation in the data lake.

---
MD_OBJECT_DEF
Comment: Defines the physical platform objects generated and managed by the framework. Supports multiple object types through reusable metadata independent of the underlying platform.

MD_OBJECT_ATTRIBUTE_DEF
Comment: Defines the physical attributes associated with each platform object, including metadata required for object generation and implementation.

MD_OBJECT_PROPERTY_DEF
Comment: Defines configurable properties associated with platform objects. Properties define platform-specific behaviors, configuration settings, and implementation characteristics used during object generation and management.

MD_OBJECT_PARTITION_DEF
Comment: Defines partition metadata associated with platform objects, including the attributes and configuration required to generate and manage partitioned objects.

---
# Data Platform Job Definition Discovery Framework
Comment: This document defines the metadata control-plane tables that govern the job defintion discovery in the data lake.

---
MD_OBJECT_DEF
Comment: Defines the physical platform objects generated and managed by the framework. Supports multiple object types through reusable metadata independent of the underlying platform.

MD_OBJECT_ATTRIBUTE_DEF
Comment: Defines the physical attributes associated with each platform object, including metadata required for object generation and implementation.

MD_OBJECT_PROPERTIES_DEF
Comment: Defines configurable properties associated with platform objects. Properties define platform-specific behaviors, configuration settings, and implementation characteristics used during object generation and management.

MD_OBJECT_PARTITION_DEF
Comment: Defines partition metadata associated with platform objects, including the attributes and configuration required to generate and manage partitioned objects.

---
# Data Platform Job Orchestration Generator Framework
Comment: This document defines the metadata control plane that governs orchestration generation, component mapping, dependencies, and generation activity for data processing pipelines.

---
MD_ORCHESTRATION_GEN_RUN
Comment: Records each orchestration generation run, including execution status, processing metrics, and summary information.

MD_ORCHESTRATION_GEN_COMP
Comment: Records the orchestration components generated during each orchestration generation run, including component type, configuration, and generation status.

MD_ORCHESTRATION_GEN_LOG
Comment: Records informational, warning, and error messages generated during orchestration generation for auditing, troubleshooting, and operational monitoring.

---
# Data Platform Job Registration and Execution Framework
Comment: This document defines the metadata control plane used to register, execute, monitor, and manage data processing workloads throughout the operational lifecycle of the metadata-driven data platform

---
MD_JOBS
Comment: Stores high-level job definitions, linking sources, targets, and datasets.

MD_JOBS_DET
Comment: Stores detailed runtime parameters for each job (e.g., S3 bucket names, tokens, expected headers).

MD_JOBS_RELATIONSHIPS
Comment: Defines upstream-to-downstream job relationships used to orchestrate event-driven and metadata-driven pipeline execution.

MD_JOB_CONFIG
Comment: Stores configuration and trigger details for jobs (e.g., EventBridge rule names, Step Function names, status flags).

MD_JOB_EXECUTION
Comment: Records every execution instance of a job, including start time, end time, and status.

MD_JOB_EXECUTION_LOG
Comment: Records informational, warning, and error messages generated during job execution for auditing, troubleshooting, and operational monitoring.

MD_JOB_EXECUTION_METRICS
Comment: Records execution metrics and performance statistics captured during job execution, including processing durations, throughput, resource utilization, and record counts.

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

