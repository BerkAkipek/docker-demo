# Docker Demo With A Simple NodeJS App

## To run this container follow these steps. 

1. Run the above command from the project content root to build the image. 
    ```bash
    docker build -t docker-demo:1.0.0 .
    ```
2. You can see the image by.
    ```bash
    docker images ls
    ```
3. Before running the container let's create a volume and not lose any data.
    ```bash
    docker volume create demo-volume
    ```
4. To create and run a container that uses demo-volume run this command. 
    ```bash
    docker run -d -p 3000:3000 --mount source=demo-volume,target=/docker-demo docker-demo:1.0.0
    ```
5. You can monitor running containers with a command.
    ```bash
    docker ps
    ```
### If you are still here thank you for your attention. 
