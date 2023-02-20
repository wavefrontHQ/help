### Proxies Browser

Proxies allow you to send your data to Tanzu Observability by Wavefront in a secure, fast, and reliable manner. The proxy works with the Wavefront server to ensure end-to-end flow control.

This page shows a paginated table that lists all existing proxies with their details:
* The **Proxy Name** column shows the name, hostname, and ID of each proxy.
* From the columns icon in the bottom-left corner of the table, you can customize the other columns to show the last check-in date and time, status, ingestion rate for particular data type, version, backlog (queue) size, and the user who created each proxy.
* From the drop-down menu in top-right corner, you can select **Deleted** to show the ephemeral proxies that were deleted during the last 24 hours and the non-ephemeral proxies that were deleted during the last 1 month.
* You can sort, search, and filter the proxies list.

The status of a proxy can be:
* **Active**: The proxy is running and sending data.
* **Orphaned**: The proxy stopped sending data. Either the sources stopped emitting data or the proxy service has been stopped.
    **Note**: You can start the stopped proxy service again only on a non-ephemeral proxy. Restarting the proxy service on an ephemeral proxy, installs a new proxy with a new ID and the old proxy becomes orphaned.
* **Stopped by Server**: The Tanzu Observability subscription has ended for the customer.
* **Token Expired**: The token has expired. You must install a new proxy.

From this page, you can:
* Install a proxy by clicking **Add new proxy**.
* Delete one or more proxies by selecting the check boxes for the proxies and clicking the **Delete** icon.
    **Note**: You cannot delete a proxy in **Active** status.
* Open a proxy dashboard by clicking the proxy name to examine its health and usage information. This dashboard contains a number of charts based on the internal metrics emitted by the proxy.
* Go to the **Wavefront Service and Proxy Data** dashboard by clicking **Usage and Proxies Data Dashboard** to examine the overall health and usage information for all proxies in the environment. This dashboard is predefined in the Wavefront Usage integration. The **Proxies: Overview** and the **Proxy Troubleshooting** sections of this dashboard contain a number of charts based on the internal metrics emitted by the proxies.


{% include proxies_links.md %}
