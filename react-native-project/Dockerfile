FROM  node:slim 

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . /app

EXPOSE 8080

CMD npm run web 