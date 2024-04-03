This is a REST API project using Postgresql

# Getting Started

First, run the server:

```
make
#and
./apiserver
```

To run all tests, use the command:

```
make test
```

Retrieving User Information (GET).This command makes an HTTP GET request to the http://localhost:8080/private/whoami endpoint to retrieve information about the current user. The -v option adds verbose output, and --session=user indicates the use of a session named user, if one exists.

```
http -v --session=user http://localhost:8080/private/whoami
```

User Authentication (POST).Description: This command makes an HTTP POST request to the http://localhost:8080/sessions address to authenticate the user. The request contains the email and password parameters required to log in. The -v option includes verbose output, and --session=user indicates the use of a session named user.
```
http -v --session=user POST http://localhost:8080/sessions email=user@example.org password=password
```

Get information about the user with the source of the request (GET).Description: This command sends an HTTP GET request to the http://localhost:8080/private/whoami address, including the Origin header with the value google.com. The -v option adds verbose output, and --session=user indicates the use of a session named user, if one exists.

```
http -v --session=user http://localhost:8080/private/whoami "Origin: google.com"
```

Sessionless User Authentication (POST): This command makes an HTTP POST request to the http://localhost:8080/sessions address to authenticate the user. The request contains the email and password parameters required to log in. In this case, the session is not used.

```
http POST http://localhost:8080/sessions email=user@example.org password=password
```
