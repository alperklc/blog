---
layout: post
title: A starter project for developing a graphql api with nodejs
date: '2018-03-08 14:23:00'
tags:
- nodejs
- express
- graphql
- apollo
- mongodb
- mongoose
- jsonwebtoken
---

A starter API project with [nodejs](https://nodejs.org/en/) + [express](https://expressjs.com) + [mongodb](https://www.mongodb.com) + [graphql (apollo)](https://www.apollographql.com) stack, secured by [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken). This repository will be a starting point for my upcoming nodejs based graphql projects. Can be a starting point for anyone who is interested in learning graphql too!

Github: https://github.com/alperklc/express-mongo-graphql-starter

Using a mongo database on default port and creating two collections: `User` and `Record`. Collections have a 1-n relation.

Api is running on port number `3333`, serving two endpoints:
- `/auth` signup and authentication, open for everyone
- `/graphql` basic crud operations and search of record entity, requires Authorization token on header

### Usage  

After all required packages are installed by `npm install` command, `node index.js` or `npm run start` will make the API running.

Once it runs on local machine or cloud environment, any API testing tool like Postman would work. API responds as expected, if the request is a HTTP `POST`, with Content-Type specified as `application/json` on the header.

Sample authentication queries to paste to the request body:

- Signup:
```
{ 
  "query": "mutation SignupUserMutation($email: String, $password: String, $username: String) {
    signupUser(email: $email, password: $password, username: $username) { user { id username } token }
  }", 
  "variables": {"password": "1234", "email": "alper@mail.com", "username": "alperklc"}
} 
```

- Authentication of a user:
```
{
  "query": "mutation SigninUserMutation($email: String!, $password: String!) { authenticateUser(email: $email, password: $password) { user { id username updatedAt } token }
  }",
  "variables": {"password": "1234", "email": "alper@mail.com"}
}
```

CRUD and search queries for Record entity:
We will get a token after login via `authenticateUser` mutation on auth endpoint. Following examples are requiring this token specified on the header (Authorization: `token`). CRUD operations are restricted to the given user.

- Create record:
```
{
  "query": "mutation createRecord($description: String) {
    createRecord(description: $description) { id }
  }",
  "variables": {
    "description": "test"
  }
}
```

- Update record:
```
{
  "query": "mutation updateRecord($description: String $id: ID!) { updateRecord(description: $description id: $id) }",
  "variables": {
    "id": "5aa03efc9769c32ba2f4f5b5",
    "description": "test edit"
  }
}
```

- Delete record:
```
{
  "query": "mutation deleteRecord($id: ID!){ deleteRecord(id: $id) }",
   "variables": {
     "id": "5aa05b6a8fef4c40d74c88fb"
   }
}
```

- Get a record by ID:
```
{
  "query": "query getRecordById($id: ID){ initialRecord: getRecordById(id: $id) { id description } }",
  "variables": {"id": "5aa03efc9769c32ba2f4f5b5"}
}
```

- Search record:
```
{
  "query": "query searchRecord($keyword: String! $dateGreaterThanEqual: String! $dateLessThanEqual: String!) { searchRecord(keyword: $keyword, dateGreaterThanEqual: $dateGreaterThanEqual, dateLessThanEqual: $dateLessThanEqual) { id description } }",
  "variables": {
    "keyword": "te",
    "dateGreaterThanEqual": "2017-12-08T00:00:00.000Z",
    "dateLessThanEqual": "2019-08-08"
  }
}
```

##### Roadmap / Future plans
- Will add unit and integration tests to this starter project.
- A UI would be helpful for frontend developers want to start developing with graphql
- Use it on my future projects.

##### How to contribute?
- Fork, develop further and send a pull request :)
- Issues are welcomed too.
    
