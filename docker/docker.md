# Docker
## What is Docker ?
>- Docker is an open-source platform that automates the deployment , scailing and management of applications, inside lightweight and portable containers. \
>- Containers allow developers to package applications with all the necessary dependencies and libraries, ensuring that they run consistently across different environments. \

## Composenents of Docker
1. Docker Engine: The core of Docker, it includes:
>- Docker Daemon (dockerd): A background service responsible for managing containers, images, networks, and volumes.
>- Docker CLI (docker): A command-line interface for interacting with the Docker Daemon.
>- REST API: An interface that applications can use to communicate with the Docker Daemon.

2. Docker Images:
>- Read-only templates that define the contents of a container. They include everything needed to run an application, such as code, runtime, libraries, environment variables, and configuration files.
3. Docker Containers:
>- Lightweight, executable units of software that encapsulate an application and its dependencies. Containers are created from Docker images and run on the Docker Engine.


4. Docker Hub: 
>- A cloud-based registry service for storing and sharing Docker images. Users can upload their own images or download images created by others.
5. Docker Compose: 
>- A tool for defining and running multi-container Docker applications using a docker-compose.yml file.
6. Docker Swarm: 
>- A native clustering and orchestration tool for Docker that allows you to manage a group of Docker engines and scale your applications across multiple containers.

## How to install Docker on Ubuntu
- Instruction here : [Link](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04#step-1-installing-docker)

### Structure of a dockerfile:
```
FROM python:3.10.12-slim
# This specifies the base image for the Docker container. In this case, it's a slim version of the Python 3.10.12 image, which is a smaller, more lightweight version of the full Python image.

WORKDIR /Blog
# This sets the working directory for the container to /Blog. Any subsequent commands (like COPY, RUN, etc.) will be executed from this directory.

# Copy the requirements file into the container
COPY requirements.txt /Blog/

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code into the container
COPY . /Blog/

# Expose the port that the FastAPI application runs on
EXPOSE 8000

# Command to run the FastAPI application using uvicorn
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]

```

#### Difference between IMAGE and CONTAINER:
> - CONTAINER is an environment to run Image.
> - Container includes:
>   1. Applications image:
>      - File system : where you can save the log files , store configuration files , ... all of this environmental stuff are provided by Container.\
>      Container also has a port that is binded to it.
>   2. Port binded: talk to application running inside of container.
>   3. Virtual file system: is virtual in container.


### Container Port and Host Port
 - Multiple Containers can run on your host machine.![image.info](multiple_containers.png)
 - Your machine has certain ports available those are open for some applications.

### Docker Compose
 - Taking care of creating a common Network.

