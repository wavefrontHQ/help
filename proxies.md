### Managing Proxies

Proxies allow you to send your data to Tanzu Observability by Wavefront in a secure, fast, and reliable manner. The proxy works with the Wavefront server to ensure end-to-end flow control.

From this page, users with the **Proxies** permission can view, create, and manage proxies.

* The **Hostname** column shows where the proxy is running.
* The **Status** column shows if the proxy is *active*, *orphaned*, or *stopped by the server*. When restarting a proxy, the proxy service restarts and creates a new service ID. The proxy with the old service ID becomes *orphaned* and is automatically deleted after 24 hours.
* The **Last Check-in** column shows when the proxy ingested data into the Wavefront service for the last time.
* The **Space Available** column shows the time left until the proxy buffer will become full if data keep arriving at the current rate.
* The **Clock Drift** column shows the difference between the clocks on the Wavefront service and the proxy. Could affect the metric timestamps because metrics are on proxy time.
* The **Queued Items** shows the amount of points per second (PPS) that the proxy has queued. When the proxy detects network
connectivity issues, it queues metrics in memory and to disk. Once connectivity is restored, the proxy
replays queued metrics but prioritizes real-time traffic.

To create a proxy, click **Add new proxy**.

To rename a proxy, click the vertical ellipsis for the proxy and select **Edit**.

To view the proxy usage chart, click the name of the proxy. You can edit the chart and save it to a new or existing dashboard.

To delete an *orphaned* or *stopped by server* proxy, select the check box for the proxy and click the **Delete** icon.

{% include proxies_links.md %}
