## Debian Cjdns Container

## Installation and Operation
Generate yourself some configs

    docker run -ti --volume --name debian-cjdns $(pwd)/cjdns:/etc/cjdns chamunks/debian-cjdns
This will create cjdns config files in a directory named cjdns nested inside of your current working directory.

You can then modify these config files to your liking. This includes modifying the port you wish to bind cjdns to inside of your container.

Once you've done this you'll want to remove the old container and start a new one with docker run again.

    docker run -d -P hostPort:containerPort --name debian-cjdns chamunks/debian-cjdns

## The Old Method
Installation is simple. On first run, cjdns will generate your IP
address. The cjdns configuration lies in `/etc/cjdns` (which is a
docker volume).

To be useful you'll have to run this in privileged mode, with the
same network stack as the host. This can be accomplished using the
docker options `--privileged --net=host`.

    docker pull mildred/cjdns
    docker run --privileged --net=host mildred/cjdns --volume /etc/cjdns:/etc/cjdns

## Links
[Docker Hub Image](https://registry.hub.docker.com/u/chamunks/debian-cjdns/)
[GitHub Repository](https://github.com/chamunks/debian-cjdns)

## Health & Statistics
#### Repository Health
[![GitHub issues](https://img.shields.io/github/issues/chamunks/debian-cjdns.svg?style=flat-square)](https://github.com/chamunks/debian-cjdns) out of [![GitHub total issues](https://img.shields.io/github/issues-raw/chamunks/debian-cjdns.svg?style=flat-square)](https://github.com/chamunks/debian-cjdns)

#### Container Build Health
[![Docker Pulls](https://img.shields.io/docker/pulls/chamunks/debian-cjdns.svg?style=flat-square)](https://registry.hub.docker.com/u/chamunks/debian-cjdns/)
[![Docker Stars](https://img.shields.io/docker/stars/chamunks/debian-cjdns.svg?style=flat-square)](https://registry.hub.docker.com/u/chamunks/debian-cjdns/)
[![Docker Build Status](http://hubstatus.container42.com/chamunks/debian-cjdns)](https://registry.hub.docker.com/u/chamunks/debian-cjdns)

#### Repository Statistics/Info
[![GitHub license](https://img.shields.io/github/license/chamunks/debian-cjdns.svg?style=flat-square)](https://github.com/chamunks/debian-cjdns)

[![GitHub forks](https://img.shields.io/github/forks/chamunks/debian-cjdns.svg?style=flat-square)](https://github.com/chamunks/debian-cjdns)
[![GitHub stars](https://img.shields.io/github/stars/chamunks/debian-cjdns.svg?style=flat-square)](https://github.com/chamunks/debian-cjdns)
