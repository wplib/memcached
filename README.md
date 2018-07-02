![memcached 1.5.x](https://img.shields.io/badge/memcached-1.5.x-green.svg)

![WPLib-Box](https://github.com/wplib/wplib.github.io/raw/master/WPLib-Box-100x.png)


# memcached Docker Container for WPLib Box
This is the repository for the [memcached-docker](https://memcached.org/) Docker container implemented for [WPLib-Box](https://github.com/wplib/wplib-box).
It currently provides versions 1.5.x


## Supported tags and respective Dockerfiles

`1.5.7`, `1.5`, `latest` _([1.5.7/Dockerfile](https://github.com/wplib/memcached-docker/blob/master/1.5.7/Dockerfile))_


## Using this container.
If you want to use this container as part of WPLib, then use the Docker Hub method.
Or you can use the GitHub method to build and run the container.


## Using it from Docker Hub

### Links
(Docker Hub repo)[https://hub.docker.com/r/wplib/memcached/]

(Docker Cloud repo)[https://cloud.docker.com/swarm/wplib/repository/docker/wplib/memcached/]


### Setup from Docker Hub
A simple `docker pull wplib/memcached` will pull down the latest version.


### Runtime from Docker Hub
start - Spin up a Docker container with the correct runtime configs.

`docker run -d --name wplib_memcached_1.5.7 --restart unless-stopped --network wplibbox -p 11211:11211  wplib/memcached:1.5.7`

stop - Stop a Docker container.

`docker stop wplib_memcached_1.5.7`

run - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.

`docker run --rm --name wplib_memcached_1.5.7 --network wplibbox -p 11211:11211  wplib/memcached:1.5.7`

shell - Run a shell, (/bin/bash), within a Docker container.

`docker run --rm --name wplib_memcached_1.5.7 -i -t --network wplibbox -p 11211:11211  wplib/memcached:1.5.7 /bin/bash`

rm - Remove the Docker container.

`docker container rm wplib_memcached_1.5.7`


## Using it from GitHub repo

### Setup from GitHub repo
Simply clone this repository to your local machine

`git clone https://github.com/wplib/memcached-docker.git`


### Building from GitHub repo
`make build` - Build Docker images. Build all versions from the base directory or specific versions from each directory.


`make list` - List already built Docker images. List all versions from the base directory or specific versions from each directory.


`make clean` - Remove already built Docker images. Remove all versions from the base directory or specific versions from each directory.


`make push` - Push already built Docker images to Docker Hub, (only for WPLib admins). Push all versions from the base directory or specific versions from each directory.


### Runtime from GitHub repo
When you `cd` into a version directory you can also perform a few more actions.

`make start` - Spin up a Docker container with the correct runtime configs.


`make stop` - Stop a Docker container.


`make run` - Run a Docker container in the foreground, (all STDOUT and STDERR will go to console). The Container be removed on termination.


`make shell` - Run a shell, (/bin/bash), within a Docker container.


`make rm` - Remove the Docker container.


`make test` - Will issue a `stop`, `rm`, `clean`, `build`, `create` and `start` on a Docker container.


