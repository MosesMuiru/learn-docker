# setting up the network
network -> if you have two container you want to connect them

use of docker compose
    avoid writing muiltiple commands everytime
    spin up muiltiple containers

know the containers you waant to use

syntax of docker compose
    docker-compose.yml
    
    ```

        services:
            redis-server:
                image: 'redis'
            node-app:
                build: .
                ports:
                - "4001:8081"
    ```

services are the containers you wanna build
one uses image called redis---pulled from registry
node-app
build you specify the dir where your docker file is located
port "localmachine": "v-machine"
    
using docker-compose the two images have access two each other
this is because it will create a default network
you can choose to create a network

some commands
    ```
        docker compose up --build This will rebuild the image and restart it

        docker compose up -d -> this runs our container in the backgroud

        docker compose down -> STOP THE CONTAINERS

        docker compose up -> this will log the errors

        docker compose ps -> this will find the running container in the recent file directory you are in

        docker ps --> shows the running containers

        docker run -t "image-name" .
    ```

there are restart policies for our container
```
    no --> never restart
    always --> attempt to restart always
    on-failure -> only restart if the container stops
    unless-stopped -> always restart unless we forcibly stop it

    the command
    restart: always

```
    
 
