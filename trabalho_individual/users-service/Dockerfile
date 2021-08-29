
FROM node:14

WORKDIR /usr/src/app

COPY package*.json ./

RUN yarn

COPY . .

EXPOSE 7101

# Adicionando um sleep de 10 segundos pra ter certeza 
# que o banco de dados está up and running (mesmo com o depends on no docker-compsoe.yml)
RUN sleep 10;

CMD ["sh","-c","yarn db:migrate && yarn watch"]
