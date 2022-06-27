# Node.js API using Fastify & TypeScript

![ci badge](https://github.com/valassis-fcalle/api-typescript-fastify/workflows/CI/badge.svg)
[![Sync Vulnerabilities Status](https://app.snyk.io/test/github/valassis-fcalle/api-typescript-fastify/badge.svg)](https://snyk.io/test/github/valassis-fcalle/api-typescript-fastify)

## Included in the boilerplate

- TypeScript (using esbuild for fast compilation)
- Env vars
- Tests (using Tap)
- Fastify
- File based routing (using [fastify-now](https://github.com/yonathan06/fastify-now))
- CI with github actions
- Docker image
- Linting

**Bring your own database** - no database connection included

## Set Up

- Install the dependencies.

```bash
yarn install
```

- Start the server in development mode.

```bash
yarn dev
```

## File Based Routing

Using [fastify-now](https://github.com/yonathan06/fastify-now) for file based routing

## Env vars

Loaded from `.env` file, with schema validation

## Backend API Development

There are a number of handy commands you can run to help with development.

| Command          | Action                                               |
| ---------------- | ---------------------------------------------------- |
| `npm run dev`    | Run the server in dev mode (restarts on file change) |
| `npm build`      | Compile TypeScript to JavaScript                     |
| `npm start`      | Start JavaScript from 'build' directory              |
| `npm test`       | Run unit tests (run `npm build` before)              |
| `npm test:watch` | Run backend tests in watch mode                      |
| `npm lint`       | Run eslint                                           |
| `npm lint:fix`   | Run eslint in fix mode                               |

## CI

Run tests on push/PR to master
Check `.github/workflows/CI.yml`

## Docker

Build docker image AFTER executing `npm run build`
The docker image copies the `build` directory, so it has to be present
