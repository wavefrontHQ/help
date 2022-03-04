### Add a GCP Integration

Adding a Google Cloud Platform (GCP) integration requires establishing a trust relationship between GCP and Wavefront. Minimum required permissions you need depend on the services you are using. See [Google Cloud Platform Overview and Permissions](http://docs.wavefront.com/integrations_gcp_overview.html) for details.


The overall process involves the following:

* Creating a service account
* Giving that account viewer privileges 
* Downloading a JSON key

1. In the **Name** text box, enter a meaningful name.
2. In the **JSON key** text box, enter your JSON key to give read-only access to a GCP project.
3. (Optional) Select the categories to fetch.
4. (Optional) In the **Metric Allow List** text box, you can add metrics to an allow list by entering a regular expression. 
5. (Optional) In the **Additional Metric Prefixes** text box, enter a comma separated list of additional metrics prefixes. 
   The metrics names that start with these prefixes will be imported in addition to what you have selected as categories.
6. (Optional) Change the **Service Refresh Rate**. The default is `5` minutes.
7. (Optional) Select to enable **Detailed Histogram Metrics**, **Delta Counts**, and **Pricing and Billing** information.
   
   Note that enabling **Detailed Histogram Metrics** and **Delta Counts** will increase your ingestion rate and costs.

8. Click **Register**.
