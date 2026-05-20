# Nginx Images

[![Image Build](https://github.com/hathagat/nginx/actions/workflows/build.yml/badge.svg)](https://github.com/hathagat/nginx/actions/workflows/build.yml)
[![Alpine Image Build](https://github.com/hathagat/nginx/actions/workflows/build-alpine.yml/badge.svg)](https://github.com/hathagat/nginx/actions/workflows/build-alpine.yml)

Custom Nginx container images based on the [upstream module Dockerfiles](https://github.com/nginxinc/docker-nginx/tree/master/modules), extended with the `geoip2` and `brotli` modules pre-installed and loaded. Apart from that, the [upstream documentation](https://github.com/nginxinc/docker-nginx/blob/master/modules/README.md) still applies.

## Features

- Based on the official `nginx:<version>` and `nginx:<version>-alpine` images
- `ngx_http_geoip2_module` loaded by default
- `ngx_http_brotli_filter_module` and `ngx_http_brotli_static_module` loaded by default
- `keepalive_timeout` removed from `nginx.conf` so it can be set per environment
- Images signed with [cosign](https://github.com/sigstore/cosign) (keyless, GitHub OIDC)

## Available images

```
ghcr.io/hathagat/nginx:latest
ghcr.io/hathagat/nginx:1

ghcr.io/hathagat/nginx:alpine
ghcr.io/hathagat/nginx:1-alpine
```

All four tags point to the same image and are rebuilt weekly (Sundays 01:00 UTC) from the latest upstream nginx 1.x release.

## Usage

The images are drop-in replacements for the corresponding `nginx:<version>` images. All environment variables, configuration paths and volume conventions from the [upstream image](https://hub.docker.com/_/nginx) are supported.

GeoIP2 requires a database to be mounted at runtime, for example:

```
-v /path/on/host/GeoLite2-Country.mmdb:/usr/share/GeoIP/GeoLite2-Country.mmdb
```

See the [GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) and [geoipupdate](https://github.com/maxmind/geoipupdate/blob/main/doc/docker.md) documentation for details.
