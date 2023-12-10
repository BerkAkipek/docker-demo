# Docker Demo With A Simple NodeJS App

To run this container follow these steps. 

1. Run above command from project content root to build the image. 

    docker build -t docker-demo:1.0.0 .

2. You can see the image by.

    docker images ls

3. Before running the container let's create a volume and not loose any data.

    docker volume create demo-volume

4. To create and run a container which uses demo-volume run this command. 

    docker run -d -p 3000:3000 --mount source=demo-volume,target=/docker-demo docker-demo:1.0.0

5. You can monitor running containers with command.

    docker ps

## If you are here still thank you for your attention. 