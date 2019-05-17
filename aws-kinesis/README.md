# ![](./img/integration_awskinesisstreams.png) AWS Kinesis

- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Metrics](#metrics)
- [Recommended metrics](#recommended-metrics)
- [License](#license)

### DESCRIPTION

Use SignalFx to monitor AWS Kinesis via [Amazon Web Services](https://github.com/signalfx/integrations/tree/master/aws)[](sfx_link:aws).

#### FEATURES

##### Built-in dashboards

- **Kinesis Streams Overview**: Overview of all streams and data from Kinesis.

  [<img src='./img/dashboard_kinesis_overview.png' width=200px>](./img/dashboard_kinesis_overview.png)

- **Kinesis Stream**: Focus on a single Kinesis Stream.

  [<img src='./img/dashboard_kinesis_stream.png' width=200px>](./img/dashboard_kinesis_stream.png)

### INSTALLATION

To access this integration, [connect to CloudWatch](https://github.com/signalfx/integrations/tree/master/aws)[](sfx_link:aws).

By default, SignalFx will import all CloudWatch metrics that are available in your account. To retrieve metrics for a subset of available services or regions, modify the connection on the Integrations page.

### USAGE

SignalFx provides built-in dashboards for this service. Examples are shown below.

![](./img/dashboard_kinesis_overview.png)

![](./img/dashboard_kinesis_stream.png)

### METRICS

For more information about the metrics emitted by AWS Kinesis, visit the service homepage at <a target="_blank" href="https://aws.amazon.com/kinesis/">https://aws.amazon.com/kinesis/</a>.

### RECOMMENDED METRICS

The following are a subset of available metrics; these statistics are recommended by Amazon for collection.

_Stream level metrics_

GetRecords.Bytes: Minimum, Maximum, Average, Sum, Count

GetRecords.IteratorAgeMilliseconds: Maximum

GetRecords.Latency: Minimum, Maximum, Average

GetRecords.Records: Minimum, Maximum, Average, Sum, Count

GetRecords.Success: Average, Sum, Count

IncomingBytes: Minimum, Maximum, Average, Sum, Count

IncomingRecords: Minimum, Maximum, Average, Sum, Count

PutRecord.Bytes: Minimum, Maximum, Average, Sum, Count

PutRecord.Latency: Minimum, Maximum, Average

PutRecord.Success: Average, Sum, Count

PutRecords.Bytes: Minimum, Maximum, Average, Sum, Count

PutRecords.Latency: Minimum, Maximum, Average

PutRecords.Records: Minimum, Maximum, Average, Sum, Count

PutRecords.Success: Average, Sum, Count

ReadProvisionedThroughputExceeded: Average

SubscribeToShard.RateExceeded

SubscribeToShard.Success

SubscribeToShardEvent.Bytes: Minimum, Maximum, Average, Sum, Count

SubscribeToShardEvent.MillisBehindLatest: Minimum, Maximum, Average, Count

SubscribeToShardEvent.Records: Minimum, Maximum, Average, Sum, Count

SubscribeToShardEvent.Success: Minimum, Maximum, Average, Sum, Count

WriteProvisionedThroughputExceeded: Average

_Enhanced shard level metrics_

IncomingBytes: Minimum, Maximum, Average, Sum, Count

IncomingRecords: Minimum, Maximum, Average, Sum, Count

IteratorAgeMilliseconds: Minimum, Maximum, Average, Count

OutgoingBytes: Minimum, Maximum, Average, Sum, Count

ReadProvisionedThroughputExceeded: Minimum, Maximum, Average, Sum, Count

WriteProvisionedThroughputExceeded: Minimum, Maximum, Average, Sum, Count


### LICENSE

This integration is released under the Apache 2.0 license. See [LICENSE](./LICENSE) for more details.
