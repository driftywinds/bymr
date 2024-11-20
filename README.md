## An arm64 docker image for the [Backyard Monsters Refitted](https://github.com/bym-refitted/backyard-monsters-refitted) server made by drifty

The BYMR server lets you play the game on your own hosted server instead of the main official ones.

The official docker images do not exist and require building everytime, and I needed one for my Pi, so I cloned the repo and built the image myself. Useful for anyone with an arm64 processor who wants to run the server. 

Also available on Docker Hub - [```driftywinds/bymr:latest```](https://hub.docker.com/repository/docker/driftywinds/bymr/general)

How to use: - 

1. Clone the original repo.
2. Edit the docker-compose.yml file to fit your needs with regards to ports, volumes and db credentials.
3. Remove the lines corresponding to building the container and write the "image" part of the docker-compose.yml to ```ghcr.io/driftywinds/bymr:latest```.
4. ```docker compose up -d```

<br>

You can check logs live with this command: - 
```
docker logs <container name> -f
```
and the server will be ready to use when you see this in the logs: -
```
 ██████╗ ██╗   ██╗███╗   ███╗    ██████╗ ███████╗███████╗██╗████████╗████████╗███████╗██████╗
 ██╔══██╗╚██╗ ██╔╝████╗ ████║    ██╔══██╗██╔════╝██╔════╝██║╚══██╔══╝╚══██╔══╝██╔════╝██╔══██╗
 ██████╔╝ ╚████╔╝ ██╔████╔██║    ██████╔╝█████╗  █████╗  ██║   ██║      ██║   █████╗  ██║  ██║
 ██╔══██╗  ╚██╔╝  ██║╚██╔╝██║    ██╔══██╗██╔══╝  ██╔══╝  ██║   ██║      ██║   ██╔══╝  ██║  ██║
 ██████╔╝   ██║   ██║ ╚═╝ ██║    ██║  ██║███████╗██║     ██║   ██║      ██║   ███████╗██████╔╝
 ╚═════╝    ╚═╝   ╚═╝     ╚═╝    ╚═╝  ╚═╝╚══════╝╚═╝     ╚═╝   ╚═╝      ╚═╝   ╚══════╝╚═════╝
 Server running on: localhost:3001
```
