# api-model
![tests](https://img.shields.io/badge/Unit%20tests-100%25-green?style=flat)
![integrations](https://img.shields.io/badge/Integration%20test-50%25-yellow?style=flat)
![docs](https://img.shields.io/badge/Documentation-100%25-green?style=flat)

This badges above can give people a good idea of what to expect about the API and what they can contribute too.

This first part of README should describe what is your API (or worker) about, for example, if my api is made to handle user registration, this part should look something like the next pharagraph.

This API handles user registrations on the system mySystem.

(you can put some image that makes your api identifiable).

## Content
- [About](#api-model)
- [Prerequisites](#prerequisites)
- [Configuration](#configuration)
- [Testing](#testing)
- [Running](#running)
- [Routes](#routes)
- [Diagrams](#Diagrams)
- [Examples](/examples/examples.md)


## Prerequisites
You should describe all the requisites to run this application.
- [![Docker](https://img.shields.io/badge/Docker-19.03.9-green?style=flat)](https://www.docker.com/)
- [![Docker-compose](https://img.shields.io/badge/Docker--compose-1.25.5-green?style=flat)](https://github.com/docker/compose/releases)
- [![mysql](https://img.shields.io/badge/mysql-8.0-green?style=flat)](https://support.rackspace.com/how-to/install-mysql-server-on-the-ubuntu-operating-system/)
- [![GNU Make](https://img.shields.io/badge/GNU%20Make-4.2.1-lightgrey?style=flat)](https://www.gnu.org/software/make/)
- [![GNU Bash](https://img.shields.io/badge/GNU%20Bash-4.2.1-lightgrey?style=flat)](https://www.gnu.org/software/bash/)
- Port avaliable: 8000

## Configuration
You have to detail the configurations needed to run the API locally, like environment variables, config files, yamls, everything that someone needs to start your API, **with examples** and any other useful information.

> This step should be done automatically via make

- Export the variables from [.env](.env) file.

**obs** : You need to create the supersecret password of the`SUPERSECRETPASSWORD` variable, follow [this]() doc to create it.

## Testing
This should be a tutorial of how to test the application, in the best scenario, at the start of this part you should have something like this, *creating makefiles makes everything easier*:

#### TL;DR: `make test`

> Execute go tests
```bash
go test ./...
```

## Running
This should be a tutorial of how to run the application, in the best scenario, at the start of this part you should have something like this, *creating makefiles makes everything easier*:

> TL;DR: `make start`

1. Turn mysql on via docker compose:
```bash
cd docker
docker-compose up
``` 
2. Make sure the environment variables are configured

3. Build go api
```bash
go build
```

## Diagrams
![uncached image](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/andrelrg/api-model/master/docs/diagram1.txt?token=ADWNZBWSVV4MXQTGPT2EENK7DDNOU)

You can put some diagrams to clarify the procceesses executed by your API.
## Routes
<!-- markdown-swagger -->
 Endpoint           | Method | Description                  | External | Authenticated | Example
 ------------------ | ------ | ---------------------------- | -------- | ------------- | ----
 `/heartbeat`       | GET    | Check if the API is alive    | **Yes**  | No            | [example](/examples/examples.md#hearbeat)
 `/create`          | POST   | Create the user in the user  | **No**   | Yes           | [example](/examples/examples.md#create) 
 `/list`            | GET    | List all created users       | **Yes**  | Yes           | [example](/examples/examples.md#list)
 `/get/:userID`     | GET    | Get a specific user          | **No**   | Yes           | [example](/examples/examples.md#get)
<!-- /markdown-swagger --> 

