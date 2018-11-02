# Docker Overview

Docker enables you to separate your applications from your infrastructure and to manage both of them in the same way.

It provides the ability to package and run an application in a loosely isolated environment called a container. You can run many containers simultaneously on a given host (physical or virtual machines).

## Docker architecture

Docker Engine is the heart of Docker and is designed as a client-server application composed by these components:

+ A server running as a daemon process (the `dockerd` command).
+ A REST API that programs can use to talk to the daemon and send command to it.
+ A command line interface (CLI) client (the `docker` command).

### Docker registries

A Docker registry stores Docker images. [Docker Hub](https://hub.docker.com/) and [Docker Cloud](https://cloud.docker.com/) are public registries and you can run your own private registry as well.

### Docker images

An image is a read-only template with instructions for creating a container.

### Docker containers

A container is a runnable instance of an image.

## The underlying technologies

### Namespaces

Docker uses a technology called `namespaces` to provide a layer of isolation for a *container*.

Docker Engine uses these types of namespaces:

+ Process (**`pid`**)
+ Mount (**`mnt`**)
+ IPC (**`ipc`**)
+ Network (**`net`**)
+ User (**`uts`**)

### Control groups

Control groups (`cgroups`) is a technology that limits an application to a set of resources. The most common uses are for container:

+ CPU limits
+ CPU reservations
+ Memory limits
+ Memory reserveations