### Register a CloudWatch Integration

{% include cloud_integrations_add_single.md integration="CloudWatch" %}

1. In the **Name** text box, enter a meaningful name.
2. From the **Role ARN** drop-down menu, select an existing Role ARN.
3. To configure which AWS metrics and tags to ingest into Tanzu Observability, you can add instances, volumes, metrics, and tags to allow lists. 

   * Add **instances** and **volumes** to allow lists by specifying EC2 tags defined on the instances and volumes. 
  
     Requires an AWS Metrics+ integration as tags are imported from EC2. 

   * Add **metrics** to allow lists by specifying a regular expression that is a complete match of the entire metric name. 

     To add **elb** and **rds** metrics to an allow list, use the regular expression **^aws\.(elb|rds).*$**. If you do not specify tags or regular expressions, all metrics are retrieved. 
  
   * Add AWS **point tags** to allow lists by specifying a regular expression.
4. Change the **Service Refresh Rate**. The default is `5` minutes.
5. Select the list of AWS products for which you want to collect metrics by using the CloudWatch integration. 
6. Click **Register**.

**Read More**

[How to Use the Metric Allows List and the Product List](https://docs.wavefront.com/integrations_aws_metrics.html#how-to-use-the-metric-allow-list-and-the-products-list)
