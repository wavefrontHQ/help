### Add a vRealize Operations Integration

The vRealize Operations integration is a full-featured native integration, that offers agentless data ingestion of vRealize Operations metric data, as well as predefined dashboards.

To register a new vRealize Operations instance, you need a Cloud Services console API token and a vRealize Operations endpoint URL. Click **How to get the API token** on the left and follow the instructions.

In the **Metric Allow List**, add metrics to an allow list by entering a regular expression. For example:

* To fetch only cost metrics, enter: <code>^vrops.vmware.(datastore|clustercomputeresource).cost.*$</code>
* To fetch only health metrics, enter: <code>^vrops.vmware.(datastore|clustercomputeresource).health.*$</code>
* To fetch only cost and health metrics, enter <code>^vrops.vmware.(datastore|clustercomputeresource).(cost|health).*$</code>


**Read More**
* [vRealize Operations Integration Overview](https://docs.wavefront.com/integrations_vrops.html)
