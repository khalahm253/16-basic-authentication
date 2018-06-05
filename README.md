![CF](https://camo.githubusercontent.com/70edab54bba80edb7493cad3135e9606781cbb6b/687474703a2f2f692e696d6775722e636f6d2f377635415363382e706e67) 16: Basic Auth
===

## Overview
This application stores information about user accounts. It takes in a passwordHash, an email, a tokenSeed, and date stamp for when the account is created. PasswordHash, email, and tokenSeed are required fields, with the email and tokenSeed being unique. When a user creates a new account, the new account takes in a username, email, passwordHash, and tokenSeed.

## Getting Started
As a user, you will need to have MongoDB installed on your computer. 

You will need to include the following scripts in your package.json in order to run the tests and mongod:

"scripts": {
    "db": "mongod --dbpath=/Users/john/codefellows/tmp/db",
    "start": "node index.js",
    "watch": "nodemon index.js",
    "test-watch": "jest --watchAll",
    "test": "jest",
    "lint": "eslint **/*.js"
  }


You will need to init the following dependencies before utilizing this application:

  "dependencies": {
    "babel-env": "^2.4.1",
    "babel-eslint": "^8.2.3",
    "babel-register": "^6.26.0",
    "bcrypt": "^2.0.1",
    "cors": "^2.8.4",
    "dotenv": "^5.0.1",
    "eslint": "^4.19.1",
    "express": "^4.16.3",
    "jest": "^22.4.4",
    "jsonwebtoken": "^8.2.2",
    "mongoose": "^5.1.4",
    "morgan": "^1.9.0",
    "require-dir": "^1.0.0",
    "superagent": "^3.8.3"
  }

## Architecture
This application is written in JavaScript and Node.js. You will need MongoDB installed and, express, and mongoose middleware. 

In order to run tests, run the command: npm run test.

In order to test as CLI. You will need to ensure that you have nodemon and httpie installed on your computer. Then, in one terminal, run the command: nodemon index.js. Then, in a separate terminal, run the commands:

To POST/CREATE - http POST :3000/user species=[name of species] firstName=[name] description=[""] gender=[male or female]

- If successful, will respond with a 200 status. If an invalid post is made, will respond with a 400 status

To GET/READ - http :3000/user id==[insert existing id]

- If successful, will respond with a 200 status. If an invalid get is made, will respond with a 404 status

