## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

Build image reservations: docker build ../../ -f Dockerfile -t booking_reservations
Build image auth: docker build ../../ -f Dockerfile -t booking_auth
Run: docker run booking_reservations

Build reservations:
docker build -t reservations -f . ../../
Build auth:
docker build -t auth -f . ../../
Build auth:
docker build -t notifications -f . ../../
Build payments:
docker build -t payments -f . ../../



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

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](LICENSE).
