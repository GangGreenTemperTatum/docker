FROM alpine:latest
LABEL maintainer="ganggreentempertatum"

# Exec Form == ENTRYPOINT ["/bin/echo", "Hi, your ENTRYPOINT instruction in Exec Form!"]
# $ docker build -t ganggreentempertatum/alpineentrypoint . -f Dockerfile
# $ docker container run ganggreentempertatum/alpineentrypoint
# Hi, your ENTRYPOINT instruction in Exec Form!

# Shell Form == 

ENTRYPOINT "Hi, your ENTRYPOINT instruction in Exec Form!"

# $ docker build -t ganggreentempertatum/alpineentrypoint . -f Dockerfile
# $ docker container run ganggreentempertatum/alpineentrypoint
# /bin/sh: Hi, your ENTRYPOINT instruction in Exec Form!: not found
# $ docker container run --entrypoint "/bin/echo" ganggreentempertatum/alpineentrypoint "Hello! "
# Hello!
