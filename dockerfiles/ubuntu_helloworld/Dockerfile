FROM ubuntu:latest

LABEL maintainer="GangGreenTemperTatum"

RUN apt-get update 
RUN apt-get install -y python3

# $ touch ./helloworld.py
# $ echo 'print ("Hello, World!")' >> ./helloworld.py
# $ touch ./a.py
# $ echo 'print ("Overriden Hello")' >> ./a.p

ADD ./helloworld.py /home/helloworld.py
ADD a.py /home/a.py

CMD [ "/home/helloworld.py" ]
ENTRYPOINT [ "python3" ]
RUN ls -halt /home/

# /ubuntu_helloworld]$ docker image build -t ganggreentempertatum/ubuntu_helloworld . -f Dockerfile
# /ubuntu_helloworld]$ docker image ls

# $ docker run --name ubuntu_helloworld1 ganggreentempertatum/ubuntu_helloworld
# Hello, World!
# /ubuntu_helloworld]$ docker run --name ubuntu_helloworld2 ganggreentempertatum/ubuntu_helloworld:v1.0 /home/a.py
# Overriden Hello

# /ubuntu_helloworld]$ docker push ganggreentempertatum/ubuntu_helloworld:v1.0
