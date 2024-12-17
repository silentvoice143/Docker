
# Docker

## What is a container?
- A way to package application with all the necessary dependencies and configuration.
- Portable artifact, easily shared and moved around.
- Make development and deployment more effecient.

### Where do container lives?
- Container repository.
- Private repositories.
- Public repositories for docker - Dockerhub.

### How container solve problems?
- #### Before Container
   - Installation process are different on each OS.
   - Many steps: Anything can go wrong.
   - configuration needed - may lead to dependency conflict.

- ### After Container
   - Own isolated environment.
   - Packaged with all needed configuration.
   - One command to install the application.
   - Run same app with two different version.
   - Developers and operations works together to package the application in a container.
   - No environmental configuration needed on server except docker runtime.


A container is:
- Layers of images.
- Mostly linux based images, because small in size.
- Application image on top.


## Docker vs Virtual machine
1> Docker virtualize the application layer and uses host kernel while Virtual machine virtual whole OS with its kernel.
2> size of docker image is less than virtual machine.
3> Docker container start and run much fast
4> Vm can run any os while docker image of linux can't run on window.

## Some docker commands

- **docker pull** : Used to pull an image from the Dockerhub.
- **docker run** : Used to run the image in a container.
- **docker run redis:0.4** : Used to pull and run.
- **docker stop** : Used to stop the running container.
- **docker ps** : Used to list all the running container.
- **docker ps -a** : Used to list all the container.
- **docker images** : Used to list all the images.
- **docker rmi** : Used to remove an image.
- **docker logs** : Used to see all logs.
- **docker run -d -p6000:6739 --name redis-latest redis:latest** : Used to name any container.
- **docker exec -it 51efeb9c2429 /bin/bash** : Used to go into the file system of a container. To exit just cmd "exit".
- **docker compose -t my-app:1.0 .** : Used to build an image of current directory dockerfile.

#### Network Related
- **docker network ls** : Used to list all container network.
- **docker network create mongo-network** : Used to create a new network in this case name is mongo-network.

## Port binding

- Bind the host port to the container.
- To bind "docker run -p6000:6739 redis"
- host port-> contianer port


