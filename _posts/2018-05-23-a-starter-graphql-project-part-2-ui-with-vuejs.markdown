---
layout: post
title: A starter graphql project - Part 2 (UI with VueJs)
date: '2018-05-23 20:42:30'
tags:
- vuejs
- graphql
- nodejs
---

In March, I've developed and shared [a starter graphql project](https://blog.alperkilci.com/a-starter-project-for-developing-a-graphql-api-with-nodejs/), which is initially intended to be a bootstrapper for Nodejs based Graphql APIs.

This time, I've added a `vue-js` frontend to the stack. It uses `apollo-client`for communicating with the backend.

UI is optimized for mobile devices.

Frontend application is capable to 
- create an user
- login
- logout
- list existing records
- search records
- create a record
- edit a record
- delete a record


**Screenshots**
![Screenshot from 2018-05-23 22-21-40.png](https://steemitimages.com/DQmaCa1YiVNDd3KqzA5Thu6m7fnPPbHkfPFLucF2Yu4UhnZ/Screenshot%20from%202018-05-23%2022-21-40.png) ![Screenshot from 2018-05-23 22-23-16.png](https://steemitimages.com/DQmWDspcgME7s7dCZs6J6KhzcE9VLmdAGXmwGo37tYzDgdR/Screenshot%20from%202018-05-23%2022-23-16.png)

![Screenshot from 2018-05-23 22-23-50.png](https://steemitimages.com/DQmUoSrhRNiZrUjDTdV6U8P4TqTVveYSfBSzJGe4jkptMf2/Screenshot%20from%202018-05-23%2022-23-50.png)![Screenshot from 2018-05-23 22-24-06.png](https://steemitimages.com/DQmb6Pc16k4qowg1g4WrTsHwFsFPm9trZJCauMw5YiCY8gR/Screenshot%20from%202018-05-23%2022-24-06.png)


**Live demo is available:** https://vue-nodejs-graphql-starter.herokuapp.com

**Development**
Backend and frontend parts of the application could be started seperately. 

API works the same, serves following endpoints:
- /auth signup and authentication, open for everyone
- /graphql basic crud operations and search of record entity, requires Authorization token on header

`npm run start` command on `./backend` folder will start the backend part, which will expose endpoints specified above, under the port `4040`.
`npm run dev` command on `./frontend` folder will start the frontend part for development, which will enable eslint for keeping the coding style consistent. Served under port `8080` in development environment.

**Usage**
`package.json` file  on the root folder contains npm scripts, which builds backend and frontend applications.
Once backend and frontend apps are built, backend app will also serve static files of frontend application in production environment.

**Repository:** https://github.com/alperklc/vue-nodejs-graphql-starter

**Deployment**
Repository contains a branch called `heroku-deploy`, which contains required parameters and npm scripts. Works on heroku, if it's deployed from this branch. Requires mLab MongoDB add on and a config variable `JWT_SECRET`.

Feel free to contact, in case of any deployment problem.

**Technologies**
nodejs, express, graphql, apollo, mongodb, mongoose, jsonwebtoken, vuejs, scss, webpack

**Roadmap / Future plans**
- Let the UI evolve into a PWA
- Improve the UI
  - add infinite scrolling to the list
  - add time interval selectors
  - and so on
- Adding docker to the stack, in order to make deployment easier.
- Will add unit and integration tests to this starter project.
- Use it on my future projects.

**How to contribute?**
- Fork, develop further and send a pull request :)
- Issues are welcomed too.