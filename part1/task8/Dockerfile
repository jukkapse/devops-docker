FROM ubuntu:16.04

RUN apt-get update && apt-get install -y git curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN git clone https://github.com/introds/introds.github.io.git

WORKDIR /introds.github.io

RUN npm install

EXPOSE 8000

CMD ["npm", "start"]