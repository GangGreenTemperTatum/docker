# ONBUILD is a special instruction, followed by other instructions, such as RUN, COPY, etc., and these instructions will not be executed when the current image is built. Only when the current image is mirrored, the next level of mirroring will be executed.
# The other instructions in Dockerfile are prepared to customize the current image. Only ONBUILD is prepared to help others customize themselves.

# Dockerfile
# FROM busybox
# ONBUILD RUN echo "You won't see me until later"

# /busyboxonbuild]$ docker build -t no_echo_here:v1.0 . -f Dockerfile
# /busyboxonbuild]$ docker tag no_echo_here:v1.0 ganggreentempetatum/no_echo_here:v1.0
# $ docker image ls

FROM ganggreentempetatum/no_echo_here:v1.0

# /busyboxonbuild]$ docker build -t no_echo_here:v1.1 . -f Dockerfile
