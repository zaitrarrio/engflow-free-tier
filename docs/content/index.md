#Overview

EngFlow's solutions keep engineers in flow by reducing the amount of time spent building and testing code and 
increasing visibility into your codebase.

## Remote Execution
Speed up your builds with 
[remote execution](https://docs.engflow.com/re/config/index.html) and 
[remote caching](https://docs.engflow.com/re/index.html#storage) using the EngFlow Free Tier or graduate to 
EngFlow Professional and benefit 
from [remote persistent workers](https://docs.engflow.com/re/client/remote-persistent-workers.html) and 
[autoscaling](https://docs.engflow.com/re/config/auto-scaling.html).

Eliminate maintenance overhead with our fully managed remote execution service in the cloud of your choice.

We support all clients that implement the open-source [Remote Execution API](https://github.com/bazelbuild/remote-apis),
including [Bazel](https://bazel.build/), [BuildStream](https://buildstream.build/), 
[Goma Server](https://chromium.googlesource.com/infra/goma/server/), [Pants](https://www.pantsbuild.org/), 
[Please](https://please.build/), [Recc](https://gitlab.com/bloomberg/recc), and [Soong](https://source.android.com/setup/build).

[Contact us](https://www.engflow.com/contact?r=docs) for a custom quote.

## Build and Test UI
If you're running Bazel or other build tools locally, your build and test results are usually output to your console. 

EngFlow's Build and Test UI lets you:

* find out why your builds and tests fail,
* share your build and test results with others for debugging,
* review historical data to discover trends,
* and analyze your runs to optimize your builds and tests.

See the [Build and Test UI documentation](https://docs.engflow.com/web_ui/index.html) for details on the full 
capabilities of EngFlow.  The EngFlow Free Tier provides a visualization onto build results through the 
[Invocation Details](https://docs.engflow.com/web_ui/invocation-page.html) page.

## Bazel Invocation Analyzer
The Bazel Invocation Analyzer is an open-source tool to help build maintainers identify problems in their builds 
and tests.

It is offered as a [standalone webapp](https://analyzer.engflow.com/) and a 
[GitHub repo](https://github.com/EngFlow/bazel_invocation_analyzer) that can be run as a CLI or integrated 
into your own projects.

See the [Bazel Invocation Analyzer documentation](https://docs.engflow.com/bia/index.html) for details.