FROM ubuntu:16.04

RUN apt-get update && \ 
    apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y git nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /frontend && \
    cd /frontend && \
    npm install && \
    apt-get purge -y --auto-remove curl git && \
    rm -rf /var/lib/apt/lists/*    

WORKDIR /frontend

EXPOSE 5000

CMD ["npm", "start"]
