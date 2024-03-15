### Managing Service Accounts
A service account authenticates with an Tanzu Observability API token.

**Important**: The usage of service accounts is **restricted** to support only a [limited list](https://docs.wavefront.com/integrations_onboarded_subscriptions.html#integrations-that-use-operations-for-applications-api-tokens) of integrations that still authenticate with Tanzu Observability API tokens. In all other cases, you should use [server to server OAuth apps](https://docs.wavefront.com/csp_server_to_server_apps.html) which authenticate with the more secure VMware Cloud services access tokens.

By default all service accounts belong to the **Service Accounts** internal system group.

From this page, **Admin** users can:
* Create and delete service accounts.
* Deactivate and activate service accounts.
* Generate, revoke, and rename API tokens for service accounts.
* Manage the permissions assigned to service accounts.

**Read More**<br/>
[Manage Service Accounts](https://docs.wavefront.com/csp_service-accounts.html)<br/>
[Authorization Model](https://docs.wavefront.com/csp_authorization.html)
