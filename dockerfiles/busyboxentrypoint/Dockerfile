# ENTRYPOINT provideS the executable while CMD is to pass the default arguments to the executable
FROM busybox:latest
CMD [ "/etc/passwd", "etc/hosts" ]
ENTRYPOINT [ "cat" ]

# /busyboxentrypoint]$ docker build -t ganggreentempertatum/busyboxentrypoint:v1.0 . -f Dockerfile
# $ docker image ls

# /busyboxentrypoint]$ docker run --name busyboxentrypoint ganggreentempertatum/busyboxentrypoint:v1.0 ... 
# This omits the contents of /etc/passwd and /etc/hosts to the terminal

# /busyboxentrypoint]$ docker run --name busyboxentrypoint2 ganggreentempertatum/busyboxentrypoint:v1.0 /etc/resolv.conf .. 
# This omits the contents of /etc/resolv.conf to the terminal

# $ /busyboxentrypoint]$ docker push ganggreentempertatum/busyboxentrypoint:v1.0
