### Edit or Register a CloudWatch Integration

{% include cloud_integrations_add_single.md integration="CloudWatch" %}

You can configure which AWS metrics and tags to ingest into Wavefront, by adding instances, volumes, metrics, and tags to allow lists. 

* Add instances and volumes to allow lists by specifying EC2 tags defined on the instances and volumes. 
  
  Requires an AWS Metrics+ integration as tags are imported from EC2. 

* Add metrics to allow lists by specifying a regular expression that is a complete match of the entire metric name. 

  To add **elb** and **rds** metrics to an allow list, use the regular expression **^aws\.(elb|rds).*$**. If you do not specify tags or regular expressions, all metrics are retrieved. 
  
* Add AWS point tags to allow lists by specifying a regular expression.

You can also change the service refresh rate (the default is `5` minutes) and select which AWS products to monitor.

**Read More**<br />
[Configuring CloudWatch Data Ingestion](https://docs.wavefront.com/integrations_aws_metrics.html#configuring-cloudwatch-data-ingestion)
