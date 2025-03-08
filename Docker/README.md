# Docker Cheat Sheet

# My Project

## Features
Here are some cool features of this project.

## Usage
Learn how to use it here.

[Jump to Installation](#installation)


Docker is a platform that allows developers to package applications and their dependencies into lightweight, portable containers. These containers run the same way on any system, eliminating the "it works on my machine" problem. Instead of installing software manually, Docker lets you create images that include everything an application needs, from code to libraries. This makes it easier to deploy and scale applications consistently across different environments, whether on a laptop, a server, or the cloud.

## Dockerfile Basics

* **`FROM <image>:<tag>`:** Specifies the base image.
* **`WORKDIR <path>`:** Sets the working directory.
* **`COPY <source> <destination>`:** Copies files from the host to the container.
* **`RUN <command>`:** Executes a command during image build.
* **`EXPOSE <port>`:** Exposes a port.
* **`CMD ["executable", "param1", "param2"]`:** Sets the default command to run when the container starts.
* **`ENV <key> <value>`:** Sets an environment variable.
* **`VOLUME <path>`:** Creates a mount point for a volume.

## Docker Compose File (docker-compose.yml)

* **`version: "3.8"`:** Specifies the Compose file version.
* **`services:`:** Defines the services.
* **`build:`:** Specifies build options.
* **`image:`:** Specifies an existing image to use.
* **`ports:`:** Maps ports.
* **`volumes:`:** Mounts volumes.
* **`environment:`:** Sets environment variables.
* **`depends_on:`:** Defines service dependencies.
* **`command:`:** Overrides the `CMD` from the Dockerfile.
* **`networks:`:** Defines networks.

## Docker Commands

### Image Management

* **Build an image:**
    ```bash
    docker build -t <image_name>:<tag> <path_to_Dockerfile>
    ```
    * `-t`: Tag the image with a name and optional tag.
    * `<path_to_Dockerfile>`: Path to the directory containing the Dockerfile. Use `.` for the current directory.
* **List images:**
    ```bash
    docker images
    ```
* **Pull an image from a registry:**
    ```bash
    docker pull <image_name>:<tag>
    ```
* **Push an image to a registry:**
    ```bash
    docker push <image_name>:<tag>
    ```
* **Remove an image:**
    ```bash
    docker rmi <image_id> or <image_name>:<tag>
    ```
    * `-f` or `--force` to force removal.

### Container Management

* **Run a container:**
    ```bash
    docker run -d -p <host_port>:<container_port> --name <container_name> <image_name>:<tag>
    ```
    * `-d`: Run the container in detached mode (background).
    * `-p`: Map ports between the host and container.
    * `--name`: Assign a name to the container.
    * `-e`: Set environment variables.
    * `-v`: Bind mount a volume.
* **List running containers:**
    ```bash
    docker ps
    ```
* **List all containers (including stopped):**
    ```bash
    docker ps -a
    ```
* **Stop a container:**
    ```bash
    docker stop <container_id> or <container_name>
    ```
* **Start a stopped container:**
    ```bash
    docker start <container_id> or <container_name>
    ```
* **Restart a container:**
    ```bash
    docker restart <container_id> or <container_name>
    ```
* **Remove a container:**
    ```bash
    docker rm <container_id> or <container_name>
    ```
    * `-f` or `--force` to force removal.
* **Execute a command inside a running container:**
    ```bash
    docker exec -it <container_id> or <container_name> <command>
    ```
    * `-it`: Interactive terminal.
    * `/bin/bash`: Open a shell.
* **View container logs:**
    ```bash
    docker logs <container_id> or <container_name>
    ```
    * `-f` to follow logs.

### Network Management

* **List networks:**
    ```bash
    docker network ls
    ```
* **Create a network:**
    ```bash
    docker network create <network_name>
    ```
* **Remove a network:**
    ```bash
    docker network rm <network_name>
    ```

### Volume Management

* **List volumes:**
    ```bash
    docker volume ls
    ```
* **Create a volume:**
    ```bash
    docker volume create <volume_name>
    ```
* **Remove a volume:**
    ```bash
    docker volume rm <volume_name>
    ```

## Docker Compose Commands

* **Build and start containers:**
    ```bash
    docker-compose up --build
    ```
    * `--build`: Build images before starting containers.
    * `-d`: Run containers in detached mode.
* **Start containers (without building):**
    ```bash
    docker-compose up
    ```
* **Stop containers:**
    ```bash
    docker-compose down
    ```
* **View container logs (from docker-compose):**
    ```bash
    docker-compose logs <service_name>
    ```
    * `-f` to follow logs.
* **Execute a command inside a service container:**
    ```bash
    docker-compose exec <service_name> <command>
    ```

## Installation
Follow these steps to install the project.
