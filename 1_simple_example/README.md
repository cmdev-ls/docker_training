# Simple Dockerfile

A very simple, basic Dockerfile that creates a linux container that could form the basis of numerous
applications.

Simply prints out information on the Alpine distribution using 
[screenfetch](https://github.com/KittyKatt/screenFetch).

## Usage

__Build__

```shell
docker build . -t simple_docker
```

__Run__

```shell
docker run simple_docker
```

## Components

Makes use of five docker commands.

* [FROM](https://docs.docker.com/engine/reference/builder/#from) - 
Initialises the build stage and base image for subsequent commands
* [ENV](https://docs.docker.com/engine/reference/builder/#env) -
Sets environment variables used in the docker build process
* [RUN](https://docs.docker.com/engine/reference/builder/#run) -
Runs a specific command or set of commands
* [WORKDIR](https://docs.docker.com/engine/reference/builder/#workdir) -
Sets the working directory within which all subsequent commands will be run
* [CMD](https://docs.docker.com/engine/reference/builder/#cmd) - 
The default command that is run by the container
  
## Debugging

You can run the container in "interactive" mode to inspect it or test commands before adding them to
the Dockerfile

```shell
docker run -it simple_docker bash
```

This overrides the default command and opens a bash session.

## Tasks
* Change the working directory at build time using 
[--build-arg](https://docs.docker.com/engine/reference/commandline/build/#set-build-time-variables---build-arg)
* Optimise the DockerFile, as it is 8 layered images will be created, what's the smallest number
that can create the same image?

  