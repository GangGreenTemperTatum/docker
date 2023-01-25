# LABEL <key>=<value> <key>=<value> <key>=<value> ...
# The LABEL instruction adds metadata to an image and is represented by a key/value pair

FROM ubuntu:latest

LABEL "com.example.vendor"="ACME Incorporated"
LABEL com.example.label-with-value="foo"
LABEL version="1.0"
LABEL description="This text illustrates \
that label-values can span multiple lines"

# LABEL's can also be represented as multiple labels in one instruction:

LABEL multi.label1="value1" multi.label2="value2" multi.label3="value3"

# OR:

LABEL multi.label1="value1" \
multi.label2="value2" \
other="value3"

# LABEL's are inehrited from your own image and any inherited parent images

# /labeltest]$ docker image build -t testingwithlabels:v1.0 . -f Dockerfile
# $ docker inspect <image-id/name>
# /labeltest]$ docker inspect image testingwithlabels:v1.0
# $ docker inspect image testingwithlabels:v1.0 | grep Labels -A 5

# /labeltest]$ docker tag testingwithlabels:v1.0 ganggreentempertatum/testingwithlabels:v1.0
# /labeltest]$ docker push ganggreentempertatum/testingwithlabels:v1.0
