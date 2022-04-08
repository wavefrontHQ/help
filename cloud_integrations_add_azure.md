### Add a Microsoft Azure Cloud Integration

Adding a Microsoft Azure cloud integration requires establishing a trust relationship between Azure and Tanzu Observability by Wavefront. The overall process involves the following:

* Getting a Tenant ID
* Creating an Azure Active Directory application that represents Tanzu Observability inside Azure and getting the Application ID.
* Creating a secret key and getting the Application secret.

You can do that either by using the Azure Cloud Shell, or the Microsoft Azure User Interface.

Follow these steps:

1. Provide the necessary information for establishing a trust relationship, and click **Next**.
   1. In the **Name** text box, enter a meaningful name for the integration.
   2. In the **Tenant ID/Directory ID** text box, enter your Microsoft Azure Tenant ID.
   3. In the **Application ID** text box, enter the Azure Active Directory Application (client) ID.
   4. In the **Application Secret** text box, enter the secret key that you created.
      **Note**: The Azure application secret that you enter is securely stored and never exposed except for read only access to the Azure APIs.
   5. (Optional) Add tags.
2. (Optional) Enter the **Metrics** information and click **Next**.
    * In the **Metric Categories** text box, enter the names of the metric categories to fetch.
    * In the **Metric Allow List** text box, add metrics to an allow list by entering a regular expression. For example, <code>^azure.(compute|dbforpostgresql).*$</code>.
3. (Optional) Enter the resource group names to fetch.
4. Select whether you want to fetch logs. 
   If you decide that you want to fetch activity logs, you can also specify the log categories to fetch, e.g. Administrative, Service health, Alert, and so on.
9. Click **Register**.
