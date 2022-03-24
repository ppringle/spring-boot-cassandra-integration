# spring-boot-cassandra-integration

## Interacting with Cassandra Locally

Starting a local Cassandra cluster locally, relies on building a Docker image locally which customizes a specific
official version of a Cassandra image to include a wrapper script which provides an enhancement which allows for a
custom keyspace to be created on container startup.

See below for an example command used to build a new image based on the definitions within the Dockerfile:

```
docker build -f ./docker/Dockerfile -t ppringle/cassandra:1.0 .
```

Once the local image is available, to start a Cassandra cluster using Docker, execute the following command:

```
docker-compose -f ./docker/docker-compose.yaml up
```