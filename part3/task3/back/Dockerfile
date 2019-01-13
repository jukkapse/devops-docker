FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y git nodejs && \
    apt-get purge -y --auto-remove curl && \ 
    rm -rf /var/lib/apt/lists/*  && \
    cd /backend && \
    npm install && \
    useradd -m backend 

USER backend 
WORKDIR /backend

EXPOSE 8000

CMD ["npm", "start"]
