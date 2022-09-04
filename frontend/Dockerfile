
FROM node:16-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm install typescript --save-dev
EXPOSE 8000
CMD [ "npm","run","dev" ]