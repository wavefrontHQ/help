### What is a Cloud Integration?

<!--This panel shows up when you select https://<server>.wavefront.com/extdata-->

Cloud integrations allow you to ingest metrics directly from cloud services. Wavefront offers a number of integrations from several vendors:

* Amazon (CloudWatch, CloudTrail and AWS Metrics+)
* Google Cloud Provider
* Microsoft Azure

**CloudWatch**<br/>
The CloudWatch integration retrieves AWS [metric and
dimension](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CW_Support_For_AWS.html) data.

**CloudTrail**<br/>
The CloudTrail integration retrieves EC2 event information and creates Wavefront **System** events that represent the AWS events.

**AWS Metrics+**<br/>
The AWS Metrics+ integration retrieves additional metrics using AWS APIs other than CloudWatch.

**Google Cloud Platform**<br/>
The Google Cloud Platform integration supports data ingestion of GCP metric data and includes predefined dashboards and alert conditions.

**Microsoft Azure**<br/>
The Microsoft Azure integration enables monitoring of Azure metrics with Wavefront and includes predefined dashboards and alert conditions.
