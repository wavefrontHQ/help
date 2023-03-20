### Add a Dynatrace Integration

The Dynatrace integration is an AI-powered, full-stack, automated performance management solution. This integration collects the metrics from a Dynatrace SaaS environment and sends them to Operations for Applications.

To set up the Dynatrace integration, you must provide the environment ID and a valid API token. Click the **How to get the Environment ID** and **How to get the API Token** links on the left and follow the instructions. After you copy the environment ID and the generated API token, follow these steps:

1. In the **Name** text box, enter a meaningful name.
2. In the **Environment ID** text box, provide the environment ID that you copied.
3. In the **API Token** text box, paste the API token that you copied.
  
   The API Token is securely stored and never exposed except for read-only access to fetch data from the Dynatrace Operations server.

4. (Optional) In the **Metric Allow List** text box, add metrics to an allow list by entering a regular expression. For example:
   
   * To fetch only Apache Tomcat and Oracle WebLogic metrics, enter: `^dynatrace.(.*)(tomcat|weblogic).*$`
   * To fetch only Kubernetes metrics, enter: `^dynatrace.(.*)(cloud.kubernetes).*$`
   * To fetch only host performance metrics, enter: `^dynatrace.(.*)(host).*$`
   * To fetch only Synthetic metrics, enter: `^dynatrace.(.*)(synthetic).*$`
5. (Optional) Change the **Service Refresh Rate**. The default is `5` minutes.
6. Click **Register**.
