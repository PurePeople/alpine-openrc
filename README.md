# Deprecated
## Please use `*-openrc` branches of [dockage/alpine](https://github.com/dockage/alpine) instead of this project. 
# alpine-openrc [![Docker Pulls](https://img.shields.io/docker/pulls/dockage/alpine-openrc.svg)](https://hub.docker.com/r/dockage/alpine-openrc/) [![Docker Stars](https://img.shields.io/docker/stars/dockage/alpine-openrc.svg?style=flat)](https://hub.docker.com/r/dockage/alpine-openrc/) [![MicroBadger](https://images.microbadger.com/badges/image/dockage/alpine-openrc:3.7.svg)](https://microbadger.com/images/dockage/alpine-openrc:3.7) [![Docker Build Status](https://img.shields.io/docker/build/dockage/alpine-openrc.svg)](https://hub.docker.com/r/dockage/alpine-openrc/) [![Docker Automated build](https://img.shields.io/docker/automated/dockage/alpine-openrc.svg)](https://hub.docker.com/r/dockage/alpine-openrc/)
    
[OpenRC](https://en.wikipedia.org/wiki/OpenRC) is the default init system of [Gentoo](https://gentoo.org), [Alpine Linux](https://alpinelinux.org              ) and other Linux distributions, which means that the software packages and daemons of those distributions support it, coming with or using the available scripts.


## Contributing

If you find this image useful here's how you can help:

- Send a pull request with your awesome features and bug fixes
- Help users resolve their [issues](../../issues?q=is%3Aopen+is%3Aissue).

## Issues

Before reporting your issue please try updating Docker to the latest version and check if it resolves the issue. Refer to the Docker [installation guide](https://docs.docker.com/installation) for instructions.

SELinux users should try disabling SELinux using the command `setenforce 0` to see if it resolves the issue.

If the above recommendations do not help then [report your issue](../../issues/new) along with the following information:

- Output of the `docker vers6` and `docker info` commands
- The `docker run` command or `docker-compose.yml` used to start the image. Mask out the sensitive bits.
- Please state if you are using [Boot2Docker](http://www.boot2docker.io), [VirtualBox](https://www.virtualbox.org), etc.

# Getting started

## Installation

Automated builds of the image are available on [Dockerhub](https://hub.docker.com/r/dockage/alpine-openrc) and is the recommended method of installation.

> **Note**: Builds are also available on [Quay.io](https://quay.io/repository/dockage/alpine-openrc)

```bash
docker pull dockage/alpine-openrc:3.7
```

Alternatively you can build the image yourself.

```bash
docker build -t dockage/alpine-openrc github.com/dockage/alpine-openrc
```

# Maintenance

## Upgrading

To upgrade to newer releases:

  1. Download the updated Docker image:

  ```bash
  docker pull dockage/alpine-openrc:3.7
  ```

  2. Stop the currently running image:

  ```bash
  docker stop alpine-openrc
  ```

  3. Remove the stopped container

  ```bash
  docker rm -v alpine-openrc
  ```

  4. Start the updated image

  ```bash
  docker run --name alpine-openrc -itd \
    [OPTIONS] \
    dockage/alpine-openrc:3.7
  ```

## Shell Access

For debugging and maintenance purposes you may want access the containers shell. If you are using Docker version `1.3.0` or higher you can access a running containers shell by starting `bash` using `docker exec`:

```bash
docker exec -it alpine-openrc sh
