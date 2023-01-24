FROM alpine:latest
LABEL maintainer="ganggreentempertatum"
# WORKDIR Absolute Path: (Set the working directory for any ADD, COPY, CMD, ENTRYPOINT, or RUN instructions that follow.)

# WORKDIR /opt
ENV DIRPATH /myfolder
WORKDIR $DIRPATH

# /opt/folder1/folder2 # echo $DIRPATH
# /myfolder

# /alpineworkdir]$ docker image build -t ganggreentempertatum/alpineeworkdir:v1.0 . -f Dockerfile
# Sending build context to Docker daemon  2.048kB

# $ docker image ls
# $ /alpineworkdir]$ docker run -it ganggreentempertatum/alpineeworkdir:v1.0
# /opt #

# WORKDIR Relative Path: (Set the working directory for any subsequent ADD, COPY, CMD, ENTRYPOINT, or RUN instructions that follow it in the Dockerfile.)

WORKDIR /opt
RUN echo "Welcome to Docker Labs" > opt.txt
WORKDIR folder1
RUN echo "Welcome to Docker Labs 1" > folder1.txt
WORKDIR folder2
RUN echo "Welcome to Docker Labs 2" > folder2.txt

# /alpineworkdir]$ docker image build -t ganggreentempertatum/alpineeworkdir:v1.1 . -f Dockerfile
# Sending build context to Docker daemon   2.56kB
# /alpineworkdir]$ docker run -it ganggreentempertatum/alpineeworkdir:v1.1
# /opt/folder1/folder2 #
# $ cd /opt
# /opt # ls -halt -R
# .:
# total 24K
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:22 ..
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:21 folder1
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:21 .
# -rw-r--r--    1 root     root          23 Jan 24 04:21 opt.txt
# 
# ./folder1:
# total 24K
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:22 folder2
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:21 .
# -rw-r--r--    1 root     root          25 Jan 24 04:21 folder1.txt
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:21 ..
# 
# ./folder1/folder2:
# total 16K
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:22 .
# -rw-r--r--    1 root     root          25 Jan 24 04:22 folder2.txt
# drwxr-xr-x    1 root     root        4.0K Jan 24 04:21 ..
