### Add a GCP Integration

Adding a Google Cloud Platform (GCP) integration requires establishing a trust relationship between GCP and Tanzu Observability by Wavefront. Minimum required permissions you need depend on the services that you are using. See [Google Cloud Platform Overview and Permissions](http://docs.wavefront.com/integrations_gcp_overview.html) for details.

The overall process involves the following:

* Creating a service account
* Giving that account viewer privileges 
* Downloading a JSON private key

To register a Google Cloud Platform (GCP) integration you need a JSON key. 

1. Provide the necessary information for establishing a trust relationship and click **Next**.
   1. In the **Name** text box, enter a meaningful name.
   2. In the **JSON key** text box, enter your JSON key to give read-only access to a GCP project.
      **Note**: The JSON key is never exposed except for read-only access to the GCP APIs.
   3. (Optional) Add tags to the integration.
2. Configure the metric settings.
   1. Select the categories to fetch.
   2. (Optional) In the **Metric Allow List** text box, add metrics to an allow list by entering a regular expression. 
   3. (Optional) In the **Additional Metric Prefixes** text box, enter a comma separated list of additional metrics prefixes. 
      The names of the metrics that start with these prefixes will be imported in addition to what you have selected as categories.
   4. (Optional) Change the **Service Refresh Rate**. The default is `5` minutes.
   5. (Optional) Select to enable **Detailed Histogram Metrics** and **Delta Counts** information.
   
      **Note**: Enabling **Detailed Histogram Metrics** and **Delta Counts** will increase your ingestion rate and costs.
3. Click **Register**.
