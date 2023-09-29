### Organization Security Settings

As an **Admin** user, on this page, you can set access to newly created dashboards and alerts:

* If you select  **Grant Modify Access To: Everyone**, you give access to all user accounts. All user accounts belong to the **Everyone** internal system group.
* If you select **Grant Modify Access To: Everyone** and select the **Service Accounts** check box, you give access to all user accounts as well as to all service accounts and server to server OAuth apps that have access to the service instance. All service accounts and all server to server OAuth apps that have access to this service instance belong to the **Service Accounts** internal system group.
* If you select **Grant Modify Access To: Object Creator**, access to new dashboards and new alerts is initially limited to the dashboard creator and the **Super Admin** users.

Any change that you make applies only to the dashboards and alerts created after the change. If you change the setting to **Object Creator**, only new dashboards and alerts have restricted access. If you later change the setting to **Everyone**, all dashboards and alerts that were created while the setting was **Object Creator** keep the restricted access.

**Read More**<br/>
[Authorization](https://docs.wavefront.com/csp_authorization.html)<br/>
[Managing Access](https://docs.wavefront.com/csp_access.html)

**Watch Videos**<br/>
[Access Control](https://youtu.be/45E4pkann0E)
