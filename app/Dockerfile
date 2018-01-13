# Dockerfile to run nodetest2
FROM node

RUN apt-get update && apt-get -y install vim

RUN mkdir -p /node/nodetest2
WORKDIR /node/nodetest2
RUN npm install -g express
RUN npm install -g express-generator
COPY . /node/nodetest2/
RUN npm install

EXPOSE 3000
ENTRYPOINT bash
