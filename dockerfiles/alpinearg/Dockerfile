# `ARG <parameter name>[=<default>]` 
# The environment variables of the build environment set by ARG will not exist in the future when the container is running
# ARG should not be used to store passwords as it is visible in `$ docker image history` output

FROM alpine:latest
LABEL maintainer="GangGreenTemperTatum"

# Setting a default value to argument "WELCOME_USER":
ARG WELCOME_USER="Docker Guru"
RUN echo "Welcome $WELCOME_USER, to Docker World!" > welcomemessage.txt
CMD cat welcomemessage.txt

# $ docker build -t alpinearg:v1.0 . -f Dockerfile
# $ docker image ls
# alpinearg                                      v1.0           15def34c34c1   18 seconds ago   7.05MB

# /alpinearg]$ docker run alpinearg:v1.0
# Welcome Docker Guru, to Docker World

# Test passing a build-time argument to override the above ARG
# $ /alpinearg]$ docker image build -t alpinearg:v1.1 . -f Dockerfile --build-arg WELCOME_USER=Dockerman
# $ docker image ls
# alpinearg                                      v1.1           d82a29bb0f91   3 seconds ago        7.05MB

# $ /alpinearg]$ docker run alpinearg:v1.1
# Welcome Dockerman, to Docker World!
