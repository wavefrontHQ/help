### Proxies Browser

This page shows a paginated table that lists all existing proxies and their details. You can:
* Add or remove table columns by clicking the icon in the bottom left corner of the table.
The **Proxy Name** column shows the name, hostname, and ID of each proxy.
* Select to show **All** or **Deleted** proxies from the drop-down menu in the top-right corner of the table. The **Deleted** list shows the ephemeral proxies that were deleted during the last 24 hours and the non-ephemeral proxies that were deleted during the last 1 month.
* Sort the table by column, search by keyword, and filter by proxy status and saved search.

The status of a proxy can be:
* **Active**: The proxy is running and sending data.
* **Orphaned**: The proxy stopped sending data. Either the sources stopped sending data to the proxy or the proxy service has been stopped.

    **Note**: You can start the stopped proxy service again only on a non-ephemeral proxy. Restarting the proxy service on an ephemeral proxy, installs a new proxy with a new ID and the old proxy transitions into irreversible orphaned status.
* **Stopped by Server**: The Tanzu Observability subscription has ended for the customer.
* **Token Expired**: The token has expired. You must install a new proxy.

From this page, you also can:
* Install a proxy by clicking **Add new proxy**.
* Delete one or more proxies by selecting the check boxes for the proxies and clicking the **Delete** icon.

    **Note**: You cannot delete a proxy in **Active** status.
* Open an individual proxy dashboard by clicking the corresponding proxy name. This dashboard contains a number of charts based on the internal metrics emitted by the proxy. You can examine the proxy health and usage information.
* Go to the **Wavefront Service and Proxy Data** dashboard by clicking **Usage and Proxies Data Dashboard**. This dashboard is predefined in the Wavefront Usage integration. The **Proxies: Overview** and the **Proxy Troubleshooting** sections of this dashboard contain a number of charts based on the internal metrics emitted by all proxies in the environment. You can examine the overall health and usage information for your proxies.


{% include proxies_links.md %}
