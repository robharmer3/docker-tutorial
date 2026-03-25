FROM node:12-stretch

RUN npm install -g nodemon

USER node

RUN mkdir /home/node/code

WORKDIR /home/node/code

COPY --chown=node:node package-lock.json package.json ./

RUN npm install

COPY --chown=node:node . .

CMD ["nodemon", "index.js"]