# Docker
## What is Docker ?
- Docker is an open-source platform that automates the deployment , scailing and management of applications, inside lightweight and portable containers. \
- Containers allow developers to package applications with all the necessary dependencies and libraries, ensuring that they run consistently across different environments. \

## Composenents of Docker
1. Docker Engine: The core of Docker, it includes:
- Docker Daemon (dockerd): A background service responsible for managing containers, images, networks, and volumes.
- Docker CLI (docker): A command-line interface for interacting with the Docker Daemon.
- REST API: An interface that applications can use to communicate with the Docker Daemon.

2. Docker Images:
- Read-only templates that define the contents of a container. They include everything needed to run an application, such as code, runtime, libraries, environment variables, and configuration files.
3. Docker Containers:
- Lightweight, executable units of software that encapsulate an application and its dependencies. Containers are created from Docker images and run on the Docker Engine.


4. Docker Hub: 
- A cloud-based registry service for storing and sharing Docker images. Users can upload their own images or download images created by others.
5. Docker Compose: 
- A tool for defining and running multi-container Docker applications using a docker-compose.yml file.
6. Docker Swarm: 
- A native clustering and orchestration tool for Docker that allows you to manage a group of Docker engines and scale your applications across multiple containers.
