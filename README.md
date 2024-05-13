
## Images

```
docker pull hello-wrold
```

## Containers

```
docker start: This command starts one or more stopped containers.
docker stop: This command stops one or more running containers.
docker restart: This command restarts a running container.
docker pause: This command pauses all processes within one or more containers.
docker unpause: This command unpauses all processes within one or more containers.
docker kill: This command sends a SIGKILL signal to one or more running containers.
docker rm: This command removes one or more containers.
docker ps: This command lists all running containers.
docker ps -a: This command lists all containers, including stopped ones.
docker exec -it container_id_or_name bash: enter docker container
docker run: run
```

## Dockerize

Create Dockerfile for project, then build the container and run it

```
docker build -t project .
```

```
docker build -t my-vite-app .
docker run -p 5173:5173 my-vite-app
```

## Dockerfile

```
FROM node:alpine: Specifies the base image to use, can be any
WORKDIR /app: Sets directory inside the container.
COPY package*.json ./: Copies package.json and package-lock.json to the working directory.
RUN npm install: Installs dependencies inside container.
COPY . .: Copies the rest of the application code.
EXPOSE 5173: Exposes port 5173, for vite there are additional config files
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]: May have been modified
```




