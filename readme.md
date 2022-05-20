# CLASSROOM SERVICE WITHOUT NAME FOR NOW

[![Exams CI](https://github.com/Binaretech/Classroom-Exam-Service/actions/workflows/node.js.yml/badge.svg)](https://github.com/Binaretech/Classroom-Exam-Service/actions/workflows/node.js.yml)
[![Web CI](https://github.com/Binaretech/classroom-web/actions/workflows/node.js.yml/badge.svg)](https://github.com/Binaretech/classroom-web/actions/workflows/node.js.yml)
[![Auth CI](https://github.com/Binaretech/classroom-auth/actions/workflows/go.yml/badge.svg)](https://github.com/Binaretech/classroom-auth/actions/workflows/go.yml)
[![Main CI](https://github.com/Binaretech/classroom-main/actions/workflows/go.yml/badge.svg)](https://github.com/Binaretech/classroom-main/actions/workflows/go.yml)
[![Mobile CI](https://github.com/Binaretech/classroom-mobile/actions/workflows/main.yml/badge.svg)](https://github.com/Binaretech/classroom-mobile/actions/workflows/main.yml)

## Arquitecture

This project is made up with three services and a web front end routed by `traefik`, two databases, a cache store and a object storage

The following image describe the arquitecture and the tecnologies used

![arquitecture](https://github.com/Binaretech/classroom/blob/main/img/clasroom-diagram.png)

Each individual service is available at:

- [Auth Service](https://github.com/Binaretech/classroom-auth)
- [Web App](https://github.com/Binaretech/classroom-web)
- [Mobile App](https://github.com/Binaretech/classroom-mobile)
- [Main Service](https://github.com/Binaretech/classroom-main)
- [Exam Service](https://github.com/Binaretech/Classroom-Exam-Service)

## Clone the source code

Since this repo contains submodules of the each individual service you should clone with `recursive` flag in order to download all the submodules

```bash
$ git clone ... --recursive
```

For running in local, docker and docker-compose is strongly recommended

Copy and configure the env file to expose the services ports

```bash
$ cp .env.example .env # configure env file
```

And finally...

```bash
$ cp .env.example .env # configure env file
$ docker-compose up -d
```

The router will be listening at port 80

The canonical ports of postgres, mongodb and redis will be exposed to the host machine for debugging purposes in addition, the traefik dashboard will be available at port `8080`
