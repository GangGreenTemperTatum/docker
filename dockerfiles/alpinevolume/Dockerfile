# Volumes in Docker creates a new volume that containers can consume and store data in
# Stored here == /var/lib/docker/volumes/ by default
# This is used to persist & backup data across containers instead of the default stateless bind mounts
# Volumes are completely managed by Docker, unlike bind mounts (local filesystem mapping)

FROM nginx:alpine
LABEL maintainer="GangGreenTemperTatum"

VOLUME /myvol
CMD [ "nginx","-g","daemon off;" ]

# /alpinevolume]$ docker image build -t alpinevolume:v1.0 . -f Dockerfile
# /alpinevolume]$ docker container run --rm -d --name alpinevolumetest alpinevolume:v1.0

#/alpinevolume]$ docker ps
#CONTAINER ID   IMAGE               COMMAND                  CREATED          STATUS          PORTS     NAMES
#423a17a502ca   alpinevolume:v1.0   "/docker-entrypoint.…"   22 seconds ago   Up 20 seconds   80/tcp    alpinevolumetest

# $ docker volume ls
#DRIVER    VOLUME NAME
#local     d572d11989cc35c9eb517e502464ef23c793d7318dc4142a434ff37d6c2d0767

#$ docker volume  inspect d572d11989cc35c9eb517e502464ef23c793d7318dc4142a434ff37d6c2d0767
#        "Mountpoint": "/var/lib/docker/volumes/d572d11989cc35c9eb517e502464ef23c793d7318dc4142a434ff37d6c2d0767/_data",

# /alpinevolume]$ docker container inspect -f '' volume-test
#         "Mounts": [
#           {
#               "Type": "volume",
#               "Name": "d572d11989cc35c9eb517e502464ef23c793d7318dc4142a434ff37d6c2d0767",
#               "Source": "/var/lib/docker/volumes/d572d11989cc35c9eb517e502464ef23c793d7318dc4142a434ff37d6c2d0767/_data",
#               "Destination": "/myvol",
#               "Driver": "local",

# OR:
# /alpinevolume]$ docker container inspect -f '' alpinevolumetest  | grep Mounts -A 5

# /alpinevolume]$ docker container exec -it alpinevolumetest pwd myvol
