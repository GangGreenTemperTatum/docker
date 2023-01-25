# The ENV instruction in Dockerfile sets the environment variable for your container when you start. 
# The default value can be overridden by passing --env <key>=<value> when you start the container.
FROM alpine:latest
LABEL maintainer="GangGreenTemperTatum"

ENV WELCOME_MESSAGE="Welcome to Docker World!"
CMD ["sh", "-c", "echo $WELCOME_MESSAGE"]
# /alpineenv]$ docker build -t alpineenv:v1.0 . -f Dockerfile
# /alpineenv]$ docker image ls
# $ docker container run alpineenv:v1.0
# Welcome to Docker World!

# Override the existing ENV when spinning up the container:

# /alpineenv]$ docker container run --env WELCOME_MESSAGE='Welcome to Fake Docker Workshop' alpineenv:v1.0
# Welcome to Fake Docker Workshop
