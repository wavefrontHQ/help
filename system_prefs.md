### Organization Settings

As an administrator with **Accounts, Groups & Roles** permission, you can set Wavefront preferences:

**New Account Defaults Tab**

Lets you to:

* Globally set whether Getting Started Progress display is the default and set a default landing page - a dashboard that you specify or the dashboard list.
* Set the default query language preferences and optionally allow users to write queries in PromQL. 
* When the default query language is WQL, you can also set whether Query Editor or Chart Builder is the default query builder. 
* Set the default groups for new user accounts. New users are assigned to all default user groups, and permissions are additive.
* Set the default groups for new service accounts. 
* Set the default permissions for new user accounts. These permissions don't apply to service accounts

**Security Tab**

Lets you give access to new dashboards and alerts to: 
* All user accounts that belong to the **Everyone** group.
* All user accounts that belong to the **Everyone** group and all service accounts that belong to the **Service Accounts** group.
* Only to the **Object Creator**. Even if you select **Object Creator**, the Super Admin user still has access.

### More Info

[Authorization in Wavefront](https://docs.wavefront.com/authorization.html)
[Managing Access](https://docs.wavefront.com/access.html)
