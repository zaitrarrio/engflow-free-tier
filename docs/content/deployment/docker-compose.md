## Getting Started w/ Docker Compose

EngFlow Free Tier may be started as a service through Docker Compose.  A sample configuration of EngFlow
deployed as a service is demonstrated in the ```docker-compose.yml``` file included in this repository.
The example demonstrates the configuration of the EngFlow remote execution service to use containers for
both local execution and remote runtime workers.

To start the EngFlow Free Tier and run build targets from the EngFlow example project, simply execute the
following command from the top-level directory of this repository:

```commandline
docker-compose up
```

EngFlow Free Tier can be deployed easily to various cloud providers through Docker Compose or directly as a container
through Kubernetes, Amazon ECS, Azure Container Apps, Google Cloud Run and any other OCI-compatible container platform.
