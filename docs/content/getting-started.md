# Getting Started

EngFlow Free Tier is distributed as a Docker image for x86_64 Linux. The images
are hosted by the [GitHub container
registry](https://github.com/EngFlow/free/pkgs/container/free). Run the
following to start up a EngFlow Free Tier instance that stores its data in
`/tmp/engflow_data`:

    $ docker run --init --rm --mount=type=bind,src=/var/run/docker.sock,dst=/var/run/docker.sock -v /tmp/engflow_data:/tmp/engflow_data -e DATA_DIR=/tmp/engflow_data -p 8080:8080 ghcr.io/engflow/free:2.8.0


Once EngFlow starts up, it will print configuration hints for Bazel.  Try it out
as a remote executor on your own Bazel project or on the [EngFlow example
repository](https://github.com/engflow/example):

    $ git clone https://github.com/engflow/example engflow-example
    $ cd engflow-example
    $ bazel test --config engflow --bes_results_url=http://127.0.0.1:8080/invocation/ --bes_backend=grpc://127.0.0.1:8080 --remote_executor=grpc://127.0.0.1:8080 //java/...

Bazel should print a URL to view the EngFlow build UI for the build in a web
browser.

EngFlow requires a Docker image to execute remote actions in, else the following error occurs:
```
ERROR: ... (Exit 34): INVALID_ARGUMENT: No matching action runner found (available: com.engflow.re.exec.docker.CachedDockerActionRunner@c4bf93d,com.engflow.re.exec.docker.DockerActionRunner@28c06c4), client-provided platform proto:
```
The EngFlow
example repository configures the image using the `rbe_autoconfig` workspace
rule from
[bazel-toolchains](https://github.com/bazelbuild/bazel-toolchains). For simple
usecases, an image may be passed via Bazel's `--remote_default_exec_properties`
flag. For instance,
`--remote_default_exec_properties=container-image=docker://docker.io/ubuntu:focal-20210827`
to run remote actions in a recent Ubuntu container.
