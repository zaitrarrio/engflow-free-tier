# Docker

EngFlow Free Tier is distributed as a Docker image for x86_64 Linux. The images
are hosted by the [GitHub container
registry](https://github.com/EngFlow/free/pkgs/container/free). Run the
following to start up a EngFlow Free Tier instance that stores its data in
`/tmp/engflow_data`:
```commandline
$ docker run --init --rm --mount=type=bind,src=/var/run/docker.sock,dst=/var/run/docker.sock -v /tmp/engflow_data:/tmp/engflow_data -e DATA_DIR=/tmp/engflow_data -p 8080:8080 ghcr.io/engflow/free:2.8.0
```
