FROM node:16-buster

WORKDIR /usr/src/app

COPY package* /usr/src/app

RUN npm install --prod

COPY *.js /usr/src/app

CMD ["node", "index.js"]
