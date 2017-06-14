# Directory API
[![Build Status](https://travis-ci.org/zero-os/0-directory.svg?branch=master)](https://travis-ci.org/zero-os/0-directory)

This directory service is the door step of the Zero-OS grid.

## How to build
```shell
cd $GOPATH/src/github.com/zero-os/
git clone https://github.com/zero-os/0-directory.git
cd directory
go generate
go build
```

## How to Use
```shell
NAME:
   0-Directory - A new cli application

USAGE:
   directory [global options] command [command options] [arguments...]

VERSION:
   0.0.1

COMMANDS:
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --debug, -d                         Enable debug logging
   --bind value, -b value              Bind address (default: ":8443")
   --connectionstring value, -c value  Mongodb connection string (default: "127.0.0.1:27017")
   --help, -h                          show help
```

### Setup mongodb
The directory uses mongodb as database. The deployement of mongodb is not convered in this readme, check the [official documentation](https://docs.mongodb.com/manual/installation/).

### Start directory server
This command will start the directory server listening on all interface on the 8080 port and connect to a mongodb instance running on localhost and port 27017
```shell
./directory --bind ":8080" --connectionstring "127.0.0.1:27017"
```

## [API specification](https://rawgit.com/zero-os/0-directory/master/specs/directory.html)

## Release schedule:
- 17 June 2017:  [v0.1.0](milestones/0.1.0.md):  
First usable version, beta state
- 19 June 2017:  [v0.2.0](milestones/0.2.0.md):  
All tested and documented
