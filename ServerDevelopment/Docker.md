What is Docker?
Docker is the most popular open-sourced container runtime tool that helps to build, test, and run containers. It is both a container system and a company.

Using Docker, you can create containers with both Linux and Windows kernels, although Windows containers are only available if you are running a Windows machine. In either case (Linux/Windows), you will have to install Docker on your local machine. Installing Docker means installing Docker Desktop, a command-line utility.

Throughout the rest of this course, you will be using the Docker containers, and in this concept, you will prepare by installing Docker Desktop (or simply Docker) on your own machine.



Docker Engine
Docker Engine is an application that consists of a daemon, an API, and a client:

The Docker daemon is a server that manages the images, containers, networks, and volumes.
The Docker client is the user interface for Docker. The client is a CLI, so most of the work you do with Docker will take place at the command line.

The client communicates with the daemon through the command line API as shown in the image below. You will be using the Docker Engine to create and run containers, so if you have not installed Docker using the links above, please be sure to do so.

Docker engine consists of the Docker Daemon, Docker API, and Docker Client
Docker engine consists of the Docker Daemon, Docker API, and Docker Client

Docker Image
A Docker image is the set of instructions for creating a container. The image typically includes a file system and the parameters that will be used for the container.

Images are comprised of multiple layers. Each layer contains specific software.

You can create a custom Docker image for a specific application. Start with a standardized parent image as the base layer. The parent image often contains the file system of a particular operating system, such as Ubuntu 18.04. Then add an additional layer to the image, on top of the base layer. You can add your application files to this additional layer. You can even add multiple additional layers, and distribute your application files across different layers, as appropriate for your needs.

You will be able to see this structure more clearly when you create Dockerfiles in the coming classroom concept.


Docker Container
You have already been introduced to containers, and a Docker container is just the Docker-specific implementation of the concept. In practice, Docker containers are created from Docker images - a container is a runnable instance of an image. Note that since the image is a set of instructions for creating a container, multiple containers can be created from the same image.


Docker Registry
Docker images can be stored and distributed using a Docker registry. In the next classroom concept, you will download and run an image from DockerHub, which is a free registry with many images you can use.
