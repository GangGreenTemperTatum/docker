# The RUN instruction execute command on top of the below layer and create a new layer.
# Written n either Shell Form == $ RUN (shell form)
# OR, Executable Form == $ RUN [“executable”, “param1”, “param2”] (exec form)
FROM alpine:latest
LABEL maintainer=:"GangGreenTemperTatum"
RUN apk add --update
RUN apk add curl
RUN rm -rf /var/cache/apk/
# /alpinerun]$ docker image build -t ganggreentempertatum/alpinerun:v1.0 . -f Dockerfile
# Sending build context to Docker daemon  2.048kB
# docker image ls 

# $ docker image history ganggreentempertatum/alpinerun:v1.0
#IMAGE          CREATED         CREATED BY                                      SIZE      COMMENT
#21f9a794edd1   2 minutes ago   /bin/sh -c rm -rf /var/cache/apk/               0B
#bdb7dac3a00d   2 minutes ago   /bin/sh -c apk add curl                         2.26MB
#8b4fd0d3fe04   2 minutes ago   /bin/sh -c apk add --update                     2.61MB
#1d6791830745   2 minutes ago   /bin/sh -c #(nop)  LABEL maintainer=:GangGre…   0B
#042a816809aa   2 weeks ago     /bin/sh -c #(nop)  CMD ["/bin/sh"]              0B
#<missing>      2 weeks ago     /bin/sh -c #(nop) ADD file:e4d600fc4c9c293ef…   7.05MB

# /alpinerun]$ docker image ls ganggreentempertatum/alpinerun:v1.0
# REPOSITORY                       TAG       IMAGE ID       CREATED         SIZE
# ganggreentempertatum/alpinerun   v1.0      21f9a794edd1   8 minutes ago   11.9MB
