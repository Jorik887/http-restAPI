This is a REST API project using Postgresql

##Getting Started

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
Retrieving User Information (GET):

```
http -v --session=user http://localhost:8080/private/whoami
```


