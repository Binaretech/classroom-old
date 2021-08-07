# CLASSROOM SERVICE WITHOUT NAME FOR NOW

[![Exams CI](https://github.com/Binaretech/Classroom-Exam-Service/actions/workflows/node.js.yml/badge.svg)](https://github.com/Binaretech/Classroom-Exam-Service/actions/workflows/node.js.yml)
[![Web CI](https://github.com/Binaretech/classroom-web/actions/workflows/node.js.yml/badge.svg)](https://github.com/Binaretech/classroom-web/actions/workflows/node.js.yml)
[![Auth CI](https://github.com/Binaretech/classroom-auth/actions/workflows/go.yml/badge.svg)](https://github.com/Binaretech/classroom-auth/actions/workflows/go.yml)[![Main CI](https://github.com/Binaretech/classroom-main/actions/workflows/go.yml/badge.svg)](https://github.com/Binaretech/classroom-main/actions/workflows/go.yml)

## Arquitecture

This project is made up with three services routed by `traefik`, two databases and a cache store

The following image describe the arquitecture and the tecnologies used

![arquitecture](/img/classroom-diagram.png)

## Clone the source code

Since this repo contains submodules of the each individual service you should clone with `recursive` flag in order to download all the submodules

```bash
$ git clone ... --recursive
```

For running in local, docker and docker-compose is strongly recommended

```bash
$ docker-compose up -d
```

The router will be listening at port 80

The canonical ports of postgres, mongodb and redis will be exposed to the host machine for debugging purposes in addition, the traefik dashboard will be available at port `8080`
