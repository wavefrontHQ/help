### Managing Service Accounts
A service account is for services that use the Wavefront API to perform certain tasks. Service accounts use a token to authenticate and are constrained from performing certain UI operations.

By default all service accounts belong to the **Service Accounts** system group.

From this page, users with the **Accounts** permission can:
* Create and delete service accounts.
* Deactivate and activate service accounts.
* Generate, revoke, and rename API tokens for service accounts.
* Manage the permissions, roles, and groups assigned to service accounts. You cannot revoke the **Service Accounts** system group. In most situations, it's best to assign permissions directly to the service account.

You can also select one or more permissions, groups, and roles on the left to see which service accounts match the selections.

**Read More**<br/>
[Manage Service Accounts](https://docs.wavefront.com/service-accounts.html)<br/>
[Authorization Model](https://docs.wavefront.com/authorization.html)
