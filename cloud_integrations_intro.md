## What is a Cloud Integration?

Cloud integrations allow you to ingest metrics directly from cloud services. Wavefront offers [Amazon Web Services](http://aws.amazon.com) (AWS)
[CloudWatch](http://aws.amazon.com/cloudwatch), [CloudTrail](http://aws.amazon.com/cloudtrail), and EC2 integrations.

### CloudWatch

The CloudWatch integration retrieves AWS [metric and
dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CW_Support_For_AWS.html) data using the AWS
CloudWatch API. If you enable AWS billing alerts, Wavefront reports the metric **aws.billing.estimatedcharges**.

Wavefront sets the value of the metric's [source](https://community.wavefront.com/docs/DOC-1031) field by service:
**EC2**: the value of the **hostname**, **host**, or **name** [EC2
tags](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) or the Amazon instance ID; **EBS**: the Amazon
instance ID; all other services: the value of the *first* CloudWatch
[dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#Dimension). Wavefront
adds the following point tags: **accountId**, **Region**, and CloudWatch dimensions.

### CloudTrail

The CloudTrail integration retrieves EC2 event information stored in log files in an AWS S3 bucket, parses the files for all events that result from write operations, and creates a Wavefront **System** event that represents the AWS event.

### EC2

The EC2 integration retrieves additional metrics with point tags using AWS API other than CloudWatch: **aws.instance.price** , **aws.reservedinstance.count**, **aws.ebs.[volumesize and volumeiops]**.
