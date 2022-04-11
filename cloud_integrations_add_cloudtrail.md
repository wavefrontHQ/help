### Register a CloudTrail Integration

{% include cloud_integrations_add_single.md integration="CloudTrail" %}

1. In the **Name** text box, enter a meaningful name.
2. From the **Role ARN** menu, select an existing Role ARN.
3. In the **Bucket Name** text box, enter the S3 bucket that contains CloudTrail logs. 
   
   In AWS, go to **CloudTrail** &gt;**Trails** to see the bucket name.
   
4. (Optional) In the **Prefix** text box, enter a log file prefix specified when you created CloudTrail. 
   
   The default prefix is `AWSLogs`. If you use a custom prefix, you must put it here without using a forward slash at the end of the prefix, i.e. a trailing slash.
   
5. In the **Region** text box, enter the AWS Region where the CloudTrail logs reside.
6. Click **Register**. 
