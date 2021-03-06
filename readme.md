[![License](http://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://raw.githubusercontent.com/tsawler/goblender/master/LICENSE)
[![Version](https://img.shields.io/badge/goversion-1.16.x-blue.svg)](https://golang.org)
<a href="https://golang.org"><img src="https://img.shields.io/badge/powered_by-Go-3362c2.svg?style=flat-square" alt="Built with GoLang"></a>
[![Go Report Card](https://goreportcard.com/badge/github.com/tsawler/vigilate)](https://goreportcard.com/report/github.com/tsawler/vigilate)

# Vigilate

This is the source code for the second project in the Udemy course Working with Websockets in Go (Golang).

A dead simple monitoring service, intended to replace things like Nagios.

## Build

Build in the normal way on Mac/Linux:

~~~
go build -o vigilate cmd/web/*.go
~~~

Or on Windows:

~~~
go build -o vigilate.exe cmd/web/.
~~~

Or for a particular platform:

~~~
env GOOS=linux GOARCH=amd64 go build -o vigilate cmd/web/*.go
~~~

## Requirements

Vigilate requires:
- Postgres 11 or later (db is set up as a repository, so other databases are possible)
- An account with [Pusher](https://pusher.com/), or a Pusher alternative 
(like [ipê](https://github.com/dimiro1/ipe))

## Run

First, make sure ipê is running (if you're using ipê):

On Mac/Linux
~~~
cd ipe
./ipe 
~~~

On Windows
~~~
cd ipe
ipe.exe
~~~

Run with flags:

~~~
./vigilate \
-dbuser='tcs' \
-pusherHost='localhost' \
-pusherPort='4001' \
-pusherKey='123abc' \
-pusherSecret='abc123' \
-pusherApp="1" \
-pusherSecure=false
~~~~


