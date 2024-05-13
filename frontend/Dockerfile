FROM node:alpine

WORKDIR /app

COPY package.json .

RUN npm install

RUN echo 'Hello from frontend!'

COPY . .

EXPOSE 5173

CMD ["npm", "run", "dev", "--", "--host"]