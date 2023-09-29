### Managing Proxies

This page shows a paginated table that lists all existing proxies and their details. You can:
* Add or remove table columns by clicking the icon in the bottom-left corner of the table.
* Select to show **All** or **Deleted** proxies from the drop-down menu in the top-right corner of the table. The **Deleted** list shows the ephemeral proxies that were deleted during the last 24 hours and the non-ephemeral proxies that were deleted during the last 1 month.
* Sort the table by column, search by keyword, and filter by proxy status and saved search.

The status of a proxy can be:
* **Active**: The proxy is running and sending data.
* **Orphaned**: The proxy stopped sending data. The reason can be:
    - The sources stopped sending data to the proxy.
    - The token has been revoked.
    - The proxy service has been stopped.

        **Note**: You can start the stopped proxy service again only on a non-ephemeral proxy. Restarting the proxy service on an ephemeral proxy, installs a new proxy with a new ID and the old proxy transitions into irreversible orphaned status.
* **Stopped by Server**: The Tanzu Observability subscription has ended for the customer.
* **Token Expired**: The token has expired. You must install a new proxy.

From this page, you also can:
* Install a proxy by clicking **Add new proxy**.
* Delete one or more proxies by selecting the check boxes for the proxies and clicking **Delete**.

    **Note**: You cannot delete a proxy in **Active** status.
* Open the individual dashboard of a proxy and see its configuration properties by clicking the corresponding proxy name.
* Go to the **Wavefront Service and Proxy Data** dashboard by clicking **Usage and Proxies Data Dashboard**.


{% include proxies_links.md %}
