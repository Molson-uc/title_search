FROM nginx

WORKDIR /user/share/react
RUN curl -fsSL https://deb.nodesource.com/setup_17.x | bash -
RUN apt-get install -y nodejs

COPY package*.json ./

ENV PATH /node_modules/.bin:$PATH

RUN npm install

COPY . .
RUN npm run build
RUN rm -r /usr/share/nginx/html
RUN cp -a build/. /usr/share/nginx/html
EXPOSE 3000