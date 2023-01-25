# The RUN instruction execute command on top of the below layer and create a new layer.
# Written n either Shell Form == $ RUN (shell form)
# OR, Executable Form == $ RUN [“executable”, “param1”, “param2”] (exec form)

FROM alpine:3.9.3
LABEL maintainer="GangGreenTempertatum"
RUN apk add --update && \
	apk add curl  && \  
	rm -rf /var/cache/apk/

# /alpinerunsmallerimage]$ docker build -t ganggreentempertatum/alpinerunsmallerimage:v1.0 . -f Dockerfile
# Sending build context to Docker daemon  9.216kB

# $ docker image ls
# /alpinerunsmallerimage]$ docker image history ganggreentempertatum/alpinerunsmallerimage:v1.0
#IMAGE          CREATED          CREATED BY                                      SIZE      COMMENT
#6b2e6bd611d9   32 seconds ago   /bin/sh -c apk add --update &&  apk add curl…   1.61MB
#55ebe5049459   36 seconds ago   /bin/sh -c #(nop)  LABEL maintainer=GangGree…   0B
#cdf98d1859c1   3 years ago      /bin/sh -c #(nop)  CMD ["/bin/sh"]              0B
#<missing>      3 years ago      /bin/sh -c #(nop) ADD file:2e3a37883f56a4a27…   5.53MB

# /alpinerunsmallerimage]$ docker image ls ganggreentempertatum/alpinerunsmallerimage:v1.0
#REPOSITORY                                   TAG       IMAGE ID       CREATED              SIZE
#ganggreentempertatum/alpinerunsmallerimage   v1.0      6b2e6bd611d9   About a minute ago   7.14MB
