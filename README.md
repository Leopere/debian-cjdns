debian-cjdns
============
[![Docker Build Status](http://hubstatus.container42.com/chamunks/debian-cjdns)](https://registry.hub.docker.com/u/chamunks/debian-cjdns)
[![License: MIT](http://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/chamunks/alpine-openssh/blob/master/LICENSE)

Installation is simple. On first run, cjdns will generate your IP
address. The cjdns configuration lies in `/etc/cjdns` (which is a
docker volume).

To be useful you'll have to run this in privileged mode, with the
same network stack as the host. This can be acomplished using the
docker options `--privileged --net=host`.

    docker pull mildred/cjdns
    docker run --privileged --net=host mildred/cjdns --volume /etc/cjdns:/etc/cjdns
