### Add an Amazon Cloud Integration

Setting up an Amazon cloud integration requires establishing a trust relationship between Amazon and Wavefront.

  You start by granting [Wavefront read-only access](https://docs.wavefront.com/integrations_aws_overview.html#give-wavefront-read-only-access-to-your-amazon-account-and-get-the-role-arn) to your Amazon account or by [giving Wavefront limited access](https://docs.wavefront.com/integrations_aws_overview.html#giving-wavefront-limited-access). 

Then, you register the integration by providing the necessary information, such as:

* For **AWS Metrics+**, configure the following integration properties:
   
   1. **Name** - Name to identify the integration.
   2. **Role ARN** - Role ARN from your Amazon account.

* For **CloudTrail**, configure the following integration properties:
   
   1. **Name** - Name to identify the integration.
   2. **Role ARN** - Role ARN from your Amazon account.
   3. **Bucket Name** - The S3 bucket that contains CloudTrail logs. 
      
      In AWS, go to **CloudTrail** &gt;**Trails** to see the bucket name.
      
   4. (Optional) **Prefix** - A log file prefix specified when you created the CloudTrail service. 
      
      The default prefix is `AWSLogs`. If you use a custom prefix, you must put it here without using a forward slash at the end of the prefix, i.e. a trailing slash.
      
   5. **Region** - AWS Region where the CloudTrail logs reside.
    
* For **CloudWatch**, configure the following integration properties:

   1. **Name** - Name to identify the integration.
   2. **Role ARN** - Role ARN from your Amazon account.
   3. Allow Lists and Service Refresh Rate - see [Configuring CloudWatch Data Ingestion](https://docs.wavefront.com/integrations_aws_metrics.html#configuring-cloudwatch-data-ingestion).

**Read More**<br />
* [Learn How to Register AWS Metrics+, AWS CloudTrail, and AWS CloudWatch](https://docs.wavefront.com/integrations_aws_overview.html#register-additional-amazon-web-services)
* [Learn How to Configuring CloudWatch Data Ingestion](https://docs.wavefront.com/integrations_aws_metrics.html#configuring-cloudwatch-data-ingestion)
