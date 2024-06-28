FROM node:lts

# Crio e navego para o diretório de execução do projeto
RUN mkdir -p /usr/src/app/front
WORKDIR /usr/src/app/front

# Copio os arquivos do projeto e corrijo as permissões de acesso
COPY meu_app_front/ .
RUN chmod -R 777 ./

# Instalo os pacotes do projeto e compilo 
RUN npm install
RUN npm run build

# Instalo apenas os pacotes de produção do projeto
RUN npm install --production

CMD ["npm", "start"]