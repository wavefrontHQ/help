## What is a Cloud Integration?

Wavefront supports cloud integrations, a mechanism that allows you to ingest metrics directly without needing to send them to a Wavefront proxy.
The [Amazon Web Services](http://aws.amazon.com) (AWS) cloud integration is the quickest and easiest way to get
AWS [CloudWatch](http://aws.amazon.com/cloudwatch) and [CloudTrail](http://aws.amazon.com/cloudtrail) data into Wavefront.

Wavefront supports three types of AWS cloud integrations: CloudWatch, CloudTrail, and EC2.

### CloudWatch
The CloudWatch integration retrieves AWS metric and dimension data from AWS services using the AWS CloudWatch
API. The complete list of metrics and dimensions that can be retrieved from AWS CloudWatch is available at Amazon
CloudWatch Metrics and Dimensions
Reference(http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CW_Support_For_AWS.html). In addition, you can
publish custom AWS metrics that are also ingested by the Wavefront CloudWatch integration.

Wavefront adds point tags to CloudWatch metrics:

- accountId - the Amazon account that reported the metric.
- Region - The region in which the service is running. Added to EC2 and EBS metrics only.
- CloudWatch dimensions. The dimensions vary by service. For example, for AWS S3, the BucketName dimension is added as a point tag.

### CloudTrail

The CloudTrail integration retrieves EC2 event information stored in JSON-formatted log files in an AWS S3 bucket and
parses the files for all events that result from an operation that is not a describe, get, or  list, and creates a
Wavefront System event.

### EC2

The EC2 integration retrieves additional metrics using AWS API calls other than CloudWatch:
aws.ebs.volumesize, aws.ebs.volumeiops, aws.ec2.statuscheckfailed_system, aws.instance.price,aws.reservedinstance.count.
