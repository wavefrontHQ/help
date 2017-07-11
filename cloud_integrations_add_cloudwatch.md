### Registering a CloudWatch Integration

{% include cloud_integrations_add_single.md integration="CloudWatch" %}

To configure which AWS metrics and tags to ingest into Wavefront you can whitelist instances, volumes, metrics, and tags. Whitelist instances and volumes by specifying EC2 tags defined on the instances and volumes. Requires an AWS Metrics+ integration as tags are imported from EC2. Whitelist metrics by specifying a regular expression that is a complete match of the entire metric name. To whitelist **elb** and **rds** metrics, use the regular expression **^aws\.(elb|rds).*$**. If you do not specify tags or regular expressions, all metrics are retrieved. Whitelist AWS tags by specifying a regular expression.
