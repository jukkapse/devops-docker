FROM node:10-alpine

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/backend-example-docker.git /backend && \
    cd /backend && \
    npm install && \
    apk del git && \
    chown -R backend .

WORKDIR /backend

USER backend

EXPOSE 8000
CMD ["npm", "start"]
