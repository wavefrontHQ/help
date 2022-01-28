### Edit or Register a CloudTrail Integration

{% include cloud_integrations_add_single.md integration="CloudTrail" %}

When you edit or register a CloudTrail instance, in addition to the name and the Role ARN, you must also provide the **Bucket Name** and the **CloudTrail Region**. 

* **Bucket Name** is the S3 bucket containing CloudTrail logs.
* **CloudTrail Region** is AWS Region where the CloudTrail logs reside.

You can optionally specify a **Prefix** of the log files. The default prefix is `AWSLogs`. If you use a custom prefix, you must put it without using a forward slash at the end of the prefix, i.e. a trailing slash.
