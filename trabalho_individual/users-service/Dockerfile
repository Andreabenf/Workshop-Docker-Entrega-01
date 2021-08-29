
FROM node:14

WORKDIR /usr/src/app

COPY package*.json ./

RUN yarn

COPY . .

EXPOSE 7101

CMD ["sh","-c","yarn db:migrate && yarn watch"]
