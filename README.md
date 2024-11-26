# JAVA_SPRING_BOOT_WITH_DOCKER_BUILD
Building a spring boot java application with docker and docker compose

### Steps to run this application

1. Clone the repository
2. Make sure to already have docker install and running on the machine
3. `CD` into the directory where the that contains the docker compose file and run the command `docker compose build` and after completion also run the command `docker compose up -d` to start the start and run the container.
4. Run the command `docker ps` which will open all the container that are currently running and it should display the following

```
CONTAINER ID   IMAGE                COMMAND                  CREATED         STATUS         PORTS                                                  NAMES
abd589aa26cb   opeseen/bkwebimage   "/docker-entrypoint.…"   3 minutes ago   Up 4 seconds   0.0.0.0:80->80/tcp, :::80->80/tcp                      webserver
b8db87cae719   opeseen/bkappimage   "bash -c './wait-for…"   3 minutes ago   Up 5 seconds   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp              appserver
853608dc9d07   opeseen/bkdbimage    "docker-entrypoint.s…"   3 minutes ago   Up 5 seconds   0.0.0.0:3306->3306/tcp, :::3306->3306/tcp, 33060/tcp   dbserver
```

5. Use the machine `ip address:80` to access the page from the web browser