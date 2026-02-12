Datalake Control Plane

The datalake control plane is responsible for:

  Resolving the job configurations

  Retrieving the source/target metadata

  Managing the execution lifecycle

  Updating the execution status

  Implemented via:

    JobRepo Class (Lambda Layer)

    DynamoDB MD_* tables
