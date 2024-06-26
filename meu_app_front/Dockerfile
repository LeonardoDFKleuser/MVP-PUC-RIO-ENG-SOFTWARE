FROM node:lts

WORKDIR /usr/src/app/front

COPY . .

RUN npm install

RUN npm run build

RUN npm install --production

CMD ["npm start"]
