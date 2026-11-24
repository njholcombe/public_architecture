AWS FreightData Pipeline
Overview
The FreightData pipeline is an operational implementation of a metadata-driven AWS data lakehouse framework using the Freight Analysis Framework (FAF) transportation dataset.
The project demonstrates the development of a data pipeline from initial source model discovery through physical object generation, job definition, orchestration, runtime registration, and execution.
Technology Stack
	Technology		Responsibility
	Python			Metadata discovery, generation and deployment automation
	Amazon 			DynamoDB Metadata management and runtime configuration
	Amazon S3		Bronze and Silver data storage
	Amazon Athena		External tables, SQL transformations and analytics
	AWS Step Functions	Job execution orchestration
	AWS Lambda		Reusable execution components
	Amazon EventBridge	Event-driven integration
	AWS IAM			Security and service authorization
Data Architecture
The pipeline implements a layered data architecture:
    • Landing: Original source data and associated metadata.
    • Bronze: Raw structured source datasets.
    • Silver: Curated Parquet fact and dimension datasets.
    • Presentation: Analytical consumption through Athena and compatible reporting technologies.
Metadata-Driven Development
The framework separates pipeline development from runtime execution.
Development consists of six architectural stages:
    1. Data Model Discovery
    2. Data Model and Object Generation
    3. Job Definition Discovery
    4. Job Orchestration Generation
    5. Job Registration
    6. Job Execution
Each stage produces metadata or deployable artifacts consumed by subsequent stages.
Deployment
The FreightData implementation is packaged independently from the underlying lakehouse infrastructure.
Existing framework deployment utilities are used to deploy Athena objects, transformation SQL, runtime metadata, job registration records, and Step Functions definitions.
This separation allows an existing pipeline to be deployed without repeating the model discovery and generation processes.
Documentation
    • Development Workflow
    • Metadata Architecture
This public repository provides architectural documentation. Implementation code, deployment artifacts, and environment-specific configuration are maintained separately.


