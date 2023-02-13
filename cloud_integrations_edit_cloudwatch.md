### Edit a CloudWatch Integration

{% include cloud_integrations_add_single.md integration="CloudWatch" %}

1. Edit the **Name** of the integration.
2. Edit the AWS metrics and tags to ingest into Operations for Applications by updating the allow lists. 

   * Add **instances** and **volumes** to allow lists by specifying EC2 tags defined on the instances and volumes. 
  
     Requires an AWS Metrics+ integration as tags are imported from EC2. 

   * Add **metrics** to allow lists by specifying a regular expression that is a complete match of the entire metric name. 

     To add **elb** and **rds** metrics to an allow list, use the regular expression **^aws\.(elb|rds).*$**. If you do not specify tags or regular expressions, all metrics are retrieved. 
   * Add the **names of the buckets** that contain the objects you want to request metrics for to allow lists. Use a regular expression.
   * Add AWS **point tags** to allow lists by specifying a regular expression.
4. (Optional) Edit the **Service Refresh Rate**. The default is `5` minutes.
5. Update the list of AWS products for which you want to collect metrics by using the CloudWatch integration. 
6. Click **Update**.
