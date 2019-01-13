FROM ubuntu:16.04 

WORKDIR /application

RUN apt update && \
    apt-get install -y python python-dev python3-pip wget ffmpeg && \
    pip3 install pycrypto && \
    pip3 install --user --upgrade yle-dl

ENTRYPOINT ["yle-dl"]