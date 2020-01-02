# fullstack-apollo-express-mongodb-boilerplate

## Features of Client + Server

* React (create-react-app) with Apollo Client
  * Queries, Mutations, Subscriptions
* Node.js with Express and Apollo Server
  * cursor-based Pagination
* MongoDB Database with Mongoose
  * entities: users, messages
* Authentication
  * powered by JWT and local storage
  * Sign Up, Sign In, Sign Out
* Authorization
  * protected endpoint (e.g. verify valid session)
  * protected resolvers (e.g. e.g. session-based, role-based)
  * protected routes (e.g. session-based, role-based)
* performance optimizations
  * example of using Facebook's dataloader
* E2E testing

## Installation

* `git clone https://github.com/harrypotter0409/Apollo-Express-mongodb.git`
* `cd fullstack-apollo-express-mongodb-boilerplate`
* `touch .env`
* `npm install`
* fill out *.env file* (see below)
* `npm start`
* start MongoDB
* visit `http://localhost:8000` for GraphQL playground

#### .env file

Since this boilerplate project is using MongoDB, you have to install it for your machine and get a database up and running. After you have created a MongoDB database, you can fill out the environment variables in the *server/.env* file.

```
SECRET=asdlplplfwfwefwekwself.2342.dawasdq

DATABASE_URL=mongodb://localhost:27017/mydatabase
```

The `SECRET` is just a random string for your authentication. Keep all these information secure by adding the *.env* file to your *.gitignore* file. No third-party should have access to this information.

#### Testing

* adjust `test:run-server` npm script with `TEST_DATABASE_URL` environment variable in package.json to match your testing database name
* one terminal: npm run test:run-server
* second terminal: npm run test:execute-test
