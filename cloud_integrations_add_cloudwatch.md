### Register a CloudWatch Integration


1. In the **Name** text box, enter a meaningful name.
2. From the **Role ARN** menu, select an existing Role ARN.
3. To configure which AWS metrics and tags to ingest into Operations for Applications, you can add instances, volumes, metrics, and tags to allow lists. 

   * Add **instances** and **volumes** to allow lists by specifying EC2 tags defined on the instances and volumes. 
  
     Requires an AWS Metrics+ integration as tags are imported from EC2. 

   * Add **metrics** to allow lists by specifying a regular expression that is a complete match of the entire metric name. 

     To add **elb** and **rds** metrics to an allow list, use the regular expression **^aws\.(elb|rds).*$**. If you do not specify tags or regular expressions, all metrics are retrieved. 
   * Add the **names of the buckets** that contain the objects you want to request metrics for to allow lists. Use a regular expression.
   * Add AWS **point tags** to allow lists by specifying a regular expression.
4. (Optional) Change the **Service Refresh Rate**. The default is `5` minutes.
5. Select the list of AWS products for which you want to collect metrics by using the CloudWatch integration. 
6. (Optional) If you select a custom list of AWS products, you can also specify custom namespaces.

    A namespace is a container for CloudWatch metrics. Metrics in different namespaces are isolated from each other, so that metrics from different applications are not mistakenly aggregated into the same statistics. 

    If you want to monitor a service which is not in the list of products, e.g. Amazon Chime SDK, in the **Custom Namespace(s)** text box, enter <code>AWS/ChimeSDK</code>. If you have defined your own custom namespace for the same service in AWS, for example <code>ABC</code>, provide the custom namespace the way you have defined it in AWS. In this case, in the **Custom Namespace(s)** text box, enter <code>ABC</code> without a prefix.

7. Click **Register**.
