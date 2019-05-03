#test in github

INFO TAB

\<monitor logo>
# \<Monitor name>

Metadata associated with the \<name> collectd plugin can be found _here_. The relevant code for the plugin can be found _here_.

- [Description](#description)
- [Features](#features)
- [Use](#use)
- [Metrics](#metrics)
- [Dimensions](#dimensions)

## Description

Monitors \<what> using the information provided by \<what> which collects metrics from \<what> instances by hitting these endpoints: 
* <link to item>
* <link to item>

## Features

For more information on the source data, see <https://...>

Monitor Source Code \<link>

Accepts Endpoints: <yes/no>

Multiple Instances Allowed: <yes/no>


## Use

What the monitor is used for -- which metrics and for what -- discussion


## Metrics

Besides the common default metrics that are described [here](https://docs.signalfx.com/en/latest/integrations/agent/monitor-config.html), the following table shows additional optional metrics available for this monitor. Metrics that are marked as Default are standard metrics that are monitored by default. You may need to add a flag to these metrics. Check the config file for flag requirements.
 

| Name | Type | Default | Description |
| ---  | ---  | ---    | ---         |
| `name1` | counter | ✔ | Total connections count per broker |
| `name2` | gauge | ✔ | Total number of consumers subscribed to destinations on the broker |
| `name3` | gauge |  | Total number of messages that have been acknowledged from the broker. |


### Optional metric configuration

To collect optional metrics, you must configure your monitor to listen for those metrics and then send those metrics to the agent.

To specify optional metrics, add a _metricsToInclude_ filter to the agent configuration file, as shown in the code snippet below. The snippet lists all available optional metrics. Copy and paste the snippet into your monitor configuration file, then delete any optional metrics that you do not want.

Note that some of the optional metrics require you to set a flag in addition to adding them to the metricsToInclude list. Check the monitor configuration file to see if a flag is required for gathering optional metrics.

```
sh
metricsToInclude:
  - metricNames:
    - name1
    - name2
    monitorType: <name>
```

## Dimensions

The following dimensions may occur on metrics emitted by this monitor. Some dimensions may be specific to certain metrics; other dimensions can be configured. You can add extra dimensions to most metrics. The Common Configuration options page [here](https://docs.signalfx.com/en/latest/integrations/agent/monitor-config.html) also describes how to configure for these extra dimensions. 

| Name | Description |
| ---  | ---         |
| `container_id` | The ID of the running container |
| `container_image` | The container image name |
| `container_name` | The container's name as it appears in the pod spec, the same as container_spec_name but retained for backwards compatibility. |
| `container_spec_name` | The container's name as it appears in the pod spec |



INSTALLATION TAB

# Installing the monitor

- [Requirements and Dependencies](#requirements-and-Dependencies)
- [Installation](#installation)
- [Configuration](#Configuration)
- [Confirmation](#Confirmation)
- [Troubleshooting](#Troubleshooting)

## Requirements and Dependencies


## Installation


## Configuration 

| Config option | Required | Type | Description |
| --- | --- | --- | --- |
| `kubeletAPI` | no | `object (see below)` | Kubelet client configuration |


The **nested** `kubeletAPI` config object has the following fields:

| Config option | Required | Type | Description |
| --- | --- | --- | --- |
| `url` | no | `string` | URL of the Kubelet instance.  This will default to `https://<current node hostname>:10250` if not provided. |
| `authType` | no | `string` | Can be `none` for no auth, `tls` for TLS client cert auth, or `serviceAccount` to use the pod default service account token to authenticate. (**default:** `none`) |
| `skipVerify` | no | `bool` | Whether to skip verification of the Kubelet TLS cert (**default:** `true`) |


### YAML config
Sample YAML config with custom query:

```sh
monitors:
- type: collectd/couchbase
  host: 127.0.0.1
  port: 8091
  collectTarget: "NODE"
  clusterName: "my-cluster"
  username: "user"
  password: "password" 
```

### More Configuration options

In addition to the common configuration options shown [here](https://docs.signalfx.com/en/latest/integrations/agent/monitor-config.html), the following configuration options can be set:

Config option	Required	Type	Description
item 						
item 						
item 						


## Confirmation

To confirm your installation is functioning properly...


## Troubleshooting

/<This is troubleshooting the monitor installation.>



USAGE TAB


# Monitoring metrics 

- [Dashboards](#Dashboards)
- [How to](#how-to)
- [Sample code for the how to](#sample-code-for-the-how-to])


## Dashboards

Dashboards in which the default metrics from this monitor display are shown below.

/<dashboard screen shots>

## How To

/<Examples of how to use the monitor, dashboards, and metrics for a meaningful task.>


## Sample code for the how to

/<This is where you can put the sample coding that matches the "how to" section above.>












