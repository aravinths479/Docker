# Docker Documentation

## Table of Contents

1. [Introduction to Docker](#introduction-to-docker)
2. [Creating Docker Images](#creating-docker-images)
   - [Using a Dockerfile](#using-a-dockerfile)
   - [Building Images](#building-images)
3. [Creating Docker Containers](#creating-docker-containers)
   - [Running Images as Containers](#running-images-as-containers)
   - [Defining Ports](#defining-ports)
4. [Managing Docker Containers](#managing-docker-containers)
   - [Starting Containers](#starting-containers)
   - [Stopping Containers](#stopping-containers)
   - [Removing Containers](#removing-containers)
5. [Docker Volumes](#docker-volumes)
   - [Use Cases](#use-cases)
6. [Docker Compose](#docker-compose)
   - [Key Features](#key-features)
7. [Docker Commands](#7-essential-docker-commands-and-their-functions)

## 1. Introduction to Docker

Docker is a platform that enables developers to develop, deploy, and run applications in containers. Containers are lightweight, portable, and isolated environments that package applications and their dependencies.

## 2. Creating Docker Images

### Using a Dockerfile

A Dockerfile is a text file that contains instructions for building a Docker image. To create a Docker image using a Dockerfile:

Write a Dockerfile specifying the base image, working directory, dependencies, and runtime commands.
Build the image using the `docker build` command.

### Building Images

To build a Docker image using a Dockerfile:

```bash
docker build -t my-node-app .
```

## 3. Creating Docker Containers

### Running Images as Containers

To create a Docker container from an image:

```bash
docker run -d -p 3000:3000 my-node-app
```

### Defining Ports

To define ports externally when running containers:

```bash
docker run -d -p 8080:3000 my-node-app
```

This command maps port 3000 from the container to port 8080 on the host.

## 4. Managing Docker Containers

### Starting Containers

To start a Docker container:

```bash
docker start <container_id>
```

### Stopping Containers

To stop a Docker container:

```bash
docker stop <container_id>
```

### Removing Containers

To remove a Docker container:

```bash
docker rm <container_id>
```

## 5. Docker Volumes

Docker volumes offer several use cases where persistent data storage and sharing are necessary. Some common scenarios include database management, configuration files, log files, static assets, persistent storage, and sharing data between the host and containers.

## 6. Docker Compose

Docker Compose is a tool provided by Docker that simplifies the process of defining and running multi-container Docker applications. It allows you to use a YAML file to define services, networks, volumes, and other configuration options for your application.

### Key Features

- Declarative Configuration
- Multi-Container Applications
- Service Definitions
- Network Isolation
- Volume Management
- Environment Variables and Secrets
- Commands and Lifecycle Management

## 7. Essential Docker Commands and Their Functions

### docker run

```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```

- Run a Docker container from an image.

### docker build

```bash
docker build [OPTIONS] PATH | URL | -
```

- Build a Docker image from a Dockerfile and a specified context.

### docker ps

```bash
docker ps [OPTIONS]
```

- List all running Docker containers.

### docker images

```bash
docker images [OPTIONS] [REPOSITORY[:TAG]]
```

- List all Docker images available on the system.

### docker pull

```bash
docker pull [OPTIONS] NAME[:TAG|@DIGEST]
```

- Pull a Docker image from a registry to the local machine.

### docker stop

```bash
docker stop [OPTIONS] CONTAINER [CONTAINER...]
```

- Stop one or more running Docker containers gracefully.

### docker rm

```bash
docker rm [OPTIONS] CONTAINER [CONTAINER...]
```

- Remove one or more Docker containers.

### docker rmi

```bash
docker rmi [OPTIONS] IMAGE [IMAGE...]
```

- Remove one or more Docker images from the local machine.

### docker exec

```bash
docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
```

- Run a command inside a running Docker container.

### docker-compose up

```bash
docker-compose up [OPTIONS] [SERVICE...]
```

- Start Docker containers defined in a docker-compose.yml file.

### docker-compose down

```bash
docker-compose down [OPTIONS]
```

- Stop and remove containers, networks, volumes, and other resources created by `docker-compose up`.

### docker network ls

```bash
docker network ls [OPTIONS]
```

- List all Docker networks available on the system.

### docker volume ls

```bash
docker volume ls [OPTIONS]
```

- List all Docker volumes available on the system.
