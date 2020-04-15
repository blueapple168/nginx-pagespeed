# ngx-pagespeed-alpine
ngx_pagespeed Dockerfile for Alpine, based on wernight/docker-alpine-nginx-pagespeed

## Docker base
This image is based on Alpine Linux version latest(3.8)

## Pagespeed Components:
### mod-pagespeed
1.13.35.2
### ngx-pagespeed
1.13.35.2
### Nginx
Stable NGINX version 1.16.0 fetched from [nginx.org](http://nginx.org/download) .

This image should be a 100% compatible drop in replacement for the official nginx image.

## Using the Dockerfile
### Use docker build command to build an image from dockerfile:
    $ docker build -t <image_tag> -f <dockerfile_path> .
  Refer [this](https://docs.docker.com/engine/reference/commandline/build/) for additional options.

### Run this container as an independent service(80 or 443):
    $ docker run -d -p 80:80 <image_tag>
      or
    $ docker run -d -p 443:443 <image_tag>  
  Refer [this](https://docs.docker.com/engine/reference/run/) for additional options.
### Run this container as an independent service with docker-compose.
    $ git clone https://github.com/blueapple168/nginx-pagespeed.git
    $ docker-compose up -d
   Refer [this](https://docs.docker.com/compose/reference/run/) for additional options.
# Configuration Pagespeed
The config is set using environments
### default values
PAGESPEED_ENABLE=on # || off
## TODO
- Be 100% compatible with nginx 1.14.0 image on dockerhub when released, for now 100% compatible with 1.12.2 image
- Create a dockerhub repo
