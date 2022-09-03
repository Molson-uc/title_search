# Use an official node runtime as a parent image
FROM node:16

WORKDIR /home/node/app

# Install dependencies
COPY package.json ./

RUN npm i

# Add rest of the client code
COPY . ./
FROM base as production

ENV NODE_PATH=./build
RUN npm run build
