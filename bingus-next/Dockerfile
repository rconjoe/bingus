FROM node

COPY package.json .
COPY yarn.lock .

ENV MONGO_URL: "mongodb://mongo:27017"
ENV DB_NAME bingusdb
ENV COL_NAME bingusData

RUN yarn install

COPY . .

RUN yarn build 

EXPOSE 3000

CMD ["yarn", "dev"]
