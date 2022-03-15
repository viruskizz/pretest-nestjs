<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

This project is build by [NestJS Framework](https://github.com/nestjs/nest). Candidate have to implement basic CRUD backend API about user.

## How to

fork this repository and clone it into your local.

## Backend Mandatory Part

1. Design User interface that relate to database ORM with NoSQL concept. Edit `users/interfaces/user.ts` as you like or add more interface file that relate to.
```ts
export interface User {
  // edit this file and add more file if need
  id: number;
}
```
2. implement CRUD api endpoint under **best practice concept** by using `controller.ts` and `service.ts` follow these endpoints
    - GET `/personals/`
    - POST `/personals/`
    - GET `/personals/:id`
    - PUT `/personals/:id`
    - PATCH `/personals/:id`
3. Use mock directory to JSON as local Database
4. implement basic api validation and user validation
   - USER_NOT_FOUND
   - USER_ALREADY_EXISTED (validate by email as primary and phone number is secondary)
   - INVALID_BODY

## Backend Bonus part
1. Create new module as Stat and implement basic stat such as count, total etc.
2. use User Module in part of this module.
3. Example Endpoint
    - GET `/stats/personals/count`
    - GET `/stats/personals/total`

## Database Part
Use serverless database connect to your backend. You have to choose between **Firebase** or **AWS Dynamodb**. All of these, there are free tier to use.
1. create Table or collection and design schemas as follows by backend interface or modify if necessary.
2. Switch from mockup in backend api to database that you selected.

## Devops and security part
Automation build and deployment to server with [serverless framework](https://www.serverless.com/)
1. Edit `serverless.yml` following by server that you use (AWS or Google Cloud).
2. Add more file to convert normal build `main.ts` code to serverless supported code.
3. implement serverless offline to build and test in local environment.
4. implement `dotenv`
5. implement `Error Calling API log` under middleware concept
6. Add custom script `start` and `deploy`  and more as you need
7. create `Github Action` or `Gitlab CI` to automate CI/CD

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](LICENSE).
