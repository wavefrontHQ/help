### Edit a CloudWatch Integration


1. Under **Access**, edit the **Name** of the integration.
2. Under **Allow Lists**, you can edit the AWS metrics and tags to ingest into Tanzu Observability by updating the existing allow lists or creating new ones. 

   * Add **instances** and **volumes** to allow lists by specifying EC2 tags defined on the instances and volumes. 
  
     Requires an AWS Metrics+ integration as tags are imported from EC2. 

   * Add **metrics** to allow lists by specifying a regular expression that is a complete match of the entire metric name. 
   * Add AWS **point tags** to allow lists by specifying a regular expression.
   * Edit the **Service Refresh Rate**. The default is `5` minutes.
5. Under **Product Configuration**, you can update the list of AWS products for which you want to collect metrics by using the CloudWatch integration. By default we collect data for all of your AWS products. 
6. Click **Update**.

**Read More**

[Configuring CloudWatch Data Ingestion](https://docs.wavefront.com/integrations_aws_metrics.html#configuring-cloudwatch-data-ingestion)<br/>
[How to Use the Metric Allows List and the Product List](https://docs.wavefront.com/integrations_aws_metrics.html#how-to-use-the-metric-allow-list-and-the-products-list)
