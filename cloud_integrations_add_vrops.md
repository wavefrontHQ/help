### Add a vRealize Operations Cloud Integration

The VMware vRealize Operations Cloud integration is a full-featured native integration, that offers agentless data ingestion of vRealize Operations Cloud metric data, as well as a predefined dashboard.

To register a new vRealize Operations Cloud instance, you need a VMware Cloud Services Console API token and a vRealize Operations Cloud endpoint URL. To understand how to generate the API token, click the **How to get the API token** link and follow the instructions.

In the **Metric Allow List**, you can add metrics to an allow list by entering a regular expression. For example:

   * To fetch only cost metrics, enter: <code>^vrops.vmware.(datastore|clustercomputeresource).cost.*$</code>
   * To fetch only health metrics, enter: <code>^vrops.vmware.(datastore|clustercomputeresource).health.*$</code>
   * To fetch only cost and health metrics, enter <code>^vrops.vmware.(datastore|clustercomputeresource).(cost|health).*$</code>

**Read More**<br/>
* [vRealize Operations Cloud Integration Overview](https://docs.wavefront.com/integrations_vrops.html)
