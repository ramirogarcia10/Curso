FROM node:14.20-alpine3.15
LABEL project="demo-docker-node"
ENV APP_DIR=app-hello
RUN apk --no-cache add tzdata=2022a-r0
ENV TZ=America/Buenos_Aires
WORKDIR /app/${APP_DIR}
COPY package*.json ./
RUN npm install 
COPY . .
EXPOSE 4000
USER node
CMD ["npm","start"]
HEALTHCHECK NONE