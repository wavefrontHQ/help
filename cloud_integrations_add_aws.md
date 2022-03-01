### Add an Amazon Cloud Integration

Setting up an Amazon cloud integration requires establishing a trust relationship between Amazon and Wavefront.

You start by granting Wavefront read-only access to your Amazon account or by giving Wavefront limited access. 

Then, you register the integration by providing the necessary information, such as:

* Name and Role ARN (for AWS Metrics+, AWS CloudTrail, and AWS CloudWatch)
* Bucket Name, Prefix, and Region (for CloudTrail only)
* Allow Lists and Service Refresh Rate (for CloudWatch only)

**Read More**<br />
* [Giving Wavefront Global Read-Only Access](https://docs.wavefront.com/integrations_aws_overview.html#give-wavefront-read-only-access-to-your-amazon-account-and-get-the-role-arn)
* [Giving Wavefront Limited Access](https://docs.wavefront.com/integrations_aws_overview.html#giving-wavefront-limited-access)
* [Register Additional Amazon Web Services](https://docs.wavefront.com/integrations_aws_overview.html#register-additional-amazon-web-services)
* [Configuring CloudWatch Data Ingestion](https://docs.wavefront.com/integrations_aws_metrics.html#configuring-cloudwatch-data-ingestion)
