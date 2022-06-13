DockerHub
DockerHub is the world’s largest registry of Docker images with more than 100,000 images available. DockerHub is the default registry for Docker. It contains images ready to run a great variety of applications.

In the next video, you will walk through the steps of pulling an image from DockerHub and running the image on your own computer.

Fetch the image
Find the Postgres image by searching on DockerHub, or use this link to go directly to the image page. Postgres is an open source relational database, and the Postgres Docker image has the database software installed.

Run the following command in your terminal to download the latest Postgres image to your machine:

docker pull postgres:latest
Create and run a container
Run the image using the docker run command, supplying a password for Postgres:

docker run --name psql -e POSTGRES_PASSWORD=password! -p 5433:5432 -d postgres:latest
Note: If you have Postgres already installed and running locally, then use a different local port other than 5432, such as 5433.

In the command above:

The --name flag allows you to specify a name for the container that can be used later to reference the container. If you don’t specify a name, Docker will assign a random string name to the container.
The -e flag stands for “environment”. This sets the environment variable POSTGRES_PASSWORD to the value password!.
The -p flag stands for “publish”. This allows you to bind your local machine’s port 5433 to the container port 5432.
The -d stands for “detach”. This tells Docker run the indicated image in the background and print the container ID. When you use this command, you will still be able to use the terminal to run other commands, otherwise, you would need to open a new terminal.
Connect to the container
If you have the Postgres client installed (prerequisite), you can use it to connect with the Docker container database using the following command:

psql -h 127.0.0.1 -p 5433 -U postgres
# Mac/Linux users can also connect from the 0.0.0.0 address
Facing issues? See the Troubleshooting steps below.

This command allows you to access the database using the same port that you exposed earlier. Note that after running that command you will need to enter the same password that you set with the POSTGRES_PASSWORD when creating the container (password!).

Mac/Linux: Successfully running Postgres database inside a container
Mac/Linux: Successfully running Postgres database inside a container

Windows 10 CMD/GitBash: Successfully running Postgres database inside a container
Windows 10 CMD/GitBash: Successfully running Postgres database inside a container

Test the container with some SQL commands. For example,
List all databases using \l command or
List all tables (relations) using the \dti command.
More commands can be found in the Postgres documentation here.
When you are finished testing Postgres, you can quit your connection to Postgres using \q
Clean-up
To stop the running Docker container, you will first need to find it. You can list the running containers with the command docker ps. Copy the id of your Postgres container. Then, You can stop a particular container using its ID.

#List all containers
docker ps --all
# Stop
docker stop <container_ID>
# Remove
docker container rm <container_ID>
Similarly, you can view the images in your local system, and remove anyone as:

# List all images
docker image ls
# Remove
docker image rm <image_ID>
Troubleshoot
All users
The default IP of the (local) host machine is 127.0.0.1. Therefore, use 127.0.0.1 instead of 0.0.0.0 while connecting with the container Postgres database:
psql -h 127.0.0.1 -p 5433 -U postgres
See this discussion about the difference between localhost and 0.0.0.0
Windows users

We recommend you to use WSL. However, if you are still using CMD or GitBash, then run the CMD/GitBash as an Administrator.

If you have a version other than Windows 10 Home, you will have to find the host IP address, using the ipconfig command in your CMD. Look out for the Ethernet adapter vEthernet IPv4 address, such as 192.168.__.___. Use that IP address in the command while connecting with the container Postgres:

psql -h 192.168.__.___ -p 5433 -U postgres
