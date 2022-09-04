
# FROM node:16-alpine
# WORKDIR /app
# COPY package*.json ./
# RUN npm install
# RUN npm install typescript --save-dev
# EXPOSE 8000
# CMD [ "npm","run","dev" ]
FROM node:16 as base
WORKDIR /home/node/app
COPY package*.json ./
RUN npm i
COPY . .

FROM base as prodaction
ENV NODE_PATH=./build
RUN npm run build