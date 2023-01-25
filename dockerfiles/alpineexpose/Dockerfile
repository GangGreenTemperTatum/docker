# The EXPOSE instruction to expose a port, the protocol can be UDP or TCP associated with the indicated port, default is TCP with no specification
# EXPOSE won’t be able to map the ports on the host machine.
# EXPOSE port can be override using -p flag while starting the container

FROM nginx:alpine
LABEL maintainer="GangGreenTemperTatum"

EXPOSE 80/tcp
EXPOSE 80/UDP

CMD [ "nginx","-g","daemon off;" ]

# alpineexpose]$ docker image build -t alpineexpose:v1.0 . -f Dockerfile
# $ docker image ls
# $ docker container run --rm -d --name exposed-nginx alpineexpose:v1.0
# $ docker ps 

# /alpineexpose]$ curl 127.0.0.1:80
# curl: (7) Failed to connect to 127.0.0.1 port 80 after 11 ms: Connection refuse

# /alpineexpose]$ docker image inspect --format= alpineexpose:v1.0 | grep ExposedPorts -A 5
#           "ExposedPorts": {
#               "80/tcp": {},
#               "80/udp": {}


# /alpineexpose]$ docker container run --rm -P -d --name exposed-nginx-p alpineexpose:v1.0
# SEE the difference:
# /alpineexpose]$ docker ps
#CONTAINER ID   IMAGE               COMMAND                  CREATED          STATUS          PORTS                                          NAMES
#c4d0d2016127   alpineexpose:v1.0   "/docker-entrypoint.…"   36 minutes ago   Up 36 minutes   0.0.0.0:55000->80/tcp, 0.0.0.0:55000->80/udp   exposed-nginx-p
#fa1e724b7a65   alpineexpose:v1.0   "/docker-entrypoint.…"   39 minutes ago   Up 39 minutes   80/tcp, 80/udp                                 exposed-nginx

# /alpineexpose]$ curl 127.0.0.1:55000 // # http://localhost:55000/
# .. Welcome to nginx!

# /alpineexpose]$ docker tag alpineexpose:v1.0 ganggreentempertatum/alpineexpose:v1.0
# /alpineexpose]$ docker push ganggreentempertatum/alpineexpose:v1.0
