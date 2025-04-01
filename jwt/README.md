# JWT

Echo with JWT simple Auth 


## Build

One can build the application with the following

```sh
go build server-jwt.go
```

## Install

You can install the application with 

```sh
go install server-jwt.go
```

The application will be installed in `$HOME/go/bin/server-jwt`

## Run

In order to run this application execute

```sh
go run server-jwt.go
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

You can call with curl to generate the token

```sh
curl -X POST -d 'username=jon' -d 'password=shhh!' localhost:1323/login
```

you should get something similar

```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE0NjE5NTcxMzZ9.RB3arc4-OyzASAaUhC2W3ReWaXAt_z2Fd3BN4aWTgEY"
}
```

Now test a request to a `/restricted` resource using the token in Authorization request header.

```sh
curl localhost:1323/restricted -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE0NjE5NTcxMzZ9.RB3arc4-OyzASAaUhC2W3ReWaXAt_z2Fd3BN4aWTgEY"
```
