# For MAC OS, disable buildkit under Docker Desktop > Engine settings.. or, set variables and restart Docker Daemon:
# export DOCKER_BUILDKIT=0 && export COMPOSE_DOCKER_CLI_BUILD=0
# Or, set variables at build runtime:
# $ DOCKER_BUILDKIT=0 docker build -t ganggreentempertatum/<tag> . -f <dockerfile-name>
FROM alpine:latest
RUN apk update
ADD http://www.vlsitechnology.org/pharosc_8.4.tar.gz .
