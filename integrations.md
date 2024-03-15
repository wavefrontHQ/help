### What Is an Integration?

Tanzu Observability integrations are the link between any system and Tanzu Observability. Integration links can be from your system into Tanzu Observability or from Tanzu Observability to an external system: data collector, alert notification, and authentication.

**Integration Categories**<br/>
Integrations are grouped into different categories. **Featured**, collector, and code instrumentation integrations include all ways to get data into Tanzu Observability: using a collector agent and Wavefront proxy, sending metrics from application code to the proxy, and Tanzu Observability pulling the data from a cloud service. 

To see the full list of categories, under **Type** click **See All**.

**Integration States**<br/>
Integration states depend on two factors:

* Whether metrics ever reported and whether they reported in the last 2 hours or in the last 7 days.
* The state of content installation, such as installed, never installed, or uninstalled

To filter the integrations by state, click a state from the left panel.

{% include integrations_links.md %}
