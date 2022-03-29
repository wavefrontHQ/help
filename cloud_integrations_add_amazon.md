### Add an Amazon Cloud Integration

Setting up an Amazon Web Services cloud integration requires establishing a trust relationship between Amazon and Tanzu Observability by Wavefront. This involves creating a role in Amazon Web Services, providing it with read-only access, and getting the Role ARN.

**Note**: Depending on the Tanzu Observability version that you use, there might be slight differences between the UI and the documented procedures for setting up and managing your AWS integration.

Then, you can register the integration:

1. In the **Name** text box, enter a meaningful name.
2. In the **Role ARN** text box, enter the Role ARN from Amazon IAM.
3. (Optional) To register CloudTrail, click **Show Advanced Options** and provide the necessary information.

   * **Bucket Name** - The S3 bucket that contains CloudTrail logs. 
   
     In AWS, go to **CloudTrail** &gt;**Trails** to see the bucket name.
   
   * (Optional) **Prefix** - A log file prefix specified when you created the CloudTrail. 
   
     The default prefix is `AWSLogs`. If you use a custom prefix, you must put it here without using a forward slash at the end of the prefix, i.e. a trailing slash.
   
   * **Region** - AWS Region where the CloudTrail logs reside.

4. Click **Register**.

For information about registering and configuring CloudWatch, see [Configure CloudWatch Data Ingestion](https://docs.wavefront.com/integrations_aws_metrics.html#configuring-cloudwatch-data-ingestion).

**Read More**<br />
* [Give Global Read-Only Access](https://docs.wavefront.com/integrations_aws_overview.html#give-read-only-access-to-your-amazon-account-and-get-the-role-arn)
* [Give Limited Access](https://docs.wavefront.com/integrations_aws_overview.html#giving-limited-access)
* [Register Additional Amazon Web Services](https://docs.wavefront.com/integrations_aws_overview.html#register-additional-amazon-web-services)
