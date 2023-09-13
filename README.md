nginx-echo is a small docker image based on Alpine that returns the request URI
and hostname of the container. It is used for demonstration purposes or
debugging.

## Extend

If you wish to extend the information returned by nginx you can extend the text
for the return directive in `default.conf`.

## Run

The image is available on Github Packages.

### docker-compose.yml
```
version: '3.1'

services:
  nginx-echo:
    image: ghcr.io/leviscop/nginx-echo:main
    container_name: nginx-echo
    hostname: your.domain.tld
    restart: unless-stopped
    ports:
      - 80:80
```
