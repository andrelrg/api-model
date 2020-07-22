# api-model
This first part of README shoul describe what is your API (or worker) about, for example, if my api is made to handle user registration, here should look something like the next pharagraph.

This API handles user registrations on the system mySystem.

(you can put some image that makes your api identifiable).

## Prerequisites
You should describe all the requisites to run this application.
- Docker
- docker-compose
- golang 1.13+
- port: 8000

## Configuration
You have to detail the configurations needed to run the API locally, like environment variables, config files, yamls, everything that someone needs to start your API, **with examples** and any other useful information.

envs:
```
MYSQLHOST=localhost
SUPERSECRETPASSWORD=obs1*
ANOTHERVAR=21123556
```

obs1* : You need to create this supersecret password, follow [this]() doc to create it.

## Testing
This should be a tutorial of how to test the application, in the best scenario, at the start of this part you should have something like this, *craeting makefiles makes everything easier*:

#### TL;DR: `make test`

> Exetute go tests
```bash
go test ./...
```

## Running
This should be a tutorial of how to run the application, in the best scenario, at the start of this part you should have something like this, *craeting makefiles makes everything easier*:

#### TL;DR: `make start`

> Turn mysql on via docker compose:
```bash
cd docker
docker-compose up
``` 
> Make sure the environment variables are configured

> Build go api
```bash
go build
```

## Routes
<!-- markdown-swagger -->
 Endpoint           | Method | Description                  | External | Authenticated | Example
 ------------------ | ------ | ---------------------------- | -------- | ------------- | ----
 `/heartbeat`       | GET    | Check if the API is alive    | **Yes**  | No            | [example]("/examples/examples.md#hearbeat")
 `/create`          | POST   | Create the user in the user  | **No**   | Yes           | [example]("/examples/examples.md#create") 
 `/list`            | GET    | List all created users       | **Yes**  | Yes           | [example]("/examples/examples.md#list")
 `/get/:userID`     | GET    | Get a specific user          | **No**   | Yes           | [example]("/examples/examples.md#get")
<!-- /markdown-swagger --> 

