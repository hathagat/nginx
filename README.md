# Nginx Images

[![Image Build](https://github.com/hathagat/nginx/actions/workflows/build.yml/badge.svg)](https://github.com/hathagat/nginx/actions/workflows/build.yml)

Images in this repository are based on [this Dockerfile](https://github.com/nginxinc/docker-nginx/blob/master/modules/Dockerfile).  
Additionally they contain the nginx modules `geoip2`, `modsecurity` and `brotli`. For more information see [upstream documentation](https://github.com/nginxinc/docker-nginx/blob/master/modules).  
To use geoip the corresponding database needs to be provided, for example as a volume: `-v /path/on/host/GeoLite2-Country.mmdb:/usr/share/GeoIP/GeoLite2-Country.mmdb`. For more information see [GeoLite2 documentation](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data).

## Available images

```
ghcr.io/hathagat/nginx:latest
ghcr.io/hathagat/nginx:1

```
