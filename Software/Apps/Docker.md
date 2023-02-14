# Docker

Information about [Docker](https://www.docker.com/),  a platform designed to help developers build, share, and run modern applications. We handle the tedious setup, so you can focus on the code.

---

## Access container

Obtain the container ID by running the following command:

```bash
docker ps
```

Access the Docker container by running the following command:

```bash
docker exec -it <container_id> /bin/bash
```

## Start Docker

```bash
systemctl start docker
```

## How to start the services?

```bash
docker-compose pull  
docker-compose up -d
```

## How to stop the services?

```bash
docker-compose down -v  
docker-compose down  
# Be aware -v kills the database (without -v, the containers will be destroyed, but the db volume survives)
```

## How to view logs?

```bash
docker-compose logs -f
```