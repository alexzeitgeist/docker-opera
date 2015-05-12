# zeitgeist/docker-opera

[Opera beta](http://www.opera.com/computer/beta) (latest version) in a Docker container.

## Requirements

* [Docker](https://www.docker.com/) 1.6+ (previous versions may work fine, but I haven't tried)
* An X11 socket

## Installation

Get the [trusted build on the docker hub](https://registry.hub.docker.com/u/zeitgeist/docker-opera/):

```bash
$ docker pull zeitgeist/docker-opera
```

or download and compile the source yourself from Github:

```bash
$ git clone https://github.com/alexzeitgeist/docker-opera.git
$ cd docker-opera
$ docker build -t zeitgeist/docker-opera .
```

## Usage

```bash
$ docker run --rm \
  -v /tmp/.X11-unix:/tmp/.X11-unix:ro \
  -e DISPLAY=unix$DISPLAY \
  zeitgeist/docker-opera
```
