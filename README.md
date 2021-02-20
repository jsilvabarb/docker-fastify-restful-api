# Docker Fastify RESTful API

Node.js RESTful API boilerplate using Traefik, Docker, Docker Compose, Fastify, JWT and Mongodb.

## Requirements
1. Node.js >= 14
2. Docker
3. Docker compose

## Getting started

Install packages using docker:

```sh
docker run --rm -it \
-v ${PWD}:/usr/src/app \
-w /usr/src/app \
node:15-alpine npm i
```

Windows users should switch the PWD variable to your current directory. Or if you have node installed in your system, install using npm:

```sh
npm install
```

## Configuration

1. Rename the .env.example file to .env and fill variables. The Postgres variables are required for Sonarqube. The SENTRY_DSN variable is not obligatory.

2. Edit your hosts file with:
  >127.0.0.1 fastify.localhost
  >127.0.0.1 sonarqube.localhost

## Run

In the root of project, run:

```sh
docker-compose up
```

Acess this url on your browser:

```sh
http://fastify.localhost/api/v1
```

If everything is ok, you will see the following message:

```json
{
  "message": "Fastify API is on fire"
}
```

## Insominia Collection

I exported Insomnia [`collection/data`](insomnia_2021-02-07.json) for so you can test all the endpoints.

## Sonarqube dashboard

To access Sonarqube dashboard, simple access in your browser:

```sh
http://sonarqube.localhost
```

![](/sonarqube.png)

[Follow the guide](SONARQUBE.md) to learn more about the settings and how to run Sonar code analysis.

## Traefik dashboard

To access Traefik dashboard, simple access in your browser:

```sh
http://localhost:8080
```

![](/traefik.png)

Happy coding!
