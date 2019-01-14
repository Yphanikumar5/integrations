# ![](https://github.com/signalfx/integrations/blob/master/collectd-elasticsearch/img/integrations_elasticsearch.png) Elasticsearch

[![GoDoc](https://godoc.org/github.com/signalfx/signalfx-agent?status.svg)](https://godoc.org/github.com/signalfx/signalfx-agent)
[![CircleCI](https://circleci.com/gh/signalfx/signalfx-agent.svg?style=shield)](https://circleci.com/gh/signalfx/signalfx-agent)

The SignalFx Smart Agent is a metric agent written in Go for monitoring
infrastructure and application services in a variety of different environments.
It is meant as a successor to our previous [collectd
agent](https://github.com/signalfx/collectd), but still uses that internally --
so any existing Python or C-based collectd plugins will still work without
modification.

For details on the SignalFx SmartAgent, see the [Smart Agent Read Me] (https://github.com/signalfx/signalfx-agent).

 - [Installation](#installation)
 - [Deployment](#deployment)
 - [Usage](###usage)
 - [Metrics](###metrics)
 - [License](###license)


## Installation

The agent is available for Linux in both a containerized and standalone form.
Whatever form you use, the dependencies are completely bundled along with the
agent, including a Java JRE runtime and a Python runtime, so there are no
additional dependencies required.  This means that the agent should work on any
relatively modern Linux distribution (kernel version 2.6+).  To get started
deploying the Smart Agent directly on a host, see the
[Smart Agent Quickstart](./docs/smart-agent-quickstart.md) guide.

### Deployment
We support the following deployment/configuration management tools to automate the
installation process.  See [Bundles](#bundles) for a list of underlying
packages for the agent.

#### Installer Script
For non-containerized environments, there is a convenience script that you can
run on your host to install the agent package.  This is useful for testing and
trials, but for full-scale deployments you will probably want to use a
configuration management system like Chef or Puppet.  You can [view the source
for the installer
script](./deployments/installer/install.sh)
and use it on your hosts by running:

```sh
curl -sSL https://dl.signalfx.com/signalfx-agent.sh > /tmp/signalfx-agent.sh
sudo sh /tmp/signalfx-agent.sh YOUR_SIGNALFX_API_TOKEN
```
### USAGE

Samples of the built-in Elasticsearch dashboard in SignalFx:

![](././img/dashboard_elasticsearch.png)

### METRICS

For documentation of the metrics and dimensions emitted by this plugin, [click here](./docs).

### LICENSE

This integration is released under the Apache 2.0 license. See [LICENSE](./LICENSE) for more details.
