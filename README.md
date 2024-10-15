# Nginx Images

[![Image Build](https://github.com/hathagat/nginx/actions/workflows/build.yml/badge.svg)](https://github.com/hathagat/nginx/actions/workflows/build.yml) 
[![Alpine Image Build](https://github.com/hathagat/nginx/actions/workflows/build-alpine.yml/badge.svg)](https://github.com/hathagat/nginx/actions/workflows/build-alpine.yml)

Images in this repository are based on [this Dockerfiles](https://github.com/nginxinc/docker-nginx/blob/master/modules).  
Additionally they contain the nginx modules `geoip2`and `brotli`. For more information see [upstream documentation](https://github.com/nginxinc/docker-nginx/blob/master/modules).  
To use geoip the corresponding database needs to be provided, for example as a volume: `-v /path/on/host/GeoLite2-Country.mmdb:/usr/share/GeoIP/GeoLite2-Country.mmdb`. For more information, see [GeoLite2](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) and GeoIP update (https://github.com/maxmind/geoipupdate/blob/main/doc/docker.md) documentations.

## Available images

```
ghcr.io/hathagat/nginx:latest
ghcr.io/hathagat/nginx:1

ghcr.io/hathagat/nginx:alpine
ghcr.io/hathagat/nginx:1-alpine
```
