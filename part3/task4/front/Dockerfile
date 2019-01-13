FROM node:10-alpine

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git /frontend && \
    cd /frontend && \
    npm install && \
    apk del git && \
    chown -R frontend .

WORKDIR /frontend
USER frontend

EXPOSE 4200

CMD ["npm", "start"]
