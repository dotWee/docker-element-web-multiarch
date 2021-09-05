<p align="center">
    <a href="https://element.io/"><img src="https://element.io/images/logo-ele-secondary.svg"/></a>
    </br>
    <a href="https://github.com/dotWee/docker-element-web/actions/workflows/cron.yml"><img src="https://github.com/dotWee/docker-element-web/actions/workflows/cron.yml/badge.svg"/></a>
    <a href="https://github.com/dotWee/docker-element-web/actions"><img src="https://badgen.net/github/checks/dotwee/docker-element-web?icon=github&label=status"/></a>
    <a href="https://github.com/dotwee/docker-element-web/blob/master/LICENSE"><img src="https://badgen.net/github/license/dotwee/docker-element-web?color=cyan&icon=github"/></a>
    <a href="https://github.com/dotwee/docker-element-web/pulls"><img alt="GitHub pullrequests" src="https://badgen.net/github/prs/dotwee/docker-element-web?label=pull-requests&icon=github"/></a>
    <a href="https://github.com/dotwee/docker-element-web/issues"><img src="https://badgen.net/github/issues/dotwee/docker-element-web?icon=github"/></a>
    <a href="https://cloud.docker.com/u/dotwee/repository/docker/dotwee/element-web"><img src="https://badgen.net/docker/size/dotwee/element-web?icon=docker&label=size"/></a>
    <a href="https://cloud.docker.com/u/dotwee/repository/docker/dotwee/element-web"><img src="https://badgen.net/docker/pulls/dotwee/element-web?icon=docker&label=pulls"/></a>
</p>

This project is on charge of checking everyday if there is a new [Element](https://element.io/) version and create the proper docker image and push it to the [hub](https://hub.docker.com/r/dotwee/element-web/) as need it.

_What makes this docker image different from the original ([`vectorim/element-web`](https://hub.docker.com/r/vectorim/element-web))?_

> This image includes nginx with support for pretty much every common cpu arch:

> - `linux/386`
> - `linux/amd64`
> - `linux/arm/v6`
> - `linux/arm/v7`
> - `linux/arm64`
> - `linux/ppc64le`
> - `linux/s390x`

# What is Element?

[Element](https://element.io/features) (formerly known as Vector/Riot) is a web client for [Matrix](https://matrix.org) an open network for secure, decentralized communication.

## How to use the docker image

### Pull the image

From GitHub Package Repository: `docker pull ghcr.io/dotwee/element-web:latest`

From Docker Hub Registry: `docker pull dotwee/element-web:latest`

### Run the image

```bash
$ docker run --name element -p 8080:80 -d ghcr.io/dotwee/element-web
```

Then you can hit [http://localhost:8080](http://localhost:8080) in your browser.

## Element configuration

```bash
$ docker run -v /host/path/config.json:/etc/element-web/config.json:ro --name element -p 8080:80 -d ghcr.io/dotwee/element-web
```
For information on the syntax of the element configuration file, see [the official documentation](https://github.com/vector-im/element-web#configjson).

## HTTP server configuration

```bash
$ docker run -v /host/path/nginx.conf:/etc/nginx/nginx.conf:ro --name element -p 8080:80 -d ghcr.io/dotwee/element-web
```

For information on the syntax of the nginx configuration files, see [the official documentation](http://nginx.org/en/docs/) (specifically the [Beginner's Guide](http://nginx.org/en/docs/beginners_guide.html#conf_structure)).

## Other references

- [GitHub repository dotWee/docker-element-web](https://github.com/dotWee/docker-element-web)
- [GitHub packages page dotwee/element-web](https://github.com/dotWee/docker-element-web/pkgs/container/element-web)
- [Docker Hub page dotwee/element-web](https://hub.docker.com/r/dotwee/element-web)
