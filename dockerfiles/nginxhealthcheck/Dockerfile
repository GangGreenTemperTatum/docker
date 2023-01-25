# The HEALTHCHECK directive tells Docker how to determine if the state of the container is normal.
# Before the HEALTHCHECK directive, the Docker engine can only determine if the container is in a state of abnormality by whether the main process in the container exits

# Default interval between health checks `--interval=<interval>` is 30 seconds
# Defaut retry value to determine unhealthy containers is 3 `--retries=<number>`

# Multiple HEALTHCHECKs in a Dockerfile will overlap and take precedence in top-down order

FROM nginx:latest
HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
    CMD curl -f http://localhost/ || exit 1
EXPOSE 80/tcp

# Here we set a check every 3 seconds to perform a curl to the localhost port and if no response after 3 seconds, is considered a failure

# /nginxhealthcheck]$ docker image build -t ganggreentempertatum/nginxhealthcheck:v1.0 . -f Dockerfile
# /nginxhealthcheck]$ docker image ls ganggreentempertatum/nginxhealthcheck
# REPOSITORY                              TAG       IMAGE ID       CREATED          SIZE
# ganggreentempertatum/nginxhealthcheck   v1.0      519223e9df92   59 seconds ago   142MB
# /nginxhealthcheck]$ docker image inspect ganggreentempertatum/nginxhealthcheck:v1.0 | grep Health -A 5

# $ docker run --name=nginx-healthcheck -d \
# > --health-cmd='stat /etc/nginx/nginx.conf || exit 1' \
# > nginx:latest
# 2daf9d07e22dcd997b218927c05b12460ca5bd18505b98c74e3f1a44c2c1da8

# $ docker ps

# /nginxhealthcheck]$ docker inspect --format '' nginx-healthcheck | grep Health -A 5

#             "Health": {
#               "Status": "healthy",
#               "FailingStreak": 0,
#               "Log": [
#                   {
#                       "Start": "2023-01-25T04:43:06.814571599Z",

# Deliberately kill NGINX health status

# /nginxhealthcheck]$ docker exec nginx-healthcheck rm /etc/nginx/nginx.conf
# /nginxhealthcheck]$ sleep 5; docker inspect --format='' nginx-healthcheck
# /nginxhealthcheck]$ sleep 5; docker inspect --format='' nginx-healthcheck | grep Health -A 5

#             "Health": {
#               "Status": "healthy",
#               "FailingStreak": 2,
#               "Log": [
#                   {
#                       "Start": "2023-01-25T04:43:36.909543311Z",

# /nginxhealthcheck]$ docker ps | grep nginx-healthcheck
# 2daf9d07e22d   nginx:latest        "/docker-entrypoint.…"   6 minutes ago    Up 6 minutes (unhealthy)   80/tcp                                         nginx-healthcheck

# Restore NGINX proxy health status
# @ docker exec nginx-proxy touch /etc/nginx/nginx.conf
