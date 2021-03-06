# Docker Commands

## List Docker processes and data

- `docker container ls` list containers, also can be shown with `docker ps`
- `docker image ls` list images, there is also the command `docker images`
- `docker volume ls` list volumes
- `docker network ls` lists networks
- `docker info` lists the number of containers and image, as well as system wide information regarding the Docker installation


## Clean out unused data and processes

- `docker system prune`
- `docker system prune --all --force --volumes`  So, to also remove the volumes (--volumes), any unused images (--all), as well as override the confirmation prompt (--force):

WARNING! This will remove:
        - all stopped containers
        - all networks not used by at least one container
        - all dangling images
        - all build cache

- `docker container prune` Remove all stopped containers
- `docker volume prune` Remove all unused volumes
- `docker image prune` Remove unused images

## Step Docker Containers
- `docker container stop [CONTAINERS...]`
- `docker container stop $(docker container ls -a -q)` <- full command for stopping Docker containers
- `docker container stop $(docker container ls -a -q) && docker system prune -a -f --volumes` <- full system clean


