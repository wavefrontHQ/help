### Adding a Proxy

In most cases a Wavefront proxy must be running in your environment before metrics begin streaming to your Tanzu Observability service from a host or application. In production, it is recommended to place a team of proxies behind a load balancer.

To authenticate to Tanzu Observability, the Wavefront proxy requires a VMware Cloud services access token with the **Proxies** service role.

**Important**: To obtain a VMware Cloud services access token, the Wavefront proxy connects to the VMware Cloud services API. For that reason, your environment must allow an outbound HTTPS connection to the VMware Cloud services platform (`https://console.cloud.vmware.com/`).

To add a proxy, you must first choose the method for the proxy to obtain the access token - using **OAuth App** or **API Token**. Then, you must choose the OS on which you want to install the proxy - **Linux**, **Docker**, **Mac**, **Windows**, or **Kubernetes**, and follow the on-screen instructions.

* **OAuth App**: You must provide the credentials - ID and secret (`<CSP_APP_ID>` and `<CSP_APP_SECRET>`), of a server to server OAuth app that is assigned with the **Proxies** service role and that is added to the VMware Cloud organization running the service. You must also provide the ID of the VMware Cloud organization (`<CSP_ORG_ID>`).

    For details on how to get the values, see [How to use OAuth 2.0 for server to server apps](https://docs.vmware.com/en/VMware-Cloud-services/services/Using-VMware-Cloud-Services/GUID-327AE12A-85DB-474B-89B2-86651DF91C77.html?hWord=N4IgpgHiBcIMpgE4DckAIAuB7NBnJqiaAhgA6kgC+QA) and [How do I manage my Cloud Services Organizations](https://docs.vmware.com/en/VMware-Cloud-services/services/Using-VMware-Cloud-Services/GUID-CF9E9318-B811-48CF-8499-9419997DC1F8.html) in the VMware Cloud services documentation.

    **Note**: The proxy exchanges the OAuth app credentials for an access token. The server to server OAuth app is configured with a TTL configuration for its access token. Before the access token expires, the proxy automatically obtains a new access token.

* **API Token**: You must provide a VMware Cloud services API token (`<CSP_API_TOKEN>`) that belongs to the VMware Cloud organization running the service and that is assigned with the **Proxies** service role.

    For details on how to get the API token, see [How do I generate API tokens](https://docs.vmware.com/en/VMware-Cloud-services/services/Using-VMware-Cloud-Services/GUID-E2A3B1C1-E9AD-4B00-A6B6-88D31FCDDF7C.html).

    **Important**: The proxy exchanges the API token for an access token. The TTL of the access token is 30 minutes. Before the access token expires, the proxy automatically obtains a new access token. The API token is configured with a TTL configuration. Before the API token expires, you must generate a new API token and reconfigure the proxy with the new API token.

**Read More**<br/>
[Install and Manage Wavefront Proxies](http://docs.wavefront.com/proxies_installing.html)