# Use uma imagem base oficial e mais leve do Node.js
FROM node:18-alpine

# Define o diretório de trabalho dentro do container
WORKDIR /app

# Copia os arquivos de definição de dependências primeiro para aproveitar o cache do Docker
COPY package*.json ./

# Instala apenas as dependências de produção para uma imagem final menor
RUN npm install --production

# Copia o restante dos arquivos da aplicação
COPY . .

# Expõe a porta que a aplicação usa
EXPOSE 8080

# Comando para iniciar a aplicação
CMD [ "node", "server.js" ]


