## Infra Project

This project provides infrastructure for running Keycloak with a PostgreSQL database using Docker Compose.

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Setup Instructions

#### 1. Create the external Docker network

This project requires an external Docker network named `shared_network`. If it does not exist, create it with:

```sh
docker network create --driver bridge shared_network
```

#### 2. Configure environment variables

Copy the example environment file and adjust the values as needed:

```sh
cp .env.example .env
```

#### 3. Start the services

Run the following command to start Keycloak and PostgreSQL:

```sh
docker-compose up
```

#### 4. Access Keycloak

Once the containers are running, access Keycloak at: [http://localhost:8080](http://localhost:8080)

### Stopping the services

To stop and remove the containers, run:

```sh
docker-compose down
```

---

For more details, see the `docker-compose.yml` file.
