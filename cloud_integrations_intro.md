## What is a Cloud Integration?

Cloud integrations allow you to ingest metrics directly from cloud services without needing to send them to a Wavefront proxy. Wavefront offers [Amazon Web Services](http://aws.amazon.com) (AWS) [CloudWatch](http://aws.amazon.com/cloudwatch), [CloudTrail](http://aws.amazon.com/cloudtrail), and EC2 integrations.

### CloudWatch
The CloudWatch integration retrieves AWS [metric and dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CW_Support_For_AWS.html) data from AWS services using the AWS CloudWatch API.

Wavefront sets the value of the CloudWatch metric [source](https://community.wavefront.com/docs/DOC-1031) field by service:

-   **EC2** - the value of the **hostname**, **host**, or **name** [EC2 tags](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html), if the tags exist and you have an EC2 integration. Otherwise, the source is set to the Amazon instance ID.
-   **ELB** - the Amazon instance ID of the EC2 instance the load balancer is attached to.
-   All other services - the value of the *first* CloudWatch [dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch_concepts.html#Dimension).

Wavefront adds point tags to CloudWatch metrics:

- **accountId** - the Amazon account that reported the metric.
- **Region** - The region in which the service is running. Added to EC2 and EBS metrics only.
- CloudWatch dimensions. The dimensions vary by service. For AWS S3, the BucketName dimension is added as a point tag.

If you enable AWS billing alerts, Wavefront reports the metric **aws.billing.estimatedcharges**.

### CloudTrail

The CloudTrail integration retrieves EC2 event information stored in log files in an AWS S3 bucket, parses the files for all events that result from an operation that is not a describe, get, or list, and creates a Wavefront **System** event that represents the AWS event.

### EC2

The EC2 integration retrieves additional metrics with point tags using AWS API other than CloudWatch:

- **aws.instance.price** - instances and how much they cost per hour.
- **aws.reservedinstance.count** - ihe number of reserved instances in each availability zone by each instance type.
- **aws.ebs.volumesize** - ihe volume size of the elastic block store attached to EC2 instance(s).
- **aws.ebs.volumeiops** - ihe volume I/O operations of the elastic block store attached to EC2 instance(s).
