### What is a Cloud Integration?

Cloud integrations allow you to ingest metrics directly from cloud services. Wavefront offers [Amazon Web Services](http://aws.amazon.com) (AWS) [CloudWatch](http://aws.amazon.com/cloudwatch), [CloudTrail](http://aws.amazon.com/cloudtrail), and EC2 integrations.

#### CloudWatch

The CloudWatch integration retrieves AWS [metric and
dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CW_Support_For_AWS.html) data.

The metric's [source](https://community.wavefront.com/docs/DOC-1031) field is set to the Amazon instance ID, or the value of [EC2 tags](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) or the *first* CloudWatch [dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#Dimension) with the point tags **accountId**, **Region**, and CloudWatch dimensions.

#### CloudTrail

The CloudTrail integration retrieves EC2 event information and creates Wavefront **System** events that represent the AWS events.

#### EC2

The EC2 integration retrieves additional metrics using AWS APIs other than CloudWatch.

{% include cloud_integrations_add.md %}
