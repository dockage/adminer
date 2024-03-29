# Adminer [![Docker Pulls](https://img.shields.io/docker/pulls/dockage/adminer.svg?style=flat)](https://hub.docker.com/r/dockage/adminer/) [![Docker Stars](https://img.shields.io/docker/stars/dockage/adminer.svg?style=flat)](https://hub.docker.com/r/dockage/adminer/) [![MicroBadger](https://images.microbadger.com/badges/image/dockage/adminer.svg)](https://microbadger.com/images/dockage/adminer) [![Docker Automated build](https://img.shields.io/docker/automated/dockage/adminer.svg?style=flat)](https://hub.docker.com/r/dockage/adminer/)
[Adminer](https://www.adminer.org) (formerly phpMinAdmin) is a full-featured database management tool written in PHP. Conversely to [phpMyAdmin](https://www.phpmyadmin.net), it consist of a single file ready to deploy to the target server. Adminer is available for MySQL, PostgreSQL, SQLite, MS SQL, Oracle, Firebird, SimpleDB, Elasticsearch and MongoDB.


## Installation

Pull the image from the docker index. This is the recommended method of installation as it is easier to update image. These builds are performed by the **Docker Trusted Build** service.

```bash
docker pull dockage/adminer:latest
```

Alternately you can build the image locally.

```bash
git clone https://github.com/dockage/adminer.git
cd adminer
docker build --tag="$USER/adminer" .
```


## Quick Start

The quickest way to get started is using [docker-compose](https://docs.docker.com/compose/).

```bash
wget https://raw.githubusercontent.com/dockage/adminer/master/docker-compose.yml
docker-compose up
```

Alternately, you can manually launch the `adminer` container.

```bash
docker run --name='adminer' -d \
  --publish=80:80 \
dockage/adminer:latest
```


## Upgrading

To upgrade to newer `adminer` releases, simply follow this 3 step upgrade procedure.

- **Step 1**: Update the docker image.

```bash
docker pull dockage/adminer:latest
```

- **Step 2**: Stop and remove the currently running image

```bash
docker stop adminer
docker rm adminer
```

- **Step 3**: Start the image

```bash
docker run --name=adminer -d [OPTIONS] dockage/adminer:latest
```

## Quick reference
* Where to get help: [website](https://dockage.dev/), [documentation](https://dockage.dev/docs/)
* GitHub repo: [dockage/adminer](https://github.com/dockage/adminer)
* Where to file issues: [GitHub issues](https://github.com/dockage/adminer/issues)
* Maintained by: The Dockage team (info at dockage.dev)
* License(s) - [license](https://github.com/dockage/adminer/blob/main/LICENSE), check 3rd party documentation for license information