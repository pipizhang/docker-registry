# Docker-registry

Run Docker Registry and Docker Registry Web with Docker Compose.

Based on the official Docker images:

* [registry](https://github.com/docker/docker-registry)
* [registry-web](https://github.com/mkuchin/docker-registry-web)

### Getting started

1. Install [Docker](https://www.docker.com/community-edition#/download) version **1.10.0+**
2. Install [Docker Compose](https://docs.docker.com/compose/install/) version **1.6.0+**
3. Clone this repository

### Bringing up the stack

```console
$ docker-compose up
```

You can also choose to run it in background (detached mode):

```console
$ docker-compose up -d
```

By default, the stack exposes the following ports:
* 5000: Registry service.
* 8080: Registry web ui.

### Nginx proxy tips
1. "413 Request Entity Too Large" error
```
client_max_body_size 0;
```
2. "blob upload unknown" error
```
proxy_set_header X-Forwarded-Proto $scheme;
```


License
-------
Copyright (c) 2018-present Peter Zhang. Released under the MIT License. See
[LICENSE.md][license] for details.

[license]: LICENSE.md

