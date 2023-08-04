# ArangoDB Cluster with Docker Compose

This guide explains how to set up an ArangoDB cluster using Docker Compose. ArangoDB is a distributed, multi-model database that supports key-value, document, and graph data models.

## Prerequisites

Before you begin, make sure you have the following installed on your machine:

- [Docker](https://docs.docker.com/get-docker/): Containerization platform used to run the ArangoDB cluster.
- [Docker Compose](https://docs.docker.com/compose/install/): Tool for defining and running multi-container Docker applications.

## Setup Instructions

Follow these steps to set up an ArangoDB cluster using Docker Compose:

1. Clone the project.
```bash
git clone git@github.com:thien-nguyenthanh/arangodb-cluster-compose.git 
```

2. Run the following command to start the ArangoDB cluster
```bash
cd arangodb-cluster-compose && docker compose up -d 
```

3. Wait for the containers to start up. You can check the container logs using the following command:
```bash
docker-compose logs -f
```

4. Once the containers are running, you can access the ArangoDB Web UI by opening a browser and navigating to `http://localhost:8529` or `http://localhost:8530`. These ports are exposed for the coordinators in the `docker-compose.yml` file.


5. From the ArangoDB Web UI, you can configure and manage your ArangoDB cluster.

## Cleaning Up

To stop and remove the ArangoDB cluster, run the following command in the directory containing the `docker-compose.yml` file:
```bash
docker-compose down
```

## Resources

- [Docker Compose documentation](https://docs.docker.com/compose/)
- [ArangoDB Docker Hub](https://hub.docker.com/_/arangodb)
- [ArangoDB documentation](https://www.arangodb.com/docs/stable/)
