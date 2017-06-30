### What is a Cloud Integration?

Cloud integrations allow you to ingest metrics directly from cloud services. Wavefront offers [Amazon Web Services](http://aws.amazon.com) [CloudWatch](http://aws.amazon.com/cloudwatch), [CloudTrail](http://aws.amazon.com/cloudtrail), and AWS Metrics+ integrations.

#### CloudWatch

The CloudWatch integration retrieves AWS [metric and
dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CW_Support_For_AWS.html) data.

The metric's [source](https://docs.wavefront.com/integrations_aws_metrics.html#wavefront-source-field) field is set to the Amazon instance ID, the value of [EC2 tags](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html), or the *first* CloudWatch [dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#Dimension). Metrics have the point tags **accountId**, **Region**, and CloudWatch dimensions.

#### CloudTrail

The CloudTrail integration retrieves EC2 event information and creates Wavefront **System** events that represent the AWS events.

#### AWS Metrics+

The AWS Metrics+ integration retrieves additional metrics using AWS APIs other than CloudWatch.

{% include cloud_integrations_add.md %}
