### Add a Dynatrace Integration

The Dynatrace integration is an AI-powered, full-stack, automated performance management solution. This integration collects the metrics from a Dynatrace SaaS environment and sends them to Wavefront.

**Limitations**

In this initial release of the Dynatrace integration, we have the following limitations:

* Billing metrics are not allowed and fetched with this release.
* You must have the <code>Annotations Key Length Limit</code> set up to <code>70</code>. The <code>Annotations Key Length Limit</code> is the maximum number of characters in a point tag key.

  **Important**: You cannot edit the default value (<code>64</code>) of the <code>Annotations Key Length Limit</code> by yourself. You must contact our customer success team to request changes.

**Obtain the Environment ID and Generate an API Token**

To set up the Dynatrace integration, you must provide the environment ID and a valid API token. 

1. Log in to your Dynatrace account.
2. Click the user icon in the header, and from the context menu, select your user name.
3. Under the **Environment access and settings** section, click the name of the environment that you want to monitor.
4. Copy the **Environment ID** shown in the URL of the form https://<code>your-environment-id</code>.live.dynatrace.com and paste it in a text file. 
5. Click **Access Tokens** in the navigation menu.
6. In the **Access Tokens** page, click the **Generate new token** button.
7. In the **Token name** text box, enter the name for the API token.
8. From the list of scopes, select **Read metrics (metrics.read)** and click the **Generate** button.
9. Copy the generated token by clicking the **Copy** button and paste it in a text file.

**Register the Dynatrace Integration**

After you copy the environment ID and the generated API token, follow these steps:

1. In the **Name** text box, enter a meaningful name.
2. In the **Environment ID** text box, provide the environment ID.
3. In the **API Token** text box, provide the API token.
  
   The API Token is securely stored and never exposed except for read-only access to fetch data from the Dynatrace Operations server.
   
4. (Optional) In the **Metric Allow List** text box, add metrics to an allow list by entering a regular expression. For example:
    * To fetch only Apache Tomcat and Oracle WebLogic metrics, enter: <code>^dynatrace.(.*)(tomcat|weblogic).*$</code>
    * To fetch only Kubernetes metrics, enter: <code>^dynatrace.(.*)(cloud.kubernetes).*$</code>
    * To fetch only host performance metrics, enter: <code>^dynatrace.(.*)(host).*$</code>
    * To fetch only Synthetic metrics, enter: <code>^dynatrace.(.*)(synthetic).*$</code>
5. (Optional) Change the **Service Refresh Rate**. The default is `5` minutes.
6. Click **Register**.
