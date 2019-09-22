# NestJSApiBoilerplateJWT
An API Boilerplate to create a ready-to-use REST API in seconds with NestJS 6.x and Passport Auth JWT System

## Installation

```
    $ npm install
```

## Config settings ormconfig.json for connect MySQL

```
{
   "type": "mysql",
   "host": "localhost",
   "port": 3306,
   "username": "my_username",
   "password": "my_password",
   "database": "my_database",
   "synchronize": true,
   "logging": false,
   "entities": [
      "src/entity/**/*.ts"
   ],
   "migrations": [
      "src/migration/**/*.ts"
   ],
   "subscribers": [
      "src/subscriber/**/*.ts"
   ],
   "cli": {
      "entitiesDir": "src/entity",
      "migrationsDir": "src/migration",
      "subscribersDir": "src/subscriber"
   }
}
```

## Install TypeScript Node

```
   $ npm install -g ts-node
```

## Running migrations with typeorm

```
   $ ts-node node_modules/.bin/typeorm migrations:run
```

## Running the app

```
    $ npm run start
```

## Getting secure resource with Curl

```
    $ curl -H 'content-type: application/json' -v -X GET http://127.0.0.1:3000/api/secure  -H 'Authorization: Bearer [:token]'
```

## Generate Token JWT Authentication with Curl

```
   $ curl -H 'content-type: application/json' -v -X POST -d '{"email": "tony_admin@nest.it", "password": "admin"}' http://127.0.0.1:3000/api/auth/login

```

## Registration user with Curl

```
   $ curl -H 'content-type: application/json' -v -X POST -d '{"name": "tony", "email": "tony_admin@nest.it", "username":"tony_admin", "password": "admin"}' http://127.0.0.1:3000/api/auth/register

```

## Forgot password with curl

```
   $ curl -H 'content-type: application/json' -v -X POST -d '{"email": "tony_admin@nest.it"}' http://127.0.0.1:3000/api/auth/forgot-password
```

## Change password User with curl

```
   $ curl -H 'content-type: application/json' -v -X POST -d '{"email": "tony_admin@nest.it", "password": "admin123"}' http://127.0.0.1:3000/api/auth/change-password  -H 'Authorization: Bearer [:token]'
```