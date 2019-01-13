FROM node:alpine

WORKDIR /introds.github.io

RUN apk add --no-cache git && \
    git clone https://github.com/introds/introds.github.io.git && \
    cd ./introds.github.io && npm install && adduser -D app

USER app 

EXPOSE 4200

CMD ["npm", "start"]