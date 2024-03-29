### Add a GCP Integration

Adding a Google Cloud Platform (GCP) integration requires establishing a trust relationship between GCP and VMware Aria Operations for Applications (formerly known as Tanzu Observability by Wavefront). Minimum required permissions you need depend on the services that you are using. See [Google Cloud Platform Overview and Permissions](http://docs.wavefront.com/integrations_gcp_overview.html) for details.

The overall process involves the following:

* Creating a service account in Google Cloud
* Giving that account viewer privileges 
* Downloading a JSON private key

To register a Google Cloud Platform integration:

1. In the **Name** text box, enter a meaningful name.
2. In the **JSON key** text box, enter your JSON key to give read-only access to a GCP project.
   **Note**: The JSON key is securely stored and never exposed except for read-only access to the GCP APIs. 
3. (Optional) Select the categories to fetch.
4. (Optional) In the **Metric Allow List** text box, you can add metrics to an allow list by entering a regular expression. 
    
    For example, to monitor all the CPU metrics coming from the Compute Engine, enter <code>^gcp.compute.instance.cpu.*$</code>.
    
   <strong>Note:</strong> Metric names consist of the actual metric name and a suffix (starting with an underscore ("_") or a dot (".")). The suffix represents an aggregation type. In the regular expression, you must use the actual metric names without the aggregation types, such as: <code>count</code>, <code>rate</code>, <code>min</code>, <code>max</code>, <code>sumOfSquaredDeviation</code>, <code>mean</code>, and so on.

   For example, for the Google Cloud Pub/Sub Engine, we collect a number of metrics, and some of them contain a suffix:

   Push request latencies metrics:

    * <code>gcp.pubsub.subscription.push_request_latencies.bucket</code>
    * <code>gcp.pubsub.subscription.push_request_latencies.count</code>
    * <code>gcp.pubsub.subscription.push_request_latencies.mean</code>
    * <code>gcp.pubsub.subscription.push_request_latencies.sumOfSquaredDeviation</code>
   
   Here, the actual metric name is <code>gcp.pubsub.subscription.push_request_latencies</code>, while <code>bucket</code>, <code>count</code>, <code>mean</code>, and <code>sumOfSquaredDeviation</code> are the aggregation types. When you create the regular expression, you must use only <code>gcp.pubsub.subscription.push_request_latencies</code>. For example, <code>^gcp.pubsub.subscription.push_request_latencies$</code>.


   Cumulative count of messages acknowledged by Acknowledge requests, grouped by delivery type:
   
    * <code>gcp.pubsub.subscription.ack_message_count_count</code>
    * <code>gcp.pubsub.subscription.ack_message_count_rate</code>

   Here, the actual metric name is <code>gcp.pubsub.subscription.ack_message_count</code>, while <code>_count</code> and <code>_rate</code> are the aggregation types. When you create the regular expression, you must use only <code>gcp.pubsub.subscription.ack_message_count</code>. For example, <code>^gcp.pubsub.subscription.ack_message_count$</code>.

5. (Optional) In the **Additional Metric Prefixes** text box, enter a comma separated list of additional metrics prefixes. 
   The metrics names that start with these prefixes will be imported in addition to what you have selected as categories.
6. (Optional) Change the **Service Refresh Rate**. The default is `5` minutes.
7. (Optional) Select whether you want to enable **Histogram** metrics ingestion.
    
   1. (Optional) Select which histogram metrics to ingest. 
   
      * **All** - The default option which means that all metrics will be ingested. 
      * **Custom** - Allows you to ingest particular histogram metrics based on their Google Cloud Platform grouping functions, such as **Count**, **Mean**, and **Standard Deviation**. When you select a grouping function, only the histogram metrics with the respective grouping function will be ingested. If you deselect all check boxes, all histogram metrics will be ingested.
   
   2. (Optional) Select to enable **Detailed Histogram Metrics**, **Delta Counts**, and **Pricing & Billing** information.

         **Note**: Enabling **Detailed Histogram Metrics** and **Delta Counts** will increase your ingestion rate and costs. 

         If you select to enable the **Pricing & Billing** information, you must also provide an API key.

10. Click **Register**.
