<h1 align="center">  {{cookiecutter.app_name}} </h1> <br>

<p align="center">
  {{cookiecutter.project_short_description}}
</p>


## Table of Contents

- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
  - [EGO](#ego)
  - [Local](#local)
  - [Docker](#docker)
- [Quick Start](#quick-start)
  - [Configure JWT Verification Key](#configure-jwt-verification-key)
  - [Run Local](#run-local)
  - [Run Docker](#run-docker)
- [Testing](#testing)
- [API](#api)
- [Acknowledgements](#acknowledgements)


## Introduction

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/e91606af4a364076a7058c5ea1c006a8)](https://www.codacy.com/app/joneubank/microservice-template-java?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=overture-stack/microservice-template-java&amp;utm_campaign=Badge_Grade)
[![CircleCI](https://circleci.com/gh/overture-stack/microservice-template-java/tree/master.svg?style=shield)](https://circleci.com/gh/overture-stack/microservice-template-java/tree/master)

TODO: Replace with introduction

## Features
TODO: Description of features

* Include a list of
* all the many beautiful
* web server features


## Requirements
The application can be run locally or in a docker container, the requirements for each setup are listed below.


### EGO
A running instance of [EGO](https://github.com/overture-stack/ego/) is required to generate the Authorization tokens and to provide the verification key.

[EGO](https://github.com/overture-stack/ego/) can be cloned and run locally if no public server is available. 


### Local
* [GO][(http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html](https://golang.org/dl/))
* [Mockgen](https://github.com/golang/mock)
* [Sqlc](https://github.com/kyleconroy/sqlc)
* [Goose](https://github.com/pressly/goose)


### Docker
* [Docker](https://www.docker.com/get-docker)


## Quick Start
Make sure the JWT Verification Key URL is configured, then you can run the server in a docker container or on your local machine.

### Configure JWT Verification Key
Update __application.yml__. Set `auth.jwt.publicKeyUrl` to the URL to fetch the JWT verification key. The application will not start if it can't set the verification key for the JWTConverter.

The default value in the __application.yml__ file is set to connect to EGO running locally on its default port `8081`.

### Run Local
```bash
$ make run
```

Application will run by default on port `1234`

Configure the port by changing `server.port` in __application.yml__


### Run Docker

First build the image:
```bash
$ docker-compose build
```

When ready, run it:
```bash
$ docker-compose up
```

Application will run by default on port `1234`

Configure the port by changing `services.api.ports` in __docker-compose.yml__. Port 1234 was used by default so the value is easy to identify and change in the configuration file.


## Testing
TODO: Additional instructions for testing the application.

## API
TODO: API Reference with examples, or a link to a wiki or other documentation source.

## Acknowledgements
TODO: Show folks some love.