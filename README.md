# Adminer [![Docker Pulls](https://img.shields.io/docker/pulls/dockage/adminer.svg?style=flat)](https://hub.docker.com/r/dockage/adminer/) [![Docker Stars](https://img.shields.io/docker/stars/dockage/adminer.svg?style=flat)](https://hub.docker.com/r/dockage/adminer/) [![Docker Automated build](https://img.shields.io/docker/automated/dockage/adminer.svg?style=flat)](https://hub.docker.com/r/dockage/adminer/)
[Adminer](https://www.adminer.org) (formerly phpMinAdmin) is a full-featured database management tool written in PHP. Conversely to [phpMyAdmin](https://www.phpmyadmin.net), it consist of a single file ready to deploy to the target server. Adminer is available for MySQL, PostgreSQL, SQLite, MS SQL, Oracle, Firebird, SimpleDB, Elasticsearch and MongoDB.


## Installation

Pull the image from the docker index. This is the recommended method of installation as it is easier to update image. These builds are performed by the **Docker Trusted Build** service.

```bash
docker pull dockage/adminer:4.2.5
```

You can also pull the `latest` tag which is built from the repository *HEAD*

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
dockage/adminer:4.2.5
```
