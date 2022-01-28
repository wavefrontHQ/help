### Edit or Register a CloudWatch Integration

{% include cloud_integrations_add_single.md integration="CloudWatch" %}

You can configure which AWS metrics and tags to ingest into Wavefront, by adding instances, volumes, metrics, and tags to allow lists. Instance and volume allow lists require an **AWS Metrics+** integration as tags are imported from EC2. 

1. In the **Instance Allow List** text box, add instances to allow lists by specifying EC2 tags defined on the instances. 
2. In the **Volume Allow List** text box, add volumes to allow lists by specifying EC2 tags defined on the volumes.
3. In the **Metric Allow List** text box, add metrics to allow lists by specifying a regular expression that is a complete match of the entire metric name. 

  To add **elb** and **rds** metrics to an allow list, use the regular expression **^aws\.(elb|rds).*$**. If you do not specify tags or regular expressions, all metrics are retrieved. 
  
4. In the **Point Tag Allow List** text box, add AWS point tags to allow lists by specifying a regular expression.
5. Change the **Service Refresh Rate**. The default is `5` minutes.
6. Filter the list of AWS products for which you want to collect metrics by using the CloudWatch integration

**Read More**<br />
[Configuring CloudWatch Data Ingestion](https://docs.wavefront.com/integrations_aws_metrics.html#configuring-cloudwatch-data-ingestion)
