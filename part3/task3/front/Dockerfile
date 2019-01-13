FROM ubuntu:16.04

WORKDIR /frontend

RUN apt-get update && \
    apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y git nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /frontend && \
    apt-get purge -y --auto-remove curl && \ 
    rm -rf /var/lib/apt/lists/* && \
    cd /frontend && npm install && \
    useradd -m frontend 

USER frontend 

EXPOSE 5000

CMD ["npm", "start"]