<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://7webs.co.in/assets/images/logos/logo_main.png" height="300" alt="Nest Logo" /></a>
</p>

## Description

#### Nestjs based application to help moving forward into a greener life-style and make it easier for users to save all there receipt in single place

[Nest](https://github.com/nestjs/nest) framework TypeScript application.

## Installation

```bash
$ yarn
```

## Database setup

1. Create Postgres database named using the following details:

```
  type: 'postgres'
  host: 'localhost'
  username: 'postgres'
  password: 'root'
  database: 'social-chat'
  port: 5432
  synchronize: true
  use_ssl: false
```

2. Add Following .env file to get started:

```
DB_HOST=localhost
DB_PORT=5432
DB_USERNAME=postgres
DB_PASSWORD=root
DB_NAME=social-chat
SWAGGER_USER=swaggerUser
SWAGGER_PASSWORD=super@20024

GOOGLE_PROJECT_ID=firebase-proj-id
GOOGLE_CLIENT_EMAIL=firebase-admin-sdk-client-email@email
GOOGLE_PRIVATE_KEY_ID=pravate-key-id
FIREBASE_STORAGE_BUCKET=firebase-proj-id.appspot.com
GOOGLE_PRIVATE_KEY=-----BEGIN PRIVATE KEY-----\nprivatekey-for-firebase-admin-it-is-used-to-authenticate-admin\n-----END PRIVATE KEY-----\n

```

## Running the app

```bash
# watch mode
$ npm run start:dev

# Test production config locally with watch mode
$ npm run start:dev:prod

# production mode no watch mode, require build first
$ npm run build
$ npm run start:prod
```

## Database migration steps

1. ### Migration generate
2. ### Add Migration file into migrations
   1. migration file will be generated in [migrations folder](src/providers/database/migrations)
   2. Remove old migration if there are any
   3. Add the new generated migration file under [migration.config.ts](src/providers/database/migration.config.ts) in
      the configuration under
      migrations array
3. ### Migration run

## Database migration scripts

```bash
# migration generate
 yarn run migration:generate

 # migration run
 yarn run migration:run
```

## Deploy to Digital Ocean

- Deployment is straight forward, just push to master and it will be deployed automatically

## Using Swagger

Swagger is used for API documentation and provides an interactive interface to explore and test the endpoints.

#### Accessing Swagger UI

Swagger UI is available at the `/api` endpoint. To access the Swagger documentation:

Ensure your application is running.
Open your web browser and navigate to `http://localhost:3000/api` for local development environment.

#### Authentication

The Swagger UI is protected by Basic Authentication. You need to use the credentials configured in your environment variables to access it.

`Username`: The value of SWAGGER_USER from your environment configuration.

`Password`: The value of SWAGGER_PASSWORD from your environment configuration.

#### Example

If you have set the following environment variables:

```bash
SWAGGER_USER=swaggerUser
SWAGGER_PASSWORD=swaggerPassword
```

## Collaboration and Development Guide

For detailed information on our collaboration and development process, please refer to our [Collaboration and Development Guide](./Collaboration-Guide.md).
