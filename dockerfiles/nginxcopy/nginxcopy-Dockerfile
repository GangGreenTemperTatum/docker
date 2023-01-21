# For MAC OS, disable buildkit under Docker Desktop > Engine settings.. or, set variables and restart Docker Daemon:
# export DOCKER_BUILDKIT=0 && export COMPOSE_DOCKER_CLI_BUILD=0
# Or, set variables at build runtime:
# $ DOCKER_BUILDKIT=0 docker build -t ganggreentempertatum/<tag> . -f <dockerfile-name>
FROM nginx:alpine
LABEL maintainer="ganggreentempertatum"
COPY index.html /usr/share/nginx/html/
ENTRYPOINT ["nginx", "-g", "daemon off;"]
# $ echo "Welcome to Dockerlabs !" > index.html

# $ docker container run --rm --name myapp1 -p 80:80 nginx-copy:v1.0
# ~]$ curl localhost
# > .. Welcome to Dockerlabs

# $ docker push ganggreentempertatum/nginx-copy:v1.0
