# CRUD

CRUD simple server application 


## Build

One can build the application with the following

```sh
go build crud.go
```

## Install

You can install the application with 

```sh
go install crud.go
```

The application will be installed in `$HOME/go/bin/crud`

## Run

In order to run this application execute

```sh
go run crud.go
```

You should get a similar output

```sh
   ____    __
  / __/___/ /  ___
 / _// __/ _ \/ _ \
/___/\__/_//_/\___/ v4.13.3
High performance, minimalist Go web framework
https://echo.labstack.com
____________________________________O/_______
                                    O\
⇨ http server started on [::]:1323

```

## Test

You can use the supplied postman collection `echo-crud.postman_collection.json` to run the tests on this API.

You can also execute directly

### CreateUser 

```sh
curl -X POST \
  -H 'Content-Type: application/json' \
  -d '{"name":"Joe Smith"}' \
  localhost:1323/users
```

### GetUser

```sh
curl localhost:1323/users/1
```

### UpdateUser

```sh
curl -X PUT \
  -H 'Content-Type: application/json' \
  -d '{"name":"Joe"}' \
  localhost:1323/users/1
```

### DeleteUser

```sh
curl -X DELETE localhost:1323/users/1
```
