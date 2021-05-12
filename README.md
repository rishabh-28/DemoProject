# DemoProject

DemoProject is NodeJS application which is having two databases, Mongodb and Mysql and working CRUD operations for each database using REST APIs

## Installation

To setup, mongoDB database is setup using Docker container.
```bash
docker run -d -p 27017:27017 --name mongodb mongo:4.0.24-xenial
```

To setup, mySQL database is setup using Docker container.
```bash
docker run -d --name m80 -e MYSQL_ROOT_PASSWORD=password -p 3306:3306 mariadb
```


Create a Jenkins Job, and declare a pipeline to dockerize the application.

## Dockerfile

```bash
FROM node:15-alpine

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 51005

CMD [ "npm", "start" ]
```

